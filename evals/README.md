# Evals

`SKILL.md` is prose that steers a model. Prose drifts. This directory holds a small,
hand-checkable set of scenarios that pin down what the skill is supposed to do:
whether it triggers, which reference files it reads, which mode it picks, and
whether the output obeys the discipline in `SKILL.md`.

This is deliberately not a test harness. There is no model call, no CI, no
dependency. The deliverable is a data file you can read as documentation and run
by hand in ten minutes.

## Files

- `scenarios.yaml` — the eval set. 28 scenarios plus five global invariants.
- `check_scenarios.py` — stdlib-only validator and pretty-printer. It checks the
  data file's shape and that every referenced path exists. It does **not** call a model.
  It bundles a minimal YAML reader rather than taking a PyYAML dependency; its output
  on `scenarios.yaml` has been diffed against PyYAML and is identical.

## Schema

Top level:

| Key | Meaning |
|---|---|
| `version` | Schema version. Currently `1`. |
| `global_invariants` | Plain-English checks that apply to every scenario where `should_trigger` is true. |
| `scenarios` | The list below. |

Each scenario:

| Key | Type | Meaning |
|---|---|---|
| `id` | string | Stable kebab-case identifier. Referenced in PR discussion. |
| `prompt` | string | Exactly what the user says. Verbatim — do not paraphrase when running. |
| `should_trigger` | bool | Whether the founder-wisdom skill should activate at all. |
| `expected_mode` | `direct` \| `socratic` \| `none` | `none` iff `should_trigger` is false. |
| `expected_files.must_include` | list | Reference files that must appear among those read. Never more than three. |
| `expected_files.must_not_include` | list | Reference files whose presence is a failure. |
| `assertions` | list | Plain-English checks on the response. |
| `rationale` | string | One line naming the `SKILL.md` rule the scenario protects. |

`expected_files` is deliberately tolerant. `SKILL.md` tells the model to read 2–3
files, so pinning an exact set would produce false failures. The pair of lists
expresses only what must be there and what must not be — anything else is free.
Where a plausible-but-secondary file exists, it is named in an assertion rather
than in either list.

## Running by hand

1. `python3 evals/check_scenarios.py` — validates the file and prints every scenario.
2. Install the skill (see the repo README) in a fresh conversation. One scenario
   per conversation: state carries, and a scenario that follows another will
   inherit its mode.
3. Paste the `prompt` verbatim. Nothing else.
4. Score it:
   - **Trigger** — did the skill activate? For Claude Code, the tool calls show
     which `references/*.md` were read. In Claude.ai, ask "which files did you
     consult?" *after* scoring the response, never before.
   - **Files** — every `must_include` present, no `must_not_include` present.
   - **Mode** — direct means axioms; Socratic means one question and a stop.
   - **Assertions** — each one a yes/no.
   - **Global invariants** — apply to every triggering scenario.
5. A scenario fails if any single check fails. Record which one; "it failed" is
   not actionable, "it read `fundraising.md` instead of `capital-valuation.md`" is.

Twenty-eight scenarios is a bit over an hour. A full pass is warranted when `SKILL.md`
routing prose changes; a spot check of the affected scenarios is enough for
anything smaller.

## Running with skill-creator

Anthropic's `skill-creator` skill has eval tooling that runs scenarios against a
skill and grades the transcript. It reads an `evals/evals.json` whose entries carry
`id`, `prompt`, `expected_output`, and `expectations`. Translate as follows:

- `prompt` → `prompt`, verbatim.
- `id` → a short note in `expected_output`; skill-creator's `id` is an integer, so
  number the entries and keep our kebab-case id as the human label.
- `should_trigger` → `expected_output` states whether the skill should engage at all.
  The negatives matter as much as the positives — a skill that fires on everything
  scores well on positives alone.
- `assertions` + the matching `global_invariants` → `expectations`, one string each.
- `expected_files` → an `expectations` entry of the form "read `references/X.md`;
  did not read `references/Y.md`." Note that skill-creator's own `files` key means
  *input* files, not the reference files read — do not map onto it.

Keep `scenarios.yaml` as the source of truth and generate the tool's input from it.
Do not fork the expectations into a second file.

## Adding a scenario

1. It must protect a rule `SKILL.md` actually states. Quote or paraphrase that rule
   in `rationale`.
2. If `SKILL.md` is ambiguous on the point, say so in the `rationale` rather than
   inventing a rule. Three scenarios already do this — `negative-boundary-mixed-regulatory`
   (mixed in-scope/out-of-scope prompts), `routing-delegation-at-5` (SKILL.md says
   "prefer," which is softer than the `must_not_include` encoding), and
   `reassurance-still-triggers` (the mode call).
3. Keep `must_include` to the one or two files the routing genuinely requires.
4. Stay inside the YAML subset the validator's bundled reader handles: two-space
   indent, `key: value`, `[a, b]` flow lists, block sequences, and `>-` folded
   scalars. Avoid anchors, inline comments, and multi-line flow collections.
5. Re-run `check_scenarios.py`.

## Known ambiguities and gaps

These are recorded so they aren't rediscovered every time:

- **"Reassurance" is an output rule, not a trigger rule.** `SKILL.md`'s
  "What this skill is not for" lists reassurance, but the entry itself says the
  skill "should still surface the axiom that pushes back." `reassurance-still-triggers`
  encodes the trigger as **true**.
- **Mixed-scope prompts are unspecified.** A prompt with an in-scope half and an
  out-of-scope half (`negative-boundary-mixed-regulatory`) has no rule in `SKILL.md`.
- **"Prefer" is soft.** The `management-execution.md` stage note says to prefer
  `time-energy.md` and `hiring.md` below ~10 people. `routing-delegation-at-5`
  reads that strictly.
- **Coverage gap at 200+.** `hiring.md`'s stage tags are all Seed–Series A, so
  `output-stage-match-late` tests stage-awareness against thin material.
- **`mode-direct-factual` fails today on the corpus, not on `SKILL.md`.** The
  scenario asserts the option-pool percentage carries a vintage tag, which is what
  `SKILL.md`'s "Output style" requires. The 10–15% pool-refresh figure in
  `capital-valuation.md` has no `*[bench YYYY-MM]*` tag, so a model reading it
  faithfully has nothing to cite. Fixing that is a corpus change, deliberately not
  made here — the scenario is correct and the corpus is the thing to repair.
