# Finalized Protocol
## Slop-Survival Study: Embedded RCT in the CMT Onboarding Exercise

A study of whether AI-generated transformation proposals, even when peer-validated as authentic-looking, survive downstream consumption by competent uninformed teams in a major BPO/SI's Communications, Media and Technology business unit.

---

## 1. Methodological status

This study is an embedded randomized controlled trial inside an existing operational process. The four design properties that establish this status, all confirmed by the operational owner of the exercise, are:

The treatment assignment (LLM-generated vs. workshop-generated proposal source) is randomized at the individual associate level via independent coin flips. This eliminates self-selection confounds on author skill, motivation, and prior LLM facility, and supports causal interpretation of any observed treatment effect on downstream outcomes.

The peer-review pool that selected the highest-authenticity-rated LLM proposals and the team-interview pool that interrogates authors during onboarding are administratively separate, with no individual occupying both roles for the same proposal. This eliminates leakage of source identity to downstream interviewers.

The 3-person executive panel composition and the 1.0–5.0 grading rubric have been stable across past cycles. This means historical grade data can be pooled across cycles for retrospective analysis and that prospective grades will be comparable to a meaningful baseline.

The peer-review filter that selected the highest-authenticity-rated LLM proposals is a post-randomization treatment intensification, not a confounded selection. The LLM arm in the analyzed sample is composed of slop at its strongest; if it still fails downstream consumption, the conclusion is robust precisely because the test was conservative.

These four properties together mean the study can answer Osipov's central operational claim — does AI-generated work, even when surface-validated as authentic, survive downstream organizational use? — with causal validity that the published workslop literature does not currently have. Niederhoffer et al. (2025) is survey-based; Kommers et al. (2026) is conceptual; the METR developer-productivity RCT (Becker et al. 2025) and the LearnLM/Eedi tutoring RCT (Wang et al. 2025) are RCTs in adjacent domains. None measures slop survival in downstream organizational consumption with embedded-RCT validity.

## 2. The construct under test

The construct is slop survival in downstream consumption. It is operationally defined as the average panel grade (1.0–5.0) of an implementation plan produced by an onboarding team that worked from a transformation proposal of randomized source (LLM-generated vs. workshop-generated). The construct is distinct from, and operationally more relevant than, the producer-teaching-capacity construct that the original A2 protocol measured.

A test of this construct produces three pieces of operationally actionable information for the BU. First, an estimate of the absolute grade gap attributable to AI-generated source proposals — a number leadership can multiply by the volume of AI-generated work flowing through the BU to estimate aggregate quality cost. Second, a decomposition of where in the consumption chain the gap manifests — at proposal screening, in the author interview, or in the implementation plan synthesis — which tells leadership where to intervene. Third, a measurement of whether team-side LLM use during downstream consumption rescues, preserves, or amplifies the source-side slop effect — which is the question that determines whether broader LLM tool deployment is net beneficial in this work setting.

## 3. Primary and secondary hypotheses

The primary hypothesis (H1) is that LLM-source proposals receive lower mean panel grades than workshop-source proposals. The pre-registered prediction is a standardized effect size in the d = 0.4–0.8 range, with a minimum operationally meaningful effect of d = 0.25 (corresponding roughly to a 0.3-point gap on the 1.0–5.0 grading scale at typical historical grade variance).

Three secondary hypotheses are pre-registered.

H2 (screening): LLM-source proposals are selected by teams at the screening stage at a rate at least equal to workshop-source proposals despite producing lower downstream grades. This is the operational test of the Kommers et al. "superficial competence" property. The predicted screening-pick ratio is at or above 1:1 LLM-to-workshop, against a downstream grade gap that favors workshop, producing a measurable selection-grade gap.

H3 (interview-mediation): Author behavior during the team interview — operationalized as response latency to team questions, external-resource reference rate, and direct-answer proportion — partially mediates the source effect on panel grade. Pre-registered prediction: at least 25% of the source → grade total effect is mediated through these author-behavior variables.

H4 (live-interview contribution): The live author interview contributes more grade points to teams working from LLM-source proposals than to teams working from workshop-source proposals. This tests whether the live element specifically rescues weak source material. Pre-registered prediction: a source × condition interaction such that the document-only-vs-interview grade gap is at least 0.5 points larger for LLM-source than for workshop-source proposals.

A fifth hypothesis is treated as exploratory rather than pre-registered, because its direction is theoretically ambiguous. H5 (downstream LLM augmentation): heavy team-side LLM use during the implementation phase either compresses the source-effect grade gap (slop rescues slop) or widens it (slop compounds slop). This is examined post-hoc with the data, and either finding is reported as a substantive result rather than as confirmation of a prior prediction.

## 4. Falsification conditions

The Osipov hypothesis as instantiated in this study is falsified by any of the following observations, each tested in the pre-specified primary analysis:

The estimated treatment effect on panel grade is null or trivially small (|d| < 0.15), with a 95% confidence interval that excludes effects above d = 0.25. This would indicate that under operational conditions in this BU, peer-validated LLM-generated proposals do not produce measurably worse downstream outcomes than workshop-generated ones.

The estimated treatment effect is in the predicted direction but does not survive controlling for proposal length, vertical sub-segment within CMT, and observable author characteristics. This would indicate the apparent effect is driven by superficial features rather than by the LLM-vs-workshop source itself.

The interview-mediation hypothesis (H3) fails. This would indicate the source effect, if real, is not attributable to the cognitive mechanism Osipov names (asymmetric internalization between author and artifact) but to something else.

The live-interview-contribution hypothesis (H4) fails — the source × condition interaction is null or in the unpredicted direction. This would indicate the live-supervision element does not contribute what Osipov claims, and the operational implication reduces to the simpler claim that LLM-generated artifacts have lower quality than workshop-generated ones, without any specific role for live interrogation.

Pre-committing to these falsification conditions before data analysis protects against post-hoc rationalization. Each falsification is independently informative and the study is designed so that all four can be tested in a single integrated analysis on a single dataset.

## 5. Four-step study sequence

The study runs in four sequential steps with parallel components where operationally feasible.

**Step 1**, weeks 1–4: pre-registered retrospective analysis of historical proposal-source assignment data and historical panel grades, restricted to (proposal source × panel grade) at the proposal level. Estimates the bivariate effect from existing data.

**Step 2**, weeks 3–8 (overlapping with Step 1): single-cycle pilot of prospective instrumentation — screening capture, interview recording and coding, individual-panelist grade capture, three-arm team assignment, source-revelation timing — to verify operational feasibility and inter-rater reliability.

**Step 3**, weeks 9 onward: full prospective study spanning whatever number of onboarding cycles the Step 1 power calculation requires, with all instrumentation active and pre-registered analyses running on accumulating data with a planned final analysis after the target sample is reached.

**Step 4**, after Step 3 reports out: cross-vertical replication in one or two non-CMT business units, using the protocol developed in Steps 2 and 3.

The four steps total approximately 9–14 months from initiation depending on cohort cadence and target sample size. Steps 1 and 2 are time-boxed; Step 3 length is a function of cohort throughput; Step 4 is initiated only if Steps 1–3 produce results justifying replication investment.

## 6. Step 1 — Retrospective analysis

The retrospective analysis is the highest-priority immediate action. It costs essentially nothing beyond data extraction and a half-day of analysis, and it produces both an answer to the basic question and the parameters needed to design Step 3 properly.

**Data scope.** Pull all historical onboarding cycles for which (i) the LLM-vs-workshop randomization was operational, (ii) the panel and rubric were the current versions, and (iii) source-assignment data and panel-grade data are jointly available at the proposal level. Both extraction filters should be operationally verifiable from existing records.

**Pre-registered primary analysis.** Mixed-effects linear regression of panel grade (panelist-averaged) on a binary indicator for proposal source (LLM = 1, workshop = 0), with random intercepts for cycle, executive panelist, and team. Robust standard errors. Two-sided test at α = 0.05. The estimand is the average treatment effect on the treated (ATT) at the proposal level. Reported with effect size d (standardized using the pooled cycle-grade standard deviation), 95% CI on d, and the raw mean grade gap in 1.0–5.0 points.

**Pre-registered secondary analyses.** Same model but with the LLM peer-review authenticity score as a moderator (does higher-authenticity slop survive better than lower-authenticity slop?). Same model with proposal length and CMT vertical sub-segment as additional fixed-effect controls (precision improvement, with random assignment these are not confound controls). Variance-component decomposition to estimate panel inter-rater reliability (ICC), cycle-to-cycle grade variance, and team-level variance — all of which are nuisance parameters needed to size Step 3.

**Decision thresholds for Step 3 design.** If retrospective d ≥ 0.4 and statistically significant, Step 3 is sized for 80% power at d = 0.6 × retrospective d (conservative attenuation assumption). If 0.15 ≤ retrospective d < 0.4, Step 3 is sized for 80% power at the retrospective point estimate (no attenuation discount, because the prospective design's added precision balances any attenuation). If retrospective d < 0.15 with a tight CI, the basic premise is questioned and Step 3 is reconsidered before proceeding — possibilities include reformulating the construct, examining whether the retrospective implementation of the random assignment had unobserved compliance issues, or pivoting to a different operational test.

**Reporting.** A 4–6 page memo presenting the retrospective effect estimate, the variance components, the implied Step 3 sample size, and a Step 3 go/no-go recommendation. Memo is circulated to the research sponsor and the BU operations owner before Step 2 begins.

## 7. Step 2 — Instrumentation pilot

The pilot uses a single onboarding cycle to validate three new measurement layers and to verify operational feasibility of the three-arm team assignment. Pilot data are not included in the Step 3 analysis (protocol changes during the pilot will systematically shift the measurements) but are essential for finalizing the operational details.

**Pilot scope.** One full onboarding cycle, with whatever number of associates and proposals it produces. All three arms (natural-screening + interview, random-assigned + interview, random-assigned + document-only) are run in roughly the planned proportions. Full instrumentation is active.

**Validation checks.** Inter-rater reliability for interview-behavior coding is computed across two trained coders working on the same set of recordings; target Cohen's κ ≥ 0.7 for categorical codes and ICC ≥ 0.75 for continuous codes. If reliability falls short, coding scheme is revised and re-piloted on a subset of recordings before Step 3 launches. Operational feasibility checks include: did the random-assignment arms function without disrupting the operational flow? Did the document-only arm produce implementation plans that are scoreable on the existing rubric? Did source revelation after panel grading work as designed? Did individual-panelist grade capture function?

**Pilot decision points.** If all checks pass, Step 3 launches at the next cycle. If coding reliability fails, coder training and scheme revision. If the random-assignment or document-only arms create operational friction, the proportions are adjusted (e.g., reducing document-only from 20% to 10%) before Step 3 launch.

**Pilot reporting.** A 2–3 page operational readiness memo confirming go-status for Step 3, documenting any protocol adjustments, and finalizing the inter-rater-reliable coding scheme.

## 8. Step 3 — Prospective study protocol

The prospective study runs across as many onboarding cycles as the Step 1 power calculation requires (typically 1–3 cycles), with all instrumentation active.

### 8.1 Three-arm design

Within each cycle, onboarding teams are randomized to one of three conditions in approximately the following proportions:

**Arm A — Natural screening + interview (50% of teams).** Teams operate under the standard exercise protocol: they review available proposals, select the one they find most likely to impress the panel, interview the author, and develop the implementation plan. The screening choice and the screening-confidence rating are captured; otherwise the operational flow is unchanged.

**Arm B — Random assignment + interview (30% of teams).** Teams skip the screening step and are randomly assigned a proposal from the available pool. They then interview the author and develop the implementation plan as in Arm A. This arm provides the unbiased estimate of the source-effect on grade, free of self-selection bias from team screening preferences.

**Arm C — Random assignment + document-only (20% of teams).** Teams are randomly assigned a proposal but do not interview the author. They develop the implementation plan from the proposal document alone, supplemented by whatever internal resources they would normally consult. This arm isolates the contribution of the live-author-interview step.

Team-to-arm assignment is randomized at the team level using stratified randomization on team-baseline-capability (a short structured task graded by the same panel rubric, administered before the main exercise) and on team composition (size, experience mix). Within Arms B and C, the team-to-proposal assignment is then randomized independently. The proposal pool from which assignments are drawn maintains the LLM/workshop balance from the upstream coin-flip randomization.

### 8.2 Instrumentation

Six measurement layers are added to the existing exercise.

**Screening capture (Arm A only).** Each Arm A team records which proposals they considered, the order of their preferences, and a brief structured rationale for their top pick (3–5 sentences, captured in writing). Their pre-development confidence in the proposal's panel-grade prospects is rated on a 1–7 scale.

**Interview recording (Arms A and B).** Author interviews are audio-recorded with consent (consent is built into the existing process and extends to research analysis). Recordings are transcribed automatically and lightly cleaned by a researcher.

**Interview coding (Arms A and B).** Two trained coders independently code each interview transcript (with audio reference available) along the dimensions specified in §8.4. Inter-rater reliability is checked monthly during the study; disagreements are reconciled by a third coder.

**Implementation plan capture.** The team's submitted implementation plan is archived in standard form for retrospective analysis. Team-side LLM tool usage during the implementation phase is captured via existing telemetry (browser monitoring, tool-use logs, or self-report — whatever the BU normally collects).

**Individual panelist grading.** Each panelist's individual 1.0–5.0 rating is captured separately, in addition to the consensus or averaged grade that is normally reported. Panelists also provide a brief structured comment on each plan — strengths, weaknesses, and any specific concerns. After all grades are submitted (and only then), each panelist independently rates each plan on a separate 1–7 scale of "how likely was the source proposal to have been LLM-generated?" This produces a panelist-source-detection measurement.

**Post-grading source revelation and team retrospective.** After all panel grades are finalized, teams are informed of the proposal source and asked to (i) retrospectively guess the source, (ii) reflect on what they found difficult about working with the proposal, and (iii) rate the author interview quality on three dimensions (helpfulness, depth, evasiveness). Author post-hoc surveys are also administered: confidence in proposal selection, prepared-vs-improvised feeling during interview, and reflection on questions they struggled with.

### 8.3 Sample size

With individual-level randomization, the unit of analysis for the primary effect is the proposal (each proposal gets one panel grade). No cluster-randomization power penalty applies. The required sample is determined by the Step 1 retrospective effect estimate via the decision thresholds in §6.

For planning purposes, assuming a retrospective d in the 0.4–0.6 range and 80% power at α = 0.05, the required prospective sample is approximately 80–150 proposals (40–75 per source arm). For Arms A and B combined (the source-effect estimate uses both), this means 80–150 teams in those arms across the prospective study. At quarterly cohort cadence and a typical CMT BU cohort size, this is achievable in 1–3 cycles. Arm C requires roughly 30–50 teams to support the H4 interaction test with 80% power.

Sample is increased above the minimum if budget permits, both for precision improvement on secondary analyses and for subgroup-analysis power on H5 (LLM augmentation moderation).

### 8.4 Coding scheme for author interviews

Two coders independently code each interview transcript along the following dimensions, with disagreements adjudicated by a third coder.

Continuous codes per interview: total team question count; author mean response latency to team questions (seconds from end of question to start of substantive response, excluding filler phrases); author external-resource reference count (instances of "let me check," "that's in the deck," "I'd refer you to," etc.); author total speaking time; team total speaking time.

Categorical codes per team question: question type (strategic, technical, financial, implementation, risk); author answer mode (direct from working memory / direct after consultation / by reference to a document / deflected with a procedural answer / unanswered); whether the answer triggered a follow-up question from the team; whether the answer contained an apparent error.

Holistic codes per interview, on 1–5 scales: author's clarity of explanation; author's responsiveness to team confusion; author's evident comfort with the material; author's apparent depth of understanding beyond the proposal text.

The coding scheme is adapted from established frameworks in tutoring research (Chi et al. 1994 self-explanation coding; LearnLM/Eedi 2025 Appendix E tutor-edit coding). Coder training requires approximately 20 hours per coder to reach acceptable reliability and is performed once at study start with periodic re-calibration.

## 9. Statistical analysis plan

All analyses below are pre-registered. Any deviation requires documentation and is reported separately as exploratory.

### 9.1 Primary analysis (H1)

Mixed-effects linear regression of panelist-averaged plan grade on a binary indicator for proposal source, with random intercepts for cycle, executive panelist, and team. Restricted to Arms A and B combined. Robust standard errors. Two-sided test at α = 0.05. Reported as effect size d (standardized on pooled cycle-grade SD), 95% CI on d, raw mean grade gap in points.

### 9.2 Confound and precision analyses

The primary analysis is repeated with proposal length, CMT vertical sub-segment, and observable author covariates (tenure, prior project experience) added as fixed-effect controls. Under random assignment these are precision-improvement controls; if the source effect substantially attenuates with their inclusion, this is reported and discussed (it would suggest randomization imbalance in the analyzed sample).

### 9.3 Screening analysis (H2)

Logistic regression of "selected at screening" on proposal source, restricted to Arm A teams and to proposals visible to those teams. Reported as odds ratio with 95% CI. Separately, the gap between screening confidence rating (1–7) and panel grade (rescaled to 1–7 for comparability) is computed by source and tested for differential gap by source.

### 9.4 Mediation analysis (H3)

Within Arms A and B, mediation analysis of the source → grade effect through the three pre-specified author behavior mediators (mean response latency, external-resource reference rate, direct-answer proportion). Each mediator entered separately and jointly. Bootstrap confidence intervals on the indirect effect. Pre-registered prediction: joint indirect effect through the three mediators is at least 25% of the total source → grade effect.

### 9.5 Live-interview contribution analysis (H4)

Source × condition interaction in a model of plan grade on source, condition (interview vs. document-only), their interaction, and random effects for cycle and panelist. Restricted to Arms B and C. Reported as the interaction coefficient with 95% CI and as the differential interview contribution by source.

### 9.6 Exploratory analysis (H5)

Plan grade modeled as a function of source, team-side LLM-use intensity during implementation, and their interaction, with appropriate controls. The interaction coefficient is reported with CI and discussed. Direction is not predicted.

### 9.7 Source-detection analyses

Two source-detection signals are analyzed. First, the team's retrospective source guess is tested against random for accuracy by source; team detection accuracy is correlated with team grade outcome. Second, the panelists' separate "likely LLM-generated" rating is tested against actual source, and the correlation between this rating and the panel grade is reported (if strong, the panel grade is partially a measure of source detection rather than purely of plan quality, and this is incorporated into the discussion of the primary effect).

### 9.8 Multiple comparisons

The four pre-registered hypotheses (H1, H2, H3, H4) are tested with Holm-Bonferroni correction for family-wise error at α = 0.05. The exploratory hypothesis (H5) and the source-detection analyses are reported with uncorrected p-values and clearly labeled as exploratory.

### 9.9 Sensitivity analyses

Three pre-specified sensitivity analyses are run on the primary effect: (i) restricted to Arm B only (the unbiased subsample, without natural-screening selection); (ii) excluding teams with extreme baseline-capability scores (top and bottom 10%); (iii) excluding any cycle with substantially anomalous overall grade distribution. The primary inference is robust if all three sensitivity analyses are directionally consistent with the main estimate.

## 10. Decision rules

Pre-committing to specific operational decisions before the data are collected protects the study from post-hoc rationalization. Three decision branches are specified.

**Branch 1 — primary effect is significant and large (d ≥ 0.4) with falsification conditions all rejected.** Operational implication: peer-validated LLM-generated transformation proposals demonstrably produce worse downstream outcomes than workshop-generated ones in this BU's CMT operations. Downstream actions: (i) revise the BU's policies on AI-assisted proposal generation for client-facing work; (ii) integrate the slop-survival measurement (in streamlined form) into routine quality assurance for AI-assisted client deliverables; (iii) launch Step 4 cross-vertical replication.

**Branch 2 — primary effect is significant but moderate (0.15 ≤ d < 0.4), or significant with one or more secondary hypotheses failing.** Operational implication: there is a measurable but not dramatic source effect, with potentially specific mechanisms identifiable from the secondary analyses. Downstream actions: (i) targeted intervention on whichever specific stage of the consumption chain showed the largest gap (screening, interview, implementation); (ii) consider running Step 3 again with adjusted protocol after the targeted intervention to test whether the gap narrows; (iii) Step 4 replication is recommended but lower priority.

**Branch 3 — primary effect is null or trivial (d < 0.15) or fails sensitivity analyses.** Operational implication: under the specific operational conditions of this BU's CMT exercise, peer-validated LLM-generated proposals do not produce measurably worse downstream outcomes. Downstream actions: (i) report the null finding internally and externally as a substantive contribution to the workslop literature; (ii) examine alternative formulations (different verticals, different AI-assistance intensities, different downstream consumers) before concluding the broader Osipov claim is wrong; (iii) Step 4 is not initiated until the null finding is interrogated.

These three branches cover the analytically meaningful outcome space and should be agreed in writing with the research sponsor and BU operations owner before Step 1 launches.

## 11. Cost and timeline

Total cost across all four steps is in the range of $40,000–$60,000, dominated by research staff time. Operational costs are minimal because Steps 2 and 3 use existing operational infrastructure with added instrumentation rather than parallel research processes.

Step 1 (retrospective analysis): approximately $4,000 in research staff time across data extraction, statistical analysis, and memo preparation. 4 weeks elapsed time, with most of that calendar time in the data extraction queue rather than in active analysis.

Step 2 (instrumentation pilot): approximately $8,000 in research staff time across coder training, pilot administration, reliability assessment, and operational readiness memo. 6 weeks elapsed time, overlapping with Step 1.

Step 3 (prospective study): approximately $25,000–$40,000 in research staff time across instrumentation operation, coding (the largest single cost component, scaling with the number of interview recordings), analysis, and reporting. Elapsed time is determined by cohort cadence: at quarterly cycles and a 1–3 cycle requirement, 9–15 months from Step 3 launch to final analysis.

Step 4 (cross-vertical replication): approximately $20,000–$30,000 per replication vertical, primarily research staff time. Initiated only on the Branch 1 or Branch 2 outcome from Step 3.

Total elapsed time from initiation to Step 3 final report is approximately 9–14 months. Step 4, if initiated, adds 6–12 months per vertical.

Compared against the Niederhoffer et al. estimated annual workslop cost of approximately $186 per affected employee per month — for a BU of, say, 2,000 associates with 40% workslop incidence, an annual cost on the order of $1.8 million — the study cost is approximately 2–3% of one year's workslop cost. The cost-to-information ratio is favorable provided the study answers any of its decision-rule branches affirmatively.

## 12. Operational requirements

Six things must be in place before Step 1 launches.

**Data access.** Researcher access to historical proposal-source assignment data and historical panel-grade data, joined at the proposal level, with appropriate privacy controls. This is the first thing to verify operationally.

**Pre-registration.** The Step 1 analysis plan in §6 is pre-registered (publicly or at minimum internally with the research sponsor) before any data analysis begins. The Step 3 analysis plan in §9 is pre-registered before Step 3 launches.

**Sponsorship clarity.** Written confirmation from the research sponsor that the study can produce a Branch 3 (null) result without organizational consequences for the research team. Studies whose null results are organizationally costly do not produce trustworthy evidence in either direction.

**Personnel agreements with affected populations.** Written confirmation that participating onboarding teams' study participation will not affect their onboarding-progress KPIs and that their interview recordings (already collected operationally) can be used for research analysis with appropriate consent. Author consent for interview-recording analysis is built into the existing operational consent and extends to research use.

**Coding capacity.** Two trained coders allocated to interview-coding work for the duration of Step 3, with a third coder available for adjudication. Coders need 20 hours of training before Step 2 launches and are available throughout Steps 2 and 3.

**Statistical analyst capacity.** A pre-identified analyst with mixed-effects modeling experience (or external statistical consulting access) for Step 1 and Step 3 analyses.

## 13. Risk register

Five risks are flagged with mitigations.

**Compliance and attrition in the upstream randomization.** Even with individual coin-flip randomization at assignment, some associates may have circumvented their assignment (e.g., LLM-arm associates who refused to use AI tools, workshop-arm associates who used AI anyway). Mitigation: Step 1 includes a compliance-and-attrition audit of the historical data; intent-to-treat analysis is reported as primary; per-protocol analysis is reported as secondary if compliance issues are detected.

**Panel composition shift during prospective study.** If a panelist leaves or is replaced during Step 3, panel-composition variance enters the prospective data in a way that the historical baseline does not capture. Mitigation: panel composition is held constant for the Step 3 duration if at all possible; if a change is unavoidable, it is recorded and modeled as a fixed effect.

**Operational disruption from instrumentation.** The screening capture, interview recording, and panelist-individual-grade capture add minor friction to an operational process that is otherwise running smoothly. Mitigation: pilot validation in Step 2 specifically tests for operational disruption and adjusts proportions of the three arms if needed. Random-assignment and document-only arms specifically may need to be reduced if they create resentment or perception of unfairness among participating teams.

**Source revelation timing leakage.** If onboarding teams discuss their experiences and source revelations across cohorts, later cohorts may enter the exercise with prior expectations about LLM vs workshop proposals. Mitigation: source revelation occurs only after panel grading is complete; teams are asked to maintain confidentiality on the specific source assignments of proposals they worked with; cohort-level random effects in the analysis absorb any cohort-to-cohort drift in baseline expectations.

**Statistical power shortfall.** If the actual prospective effect is smaller than the Step 1 estimate (regression to the mean in observational data is common), the prospective study may be underpowered for the primary effect. Mitigation: Step 3 sample size is set with a conservative attenuation discount on the Step 1 estimate per §6; the study is designed to extend across additional cycles if the planned sample falls short of the pre-specified power threshold at interim analysis.

## 14. Reporting and dissemination

Three reporting outputs are planned.

A Step 1 retrospective memo, internal to the research sponsor and BU operations owner, containing the historical effect estimate, variance components, Step 3 sample-size recommendation, and Step 3 go/no-go.

A Step 3 prospective study report, comprising a primary technical report (full results, all hypotheses, sensitivity analyses) and an operations-team-facing summary (decision-rule branch determination, recommended actions, cost-benefit estimate). Internal distribution to the research sponsor, BU leadership, and operations owners.

A research publication, prepared after Step 3 completes and before or alongside Step 4. The embedded-RCT design and the slop-survival construct are novel enough relative to the published literature (Niederhoffer et al. 2025; Kommers et al. 2026; Becker et al. 2025; Wang et al. 2025) to support a target venue in the AI-and-organizations or HCI literature. Publication is conditional on sponsor approval and on appropriate handling of any commercially sensitive details.

## 15. What this protocol delivers

When complete, this study produces:

A causal estimate of whether peer-validated LLM-generated work survives downstream consumption in real organizational use, derived from an embedded RCT in an existing operational process — an evidence type not currently available in the published workslop literature.

A decomposition of where in the consumption chain the source effect manifests (screening, interview, implementation), enabling targeted operational intervention.

A measurement of whether downstream LLM use rescues, preserves, or amplifies upstream slop, addressing a question the existing literature has not approached.

An operational instrument the BU can deploy at routine cost (≈$500/proposal at scaled deployment, after the initial study investment) for ongoing slop-survival monitoring on AI-assisted client deliverables.

A pre-registered, falsifiable, embedded-RCT contribution to the broader research program on AI slop in organizational settings, with publication potential in venues that the survey-and-conceptual existing literature does not occupy.

The study is methodologically as strong as the operational context permits. The key methodological assets — individual-level random treatment assignment, separated peer-review and interview pools, stable panel and rubric across cycles, post-randomization treatment intensification through peer-review filtering — together produce evidence quality that purpose-built academic studies of this question would struggle to match without substantially larger budgets and longer timelines. The operational embedding is the methodological asset; preserving it through the three-arm design, the pre-registered analyses, and the pre-committed decision rules is the primary design discipline the study requires.
