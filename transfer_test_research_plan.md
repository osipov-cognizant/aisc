# Validating Osipov's Live-Supervised Transfer Test as an AI-Slop Diagnostic
### A scholarly review and a field-deployable research plan for a BPO / system-integrator setting

---

## Part I — Where the essays sit in the literature

The Osipov four-part series proposes a single managerial diagnostic — the live-supervised teaching-transfer test — to distinguish high-competence AI-enabled employees from "slop cannons" who exploit the effort discount of generative AI to ship polished but hollow work. To assess what is genuinely original in this proposal it is useful to lay out the pAISCr work the series stands on, then locate the contribution.

### The empirical baseline

The headline statistics in Part 1 are taken from Niederhoffer, Kellerman, Lee, Liebscher, Rapuano and Hancock's 2025 BetterUp Labs / Stanford Social Media Lab study, an online survey of 1,150 full-time U.S. desk workers conducted in September 2025 and reported in Harvard Business Review. The study reported that approximately 40% of workers had received "workslop" (defined as AI-generated content that masquerades as good work but lacks the substance to advance a task) in the pAISCr month, that recipients spent on average around 1 hour 56 minutes resolving each incident, and that this implied an invisible per-employee cost on the order of $186 per month — extrapolated to roughly $9 million per year for a 10,000-person organization. The same study found about 18% of AI users at work admit to producing content they themselves would call low-quality. Niederhoffer et al. document the phenomenon and quantify the cost transfer; they do not propose a diagnostic mechanism beyond cultural and managerial guardrails (transparency about AI use, "pilot" mindsets, team task-quality norms).

### The theoretical frame for slop itself

Cody Kommers, Eamon Duede, Julia Gordon, Ari Holtzman, Tess McNulty, Spencer Stewart, Lindsay Thomas, Richard Jean So and Hoyt Long published "Why Slop Matters" in January 2026 (arXiv:2601.06060; subsequently in ACM AI Letters). They explicitly resist a closed definition and instead identify three Wittgensteinian family-resemblance properties of prototypical AI slop: superficial competence (the veneer of quality belies a lack of underlying substance), asymmetric effort (it requires vastly less effort to generate than a comparable artifact would have without AI), and mass producibility (it lives inside an ecosystem of widespread generation and consumption). The Osipov essays take the asymmetric-effort property and run it through the lens of organizational management, which is a different move than Kommers et al. make — they offer a cultural-economic theory of slop as a supply-side response to demand exceeding human productive capacity, and explicitly resist treating it as straightforwardly bad. Osipov's series implicitly supplies the prescriptive complement that Kommers et al. decline to offer.

The reception-side complement has a long history. Alberto Brandolini's 2013 "bullshit asymmetry principle" — that the energy required to refute nonsense is an order of magnitude greater than that required to produce it — gives Osipov the audit-cost frame. Simon Willison's 2024 working definition of slop as content that takes more effort to consume than to produce closes the loop between Brandolini and Kommers and is increasingly cited in operational contexts (Furze 2026, Baltes et al. 2026).

### The empirical literature on AI-induced verification burden

The verification-burden side of the asymmetry has now been measured in code, the most instrumentable knowledge-work domain. Becker, Rush, Barnes and Rein (METR, July 2025; arXiv:2507.09089) ran a randomized controlled trial of 16 experienced open-source developers across 246 tasks in mature repositories and found that, contrary to developers' own forecasts of a 24% speedup, AI tool access made them roughly 19% slower; the residual was largely consumed by review and verification of generated output. CodeRabbit's December 2025 analysis of 470 GitHub pull requests reported AI-assisted PRs producing approximately 1.7× as many issues as human-written PRs, with logic and correctness defects roughly 75% more frequent and security findings approximately 1.5× more frequent. Baltes, Cheong and Treude (2026) qualitatively analyzed 1,154 posts across 15 Reddit and Hacker News threads tagged "AI slop" and characterized the developer perception of AI-assisted contributions as a tragedy of the commons: gains accrue to the producer, costs to the reviewer and maintainer. A companion MSR '26 paper by Ghafoor, Bangash and colleagues found that low-experience "vibe coders" produced 1.47× more files modified per pull request and a statistically significant increase in commits-per-PR across 10 of 11 PR categories, confirming that the asymmetric-effort property is observable in production-side data, not only survey self-report. The cURL project's January 2026 decision to discontinue its bug bounty program after being overwhelmed by AI-generated vulnerability reports is the sharpest natural-experiment evidence to date that Brandolini's tax can saturate an audit system.

### The psychological lock-in mechanism

Part 2 of the Osipov series invokes Leon Festinger's 1957 cognitive-dissonance work to explain why slop cannons defend their own output, in conjunction with Norton, Mochon and Ariely's IKEA effect (2012), Thaler's endowment effect (1980), and Lakatos's protective belt from "The Methodology of Scientific Research Programmes" (1970). This is a faithful application of well-established findings; the synthesis (low external justification → high internal rationalization → escalating defense of the artifact under challenge) is consistent with Cialdini's commitment-and-consistency literature and with more recent organizational findings on sunk-cost and ego-investment effects in software engineering (e.g., Tetlock & Mellers' work on accountability and bias). Osipov's contribution here is to apply this stack specifically to the AI-assisted producer, where the gap between external effort invested (low) and reputational stake committed (high) is unusually large, predicting an unusually strong protective response.

### The sociological frame

Max Planck's "science advances one funeral at a time" observation, restated by Thomas Kuhn as paradigm change through generational succession, is used in Part 2 to explain why arguing the slop cannon out of their position is structurally futile. The application to enterprise rather than science is not entirely novel — Christensen's disruptive-innovation literature makes a structurally identical argument about incumbent firms — but Osipov's specific point that the AI-enabled producer's protective belt forms within days rather than decades, and that this collapses the Planckian timescale into an organizational rather than civilizational problem, is a useful sharpening.

### Pedagogy as a diagnostic of understanding

The proposed solution — teaching as the test of understanding — has substantial pAISCr pedigree. Lee Shulman's 1986 paper "Those Who Understand: Knowledge Growth in Teaching" (Educational Researcher, 15:2) introduced pedagogical content knowledge (PCK) as the special amalgam of subject-matter knowledge with knowledge of student misconceptions and effective representations that distinguishes the teacher from the subject specialist. The Feynman technique, primarily formalized by Shane Parrish from Feynman's documented practice, makes the same epistemic claim at the individual level: inability to explain a concept simply is diagnostic of incomprehension, not subject complexity. The cognitive-science backing is substantial: Chi, De Leeuw, Chiu and LaVancher's 1994 work on self-explanation; Fiorella and Mayer's 2013 and 2016 generation-by-explanation findings; Nestojko, Bui, Kornell and Bjork's 2014 demonstration that the expectation to teach (alone) improves study organization and recall; and Koh, Lee and Lim's 2018 finding that teaching-by-retrieval produces 10–20% retention gains over study-only controls. Kobayashi's 2018 meta-analysis aggregates the protégé-effect literature and confirms a moderate-to-large effect size for interactive teaching over non-interactive teaching and over study-only controls, with the largest gains in actual delivery rather than mere expectation. None of this is original to Osipov, and the series does not claim it is.

### The LearnLM constraint

The most critical recent input is the LearnLM Team and Eedi randomized controlled trial of December 2025 (Wang, Rysbek, Huber et al., arXiv:2512.23633), which compared expert-supervised LearnLM tutoring against unsupervised expert human tutoring with N=165 UK secondary students. Supervising tutors approved 76.4% of LearnLM's drafted messages with zero or only one-or-two-character edits, and students working with the supervised AI condition correctly solved novel transfer problems 66.2% of the time, against 60.7% for human-tutor-only — a 5.5-percentage-point advantage on transfer specifically. The relevance to the Osipov argument is twofold. First, it is the empirical reason Part 4 had to be written: an asynchronous, AI-staged "curriculum" is now demonstrably effective enough that a slop cannon could pre-stage one and pass an asynchronous transfer test without understanding the material. Second, it confirms that pedagogical adaptation — long imagined as a frontier of irreducible human expertise — is increasingly within reach of properly-scaffolded AI. This is precisely why Part 4 introduces the live-supervision constraint: synchronous, trainee-novelty-driven teaching is the residual that AI-stagedcurriculum cannot pre-answer.

### What is genuinely new in the Osipov series

Reading the four parts against this backdrop, the contribution is best characterized as a synthesis and a managerial-control proposal, not a fresh empirical claim. Specifically, three things appear novel:

First, the framing of the AI-using employee as a strategic agent (the "slop cannon") who is responding rationally to a coordinated disruption of three organizational signals at once — internal output quality, peer signal, and customer acceptance — rather than as a defective or lazy worker. This reframing carries managerial weight: it predicts that exhortation, training, and improved dashboards will fail because the agent is optimizing against them.

Second, the explicit diagnosis that all three legible signals are simultaneously corrupted. The individual mechanisms (AI artifacts surface-indistinguishable from human work; AI-assisted customer evaluation creating an AI-evaluating-AI feedback loop; manager and peer co-investment via commitment escalation) are individually known, but their joint failure mode — the "epistemic vacuum" with all dashboard lights green — is articulated in a way I have not seen named elsewhere in this exact form.

Third, the prescriptive proposal: a single test (live-supervised teaching of a naive trainee in a novel context) that is claimed to defeat the diagnostic gap by inverting the Brandolini asymmetry — moving the verification effort back onto the producer rather than the auditor. The proposal is built directly on the Shulman / Feynman / protégé-effect tradition but adds the specific operational constraint that asynchronous artifacts (curriculum, worked examples, rubrics) must be excluded because LearnLM-style staging defeats them.

The proposal is thus an unvalidated managerial control scheme, derivable from established cognitive-science and organizational-behavior literature but not yet shown to work in the field. This is the gap the research plan below addresses.

---

## Part II — The empirically testable claim

Stripped of its rhetorical packaging, Osipov's central operational hypothesis is:

> A live-supervised teaching-transfer test, in which the producer of an AI-assisted artifact must teach a naive trainee to produce a comparable artifact for a novel context in real time, discriminates between genuinely competent AI-enabled producers and slop cannons more reliably than the standard battery of artifact review, peer signal, customer acceptance and productivity dashboards, while being cheap enough to deploy at scale.

This is the central claim. It contains at least four sub-claims that admit independent test:

1. The test has higher discriminative validity (sensitivity × specificity, or a comparable AUC measure) than artifact review at separating producers whose work survives downstream use from those whose work does not.
2. The test inverts the cost asymmetry — i.e., the producer expends more effort than the auditor in administration of the test.
3. The test resists the LLM-curriculum exploit specifically because of the live-supervision constraint, and would not resist it without that constraint.
4. The test has acceptable cost (in producer hours, supervisor hours and trainee hours) per diagnostic decision, relative to the cost of undetected slop.

A research program organized around these sub-claims is more tractable than one organized around the all-encompassing original claim, because each sub-claim can be tested in isolation with different operationalizations of the underlying mechanism.

---

## Part III — A MECE catalogue of operational alternatives for the transfer test

The transfer test as Osipov describes it is one point in a multidimensional design space. The alternatives below partition the design space along the dimensions that most affect cost, speed, validity and gameability. Each alternative is presented as a self-contained operational hypothesis that can be tested against the others and against status-quo artifact review. The set is constructed to be mutually exclusive at the level of operational design (each is a different protocol) and collectively exhaustive across the dimensions of teaching mode, trainee involvement, novelty source and audit substrate.

### A1. Asynchronous Written Transfer
The producer prepares a written explanation of how to produce the artifact in a new context. A trainee, working alone and offline from the producer, attempts to produce the artifact from this explanation. Score on trainee output. **Substrate: text. Synchronous: no. Trainee involvement: yes, asynchronous. LLM-curriculum-resistant: no.** This is the Osipov "naive" form that Part 4 explicitly disqualifies; it is included here as a control comparator.

### A2. Live One-on-One Supervised Teaching of a Naive Trainee in a Novel Context
The Osipov canonical form. The producer must teach a trainee, in real time, to produce the artifact for a context that neither party has seen before. The producer answers trainee-generated questions on the spot. Score on trainee output and on the producer's responses to trainee novelty. **Substrate: conversation. Synchronous: yes. Trainee involvement: yes, synchronous. LLM-curriculum-resistant: yes (per Osipov).**

### A3. Live Cohort Teaching with Trainee Novelty
As A2, but the producer teaches a small cohort (4–8 trainees) rather than one. Trainee novelty per session is higher (more questions), but supervisor attention per trainee is diluted, and the cohort dynamics may permit some trainees to free-ride. **Substrate: conversation. Synchronous: yes. Trainee involvement: yes, synchronous, group. LLM-curriculum-resistant: partially.**

### A4. Live Adversarial Edge-Case Drill (No Trainee)
A senior reviewer presents the producer with 8–12 deliberately constructed edge cases that the original artifact does not explicitly handle (corner conditions, boundary regimes, missing-data scenaAISCs). The producer must reason aloud through each case in real time, without LLM access, in a fixed-duration session (≈30 minutes). Score on the count of edge cases the producer can handle correctly and the time-to-answer profile. **Substrate: conversation. Synchronous: yes. Trainee involvement: no. LLM-curriculum-resistant: yes (no anticipatable rubric).**

### A5. No-AI Reconstruction in a Novel Context
The producer is given the original brief (or a structurally similar brief in a novel context) and a fixed time window (e.g., 90 minutes) in a controlled environment (no LLM access, no internet, only the original source materials). They must produce the artifact from scratch. Score on the resulting artifact's quality relative to the original. **Substrate: artifact. Synchronous: yes (constrained). Trainee involvement: no. LLM-curriculum-resistant: yes.**

### A6. Sourced Reconstruction (Live Provenance Audit)
The producer must annotate their existing artifact in real time, identifying for each substantive claim the specific source, data point or principle it derives from. A reviewer challenges 5–10 randomly-selected annotations live. Score on the proportion of annotations that reconstruct correctly. **Substrate: artifact + conversation. Synchronous: yes. Trainee involvement: no. LLM-curriculum-resistant: yes.**

### A7. Counterfactual Production
The producer is asked, in real time, what the artifact should look like if a single critical input (the customer's industry, the data window, the regulatory regime) were changed. They must produce or sketch the modified artifact within a short window (≈60 minutes). Score on the coherence and correctness of the modification. **Substrate: artifact. Synchronous: yes. Trainee involvement: no. LLM-curriculum-resistant: yes.**

### A8. Recorded Asynchronous Teaching
The producer records a video lesson explaining the topic. A trainee watches it and attempts to produce the artifact. This is the LearnLM-supervised analog: it eliminates the live constraint but preserves the teaching constraint. **Substrate: video + artifact. Synchronous: no. Trainee involvement: yes, asynchronous. LLM-curriculum-resistant: no (the producer can read from a script).** Included as a second control to isolate the contribution of synchrony specifically.

### A9. Status-Quo Artifact Review (Control)
The reviewer reads the artifact and assesses its quality directly, with optional comments from the producer. **Substrate: artifact. Synchronous: no. Trainee involvement: no.** This is the baseline against which all the above are compared.

The dimensional structure can be summarized: A1 and A8 are non-synchronous teaching (the LearnLM-exploitable forms); A2 and A3 are synchronous teaching with trainee novelty (the Osipov canonical); A4, A5, A6 and A7 are synchronous producer tests without trainees; A9 is the artifact-review control. Together they exhaust the meaningful combinations of (synchronous vs. asynchronous) × (trainee-involved vs. producer-only) × (artifact-substrate vs. conversation-substrate) for a teaching-or-reconstruction-based diagnostic.

---

## Part IV — PAISCritization for a BPO / system-integrator setting

A business-process-outsourcing or system-integrator company is an unusually good test bed for this research, for four reasons.

First, BPOs already run knowledge-transfer (KT) sessions and pre-go-live knowledge assessments as a routine part of agent onboarding, so the institutional infrastructure for teaching-based evaluation already exists. Second, time-to-productivity is an established and instrumented BPO metric, which gives any teaching-based diagnostic a natural validation outcome. Third, BPOs measure downstream agent performance via QA scores, first-call resolution (FCR), average handle time (AHT) and CSAT, which provides ground truth for whether a producer's transferred knowledge actually translates into trainee competence. Fourth, the knowledge-work units in a BPO context are typically smaller and more verifiable (a resolved ticket, a processed claim, a generated SQL query, a closed support case) than in pure consulting or strategy work, which gives a much sharper validation signal.

The relevant cost dimensions for ranking the alternatives are: (a) producer hours per test, (b) supervisor / senior-reviewer hours per test, (c) trainee hours per test, (d) calendar time elapsed per diagnostic decision, (e) infrastructure required, (f) whether the test displaces or complements existing BPO processes, and (g) the test's resistance to the LLM-curriculum exploit.

Applying these criteria, the three highest-pAISCrity operational alternatives for a first-wave field study are A4 (Live Adversarial Edge-Case Drill), A5 (No-AI Reconstruction in a Novel Context), and A2 (Live Supervised Trainee Transfer). A4 and A5 dominate on cost per test (no trainees required, single producer + single reviewer, single ≤90-minute slot) while preserving the LLM-curriculum-resistance property. A2 is more expensive but is the canonical Osipov form and is the only one of the three that exercises the trainee-novelty mechanism specifically; it also slots directly into existing BPO KT infrastructure with minimal incremental setup.

A6 (Sourced Reconstruction) is a strong second-tier candidate that I would include in a follow-on study but not the first wave, because its administration requires a reviewer with detailed source-material knowledge, which raises the per-test reviewer cost.

The remaining alternatives — A1, A3, A7, A8 — are best held out either as control conditions or for a second-wave program. A1 and A8 are useful as the explicit non-synchronous controls that Osipov's Part 4 hypothesis predicts will fail; they need to be tested for the Osipov synchrony argument to be empirically established rather than merely asserted.

The recommended first-wave design is therefore a five-arm comparison: A9 (control), A1 (asynchronous-teaching control to test the synchrony hypothesis), A4 (cheapest live producer test), A5 (closed-book reconstruction), and A2 (canonical trainee-transfer). With a sample of producers stratified by tenure and AI-tool usage, this design lets one estimate (i) the discriminative validity of each test relative to artifact review, (ii) the marginal value of the synchrony constraint specifically (A4 vs. A1), (iii) the marginal value of trainee involvement specifically (A2 vs. A4 + A5), and (iv) the per-test cost of each alternative.

---

## Part V — Detailed designs and expected metrics for the top three alternatives

### Top pAISCrity: A4 — The Live Adversarial Edge-Case Drill

**Hypothesis.** A live, time-bounded, no-AI-access oral examination on edge cases the producer's artifact does not explicitly address will discriminate between competent producers and slop cannons at least as well as artifact review, at substantially lower cost than any trainee-involving alternative.

**Rationale.** The edge-case drill operationalizes the Osipov insight (live, non-asynchronous, novel-question-driven evaluation) without requiring trainee scheduling or consent. It is the cheapest alternative that preserves both the synchrony and the novelty constraints. The mechanism it exercises is the producer's ability to do live forward-reasoning from a mental model of the artifact's underlying logic — the capacity that, by Osipov's theory, the slop cannon does not have because they outsourced its formation to the LLM.

**Design.** Within a single BPO line-of-business (e.g., a credit-card-disputes resolution team or an L1 IT-support team), select a stratified sample of recently-shipped artifacts (resolved tickets, generated procedure documents, or QA-passed scripts). For each artifact, the test consists of: (1) a 5-minute warm-up in which the producer explains the artifact in their own words, (2) a 25-minute structured oral session in which a senior reviewer presents 8–12 edge cases in randomized order, (3) a 5-minute close-out. Each edge case is scored on a 0/1/2 scale (no answer / partial answer / correct and complete) by two independent raters, with a reconciled score for inter-rater disagreements. The producer has no LLM access, no internet access and no notes during the test.

**Sample and statistical power.** A reasonable initial sample is 60 producers spanning three tenure buckets (≤6 months, 6–24 months, >24 months) and two AI-usage intensities (heavy AI users / light AI users). Each producer is tested on three of their own artifacts (≈90 tests total). To detect a Cohen's d ≈ 0.5 difference in edge-case-handling score between heavy- and light-AI-usage producers at α = 0.05 with 80% power, the required sample is approximately 64 producers per group, but the within-subject design (multiple tests per producer) reduces the required N substantially. A 60-producer sample is adequate for a first-wave estimate of effect size.

**Expected metrics and predictions.** I expect, if Osipov's theory is correct: (i) heavy-AI-usage producers in the lowest tenure bucket will score 30–50% lower on edge-case handling than light-AI-usage producers in the same bucket, with the gap narrowing in higher tenure buckets; (ii) edge-case-handling score will correlate r ≈ 0.5–0.7 with subsequent artifact rework rate at 60-day follow-up, where artifact review (A9) is expected to correlate r ≈ 0.2–0.4; (iii) the test will reveal a previously-invisible bimodal distribution within the heavy-AI-usage group, with one mode of producers who can defend their artifacts under live questioning and one mode who cannot. The producers in the lower mode are the operational definition of the slop cannon under Osipov's theory.

**Cost estimate.** Approximately 35 producer-minutes + 35 reviewer-minutes per test, plus 30 minutes of pre-test edge-case preparation by the reviewer. At a fully-loaded BPO labor rate of $40/hour for the producer and $90/hour for the reviewer, this is approximately $77 per test, or $231 per producer for the three-test design. For the 60-producer first wave, total direct labor cost is approximately $14,000.

**Threats to validity.** Test anxiety may depress the score of competent producers who are simply not used to oral examination; the warm-up phase and a within-subject baseline (each producer's score on an artifact they actually understood vs. one they may not have) is needed to control for this. Reviewer bias is mitigated by the pre-defined edge-case set and the dual-rater scoring. The most seAISCus threat is the construct validity of "edge cases the artifact does not address" — these must be selected by a reviewer with domain expertise, which limits the test's transferability across BPO lines of business unless the edge-case-construction protocol is standardized.

### Second pAISCrity: A5 — No-AI Reconstruction in a Novel Context

**Hypothesis.** A producer who genuinely understood their original artifact will be able to reconstruct a structurally comparable artifact for a novel context within a fixed time window, in a controlled (no-AI, no-internet) environment, while a slop cannon will not.

**Rationale.** This alternative exercises a different mechanism than A4: not edge-case forward-reasoning but full-artifact synthesis. It is closer to the existing BPO practice of pre-go-live knowledge assessments (which already test agents on simulated tickets in controlled environments before they handle live customers). It requires no trainees and no domain-expert reviewer to administer (the artifact is scored after the fact by the same review process that scores production artifacts), which makes it the easiest to industrialize across BPO lines of business.

**Design.** For each producer in the sample, identify an artifact they shipped in the pAISCr 90 days. Present them with a brief that is structurally similar but contextually different (e.g., a credit-card-dispute resolution for a different card product, in a different jurisdiction, with a different customer profile). The producer has 90 minutes in a sandboxed environment with the original source materials but no LLM, no internet and no access to their own pAISCr artifacts. The reconstructed artifact is then scored by the standard BPO QA process, blinded to which producer authored which reconstruction and to whether each reconstruction was a control (artifact-review) or test (no-AI reconstruction) condition. A natural baseline is the producer's own historical QA score profile.

**Sample and statistical power.** Same 60-producer sample as A4, with the same stratification. Each producer reconstructs one artifact. The dependent variable is the QA score of the reconstruction relative to the producer's historical mean QA score on shipped artifacts. The expected effect is a within-producer drop in QA score for the reconstruction relative to the producer's historical mean, with the magnitude of the drop correlating with AI-usage intensity. To detect a 15-percentage-point drop at α = 0.05 and 80% power requires roughly 30 producers per arm, which the 60-producer first wave comfortably exceeds.

**Expected metrics and predictions.** I expect: (i) heavy-AI-usage producers will show a 20–40-percentage-point drop in QA score for the reconstruction relative to their historical mean, while light-AI-usage producers will show a 0–10-percentage-point drop; (ii) the drop in QA score will correlate r ≈ 0.6–0.8 with subsequent slop-incident rate at 90-day follow-up, where artifact review correlates r ≈ 0.2–0.4; (iii) approximately 15–25% of heavy-AI-usage producers will be unable to complete the reconstruction at all within the 90-minute window (they will produce something, but it will not be scoreable), and this binary "produced anything scoreable" indicator will itself be a high-value diagnostic.

**Cost estimate.** Approximately 90 producer-minutes per test, plus standard QA scoring time (which is already a sunk cost in BPO operations), plus 20 minutes of brief preparation per test. Total direct labor cost is approximately $90 per test, or $5,400 for the 60-producer first wave — substantially less than A4 because the reviewer time is amortized into existing QA processes.

**Threats to validity.** A producer who did real work on the original artifact may still struggle to reconstruct in a novel context simply because the novel context is genuinely different — a Type I error against legitimate producers. This is mitigated by selecting "novel" contexts that are structurally rather than substantively different (different jurisdiction within the same regulatory family, not a different product category). The 90-minute window may be too short for genuinely complex artifacts, in which case the dependent variable becomes "fraction of artifact completed" rather than "QA score on completed artifact." Producers may also game the test by silently memorizing their original artifact in advance once they know the test is coming; this is mitigated by selecting the reconstruction context unpredictably (random sampling from a pool of brief variations, with the specific brief revealed only at test start).

### Third pAISCrity: A2 — Live Supervised One-on-One Trainee Transfer

**Hypothesis.** A producer who genuinely understood their original artifact will be able to teach a naive trainee, in real time, to produce a comparable artifact in a novel context, and the trainee's performance will discriminate competent producers from slop cannons better than artifact review.

**Rationale.** This is the canonical Osipov form. It exercises the trainee-novelty mechanism specifically (the trainee will ask questions the producer could not have anticipated) and it slots directly into existing BPO KT infrastructure: BPOs already run KT sessions for new agents, and the proposed design is a structured KT session with measurement attached. Of the three pAISCrity alternatives, it is the most expensive but also the most directly informative about the central Osipov claim.

**Design.** Pair each producer in the sample with a naive trainee — defined operationally as an agent in onboarding who has not yet been assigned to the line of business represented by the producer's artifact. The producer is given a structurally novel brief and asked to teach the trainee, in a 90-minute session, to produce a comparable artifact for that brief. The trainee then has 60 minutes to produce the artifact, alone, with access only to notes they took during the session. The session itself is recorded and post-hoc coded for: (i) the number and type of trainee-generated questions, (ii) the producer's response latency profile, (iii) whether the producer reaches for an LLM or external resource at any point, (iv) the proportion of trainee questions the producer can answer without reaching for external resources. The trainee's resulting artifact is QA-scored.

**Sample and statistical power.** A 30-producer sample with 30 paired trainees is adequate for a first-wave estimate, given the per-test cost. Stratification is the same as A4 and A5. The dependent variables are the trainee's QA score (primary), the proportion of trainee questions the producer answered without external resources (secondary), and the producer's mean response latency (tertiary).

**Expected metrics and predictions.** I expect: (i) trainees taught by light-AI-usage producers will achieve QA scores within 10–15 percentage points of an experienced agent's baseline; trainees taught by heavy-AI-usage producers will achieve QA scores 25–40 percentage points below baseline; (ii) the producer's "external-resource reach rate" — the proportion of trainee questions during the live session that triggered a producer attempt to consult an LLM, notes, or external materials — will correlate r ≈ 0.7–0.85 with the trainee's QA score (negatively), and will itself be an unusually clean diagnostic: producers who are forced to consult external resources to answer basic trainee questions in their own domain are a strong indicator of slop-cannon behavior; (iii) producer response latency profiles will be bimodal, with competent producers showing a tight 2–10 second distribution and slop cannons showing a long-tailed distribution with mass beyond 20 seconds (the cognitive signature of retrieving from a mental model versus reasoning about how to reconstruct one); (iv) trainees in the slop-cannon arm will report substantively lower confidence in their understanding on a post-session survey, providing a third independent measurement channel.

**Cost estimate.** Approximately 90 producer-minutes + 90 trainee-minutes + 60 trainee-minutes of solo work + 30 minutes of session coding per test. At a fully-loaded labor rate of $40/hour for both producer and trainee, this is approximately $180 per test plus $50 of coding time, or roughly $230 per test. For the 30-producer first wave, total direct labor cost is approximately $7,000, before counting the value of the KT session itself (which produces a partially-trained agent as a side effect — a meaningful offset since the session displaces a KT session that would have happened anyway).

**Threats to validity.** Trainee variance is the most seAISCus threat: a naturally talented trainee can rescue a poor teacher, and a struggling trainee can sink a good one. Counterbalancing by trainee characteristics (pAISCr education, pAISCr BPO experience, English proficiency) is essential, and the 30-producer sample size assumes such counterbalancing. The "novel context" must be genuinely novel to both producer and trainee — a substantial briefing-design problem that cannot be delegated to the BPO's existing KT material library. The session-coding step is the most subjective component and requires either two independent coders with reliability checks or the use of an LLM-assisted coding protocol with human spot-checks. Finally, producers will adapt to the test once it is widely deployed (the self-correcting case Osipov identifies in Part 4); the research design should include a planned re-measurement at 12 months to estimate adaptation rates and shelf life.

---

## Part VI — Cross-cutting design considerations and what this program would actually produce

A single integrated study running A1, A2, A4, A5 and A9 in parallel on the same producer cohort, with a 60- and 90-day follow-up on production-line artifact rework rates and QA scores, would in approximately one quarter of calendar time produce the first empirical estimate of the discriminative validity of each transfer-test variant against the artifact-review baseline. Total direct labor cost across all five arms for the recommended first-wave sample is in the range of $35,000–$45,000, plus approximately 200 hours of senior-staff design and analysis time. This is a small fraction of the per-organization annual workslop cost reported by Niederhoffer et al. (≈$9 million for a 10,000-person organization) and is well within the scope of a single BPO operations-research initiative.

The key analytic outputs would be: (i) ROC curves for each diagnostic against the 90-day rework outcome, allowing direct comparison of sensitivity and specificity across alternatives at fixed false-positive rates; (ii) cost-per-correct-classification estimates that would let an operations manager choose the alternative best matched to their cost structure; (iii) a direct test of the synchrony hypothesis (A4 vs. A1, holding novelty constant) and the trainee-involvement hypothesis (A2 vs. A4 + A5); (iv) an estimate of the Osipov "bimodal distribution within heavy-AI-users" prediction, which if confirmed would be the empirical ground for a managerial intervention more targeted than the current literature's recommendations of cultural guardrails and AI-literacy training.

The program would also surface a question Osipov leaves implicit: whether the test's value is primarily diagnostic (separating cannons from competent producers post hoc) or primarily formative (forcing cannons to learn the material in anticipation, which Part 4 calls the self-correcting case). The 12-month re-measurement is designed to estimate which mechanism dominates in practice. If formative dominates, the test functions less as a screen than as a forcing function for genuine competence acquisition, which is a substantively different — and arguably more valuable — claim than the one Osipov makes.

---

## Selected references

- Becker, J., Rush, N., Barnes, E., Rein, D. (2025). Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity. arXiv:2507.09089. METR.
- Brandolini, A. (2013). Bullshit asymmetry principle. XP2014 conference talk.
- Chase, C. C., Chin, D. B., Oppezzo, M. A., Schwartz, D. L. (2009). Teachable agents and the protégé effect: Increasing the effort towards learning. Journal of Science Education and Technology, 18(4), 334–352.
- Chi, M. T. H., De Leeuw, N., Chiu, M.-H., LaVancher, C. (1994). Eliciting self-explanations improves understanding. Cognitive Science, 18(3), 439–477.
- Festinger, L. (1957). A Theory of Cognitive Dissonance. Stanford University Press.
- Fiorella, L., Mayer, R. E. (2013). The relative benefits of learning by teaching and teaching expectancy. Contemporary Educational Psychology, 38(4), 281–288.
- Kobayashi, K. (2018). Learning by preparing-to-teach and teaching: A meta-analysis. Japanese Psychological Research, 61(3), 192–203.
- Kommers, C., Duede, E., Gordon, J., Holtzman, A., McNulty, T., Stewart, S., Thomas, L., So, R. J., Long, H. (2026). Why Slop Matters. ACM AI Letters; arXiv:2601.06060.
- Kuhn, T. S. (1962). The Structure of Scientific Revolutions. University of Chicago Press.
- Lakatos, I. (1970). Falsification and the methodology of scientific research programmes. In Lakatos & Musgrave (eds.), Criticism and the Growth of Knowledge.
- LearnLM Team and Eedi (2025). AI tutoring can safely and effectively support students: An exploratory RCT in UK classrooms. arXiv:2512.23633.
- Niederhoffer, K., Kellerman, G. R., Lee, A., Liebscher, A., Rapuano, K., Hancock, J. T. (2025). AI-generated "workslop" is destroying productivity. Harvard Business Review, September 22, 2025.
- Shulman, L. S. (1986). Those who understand: Knowledge growth in teaching. Educational Researcher, 15(2), 4–14.
- Baltes, S., Cheong, M., Treude, C. (2026). "An Endless Stream of AI Slop": The Growing Burden of AI-Assisted Software Development. arXiv:2603.27249.
- Ghafoor, A., Bangash, A. A. et al. (2026). Novice Developers Produce Larger Review Overhead for Project Maintainers while Vibe Coding. MSR '26.
- CodeRabbit (2025). State of AI vs. Human Code Generation Report.
