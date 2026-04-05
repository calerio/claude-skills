---
name: critical-evaluation
description: >
  Use this skill whenever the user uploads or pastes an article, essay, opinion piece, blog post, news report, academic paper, or any text and wants it critically analysed.
  Triggers include phrases like "analyse this", "is this propaganda", "break this down", "evaluate this article", "what is the intent here", "go through this with the frameworks", "what's wrong with this argument", "is this legit", "steelman this", or any casual request to scrutinise a piece of writing.
  Always use this skill when an article or piece of writing is provided for critical scrutiny — even if the request is casual or the topic is unfamiliar.
  Produces a structured critical evaluation using combined analytical frameworks: genre detection, claim taxonomy with evidence quality, speech act analysis, rhetorical device identification, falsifiability assessment, intent classification, audience analysis, framing analysis, source evaluation, and a steelman of the core argument.
---

# Critical Evaluation Skill

A structured, topic-agnostic framework for critically analysing articles, essays, opinion pieces, news reports, academic papers, and any argumentative or informational text. Combines multiple analytical lenses into one coherent evaluation.

**Core constraint:** Do not make moral judgements about the subject matter. Do not endorse or condemn the article's position. Describe, classify, and analyse only. You may and should freely assess the *quality of reasoning* — logical weakness, evidential gaps, rhetorical sleight of hand — but never rule on whether the *cause or position itself* is right or wrong.

---

## Output Structure

Produce the following sections in order:

---

### 1. ARTICLE TYPE & GENRE

Before anything else, identify what kind of text this is. The genre sets the baseline expectations against which everything else is measured.

Classify using one or more of:

| Genre | Baseline expectation |
|---|---|
| **Hard news report** | Neutral, fact-first, inverted pyramid, sources attributed |
| **Analysis / explainer** | Contextualises facts, interpretive but grounded in evidence |
| **Op-ed / opinion column** | Openly subjective, argument-driven, expected to persuade |
| **Editorial** | Institutional voice, prescriptive, represents outlet's position |
| **Investigative journalism** | Evidence-heavy, primary sources, exposes wrongdoing |
| **Polemic / essay** | Sustained argument, often passionate, literary register |
| **Academic / research paper** | Peer-reviewed (or aspiring to be), methodology-driven, citations |
| **First-person testimony** | Experiential, authority derives from witness status |
| **Blog / newsletter / Substack** | Variable — could be any of the above but with fewer editorial checks |
| **Advocacy / campaign material** | Openly mobilising, calls to action, aligned with an organisation |

State the genre and note whether the piece *behaves consistently with its genre* or whether it borrows the conventions of one genre while functioning as another (e.g. a news report that reads like an op-ed, or an op-ed that presents itself as investigative journalism).

---

### 2. SUMMARY

A neutral, compressed summary of the article's content. 3–5 sentences. No editorialising. Stick to what the piece actually says.

---

### 3. CLAIM TAXONOMY & EVIDENCE QUALITY

Go through the article's major claims and classify each one using this system:

| Category | Definition | Example |
|---|---|---|
| **Fact** | Verifiable, uncontested, falsifiable | "GDP grew 2.1% in Q3 2024" |
| **Contested empirical claim** | Looks like a fact but evidence is genuinely disputed among experts | "Lockdowns reduced COVID mortality" |
| **Opinion** | Subjective assessment or preference | "This policy is a moral failure" |
| **Normative judgement** | Ethical/moral claim about what ought to be | "Universal healthcare is a human right" |
| **Narrative** | An interpretive frame that organises facts into a story; not directly falsifiable | "The West is in decline" |

List 5–8 major claims from the article. For each, provide:

1. **The claim** — quote or paraphrase it
2. **Classification** — which category it belongs to
3. **Presentation gap** — is it presented *as* a different category than it actually is? (e.g. a narrative dressed as a fact, an opinion presented as settled consensus)
4. **Evidence quality** — what evidence does the author provide for this claim? Rate it:
   - **Strong**: Peer-reviewed research, official statistics, primary documents, multiple independent sources
   - **Moderate**: Credible reporting, named expert opinion, single-source but verifiable data
   - **Weak**: Anecdote, unnamed sources, appeal to common knowledge, no evidence offered
   - **None**: Claim is asserted without support

---

### 4. SPEECH ACT ANALYSIS

Classify what the author is *doing* with language throughout the piece, using Austin/Searle's speech act categories:

- **Describing**: Reporting what happened
- **Evaluating**: Assessing whether something is good/bad
- **Interpreting**: Explaining what something means
- **Prescribing**: Arguing what should be done
- **Performing**: Using language to *do* something (accuse, warn, rally, condemn, absolve)

Identify the dominant speech acts. Note any places where the author is *performing* something (rallying, accusing, alarming) while presenting it as mere *describing*.

---

### 5. RHETORICAL DEVICES & REASONING PATTERNS

Identify notable rhetorical techniques and reasoning patterns used in the piece. Flag both effective techniques and problematic ones. Common patterns to watch for:

**Persuasion techniques:**
- Appeal to authority, appeal to emotion, appeal to common sense
- Anecdote used as evidence, vivid particular standing in for general trend
- Strategic concession (acknowledging a minor point to strengthen a larger claim)
- Inclusive "we" or "our" to manufacture consensus

**Logical weaknesses (if present):**
- Straw man (misrepresenting an opposing position)
- False dichotomy (presenting only two options when more exist)
- Motte-and-bailey (defending a weak claim by retreating to a stronger one)
- Equivocation (shifting the meaning of a key term mid-argument)
- Cherry-picking (selective evidence)
- Post hoc reasoning (correlation presented as causation)
- Begging the question (assuming the conclusion in the premise)

**Framing techniques:**
- Loaded language, euphemism, or dysphemism
- Passive voice to obscure agency ("mistakes were made")
- Strategic juxtaposition (placing unrelated facts next to each other to imply a connection)

Only flag what is actually present — do not force a checklist. Note whether the devices are used transparently or covertly.

---

### 6. FALSIFIABILITY AXIS

Rate the article's central thesis on this spectrum:

```
CLEARLY FALSIFIABLE ←————————————————→ NOT FALSIFIABLE
     (fact-claim)    (empirical dispute)  (opinion/value)  (narrative/ideology)
```

Address two questions:

1. **Could the core argument be proven wrong, and how?** What evidence would need to emerge? What data would count against it?
2. **Does the author acknowledge any conditions under which they would revise their position?** If no such conditions are stated or implied, the argument is closer to ideological commitment than to empirical inquiry — note this.

---

### 7. INTENT CLASSIFICATION

Classify the article's primary intent. Use one or more of:

- **Inform**: Convey facts or findings neutrally
- **Contextualise**: Place an event within a broader explanatory frame without necessarily arguing for a position
- **Persuade**: Change the reader's view on a specific question
- **Mobilise**: Move the reader to action or allegiance
- **Alarm**: Create urgency or fear around a threat
- **Provoke**: Deliberately inflammatory to generate engagement or reaction, distinct from genuine alarm
- **Legitimise**: Provide cover or authority for a position already held
- **Delegitimise**: Undermine the credibility of a person, group, or idea
- **Bear witness**: First-person testimony; primary purpose is to record experience

Most articles have more than one intent. Rank them from dominant to secondary.

---

### 8. AUDIENCE ANALYSIS

Identify who this piece is written *for*. This shapes how every other finding should be interpreted.

- **Preaching to the choir**: Written for people who already agree; reinforces existing beliefs
- **Converting sceptics**: Written to persuade people who are undecided or mildly opposed
- **Reaching across the aisle**: Written to engage people who actively disagree
- **Informing the uninformed**: Written for readers with no prior position on the topic
- **Signalling to elites / institutions**: Written to influence decision-makers, not a general audience
- **Building in-group identity**: Written to define and strengthen a community

Note whether the piece's tone and assumptions are well-calibrated to its apparent audience, or whether it would likely alienate the readers it seems to be targeting.

---

### 9. FRAMING & OMISSION

Note:
- What the piece consistently emphasises
- What is absent or underweighted given the topic
- Whether extreme or atypical cases are presented as representative
- Any language choices that load the framing (e.g. "freedom fighter" vs "terrorist", "regime" vs "government", "surge" vs "increase")
- Whether counterarguments are engaged with, dismissed, or simply absent

---

### 10. SOURCE & CONTEXT FLAGS

- Who is the author and what is their track record, institutional affiliation, or known position?
- Where is it published and what is that outlet's known editorial line or audience?
- What is verifiable independently vs what relies solely on the author's account?
- Any conflicts of interest, funding sources, or methodological limitations worth flagging?
- Is there relevant context the reader would need to properly evaluate this piece that the article itself does not provide?

---

### 11. STEELMAN

State the strongest, most charitable version of the article's central argument — even if the article itself makes it poorly. This is not an endorsement; it is an intellectual exercise to ensure genuine engagement with the position rather than easy dismissal.

Format: "The strongest version of this argument is: ..."

If the article is primarily informational rather than argumentative, steelman the interpretive frame it uses instead.

---

### 12. OVERALL CLASSIFICATION

End with a single structured line using this template:

> **This piece is best described as:** [genre] + [dominant intent] + [epistemic status] + [outlet/author positioning]

Examples:
- "Op-ed with persuade/alarm intent, grounded in a mix of verifiable facts and contested empirical claims, published in a centre-left broadsheet by an author with an established position on the topic"
- "Investigative report with inform/delegitimise intent, well-sourced with primary documents, published in an outlet known for adversarial journalism"
- "Substack essay with persuade/contextualise intent, relying heavily on narrative framing with moderate evidence, by an independent commentator"

---

## Tone & Constraints

- **Do not make moral judgements** about the subject matter or the positions involved
- **Do not endorse or condemn** the article's position
- **Do freely assess reasoning quality** — you can and should say "this argument is logically weak", "this evidence doesn't support this conclusion", or "this rhetorical move obscures the actual claim"
- **Describe and classify only** when it comes to the substance of the debate itself
- If a claim is contested, say so and note what the dispute is — do not resolve it
- Distinguish clearly between what the article *says* and what is *independently verifiable*
- Do not assume bad faith without evidence of it — but do note when rhetorical choices have the *effect* of misleading, regardless of intent
- Maintain the same analytical rigour regardless of whether you agree or disagree with the article's position
