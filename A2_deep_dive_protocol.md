# A2 — Live Supervised One-on-One Trainee Transfer
### A field-deployable protocol for a BPO / system-integrator setting

This document is a deep elaboration of Alternative A2 from the broader transfer-test research plan. It is intended to function as an implementation protocol — sufficient detail that a BPO operations team could budget it, get it approved by labor relations and information security, run a pilot, and produce defensible evidence for or against Osipov's central claim within a single calendar quarter.

---

## 1. What this test actually measures

Before the operational details, it is worth being explicit about the underlying construct, because the protocol's design choices follow from it. The live supervised one-on-one trainee transfer is not a test of "does the producer know their material" in the abstract — it is a test of whether the producer holds an internal causal model of the artifact's logic that is generative enough to (a) be reorganized in real time around an unfamiliar context, (b) be expressed in language the producer did not pre-rehearse, and (c) survive interrogation by a counterparty whose questions the producer could not have anticipated.

This is a sharper construct than "understanding" or "expertise" in the colloquial sense. A producer who memorized the exact artifact perfectly will fail this test. A producer who can recite a polished explanation but cannot adapt it to a structurally novel context will fail this test. A producer who built the artifact by composing LLM outputs without internalizing the chain of reasoning behind them will fail this test, by Osipov's prediction, almost categorically.

The construct draws on two converging traditions. From cognitive science, it operationalizes what Chi, De Leeuw, Chiu and LaVancher (1994) called productive self-explanation — the ability to generate explanations that go beyond the surface features of the studied material — and what Fiorella and Mayer (2016) demonstrated is strongest precisely when the explainer must produce explanations without referring back to the source. From the pedagogy literature, it operationalizes Shulman's (1986) pedagogical content knowledge: not raw subject knowledge, but the integrated capacity to anticipate and respond to the specific misconceptions of a learner who lacks the producer's background. The reason the trainee must be naive is that a peer counterparty will share the producer's blind spots; only an outsider's questions will surface gaps that the producer does not know they have.

The reason the test must be live and synchronous is the LearnLM constraint: the LearnLM Team and Eedi (2025) RCT demonstrated that a pedagogically fine-tuned model with the right context can produce expert-approved tutoring messages 76.4% of the time and improve student transfer by 5.5 percentage points over unsupervised human tutoring. A producer with LLM access and time to prepare can therefore stage a curriculum of arbitrary quality and pass an asynchronous teaching test without holding the underlying causal model themselves. Live, real-time interaction with a trainee whose questions cannot be pre-fetched is, on current evidence, the residual that remains outside this exploit.

The dependent measure is therefore not the producer's exposition quality (which is gameable) and not the trainee's eventual mastery (which is too noisy and too many steps removed from the producer). The dependent measure is the trainee's ability to produce a passable artifact independently after the session, conditioned on the producer's real-time behavior during the session — which lets us decompose how much of the trainee's outcome is attributable to teaching quality versus trainee characteristics. This is a closer analog of the Eedi protocol than of any standard performance review.

## 2. The central hypothesis and its decomposition

The central hypothesis is:

> A producer who genuinely understood and internalized the construction of their AI-assisted artifact will be able to teach a naive trainee, in real time and in a structurally novel context, to produce a comparable artifact at acceptable quality, while a slop-cannon producer — one whose original artifact was assembled from LLM output without internalization — will not.

This central claim decomposes into four sub-hypotheses, each of which is independently testable and each of which sharpens or constrains the central claim if it fails on its own.

H2a (the discriminative validity claim): Trainee artifact-quality scores will significantly differentiate producers stratified by AI-usage intensity, with the gap appearing only for trainees in genuinely novel contexts and not for trainees in same-context conditions.

H2b (the live-interaction claim): The producer's behavior during the live session — specifically, response latency to trainee-generated questions, frequency of reaching for external resources, and proportion of trainee questions answered without falling back to the artifact text — will predict trainee outcomes incrementally beyond what a transcript or a recording alone would predict. If H2b fails, then the synchronous element is not contributing what Osipov claims and a recorded asynchronous teaching protocol (A8) would be sufficient.

H2c (the trainee-novelty claim): Trainees in the live one-on-one condition will generate questions that the producer could not have plausibly anticipated, and the producer's handling of these specifically (rather than of the rehearsable material) will drive the diagnostic signal. If H2c fails, then trainees are functioning as a kind of expensive prompt-generator and the cheaper Edge-Case Drill (A4) captures the same signal.

H2d (the cost-effectiveness claim): The diagnostic value per dollar of A2 will exceed that of the artifact-review baseline, justifying its deployment in operational settings even though it is more expensive per test than A4 or A5.

A clean program tests all four; an abbreviated program tests H2a and H2d, on the understanding that null findings on either are dispositive against the central claim.

## 3. Why this alternative is uniquely informative

A2 occupies a specific point in the design space that no other alternative reaches. A4 and A5 — the producer-only tests — exercise the producer's mental model but provide no information about whether the producer can transfer it. A1 and A8 — the asynchronous teaching alternatives — exercise the transfer mechanism but lose the live constraint that defeats LLM-staged curricula. Only A2 exercises both the producer's internal model and the live, novelty-driven transfer mechanism in one test.

Two further properties make A2 uniquely valuable in a BPO context. First, the trainee in A2 is not wasted — the session produces a partially-trained agent as a side-effect, which means the operational cost is partly defrayed by the value of the training itself. (This is directly analogous to the LearnLM/Eedi protocol, where the supervised AI tutor's instruction was not wasted on the student even when its primary purpose was research.) Second, the BPO already runs knowledge-transfer (KT) sessions as a routine part of agent onboarding; A2 is recognizable to the BPO as a structured KT session with measurement attached, rather than as a foreign research instrument that will need new categories of stakeholder approval. This dramatically reduces the friction of getting the test approved by labor relations, finance and operations.

The cost is real — A2 is roughly three times the per-test cost of A4 and roughly two and a half times the per-test cost of A5 — but the diagnostic information is qualitatively different. A2 is the only test that surfaces the bimodal distribution of teaching capacity within the heavy-AI-using producer population, which is the empirical claim that most directly speaks to Osipov's central thesis.

## 4. The full protocol

The protocol is structured as four phases. Phase 0 is pre-test setup and runs continuously across the study. Phases 1–3 are the per-test sequence and run for each producer–trainee pair.

### Phase 0 — Pre-test setup (continuous)

Three pre-test workstreams need to be running in parallel before any test sessions begin: brief construction, trainee recruitment and matching, and producer notification.

**Brief construction.** For each line of business in the study, the research team constructs a brief library — a set of structurally novel briefs that share the same procedural logic as the original artifacts in scope but differ along at least two of: customer segment, jurisdiction, product line, channel, escalation tier, and data inputs. A useful target is 30 briefs per line of business at study start, with pilot validation that each brief produces an artifact of comparable scope to the originals (within ±25% of typical artifact word count or ticket length). Briefs must not be constructible by simple prompt rewriting — that is, the LLM-staged-curriculum exploit must not be able to produce a passable artifact for the brief just by pattern-matching on the original artifacts. The brief library is locked before any testing begins and producers are not informed which brief they will receive until the session start. This is the single most critical and most labor-intensive component of the study; section 5 covers it in detail.

**Trainee recruitment and matching.** Trainees are drawn from the BPO's onboarding pipeline. The operational definition of "naive" is: an agent in their first 30 days post-hire who has been assigned to a different line of business than the producer's. This eliminates contamination from prior exposure to the specific procedures, while preserving the trainee's general BPO orientation (so that the test is measuring transfer of substantive content, not basic platform familiarity). Trainees are matched to producers using a simple stratification on prior education, prior call-center experience (in years), and English proficiency band. Matching is not blocking — each producer is randomly paired with one trainee from the matched pool — but the stratification ensures that systematic trainee differences are balanced across the producer arms.

**Producer notification.** Producers in the study are informed at recruitment that they will be asked to teach a new agent in a live session. They are not informed which of their artifacts will be the test subject and they are not informed of the brief until session start. This is essential: the test is meaningless if the producer has time to study or restage the material with LLM assistance. The notification window is kept short (24–48 hours before the session) to minimize anticipatory rehearsal. Producers consent to the recording of the session for QA purposes, which is already standard BPO practice, so this requires no special-purpose consent mechanism.

### Phase 1 — The 90-minute session

The session itself is structured into five blocks. Total duration is 90 minutes plus a 15-minute buffer for setup and post-session debrief.

**Block 1 — Orientation (5 minutes).** The supervising researcher introduces the producer and trainee, confirms recording consent on both sides, and presents the brief. The brief is presented verbally and in writing simultaneously and is the first time either party sees it. The producer is told they have 85 minutes to teach the trainee enough to produce the artifact independently afterward. They are told they may use any internal resources (knowledge base, source documents, the original artifact) but no LLM and no internet. This constraint is enforced by the controlled environment in which the session takes place (a sandboxed terminal or a moderated Zoom session with screen sharing enabled).

**Block 2 — Producer-led exposition (25 minutes).** The producer explains the brief, the approach they would take, and walks the trainee through the structure of the artifact they would produce. The trainee is encouraged but not required to ask questions during this block. The session researcher observes silently and timestamps notable events (long pauses, producer reaching for resources, signs of producer struggle).

**Block 3 — Trainee question-driven phase (40 minutes).** The trainee is given a structured question prompt sheet — not specific questions, but categories of questions to surface during this block (questions about why a particular step is needed, questions about what happens if a stated condition is not met, questions about how to handle a deliberately ambiguous case in the brief, questions about what the underlying business or regulatory constraint is, questions about how the producer would know if the artifact were wrong). The trainee is instructed to ask at least eight questions across at least four of the five categories during this block. This trainee structure is important: without it, naive trainees default to passive listening, which deprives the test of its core mechanism.

**Block 4 — Trainee-led summary (15 minutes).** The trainee summarizes back what they have learned, identifies aspects they are still uncertain about, and asks any final clarifying questions. The producer can correct misunderstandings but cannot teach new material in this block. This block is diagnostic for both parties: it reveals what actually transferred (the trainee's summary as a low-bandwidth restatement of the producer's mental model) and how the producer responds to imperfect comprehension.

**Block 5 — Producer-only debrief (5 minutes).** The trainee leaves. The researcher asks the producer three structured questions: (i) what did the trainee not understand that they should have? (ii) what would you do differently if you taught this again? (iii) on a scale of 1 to 7, how confident are you that the trainee will produce a passable artifact independently? These responses are recorded but kept blinded to scorers in Phase 3.

### Phase 2 — Trainee independent work (60 minutes)

Immediately following the session — the same day, ideally within an hour — the trainee is moved to a sandboxed environment and given 60 minutes to produce the artifact for the brief. They have access only to: the brief itself, the notes they took during the session, and the BPO's standard knowledge base (which they would have access to in normal operation). They have no access to the producer, no access to LLM tools, no access to the original artifact, and no access to a session recording. The 60-minute window is shorter than typical artifact production time (which deliberately stresses the trainee's grasp of the material; a producer who taught well will have given the trainee enough scaffolding to work efficiently, while a producer who taught poorly will leave the trainee floundering). The trainee's resulting artifact is the primary dependent variable.

### Phase 3 — Scoring and coding

Three independent scoring streams run on the data collected.

**Stream A — Trainee artifact QA scoring.** The trainee's artifact is scored using the BPO's standard QA rubric for that line of business, by QA scorers blinded to which producer authored the originating session and to which arm of the study the producer belongs. This produces the primary dependent variable: a 0–100 quality score per trainee artifact, comparable to scores produced for live agent work.

**Stream B — Session video coding.** Two independent trained coders watch the session recording (or work from the transcript and audio) and code along the dimensions specified in section 8 below. Inter-rater reliability is assessed using Cohen's kappa for categorical codes and intraclass correlation for continuous codes; a target of κ ≥ 0.7 and ICC ≥ 0.75 is set, with disagreements reconciled through a third coder.

**Stream C — Trainee post-session survey.** The trainee completes a 12-item survey within 24 hours, rating their confidence in their understanding, their perception of the producer's expertise, their perception of how well the producer responded to their questions, and an open-ended question about what they wish had been clearer. Survey items are adapted from the LearnLM/Eedi participant-perspective methodology (their Appendix G).

## 5. Brief construction methodology

This is the protocol's hardest design problem and the one most likely to be done badly. Three principles govern it.

First, novelty must be structural, not cosmetic. A brief that is identical to the original artifact except that the customer's name is changed, or the date is shifted, is not novel — it is the same brief with surface decoration. A genuinely novel brief shifts at least one structural variable: the relevant regulatory regime, the customer category, the input data shape, the success criterion, or the relationship between the artifact and downstream processes. The test of structural novelty is whether a producer who applied the original artifact's logic mechanically would produce something materially wrong; if they would still produce something passable, the brief is not novel enough.

Second, novelty must be inside the producer's domain of competence, not outside it. A test that asks an L1 IT-support agent to handle a derivatives-trading dispute is not measuring whether the agent understood their original artifact — it is measuring something else. The novelty must be within the same broad procedural family as the original. This is a calibration that has to be done line-of-business by line-of-business, with input from senior practitioners.

Third, briefs must be constructed adversarially against the LLM-staged-curriculum exploit. The construction protocol is: a senior practitioner drafts a candidate brief; a researcher prompts a frontier LLM with the original artifact and asks it to "produce a curriculum that would let a new agent handle situations like this brief"; if the LLM-produced curriculum is sufficient for the brief, the brief is rejected and rewritten. The brief library is only locked when no remaining brief is solvable by the LLM-curriculum approach. This is a labor-intensive process and is the largest component of the pilot-phase timeline (section 11).

A reasonable target for first-wave deployment is 30 validated briefs per line of business, drawn from a pool of roughly 100 candidates. Approximately 70% of candidate briefs will fail one of the three criteria and be discarded or rewritten.

## 6. Trainee selection, matching and counterbalancing

Trainees are drawn from the BPO's standing onboarding cohorts. The eligibility window is days 5–25 post-hire — early enough that they have not yet been line-of-business trained, late enough that they understand the BPO's basic systems and can navigate the sandboxed environment without instruction. Trainees who have prior call-center experience in a BPO operating in the same domain as the test line of business are excluded.

Matching variables are: highest education level (binary: bachelor's degree or above vs. below), prior call-center experience (in years, banded), and English proficiency band (using whatever standardized internal measure the BPO uses; in most BPOs this is a 1–5 or 1–7 scale assigned during hiring). Within each matching cell, trainees are randomly assigned to producer arms.

Counterbalancing of trainees across producer-AI-usage arms is essential. If by chance the heavy-AI-usage producers are paired with weaker trainees, the apparent diagnostic effect is contaminated by the trainee variance. The matching cells must be balanced across arms before pairing assignments are issued.

Trainees are compensated at their normal hourly rate during the session (ideally with a small completion bonus to incentivize full participation in Phase 2's 60-minute solo work). Their participation does not count against their onboarding-progress KPIs, which removes a perverse incentive to underperform.

## 7. Dependent variables and operationalization

The primary dependent variable is the trainee's artifact QA score (Stream A in section 4), scaled 0–100 according to the BPO's standard QA rubric for the relevant line of business. The reasons for choosing this as the primary measure rather than, say, a session-specific assessment are: (a) it uses an existing instrument with established reliability and BPO-relevant validity; (b) it is meaningful to BPO operations leaders, who already know how to interpret QA scores; (c) it is blinded to study arm assignment by construction (the QA scorers don't know whose session preceded the artifact).

Secondary dependent variables (specified in advance, to control researcher degrees of freedom) are:

The producer's external-resource reach rate during Phase 1 — the count of times the producer consulted the internal knowledge base, their notes, or the original artifact, normalized by session duration and by trainee question count. The hypothesis is that this rate will be higher for slop-cannon producers, whose mental model is incomplete enough that they cannot answer trainee questions from working memory.

The producer's mean response latency to trainee questions during Phase 1, measured in seconds from the end of the trainee's question to the start of the producer's substantive response (filler phrases like "good question" or "let me think" are excluded from the response start). The hypothesis is that this will be bimodal across producers — a tight 2–10 second distribution for producers operating from a mental model and a long-tailed distribution beyond 20 seconds for producers reconstructing from the artifact text.

The proportion of trainee questions answered "directly" (vs. "by reference" — e.g., "let me check the document") during Phase 1, scored from the session coding. Hypothesis: substantially lower for slop cannons.

The trainee's confidence rating from Stream C, on the 7-point scale. Hypothesis: lower for trainees who were taught by slop cannons, even controlling for the producer's affect during the session.

The trainee's open-ended survey response, coded for whether the trainee identifies specific gaps in the producer's explanation. Hypothesis: trainees taught by slop cannons identify more gaps and identify gaps that map to the producer's external-resource-reach moments.

The producer's self-assessed confidence (the 1–7 rating from Block 5 of the session). Hypothesis: this is moderately positively correlated with trainee outcomes for light-AI-usage producers and weakly or even negatively correlated for heavy-AI-usage producers — the slop-cannon producer's metacognition is itself unreliable.

## 8. Session coding scheme

Two coders independently code each session along the following dimensions, with disagreements adjudicated by a third.

Continuous codes: total trainee question count; producer mean response latency; producer external-resource reach count; producer total speaking time; trainee total speaking time; ratio of producer speaking time to trainee speaking time across the five blocks.

Categorical codes per trainee question: question category (one of the five categories specified in Phase 1, Block 3); producer answer mode (direct from working memory / direct after consultation / by reference to a document / deflected with a procedural answer / unanswered); whether the producer's answer triggered a follow-up question from the trainee; whether the answer contained an error that the producer self-corrected; whether the answer contained an error that was not self-corrected.

Holistic codes per session, on 1–5 scales: producer's clarity of explanation; producer's responsiveness to trainee confusion; producer's pacing; producer's use of analogy or worked example; producer's evident comfort with the material.

The coding scheme is adapted from established frameworks in tutoring research (Chi and colleagues' coding of self-explanation; the Eedi tutor-edit categorization in Appendix E of the LearnLM/Eedi paper). Coder training is non-trivial — approximately 20 hours per coder to reach acceptable reliability — and is the second-largest setup cost after brief construction.

## 9. Statistical analysis plan

The primary analysis is a mixed-effects regression of the trainee artifact QA score on producer AI-usage intensity, with random effects for line of business and for matched trainee-producer pair, controlling for trainee education level, prior experience, and English proficiency. The pre-registered analysis specifies a two-tailed test at α = 0.05 with multiple-comparison correction across the four sub-hypotheses (H2a–H2d) using Holm-Bonferroni.

Secondary analyses include: (i) a quantile regression of QA score on producer AI usage to test for heterogeneous effects across the QA distribution (the bimodal-distribution prediction from Osipov's theory should manifest as a substantially larger effect at the lower quantiles than at the median); (ii) a mediation analysis with producer external-resource reach rate, mean response latency, and direct-answer proportion as candidate mediators of the AI-usage → QA-score relationship; (iii) a comparison of A2's diagnostic ROC against A4 and A5 on the 90-day downstream rework outcome (this requires the integrated five-arm study from the parent research plan, not A2 alone).

The pre-registered prediction from Osipov's theory is that the AI-usage main effect on QA score will be statistically significant with a standardized effect size of d ≈ 0.6–0.8, that the mediation analysis will show external-resource reach rate and direct-answer proportion as significant mediators jointly explaining at least 40% of the AI-usage → QA-score relationship, and that the quantile regression will show the AI-usage effect at the 10th percentile of QA score is at least 1.5× the effect at the median.

The pre-registered falsifying conditions are: (a) the AI-usage main effect is not significant or is below d = 0.3; (b) the candidate mediators do not jointly mediate at least 20% of the effect; (c) the quantile-regression effect at the 10th percentile is not larger than at the 90th percentile. Any of these would be evidence against Osipov's specific predictions; all three would be strong evidence against the live-supervised teaching mechanism as a useful diagnostic in the BPO context.

## 10. Sample size and power analysis

For the primary analysis — detecting an effect of d = 0.6 between heavy-AI-usage and light-AI-usage producer arms on trainee QA scores at α = 0.05 with 80% power — the minimum required sample is 30 producer–trainee pairs per arm if the design is between-subjects with no covariate adjustment. The mixed-effects design with covariate adjustment for trainee characteristics typically reduces the required sample by 20–30%, so 22–25 pairs per arm is operationally sufficient if the matching variables explain the predicted variance share. A first-wave target of 30 pairs per arm (60 producers total, with one trainee each) provides a safety margin and supports the secondary mediation analyses, which require somewhat larger samples than the main effect.

Stratification within the producer arm should ensure roughly even representation across the three tenure buckets (≤6 months, 6–24 months, >24 months) so that the tenure × AI-usage interaction can be estimated; if Osipov's theory is correct, the AI-usage effect should be largest in the lowest tenure bucket (where the producer has had the least time to acquire genuine domain knowledge that compensates for over-reliance on the LLM).

A pilot phase of 6–10 producer–trainee pairs is necessary before the main study to validate the coding scheme reliability, the brief library, the timing of session blocks, and the workability of the sandboxed environment.

## 11. Pilot phase

The pilot serves four functions: validating the brief library, training and calibrating the session coders, time-checking the protocol blocks, and surfacing operational issues with the sandboxed environment and the trainee logistics.

Pilot duration is roughly four weeks. Week 1 is spent on brief construction and adversarial validation against the LLM-curriculum exploit (the most labor-intensive setup task). Week 2 trains the session coders to acceptable inter-rater reliability on a small set of pre-recorded test sessions. Week 3 runs 4–6 pilot sessions across two lines of business, with the research team observing and revising the protocol. Week 4 reconciles the pilot data, finalizes the protocol, and produces the operations-team-facing run book for the main study.

Pilot data are not included in the main analysis, as protocol changes during the pilot will systematically shift the measurements. However, qualitative observations from the pilot — particularly trainee feedback on the structured question-prompt sheet — are essential for finalizing the protocol.

## 12. Cost model

A per-session cost breakdown follows. Assumed labor rates (fully loaded, including benefits and overhead, in USD): producer at $40/hour, trainee at $30/hour, supervising researcher at $90/hour, QA scorer at $50/hour, session coder at $45/hour. These are plausible BPO operating-cost figures; substituting actual organizational rates is straightforward.

Per session: producer time during session, 90 minutes ($60); trainee time during session and Phase 2 solo work, 150 minutes ($75); supervising researcher time, 105 minutes ($157); QA scoring of trainee artifact, approximately 25 minutes ($21); session coding, two coders × 60 minutes each + adjudication time, approximately 130 coder-minutes total ($98); trainee post-session survey administration and analysis, approximately 15 minutes ($11). Total per-session direct cost: approximately $422.

For the 60-producer first-wave study, total direct labor cost is approximately $25,000 (producer–trainee pairs are 1:1 in the basic design; if the study runs cross-stratified arms with multiple sessions per producer, costs scale linearly).

Pilot phase setup adds approximately $15,000–$20,000 for brief construction (estimated 80–120 senior-practitioner hours plus researcher review time), $5,000 for coder training, and $3,000 for environment setup and IT provisioning. Total pilot setup is in the $25,000 range.

Senior-staff design and analysis time across the full study (research lead, statistician, operations sponsor) adds approximately 250 hours, which at $150/hour blended rate is roughly $38,000.

The full first-wave program — pilot setup plus 60 primary sessions plus analysis — is therefore in the range of $90,000–$100,000. In the parent research plan's five-arm design, A2 is the largest single arm by cost; its share of the overall study budget is roughly 60%.

This compares against an estimated annual workslop cost (per Niederhoffer et al. 2025) of approximately $186 per affected employee per month. For a 5,000-agent BPO with 40% workslop incidence (the baseline figure from the Niederhoffer study), annual workslop cost is approximately $4.5 million. The A2 study cost is therefore approximately 2% of one year's workslop cost, which sets a low bar for the diagnostic-information-per-dollar threshold the study has to clear to justify operational deployment.

## 13. Threats to validity (expanded)

The most serious threats and their mitigations:

Trainee variance overwhelming the signal — the largest threat. Mitigated by stratified matching, by counterbalancing across arms, by using the trainee's pre-test typing speed and basic-comprehension score as covariates, and by the within-line-of-business random effects in the analysis. The 60-pair sample size assumes roughly 25% of variance is trainee-attributable; if pilot data suggest higher trainee variance, the sample size should be revised upward.

Producer adaptation to the test once it is widely deployed — a real but slower-acting threat. Producers will, over time, learn what the test feels like and prepare for it (which is the self-correcting case Osipov identifies as a feature, not a bug, in Part 4). The 12-month re-measurement (section 17) is designed specifically to estimate this adaptation rate. For the first-wave study, producers are by construction naive to the protocol.

Hawthorne effects on producer performance during the session — producers may perform differently knowing they are being observed for a research study. Mitigated by framing the test as an extended KT session (which is a familiar BPO context), by recording sessions as a normal QA practice, and by including a non-research-framed comparison condition in a follow-on study if the Hawthorne effect is suspected to be large.

Brief novelty being inadequately calibrated — the brief is either too easy (the producer can pattern-match without understanding) or too hard (even competent producers struggle). Mitigated by the adversarial validation in section 5 and by the pilot data check on the relationship between brief difficulty and producer-arm separation. If the briefs are well-calibrated, the AI-usage effect should be evident; if briefs are too easy, the effect collapses; if too hard, all producers struggle and the arms don't separate.

Coder bias — coders may form opinions about producer competence early in a session and let those opinions color later codes. Mitigated by the structured coding scheme, by the inter-rater reliability check, by blinding coders to which producer-arm each session belongs, and by random ordering of session presentation to coders.

The LearnLM-style staging exploit applied to live sessions — a sophisticated producer might use voice-recognition with a screen-mirrored LLM to whisper-prompt them through the session. Mitigated by the controlled sandboxed environment, by visible-on-camera screen sharing, and by the unpredictability of the brief at session start (no pre-staged prompt can anticipate it). If this exploit becomes a real concern, the test environment should require dual-camera setup (one on the producer's face, one over the producer's shoulder showing their full screen).

Trainee strategic behavior — a trainee who wants the producer to look bad (or good) might ask harder (or easier) questions. Mitigated by the structured question-prompt sheet, which constrains trainee question choice, and by the trainee's ignorance of the study's research framing (trainees are told they are participating in a structured KT session with measurement, not in a study about producer competence).

Selection effects on producer recruitment — producers who agree to participate may differ systematically from those who decline. In the BPO context this is partly addressed by making the study a routine part of an existing process rather than an opt-in; in any case, the analysis should report participation rates and any observable differences between participants and non-participants.

## 14. Integration with BPO operations

A2 is operationally novel only in its measurement layer — the underlying activity (a structured KT session followed by a sandboxed practical exercise) is a routine BPO activity that already happens. This makes integration into BPO operations comparatively straightforward.

Three integration points need to be worked out in advance with operations leadership.

Scheduling — the 90-minute session plus 60-minute solo work needs to fit into the producer's and trainee's schedules without disrupting their primary work. In BPO operations this is typically handled by scheduling the session during the trainee's onboarding window (when they are not yet on production tickets) and by using the producer's existing KT-session allocation (most BPO operations carve out 1–4 hours per agent per month for KT activity).

Information security and data handling — the brief and the trainee's artifact must not contain real customer PII. This is solved by using synthetic-but-realistic briefs, which is also required for the LLM-adversarial-validation step in section 5. The session recordings are handled under the BPO's existing QA recording policies, which typically require encryption at rest, access logging, and a defined retention period.

Labor relations — in some BPO geographies (notably the Philippines, India, parts of Eastern Europe, and unionized European operations), recording employees for a research purpose requires specific consent processes and possibly works-council notification. The study should be designed with the most restrictive applicable framework in mind, even if that means some sites are excluded from the first wave. Recording for QA purposes is universally permitted under existing BPO contracts; recording for research is typically permitted with explicit consent.

## 15. Decision rules and downstream actions

A research study that does not pre-specify what an organization will do with the results invites motivated reasoning after the fact. Three decision-relevant outcomes should be identified in advance.

If the AI-usage main effect on trainee QA score is significant and large (d ≥ 0.6), and the mediation analysis confirms the proposed mechanisms (external-resource reach, response latency, direct-answer proportion), the operational implication is that A2 — or a streamlined operational variant of it — is a viable screening instrument for distinguishing competent from non-competent AI-using producers in this BPO context. The downstream action is to design a streamlined version (perhaps a 45-minute session with tighter coding) for routine deployment in promotion, project assignment, or quality intervention decisions.

If the AI-usage effect is significant but moderate (d in the range 0.3–0.6), the operational implication is that A2 carries diagnostic information but is not strong enough to be a sole-source screening tool. The downstream action is to combine A2's output with existing artifact-review and QA scores in a multi-instrument scoring model, with weights estimated from the data.

If the AI-usage effect is null or negligible (d < 0.2), the operational implication is that the live-supervised teaching mechanism does not capture what Osipov claims it captures in this context. This is itself a substantive finding and should be published as such; the downstream action is to investigate why — whether the brief library failed structural-novelty, whether trainee variance overwhelmed the signal, or whether the population of "heavy AI users" in this BPO has a quality distribution different from what the workslop literature describes.

Pre-committing to these three decision branches before the data are collected protects against post-hoc rationalization in either direction.

## 16. Rollout and scaling plan

If the first-wave study produces results in the first or second decision-rule category, a scaled rollout follows in three phases.

Phase R1 (months 4–9 after first wave): protocol streamlining and validation in two additional lines of business. The session is shortened to 60 minutes by tightening Block 2 and removing Block 5 (the producer-only debrief, which is research-valuable but operationally redundant); the coding scheme is reduced to the three highest-yield variables (response latency, external-resource reach, direct-answer proportion); brief libraries are constructed for the new lines of business using the validated methodology from section 5.

Phase R2 (months 9–18 after first wave): integration into the BPO's existing performance review process. The streamlined A2 becomes one of several inputs into performance review decisions for AI-using agents, with explicit weighting determined by the multi-instrument scoring model from section 15.

Phase R3 (months 18+): the protocol becomes a routine pre-promotion or pre-project-assignment instrument for senior agent roles. At this scale, throughput becomes the binding constraint — a single supervising researcher can run roughly 12–15 sessions per week at full coding intensity, so a 5,000-agent BPO covering 25% of agents annually requires 4–6 trained session researchers and a coding team of similar scale. The cost model in section 12 scales to roughly $500 per producer per year at this throughput, which is a small fraction of the per-employee workslop cost.

## 17. Twelve-month re-measurement and adaptation tracking

Osipov identifies in Part 4 that the test has a shelf life — once cannons know it is coming, they will prepare for it, which either degrades its diagnostic value (if they prepare by superficial rehearsal) or destroys its diagnostic purpose by curing the underlying problem (if they prepare by actually learning the material). The 12-month re-measurement is designed to estimate which is happening.

The design is to re-test a randomly-selected subset of the original cohort 12 months after the first-wave study, using the same protocol but a fresh brief library (drawn from the same construction methodology, but distinct briefs to prevent direct rehearsal). Three outcomes are possible.

If the re-test results show no overall change in the AI-usage effect, the test's diagnostic validity is durable and producer adaptation is either negligible or genuinely curative (these two cases can be distinguished by examining whether the heavy-AI-usage producers' raw scores improved or stayed flat — if improved, adaptation was curative; if flat, no adaptation occurred).

If the re-test results show degradation of the effect (the gap between heavy- and light-AI-usage producers narrows but raw scores in both arms increase), this suggests producers have learned to perform on the test without necessarily improving their underlying competence — the "teaching to the test" failure mode familiar from standardized education assessment. The diagnostic value of the test is in question and the test format will need refresh.

If the re-test results show degradation of the effect with raw scores rising in the heavy-AI-usage arm specifically and downstream rework rates also falling for those producers, this is the strongest possible result — the test is functioning as a forcing function for genuine learning, which is operationally more valuable than its pure diagnostic function. This would be the strongest empirical case for permanent operational deployment.

## 18. Ethics, consent, and incentive alignment

The study involves human subjects (producers and trainees) in an employment context, which raises specific ethical considerations beyond a standard research review.

Producer consent must be genuinely free, not coerced by the implication that refusing to participate will harm their performance review. In practice this requires a clear separation between study participation and personnel decisions: the BPO must commit, in writing and to the participating agents, that study results will not be used in performance reviews during the first-wave study. (This commitment relaxes for later phases once the diagnostic instrument has been validated and integrated into the formal review process.)

Trainee consent is structurally less complicated — trainees are participating in what they would experience as a particularly thorough KT session — but they must be told the session is being recorded for research purposes (in addition to the standard QA recording purpose) and they must be allowed to decline without their onboarding being affected.

Incentive alignment requires that producers do not gain materially from poor performance (which would not be a problem here because no producer would expect that poor teaching would advantage them) and that trainees do not gain materially from poor performance in their solo work (which is mitigated by paying them a flat completion bonus rather than performance-tied compensation for the study work). The producer's confidence rating in Block 5 is recorded but not shared with the producer's manager.

For the BPO's institutional review (whether formal IRB or internal ethics committee), the study fits into an existing category — workforce research with consent, recording under existing QA policies, no medical or vulnerable-population components — and should not require unusual review process.

## 19. What would actually falsify Osipov's theory

A rigorous test specifies in advance what evidence would defeat the hypothesis under test, and this study does so explicitly.

The Osipov hypothesis is falsified, in the BPO context, if any of the following holds in the analyzed data:

The AI-usage main effect on trainee QA score is null or trivially small (d < 0.2) and this remains true after adequately controlling for trainee variance and within plausible re-specifications of the model. This would mean the test does not discriminate, full stop.

The AI-usage main effect is significant, but it does not survive controlling for the producer's tenure and prior domain experience. This would mean the test is just measuring tenure (an established signal) rather than a slop-cannon-specific construct.

The asynchronous comparator (A8, recorded teaching) achieves discriminative validity equivalent to A2 at lower cost. This would mean the synchrony constraint is not contributing what Osipov claims, and the operational recommendation reduces to the cheaper alternative.

The producer-only Edge-Case Drill (A4) achieves discriminative validity equivalent to A2 at lower cost. This would mean the trainee-novelty mechanism is not contributing what Osipov claims, and again the operational recommendation reduces to the cheaper alternative.

The mediation analysis fails — the proposed mechanisms (external-resource reach, response latency, direct-answer proportion) do not jointly mediate the AI-usage effect on QA score. This would mean the test is detecting something, but not the cognitive construct Osipov names.

Any one of these is sufficient to substantially weaken the operational case for A2 specifically. The study is designed so that all of them are testable in a single integrated analysis, with no further data collection required.

## 20. Comparison with the LearnLM/Eedi protocol

It is worth being explicit about the parallels with the LearnLM/Eedi RCT, both because that paper's methodological choices are well-considered and because it represents the closest published design to A2.

The structural parallels: both designs use random assignment within a controlled environment; both measure both immediate outcomes and transfer to novel tasks; both use multi-channel measurement combining quantitative outcome scores with participant-reported subjective measures; both include detailed coding of the live interaction; both report cost and throughput simulations for operational deployment.

The structural differences: LearnLM/Eedi tested the AI's tutoring ability under human supervision, while A2 tests the human producer's tutoring ability without AI supervision. LearnLM/Eedi used pre-existing learning content (Eedi's curriculum), while A2 requires a newly-constructed brief library specifically designed against the LLM-curriculum exploit. LearnLM/Eedi measured student learning, while A2 measures producer competence indirectly through trainee outcome — the trainee in A2 is an instrument, not the subject.

The methodological lift to do for A2 specifically: the brief library construction, the producer-side coding scheme, and the trainee-as-instrument framing are the three components that have no direct analog in LearnLM/Eedi and are the components that need the most pilot validation. The trainee survey design and the cost-modeling approach can be adapted with minimal modification from the LearnLM/Eedi paper's appendices G and H respectively.

---

## A note on what this protocol does not test

A2 tests whether the live-supervised teaching transfer can discriminate slop cannons from competent producers in a BPO context. It does not test whether the diagnostic, once routinely deployed, reduces overall workslop incidence — that is a separate question, requiring an interrupted-time-series or stepped-wedge study at the operational level. Nor does it test whether the formative effect Osipov identifies (cannons preparing for the test learn the material) actually occurs in practice — that is what the 12-month re-measurement in section 17 estimates, but a single re-measurement with a single cohort is suggestive at best.

The A2 protocol is the diagnostic-validity study. The reduce-overall-workslop study and the formative-effect study are distinct downstream investigations that should follow if A2's results justify them.
