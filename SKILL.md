---
name: founder-wisdom
description: Surfaces hard-won axioms and pattern-matched wisdom from experienced startup founders and operators across hiring, fundraising, product, sales, finance, co-founders, governance, strategy, management, and crisis. Use this skill whenever someone is wrestling with a startup, scale-up, or early-stage company decision — including hiring or firing, raising capital, picking a co-founder, pricing, building a board, managing burn, questions about valuation, dilution, cap-table and exit math, the cost of capital, venture debt, or which SaaS metrics and KPIs actually matter, selling the company — running an M&A process, bankers, LOIs and exclusivity, earn-outs, escrow, acqui-hires, and what the deal actually pays out — navigating a pivot, surviving a crisis, questions about moats, defensibility, competition, or positioning against incumbents, questions about delegation, 1:1s, org design, or becoming a manager, how AI changes the way a startup team works, sells, and hires, who stays accountable when an agent does the work, or any "I'm a founder and I'm not sure what to do" moment. Trigger even when the person doesn't explicitly ask for "advice" — questions framed as "should I…", "is it normal that…", "we're thinking about…", or "how do experienced founders handle…" are all in scope. Also useful when the person is helping someone else with founder-stage decisions (advisor, coach, mentor, investor).
metadata:
  version: "1.7.0"
---

# Founder Wisdom

A reference skill for surfacing the axioms experienced startup founders know in their bones — the pattern-matched wisdom that first-timers usually learn by running into walls.

## What this skill is for

Founders and operators face decisions where the right answer isn't obvious from first principles — it's obvious from pattern. "Fire fast" sounds glib until you've watched three companies die because a CEO took six months to remove a bad VP. "Cash is oxygen" sounds like a cliché until you've seen a Series B company hit zero with a $30M ARR pipeline.

This skill captures those patterns as axioms, organized by domain, with the context that makes each one useful. It is opinionated and pattern-matched, not neutral or comprehensive. Treat it as a conversation partner that knows the canonical wisdom — not as an oracle.

## Two modes of operation

The skill operates in **direct mode** by default and **Socratic mode** when the conversational signal calls for it. Most uses will be direct.

### Direct mode (default)

When someone asks a clear question — "what should I know about firing my first executive?" or "how do experienced founders handle a down round?" — surface the relevant axioms directly. Lead with the axiom, then the reasoning, then the qualifier. Example:

> **Hire slow, fire fast.** Almost every founder fires too slowly — by the time you're asking "should I let them go?", the answer is yes and was yes two months ago. The exception: never fire in anger, and never on a Friday.

Pull 3–7 axioms maximum per response. More than that and you're dumping a list instead of giving advice. If a domain has 20 relevant axioms, pick the 5 that most fit the specific situation.

### Socratic mode

When someone is processing a live decision rather than gathering information, don't hand them the axiom. Ask the question the axiom answers. This is more powerful because it forces them to articulate what they already know but haven't faced. This mode is particularly relevant in coaching, mentoring, or peer-advisory conversations, but it also applies any time a founder is wrestling with ambivalence rather than seeking facts.

**Trigger Socratic mode when:**
- The person is helping someone else with a founder-stage decision (advisor, coach, mentor)
- The person explicitly asks for help thinking through something rather than for advice
- A coaching or reflective frame has been set earlier in the conversation
- The conversation has the texture of someone working through ambivalence rather than seeking information

**Examples of Socratic translation:**

| Axiom | Socratic question |
|---|---|
| Fire fast | "How long has it been since you first knew this person needed to go?" |
| Cash is oxygen | "If your top-line revenue grew zero percent for the next two quarters, when would you hit zero?" |
| Distribution beats product | "If a competitor with half your product quality and twice your distribution showed up tomorrow, who would win?" |
| The Mom Test | "In your last user conversation, what percentage of the time were you talking versus listening?" |
| Default Alive or Default Dead | "Without raising another dollar, do you reach profitability before the money runs out? Yes or no — what does the math actually say?" |
| Rumelt's kernel | "In two sentences: what is the critical obstacle in front of this company right now? Not the goal — the obstacle." |
| Give away your Legos | "What work are you holding onto because you love it, that someone else should own by now?" |
| The waterfall determines the payout | "If the company sold tomorrow for exactly what you raised times two — what would you personally receive? Walk me through the stack." |

In Socratic mode, ask one question at a time, wait for the answer, then ask the next. Do not stack three questions in one message.

Whenever Socratic mode is active, read `references/socratic-technique.md`. It carries the full translation table — axiom-to-question mappings across all domains — followed by the conduct of the questioning itself: sequencing (build context before firing the hard question), steelmanning before pushback, handling founder deflections ("it depends," "we're about to close," "my co-founder is fine with it"), the pre-mortem move, parking unanswered questions, and when to stop and synthesize.

**The Harris meta-axiom.** Aaron Harris (former YC partner) observed that the quality of advice depends on two things: the quality of the advisor *and* the asker's ability to describe reality to someone with less context. The second is harder and more often the limiting factor. The implication for this skill: in reflective or coaching contexts, the most valuable move is often to help the person articulate what's actually happening, not to dispense an axiom. The act of constructing the context for an outsider frequently produces the insight without any advice having been given. When a conversation feels stuck on surface symptoms, ask a question that forces the person to compress and externalize the underlying context — not a question designed to lead them to a specific axiom.

## How to choose which axioms to surface

The corpus is organized by **domain** in the `references/` directory. Read only the files relevant to the situation — don't load all of them. The current domains:

- `references/hiring.md` — Hiring, firing, comp, equity grants, the first HR hire, Horowitz's "undeniable strengths" and "right kind of ambition," Skok's behavioral test for values ("what would you do?" beats "do you believe?"), the Eric Schmidt quiet-room move, the Netflix keeper test (Elizabeth Stone), and the AI-era talent shift: systems thinkers over narrow specialists, and why to keep hiring juniors
- `references/fundraising.md` — Raising capital, terms, runway, valuations, investor relations, Skok's audience-as-hero reframe and ABC backwards design (Act → Believe → Care), the smallest-next-step ask, Lily Lyman's Five A's (Aptitude, Attitude, Ability, Authenticity, Attractor), and the AI-era weakening of the early-capital case for B2B SaaS
- `references/product.md` — Product-market fit, pivots, feature discipline, customer development, Vohra's PMF Engine with the High Expectation Customer, Bezos's Type 1 vs. Type 2 decisions, Jobs to be Done, Skok's Four U's (unworkable / unavoidable / urgent / underserved), Helen Riley's pre-declared kill criteria from Alphabet X, Emanuel's reframe of Five Whys as a stack of distinct companies, and Chesky's "you can't A/B test a sofa" plus the failed-launch triage (bad product, bad strategy, or bad execution)
- `references/sales-gtm.md` — Pricing, the founder-as-seller, sales cycles, discounting, the AARRR / Pirate Metrics funnel, Skok's SLIP test (Simple to install, Low initial cost, Instant ongoing value, Plays well), the ~10x gain/pain ratio required to overcome inertia, the "why wouldn't you buy?" inversion of the discovery interview, Gardner's sub-three-month time-to-value enterprise threshold, Green's "B2B is shoe leather, B2C is marketing" distinction, and an AI-era GTM section: building GTM like a product once convergence removes the technical differentiator, automating GTM in order of workflow legibility, the agent that inherits its teacher's ceiling, the playbook that must be written before it can be automated, running agents over call recordings, segmenting on value predictors rather than headcount, and ERR versus ARR
- `references/finance-ops.md` — Cash, burn, close cycles, CFO timing, forecasting, Paul Graham's Default Alive vs. Default Dead test, the burn-multiple benchmark ladder, the four stages of runway proximity, the SaaS expense-ratio inversion (~60% S&M / ~20% R&D at maturity), and an operating-metrics section: bookings vs. billings vs. revenue vs. ARR, cohort retention curves, logo vs. dollar retention, the Rule of 40 as a scale-stage metric, Gurley's LTV skepticism, AI-era gross margin under inference COGS, AI pilots reported as ARR and the ERR (experimental run-rate revenue) correction, and metric cadence
- `references/capital-valuation.md` — What capital costs and what the company is worth: equity as the most expensive money, payback period as the founder's hurdle rate, working capital and annual prepay as free capital, venture debt's covenant risk, compounding dilution and option pool refreshes, ARR multiples set by growth/NRR/gross margin, the liquidation waterfall and the founder dead zone, 409A vs. preferred price, down rounds vs. structure, anti-dilution mechanics, and founder secondaries. Consult for "what is this round really costing me," "what will I actually get at exit," valuation questions, debt-vs-equity, or option-value conversations with employees
- `references/exits-ma.md` — Running a sale process once you're selling: banker-or-not, manufacturing competitive tension, LOI and the cost of exclusivity, diligence as a repricing mechanism, earn-outs, escrow and indemnity, retention packages coming out of founder consideration, why deals die in the last 20%, acqui-hire pricing, and headline number vs. waterfall payout. Consult for "we got an offer," "should we hire a banker," "is this earn-out reasonable," or any live M&A process. *(For whether to take the Corp Dev meeting at all, see `yc-canon.md`; for the waterfall math, `capital-valuation.md`.)*
- `references/cofounders-equity.md` — Co-founder dynamics, splits, vesting, the founder breakup, and Green's CTO-co-founder audition rule (start them as a contractor before committing equity)
- `references/governance.md` — Boards, independent directors, board communication, Reid Hoffman's three-light framework
- `references/time-energy.md` — Founder calendar, delegation, sleep, sustainable pace, founder isolation as a systems failure with a structural fix rather than a mood to wait out, and Amar Bose's "keep your bags packed" — when leaving (a toxic environment, the wrong team, a compromising investor) is the move, not a failure of grit
- `references/customers-market.md` — Market size, distribution, competition, love vs. like, Skok's Disruptive / Discontinuous / Defensible test (sharper than "10x better"), the disruptive-business-model lever (Symantec/Norton vs. McAfee), Minimum Viable Segment, and Gardner's product-company gap (PMF earns you a Series A, not a company)
- `references/crisis-resilience.md` — Layoffs, bad news, runway crunch, CEO emotional thermostat, Horowitz's peacetime vs. wartime CEO frame, Chesky on crisis as the thing that converts a correct diagnosis into a mandate, and the Alphabet X "never throw anything away" rule for harvesting reusable tech from failed projects (Loon → Taara)
- `references/culture.md` — Company culture, values, first 20 employees, vision, hiring as the cultural filter, Skok's culture-as-operating-system frame (Enterprise Rent-A-Car on 9/11), the "bacteria default" failure mode, the "degree off course becomes a mile at scale" geometric drift, the discipline of rewarding *attempted* breakthroughs not just successful ones, Elizabeth Stone's talent density as the input every other freedom is downstream of, and why the process you add after a visible failure taxes everyone who didn't fail
- `references/startup-mechanics.md` — Incorporation, vesting, IP assignment, founder stock, Stripe Atlas vs. Clerky, the 83(b) election and e-filing via Form 15620, QSBS / Section 1202 (including the 2025 OBBBA tiered structure), Section 1045 rollovers, the pre-money option pool trap
- `references/yc-canon.md` — The Y Combinator canon, essay half: PG, Altman, Livingston, Ralston, Buchheit, Harris, and Seibel on fundraising. "Do things that don't scale," "don't talk to Corp Dev," the (b×d)/c prioritization formula, the 90/10 solution, "make what you measure / denial is the silent killer," "fundraising rounds are not milestones," momentum/post-YC slump, unit economics, "companies die of suicide not murder," the Harris meta-axiom on taking advice, and YC's pocket guide. Consult whenever a question touches early-stage decisions or could benefit from the most-cited body of startup wisdom.
- `references/yc-canon-product.md` — The Y Combinator canon, product half: Seibel, Alströmer, Migicovsky, Caldwell, Reinhardt. "Hair on fire" customers and the building-is-on-fire test for PMF, the Sean Ellis / Superhuman 40% test, the Minimum Evolvable Product, the search-vs-persuasion frame for early users, path dependency / early-user DNA, Migicovsky's five user-interview questions and the Mom Test, Reinhardt on validation, Caldwell's pivot framework with idea-quality scores, Seibel's eight mistakes and product cadence. Consult for pre-PMF questions, early-user research, and pivot decisions.
- `references/strategy-moats.md` — Durable competitive advantage: Helmer's 7 Powers (benefit + barrier test, the Power Progression, counter-positioning and cornered resource as the startup-stage powers), Rumelt's strategy kernel (diagnosis → guiding policy → coherent action) and the four signs of bad strategy, Thiel's competition-is-for-losers and start-small-and-monopolize, Greenwald's barriers-to-entry test, Christensen's disruption dynamics, Porter's compete-to-be-unique, and a quantitative section on Helmer's math (the Fundamental Equation of Strategy, differential margin, scale/network as ratios rather than ranks, the time-dependence of brand and process power). Consult whenever a question touches moats, defensibility, competition, positioning against incumbents, "what's our strategy," or investor pushback on differentiation.
- `references/management-execution.md` — Becoming a manager and building the execution machine: Grove's output equation, leverage, task-relevant maturity, 1:1s, and meetings-as-medium; Mochary's written-decision and calendar disciplines; Gil's hire-for-the-next-18-months and reorg counsel; Molly Graham's "give away your Legos"; and the founder-mode counter-canon — Chesky on never negotiating the operating model, details-are-not-micromanagement, the empowerment trap, not delegating what you're best at, bureaucracy as a dependency cascade, and metrics subordinate to the launch calendar, with Paul Graham's "Founder Mode" on skip-level engagement and the scope rule reconciling the two canons. It also carries an AI-era operating section: accountability as the one thing that can never be handed to an agent, comprehension as the binding constraint once code generation is cheap, and encoding the judgment that used to live only in the veterans' heads. Consult for questions about delegation, 1:1s, feedback, meetings, org design, reorgs, decision-making process, who owns the outcome when an agent did the work, founder mode, "am I micromanaging," whether to hire a CPO, or a founder struggling with the IC-to-manager transition. *(Mostly 10+ employees; below that, prefer `time-energy.md` and `hiring.md`.)*
- `references/socratic-technique.md` — The full axiom-to-question translation table, plus how to conduct Socratic mode: question sequencing, Rapoport's Rules steelmanning, deflection handling, the pre-mortem, parking, exit criteria. *(Table and technique, not axioms — read whenever Socratic mode is active.)*
- `references/meta.md` — Wisdom about wisdom: stage-relevance, founder peer groups, contextuality, how to take advice, Helen Riley's "rigor kills innovation if applied too early," Green's "early-stage currency is learning, not revenue," Megan Smith's scout-before-you-start rule, Skok's communication acid test (can the listener say it back?), and Chesky's disbelieve-about-thirty-percent test for whether your judgment is actually updating

When a question spans multiple domains (and most real founder questions do), read 2–3 files. Don't read more than that unless explicitly asked for a comprehensive scan.

## How to stage-match

A pre-seed founder asking about hiring needs different axioms than a Series C CEO asking the same thing. When you can infer stage from context, prefer axioms tagged for that stage. When you can't, ask one short clarifying question or pick the axioms that hold across stages.

An axiom carries a `*(Stage: …)*` tag only when it doesn't hold at every stage; an untagged axiom holds across stages and is safe to surface to anyone. Treat a tag that doesn't match the founder's stage as a reason to skip the axiom, not to caveat it.

Rough stage map:
- **Pre-seed / Seed (0–10 people)**: Co-founder dynamics, first hires, product-market fit, raising the first round
- **Series A (10–50)**: First executive hires, repeatable sales motion, building a real finance function
- **Series B (50–200)**: Layering management, board sophistication, scaling sales/marketing, real HR
- **Series C+ (200+)**: Org design, succession, professionalization, IPO-readiness

`Pre-PMF` is a tag value too, and it cuts across the headcount map — match it to whether the company has found product-market fit, not to its round.

## Output style

- Use the **bolded axiom + explanation** format above. The axiom itself should be quotable in one sentence.
- Don't over-hedge. Founders need conviction in advice; weaselly "it depends" responses are useless. When something genuinely is contextual, say so plainly and explain the dependency.
- Don't moralize. These are observed patterns, not commandments.
- When relevant, name the limit of the axiom. "Fire fast — except never in anger, never on a Friday" is more useful than just "fire fast."
- Avoid stacking unrelated axioms. Better to give three deeply relevant ones than ten generic ones.
- Benchmarks age; axioms don't. Any figure tagged *[bench YYYY-MM]* in the corpus is a market snapshot, not a law — burn multiples, CAC payback bands, Rule of 40 medians, dilution norms, and multiples all move with the funding environment. Cite the structure with conviction and the number with its vintage: "the ladder investors use is burn multiple under 1.5x — that's the benchmark as of mid-2026, worth checking current data." Never present a dated threshold as timeless.
- Attribute when relevant. Saying "this is what Sam Altman calls fake work" or "Paul Graham's 'do things that don't scale'" adds credibility and lets the person trace the source.

## What this skill is not for

- Detailed legal advice (term sheets, employment law, IP) — defer to qualified counsel.
- Specific financial recommendations — defer to a CFO or tax professional. The finance files (`finance-ops.md`, `capital-valuation.md`) give founders the mechanics and the vocabulary to ask better questions; they do not substitute for a CFO, a tax specialist, or securities counsel.
- Industry-specific operational knowledge (e.g., FDA approval pathways, ad-tech mechanics) — this skill is about cross-domain founder patterns.
- Reassurance. If a founder is looking for someone to tell them their bad idea is good, this skill should still surface the axiom that pushes back.
- Bias-free balance. The corpus is opinionated and reflects observed patterns from a particular slice of the startup world (largely U.S., largely venture-backed, largely software). Geographic, sectoral, and structural exceptions exist. Name them when relevant.

## Meta-note on use

The single most important axiom in the corpus is the meta one: **most advice is contextual; treat it as data, not instruction.** Apply this to the skill itself. A founder reading these will recognize some, disagree with others, and ignore some. That's correct. The value is in the *encounter* with the pattern, not in obedience to it.
