# Academic Writing Revision Checklist

Use this checklist strictly and sequentially when revising or reviewing scientific and academic texts. The goal is to maximize precision, conciseness, logical cohesion, and scientific rigor while preserving verified meaning.

Example sentences in this checklist illustrate editing patterns. Do not treat their technical content as verified facts or insert them into a manuscript unless the manuscript or cited evidence supports them.

## Phase 0: Revision Scope Setup

- [ ] **Identify Revision Constraints**

Identify the target audience, journal or proposal format, word limit, and required tone before revising.

- [ ] **Preserve Technical Meaning**

Preserve the author's intended technical meaning. Do not improve style by changing claims beyond the available evidence.

Decision rule: If a revision changes the scope, certainty, mechanism, temperature range, material system, or causal relationship of the original claim, flag it instead of silently rewriting it.

Bad: "The data proves that cryogenic operation eliminates current collapse."

Good: "The data indicates reduced current collapse under the tested conditions."

## Phase 1: Precision and Clarity Verification

- [ ] **Specify Vague Language**

Scan for open-ended statements and replace them with exact parameters or specific context.

Bad: "This is an unresolved problem."

Good: "The scaling behavior remains unquantified under the tested operating conditions."

- [ ] **Resolve Ambiguous Adjectives**

Identify multi-meaning modifiers, such as "fragile" or "strong", and replace them with precise scientific descriptions.

Example: Change "fragile" to "mechanically brittle", "phase unstable", or "possessing a low electrical breakdown voltage" depending on context and evidence.

- [ ] **Quantify Qualitative Adverbs ("Show, Don't Tell")**

Replace qualitative descriptors with exact metrics, percentages, or mathematical orders of magnitude when those values are provided.

Bad: "The measured response changes significantly at low temperature."

Good: "The measured response changes by [verified value] at [verified temperature range]."

- [ ] **Standardize Terminology**

Verify that a single technical term is used consistently throughout the text. Remove "elegant variation", meaning synonyms used for technical terms only to vary vocabulary.

- [ ] **Delete Redundant Modifiers (Tautologies)**

Remove modifiers that duplicate the meaning of the core word.

Bad: "Completely eliminate", "absolutely essential", "future potential", "new innovation".

Good: "Eliminate", "essential", "potential", "innovation".

- [ ] **Explain Niche Jargon**

Identify highly domain-specific jargon. Provide a brief, seamless, in-line explanation for readers outside the immediate sub-field.

- [ ] **Remove Orphan Abbreviations**

Delete acronyms or defined concepts if the term only appears once in the entire text.

## Phase 2: Conciseness and Flow Engineering

- [ ] **Convert Nominalizations to Strong Verbs**

Find core actions hidden inside nouns and convert them to direct verbs to propel the sentence forward.

Bad: "The model provides an estimation of the channel temperature."

Good: "The model estimates the channel temperature."

- [ ] **Combine into "Property/Action -> Consequence" Structures**

Merge fragmented sentences and remove excessive bridging phrases. Combine statements of fact directly with their resulting impact.

Bad: "The material has property X. This property improves outcome Y."

Good: "Property X improves outcome Y under [verified condition]."

- [ ] **Verify Sentence Purpose**

Evaluate every sentence individually. Delete "orphan facts", even if technically true, if they do not actively advance the core argument or provide immediate, necessary context.

Decision rule: A sentence should define the problem, justify the approach, explain evidence, interpret results, state a limitation, or advance the conclusion. If it does none of these, delete or relocate it.

Example: A historical detail about a material should be removed unless it directly explains the present experiment, design choice, or research gap.

- [ ] **Remove Argument Echoing**

Check for repetitive looping of the exact same argument across a paragraph or section. Make the point clearly once and advance the narrative.

- [ ] **Use Transitions Only for Clear Logical Relationships**

Permit transition words, such as "Furthermore", "Moreover", "Additionally", "Consequently", and "Therefore", only when they accurately mark a clear logical relationship. Remove them when they merely decorate the prose or disguise a weak connection. When possible, connect sentences by linking the subject of the new sentence to the object of the previous one.

Bad: "Furthermore, the device shows reduced degradation. Moreover, this behavior supports the design."

Good: "The reduced degradation supports the device design."

Acceptable: "The measured resistance increased after thermal cycling. Therefore, the analysis treats cycling as a stress condition rather than a neutral storage interval."

## Phase 3: Tone and Formatting Calibration

- [ ] **Strip Hyperbole**

Delete subjective, exaggerated, or non-scientific adjectives, such as "exceptional", "first-ever", "unprecedented", and "perfect".

- [ ] **Calibrate Scientific Certainty (Hedging)**

Replace absolute verbs, such as "proves" and "guarantees", with precise, empirically appropriate verbs, such as "demonstrates", "indicates", and "suggests", unless dealing with pure mathematical certainty.

Bad: "The data proves that mechanism X causes outcome Y."

Good: "The data indicates that mechanism X contributes to outcome Y."

- [ ] **Enforce Objective Active Voice**

Rewrite first-person pronouns, such as "we" and "I", and clunky passive voice, such as "It was demonstrated that". Make the data, the model, or the literature the active subject of the sentence.

Bad: "It was demonstrated that condition X exacerbates response Y."

Bad: "We demonstrated that condition X exacerbates response Y."

Good: "Empirical testing demonstrates that condition X exacerbates response Y."

- [ ] **Convert Bullets to Natural Prose**

Transform bullet-heavy explanations into cohesive paragraph flow where prose is expected by the venue.

- [ ] **Remove Endless Dashes and Hyphens**

Break up long, disjointed clauses bridged by dashes into clear, properly punctuated, separate sentences.

## Phase 4: Scientific Rigor and Structural Integrity Verification

- [ ] **Validate Problem Statements**

Ensure the core research gap is rooted in established physics or documented literature. Flag and rewrite any contrived, "strawman" problems that do not reflect actual scientific or engineering challenges.

Decision rule: A valid problem statement should identify what remains unknown, why existing methods do not resolve it, and why the gap matters scientifically or technically.

Bad: "No one has studied this material carefully."

Good: "Existing studies report [known condition], but do not quantify [specific unresolved behavior] under [tested condition]."

- [ ] **Verify Citation Coverage**

Check all factual claims, baseline metrics, and novelty statements to ensure they are anchored by appropriate references.

Action: If an author claims a method is "novel" or "first-of-its-kind", ensure the preceding literature is accurately cited and contextualized to prove the gap. Additionally, check the publication years of these cited references to verify that the comparison is against recent, state-of-the-art work rather than outdated literature.

Decision rule: Claims about prior work, performance benchmarks, material properties, mechanisms, and novelty require citations unless they are directly supported by data presented in the same text.

- [ ] **Classify Claims Correctly**

Verify that each claim is classified correctly as evidence, interpretation, limitation, or implication.

Example:

  - Evidence: "The measured resistance increased from 10 ohms to 15 ohms."
  - Interpretation: "This increase is consistent with additional scattering."
  - Limitation: "The measurement does not isolate the contribution of contact resistance."
  - Implication: "The result suggests that interface quality may constrain performance."

- [ ] **State Limitations and Boundary Conditions**

Check that limitations and boundary conditions are stated where the evidence does not support general conclusions.

Decision rule: When a conclusion depends on a specific temperature range, bias condition, geometry, sample size, measurement setup, or model assumption, state that boundary explicitly.

Bad: "The device is stable at cryogenic temperatures."

Good: "The device remained stable across the tested cryogenic temperature range and bias conditions."

- [ ] **Confirm Citation Specificity**

Confirm that citations support the specific claim being made, not just the general topic.

Bad: "Cryogenic operation improves reliability [1]." Citation [1] only describes cryogenic measurement methods.

Good: "Cryogenic operation requires specialized measurement methods [1]."

- [ ] **Cross-Examine Data Consistency**

Cross-reference all numerical values, percentages, and metrics mentioned in the text against the data presented in the accompanying figures and tables to guarantee exact alignment. Verify that mathematical logic is strictly sound, particularly regarding baselines.

Example: Ensure percentage comparisons use the correct denominator. "A shows a 20% increase from B" with B = 100 and A = 120 does not equate to "B is a 20% reduction from A" because a 20% reduction of 120 is 96, not 100.

- [ ] **Audit Figure/Table Sequencing**

Confirm that all figures and tables are numbered sequentially, such as Figure 1 and Figure 2, and that every figure and table is explicitly called out and discussed in the main text.

- [ ] **Define Equation Variables**

Audit every mathematical equation. Ensure every variable is clearly defined immediately before or after the equation appears.

- [ ] **Evaluate Evidence Presentation**

Verify that logical leaps are avoided. Ensure that empirical evidence directly and logically supports the subsequent conclusions without overextending the data's implications.

Decision rule: Do not convert correlation into causation, limited measurements into general laws, or a single device result into a technology-wide conclusion.

Bad: "The reduced resistance proves that the interface mechanism controls device reliability."

Good: "The reduced resistance is consistent with an interface-related contribution to device behavior."

- [ ] **Audit Multi-Level Flow and Logic**

Perform a final logic-flow pass at the sentence, paragraph, and section levels. Ensure each sentence connects to the preceding and following context rather than reading as an isolated fact. Confirm that each paragraph has a clear internal progression, and that each section advances the larger argument in a coherent order.

Decision rule: A technically correct sentence should still be revised or relocated if its relationship to the surrounding argument is unclear.

Bad: "The device was measured at 77 K. Gallium nitride has a wide bandgap. The packaging parasitics were reduced."

Good: "The device was measured at 77 K to evaluate low-temperature operation. In this regime, gallium nitride's wide bandgap supports high-field operation, while reduced packaging parasitics help isolate the device-level response."

## Phase 5: Final Output Audit

- [ ] **Produce a Revision Log**

Produce a concise revision log identifying major changes to claims, structure, terminology, and evidence support.

Example revision log:

  - Clarified the research gap by specifying the tested operating range.
  - Replaced unsupported novelty language with a cited comparison to prior work.
  - Added boundary conditions to prevent overgeneralizing the measured result.

- [ ] **Perform Final Accuracy and Prose Review**

Re-read the revised text once for scientific accuracy and once for prose quality.
