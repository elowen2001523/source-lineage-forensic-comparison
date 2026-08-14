# Source-Lineage Forensic Comparison Framework

**A label-neutral, cross-domain methodology for reconstructing and comparing source lineages across research, AI, software, technical systems, organizations, and creative work.**

**Author:** Chuanyan Liu / Elowen
**Version:** v2.0
**Edition:** GitHub Public Release Edition
**Repository:** `source-lineage-forensic-comparison`

> **The goal is discrimination, not accusation.**

---

## What is this?

The **Source-Lineage Forensic Comparison Framework** is a structured methodology for investigating **which source-lineage explanation best accounts for the development of a work**.

It is designed for comparisons involving:

* academic papers and research programs
* AI and machine-learning systems
* software and technical architectures
* products and organizational outputs
* technical writing
* model-generated or AI-assisted work
* cross-language materials
* creative works
* multi-version and multi-author projects

Traditional comparison often asks:

> Do these two outputs look similar?

This framework asks a harder question:

> **What lineage best explains the observed structure, and does that explanation survive native-history reconstruction, prior-art control, calibration, alternative explanations, authorship changes, AI or translation effects, intermediary transmission, and provenance testing?**

The framework does not assume that the earliest visible candidate source is the original source.

It does not assume that the Target directly accessed the original Source.

It does not assume that multiple similarities are independent evidence.

And it does not treat the Source itself as a automatically “clean” originality baseline.

---

# Core principle

A strong source-lineage analysis should first establish:

1. what the **Source's own history** can explain,
2. what the **Target's own history** can explain,
3. what **common prior art** can explain,
4. whether **multiple sources or intermediaries** provide a better model,
5. whether apparently distinctive features are actually common in the background population,
6. whether AI, translation, organizational templates, or contributor changes create benign convergence,
7. and whether the remaining evidence is genuinely independent.

Only after those layers are separated should chronology, access, authorization, knowledge, conduct, and governance increase the strength of a source-level conclusion.

---

# What v2.0 changes

Version 2.0 expands the framework beyond a simple:

`Source → Target`

comparison.

It models provenance as a **lineage graph**.

Possible structures include:

```text
Source A ───────→ Target
```

```text
Source A → Intermediary B → Target
```

```text
Prior Art P
   ↙      ↘
Source A  Target
```

```text
Source A ─┐
Source B ─┼──→ Target
Source C ─┘
```

```text
Native Target History ─┐
Prior Art ──────────────┼──→ Target
External Source ────────┘
```

This allows the framework to represent direct influence, mediated influence, common ancestry, mixed synthesis, serial transmission, and parallel convergence.

---

# Competing hypotheses

v2.0 keeps several explanations active at the same time.

### H0 — Native / Independent

The Target is primarily generated from its own prior history.

### H1 — Common Prior Art / Convergence

The observed correspondence is explained by shared literature, standards, engineering constraints, common models, or broader environmental pressure.

### H2 — Direct Source Influence

A specific Source materially influenced important Target structures after direct access.

### H3 — Mixed Synthesis

The Target combines native development, common prior art, and one or more external sources.

### H4 — Multi-Source Ecology

Different external sources or intermediaries better explain different high-level regions of the Target.

### H5 — Mediated Transmission

The Target may not have directly accessed the original Source, but may have received structurally conserved information through an intermediary.

The framework does not force every case into a single-source explanation.

---

# 1. Source and Target are audited symmetrically

One of the most important v2.0 upgrades is:

> **The Source must also prove its own lineage.**

A candidate Source is not automatically treated as an original, stable baseline.

Before comparison, the framework asks:

* When did the Source's key conceptual bridge first appear?
* Is that structure stable across the Source author's earlier work?
* Did a new contributor introduce it?
* Can common prior art explain it?
* Does the Source have its own Claim → Formalization → Implementation history?
* Is the candidate feature actually an unexplained anomaly inside the Source itself?

This creates a **Source Native Generator / Source Generator Validity** test.

The Target receives the same treatment through its own Target-before lineage reconstruction.

Only after both sides are frozen does formal alignment begin.

---

# 2. Multi-Source Lineage Graph

Real provenance is often not binary.

The framework therefore models lineage as a graph whose nodes may include:

* papers
* authors
* teams
* organizations
* models
* repositories
* internal documents
* blogs
* talks
* intermediate publications
* prior art

Possible edge types include:

| Edge                 | Meaning                                                    |
| -------------------- | ---------------------------------------------------------- |
| Direct influence     | Source directly influences Target                          |
| Mediated influence   | Source → intermediary → Target                             |
| Common ancestor      | Both descend from earlier prior art                        |
| Mixed synthesis      | Multiple sources explain different regions                 |
| Serial transmission  | A structure is repeatedly re-encoded across several steps  |
| Parallel convergence | Similar constraints independently generate similar results |

If several lineage graphs remain viable, the framework preserves them instead of selecting whichever one “looks most similar.”

---

# 3. Intermediary Transmission

Direct access is not always necessary for historical influence.

A structure may travel through:

```text
Original Source
      ↓
technical reinterpretation
      ↓
blog / paper / code / AI summary
      ↓
Target
```

An intermediary may:

* rename concepts
* compress a theory
* translate it
* formalize it
* remove context
* convert it into engineering terminology
* expose only a subset of the original structure

The audit therefore tracks:

**Original Source → Intermediary → Target**

and examines which high-information features survive each transformation.

---

# 4. Candidate Source Selection Control

A major forensic risk is **source shopping**.

An auditor can look at the Target first, search thousands of works, and eventually find something that appears unusually similar.

Freezing a fingerprint afterward does not fully remove that bias.

v2.0 therefore requires a **Candidate Source Selection Log** recording:

* when a candidate entered the pool
* why it was selected
* whether the auditor had already seen the Target
* how many candidates were tested
* which candidates failed
* which queries and platforms were used
* what search rules were applied

Negative candidates should not silently disappear.

---

# 5. Calibration and Background Prevalence

A pattern is only useful as a source fingerprint if it is relatively uncommon outside that source.

The framework therefore recommends calibration sets such as:

* same-domain negative controls
* cross-domain negative controls
* same-author negative samples
* same-organization samples
* AI-generated controls
* human-edited AI controls

This helps distinguish:

> “This resembles the Source.”

from:

> “This is how almost everyone in this field writes or solves the problem.”

The framework does **not** convert these controls into a pseudo-precise plagiarism probability.

Their purpose is calibration.

---

# 6. AI-Mediated Homogenization Control

Modern AI-assisted writing can cause unrelated authors to converge on similar surface patterns.

Examples include:

* standardized abstract structures
* predictable section ordering
* technical tone
* phrases such as “we observe,” “therefore,” or “specifically”
* Claim → Mechanism explanatory templates
* polished transition language

These signals should generally receive low weight.

More informative features include:

* rare conceptual bridges
* non-obvious ordering
* unusual boundary conditions
* the same rare exception
* the same error and repair sequence
* stable cross-domain reasoning policies

The framework therefore attempts to separate **AI surface convergence** from deeper lineage signals.

---

# 7. Cross-Language and Translation Audit

Cross-language provenance creates two opposite risks:

### False positives

Machine translation or shared technical vocabulary may make independent works appear unusually similar.

### False negatives

A genuine lineage relationship may become invisible after translation or terminology substitution.

The framework therefore compares:

* semantic roles
* relation graphs
* rhetorical function
* language-neutral logical skeletons
* language-specific prior art
* machine-translation convergence

Surface wording is treated as only one low-level signal.

---

# 8. Error / Defect Inheritance

Shared correct answers are often produced by shared problems.

Shared **rare mistakes** can be much more informative.

The framework separately audits:

* rare factual errors
* unnecessary formal errors
* strange classifications
* incorrect citation chains
* unusual implementation bugs
* peculiar workarounds
* correction coupling

A shared error is not automatically a lineage result: common bugs, shared templates, and prior implementations must still be controlled.

---

# 9. Failure → Repair → Refinement Lineage

Even more informative than a shared error can be a shared **repair history**.

For example:

```text
Failure E
   ↓
Repair P1
   ↓
Residual problem
   ↓
Refinement P2
```

If two systems independently face the same problem, they may initially converge.

They are more likely to diverge once multiple repair strategies become available.

The framework therefore treats a rare:

**E → P1 → P2**

repair sequence as a distinct lineage object.

---

# 10. Temporal Burst and Change Velocity

A new idea appearing quickly is not proof of external influence.

But the **density and timing of change** can still be informative.

v2.0 examines:

* conceptual novelty density
* simultaneous appearance of several new bridges
* exposure-to-appearance lag
* historical innovation rate
* bundled emergence of new framing, formalization, citations, and architecture

The relevant comparison is not simply:

> “Was this developed quickly?”

but:

> “Was this pattern of change unusually concentrated relative to the subject's own historical baseline?”

---

# 11. Human Knowledge Transfer Graph

Knowledge can enter an organization without appearing directly in a citation list.

Possible transmission paths include:

* new employees
* advisors
* interns
* research collaborators
* acquired teams
* external contractors
* open-source contributors
* reviewers
* partner organizations

The framework therefore maps:

**person / team → prior expertise → join time → exposure path → affected module**

This can support a source-lineage explanation.

It can also provide strong counterevidence when an apparently anomalous new capability is naturally explained by a newly added contributor.

---

# 12. Rediscovery Difficulty

“Someone could have independently discovered this” is a valid possibility.

But not every structure imposes the same independent-generation burden.

v2.0 therefore uses a qualitative Rediscovery Difficulty scale:

| Level                  | Typical pattern                                                    |
| ---------------------- | ------------------------------------------------------------------ |
| R0 — Low               | Obvious engineering consequence                                    |
| R1 — Moderate          | Several choices, but each is common                                |
| R2 — High              | Rare bridge + non-obvious sequence                                 |
| R3 — Very High         | Rare bridge + rare exception or negative space                     |
| R4 — Extreme candidate | Rare bridge + rare error + same repair path + temporal convergence |

This is **not a probability model**.

It exists to make the independent-development explanation explicit and auditable.

---

# 13. Expected Evidence Availability

Missing evidence should not automatically be treated as suspicious.

The framework asks:

> **Should this type of activity normally have produced a record?**

For example:

* open-source development normally produces commits
* a private conceptual insight may not produce drafts
* enterprise engineering may produce internal design documentation
* some organizations preserve detailed review records while others do not

Relevant questions include:

* What records would normally exist?
* Does the organization preserve them in other contemporary projects?
* Are only the disputed components undocumented?
* Are the records simply private or inaccessible?

Unavailable evidence remains **Unknown**, not malicious by default.

---

# 14. Pre-Registered Counterfactual Prediction

v2.0 strengthens out-of-sample testing by requiring predictions before sealed Target material is revealed.

If a Source fingerprint is genuinely explanatory, the auditor should be able to predict things such as:

* which bridge the Target will prefer
* which natural alternatives it will reject
* how it will handle boundary conditions
* which variables it will systematically ignore
* what evidence would falsify the fingerprint

The prediction is recorded first.

The sealed material is revealed afterward.

Both successes and failures must be preserved.

---

# 15. Evidence Dependency Graph

One of the central v2.0 principles is:

> **Many pieces of evidence are not necessarily many independent pieces of evidence.**

Suppose the same underlying conceptual structure appears as:

* similar wording
* a similar diagram
* a similar abstract
* a similar claim

Those may be four manifestations of one underlying correspondence.

The framework therefore classifies evidence as:

* **Independent**
* **Partially dependent**
* **Derived**
* **Duplicate manifestation**
* **Correlated by process**

Examples of process correlation include outputs generated by the same AI model, document template, organizational review process, or translation system.

The final report should identify which evidence streams truly converge independently.

---

# 16. Strong evidence-chain model

v2.0 separates the following evidence streams:

| Stream                     | Question                                                                      |
| -------------------------- | ----------------------------------------------------------------------------- |
| **S — Structure**          | What is structurally unusual?                                                 |
| **F — Fingerprint**        | Is it part of a stable Source generator?                                      |
| **SN — Source Native**     | Can the Source explain the structure through its own history?                 |
| **TN — Target Native**     | Can the Target explain it through its own history?                            |
| **M — Multi-Source Graph** | Is there a better common-ancestor, intermediary, or multi-source explanation? |
| **E — Error / Repair**     | Are rare mistakes or repair paths inherited?                                  |
| **T — Temporal**           | Does the chronology and rate of change fit?                                   |
| **A — Access**             | Who accessed what, directly or indirectly?                                    |
| **L — License**            | What was authorized?                                                          |
| **K — Knowledge**          | What could be proven known at each relevant time?                             |
| **C — Conduct**            | What happened afterward?                                                      |
| **G — Governance**         | What organizational controls existed or failed?                               |
| **D — Dependency Audit**   | How many of these evidence streams are actually independent?                  |

The framework first establishes structural and lineage anomalies.

Access and provenance are added later.

Evidence independence is checked before the final classification.

---

# Classification levels

| Level    | Classification                      |
| -------- | ----------------------------------- |
| **L0**   | No meaningful anomaly               |
| **L1**   | Surface / Template Correspondence   |
| **L2-A** | Structural Anomaly                  |
| **L2-B** | Generator / Native-Lineage Anomaly  |
| **L2-C** | Error / Repair Anomaly              |
| **L2-D** | Multi-Source / Intermediary Anomaly |
| **L3**   | Lineage Convergence                 |
| **L4**   | Provenance Convergence              |

### L0

The observed correspondence is adequately explained by prior art, background prevalence, AI or translation convergence, authorship structure, or native development.

### L1

Surface or template-level correspondence exists without high-specificity lineage evidence.

### L2-A

A rare structural combination, conceptual bridge, or ordering requires further explanation.

### L2-B

The Source has a stable generator while the Target's earlier native history does not yet naturally explain the same high-level structure.

### L2-C

Rare errors, non-optimal paths, or repair sequences correspond.

### L2-D

A multi-source or intermediary lineage explains the evidence better than a direct single-source model.

### L3

Structural evidence, Source-native analysis, Target-native analysis, calibration, and alternative-generator testing still converge on a stable lineage anomaly.

### L4

L3 is supplemented by independent provenance evidence such as chronology, access, knowledge, authorization, or conduct.

**L4 is still not an automatic legal conclusion.**

---

# Recommended audit workflow

A full v2.0 audit can proceed as follows:

1. Define the question, cutoff, and scope.
2. Freeze the candidate Source pool.
3. Create the Candidate Source Selection Log.
4. Build separate Source and Target corpora.
5. Record search coverage and unavailable materials.
6. Reconstruct Source-before native lineage.
7. Freeze the Source Native Generator and Source Fingerprint.
8. Build calibration controls.
9. Reconstruct Target-before native lineage.
10. Independently analyze Target-after structure.
11. Build the Multi-Source Lineage Graph.
12. Compare conceptual bridges, structural combinations, negative space, and reasoning policies.
13. Apply prior-art and base-rate controls.
14. Apply AI and translation convergence controls.
15. Audit Error / Defect Inheritance.
16. Audit Failure → Repair → Refinement lineage.
17. Analyze temporal burst and change velocity.
18. Build the Human Knowledge Transfer Graph.
19. Evaluate Expected Evidence Availability.
20. Pre-register counterfactual predictions.
21. Run sealed out-of-sample tests.
22. Perform version forensics.
23. Only then add Access and Authorization evidence.
24. Build Knowledge / Notice / Conduct timelines.
25. Audit organizational governance.
26. Build the Evidence Dependency Graph.
27. Test H0–H5 and the strongest competing lineage graphs.
28. Issue a graded report separating fact, inference, unknowns, counterevidence, and legal questions.

---

# Using this framework with Generative Continuity Audit Framework v2.0

These two frameworks are designed to work together.

## Generative Continuity Audit Framework v2.0

Answers:

> **How did this Target generate itself?**

It reconstructs:

* Target Native Generator
* Generator Identity
* conceptual bridges
* missing intermediate states
* generative seams
* semantic transformation
* information conservation
* historical negative space
* corpus completeness

Its purpose is to identify what the Target's own history can and cannot explain **before specific external Sources are introduced**.

---

## Source-Lineage Forensic Comparison Framework v2.0

Answers:

> **Given several possible sources and transmission paths, which lineage best explains the remaining anomalies?**

It adds:

* Source-side native-lineage validation
* candidate-source controls
* multi-source lineage graphs
* intermediary transmission
* calibration sets
* AI / translation controls
* error and repair inheritance
* temporal analysis
* human knowledge transfer
* provenance
* evidence-dependency auditing

---

# Recommended dual-framework workflow

```text
TARGET
  │
  ▼
Generative Continuity Audit v2.0
  │
  ├─ Target Native Generator Freeze
  ├─ Generator Identity Baseline
  ├─ Conceptual Bridge Provenance
  ├─ Missing Intermediate States
  ├─ Semantic Transformation Chain
  └─ Corpus Completeness
  │
  ▼
Frozen Generative Anomaly Objects
  │
  ▼
Source-Lineage Forensic Comparison v2.0
  │
  ├─ Candidate Source Pool Freeze
  ├─ Source Native Lineage Audit
  ├─ Multi-Source / Intermediary Graph
  ├─ Calibration & Prior-Art Control
  ├─ AI / Translation Control
  ├─ Error / Repair Lineage
  ├─ Temporal & Human Transfer Analysis
  └─ Evidence Dependency Graph
  │
  ▼
Provenance Layer
  │
  ├─ Chronology
  ├─ Access
  ├─ Authorization
  ├─ Knowledge
  ├─ Conduct
  └─ Governance
  │
  ▼
Final Classification
```

The key rule is:

> **Do not let a candidate Source shape the Target-native analysis.**

First determine where the Target genuinely has unexplained generative discontinuities.

Only then ask whether an external lineage explains those specific discontinuities.

---

# When to use which framework

| Situation                                                                        | Recommended approach                                            |
| -------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| You only want to know whether a work naturally developed from its own history    | **Generative Continuity Audit v2.0**                            |
| You already have several candidate sources                                       | **Source-Lineage Forensic Comparison v2.0**                     |
| The dispute involves multiple authors, versions, sources, or intermediaries      | **Use both**                                                    |
| You only have surface similarity and weak historical evidence                    | Start with **Generative Continuity Audit**                      |
| You already have strong access or notice evidence but unclear structural lineage | Return to **both frameworks** before drawing source conclusions |

---

# Reporting discipline

The framework distinguishes:

### FACT

What can be directly verified.

### INFERENCE

What the evidence supports but does not directly prove.

### UNKNOWN

What remains unresolved.

### COUNTEREVIDENCE

Evidence supporting native, benign, or alternative explanations.

### ALTERNATIVE

A competing lineage model that must be tested.

Public reporting should prefer language such as:

* structural anomaly
* native-lineage anomaly
* error/repair correspondence
* candidate intermediary transmission
* multi-source lineage candidate
* provenance convergence
* insufficient evidence to establish a source relationship

rather than prematurely converting analytical findings into accusations.

---

# What this framework does not assume

The framework does **not** assume that:

* similarity means copying
* a candidate Source is necessarily original
* direct access is required for all influence
* missing records mean misconduct
* multiple similarities are independent evidence
* AI-like writing proves common provenance
* translation similarity proves source dependence
* a shared error automatically proves copying
* rapid innovation proves external influence
* a lineage anomaly automatically establishes legal liability

Each of these requires separate testing.

---

# Evidence preservation

Serious audits should preserve:

* original files
* hashes
* timestamps
* URLs
* repository history
* archived pages
* candidate-source search logs
* negative search results
* version history
* contributor records
* translation / AI pipeline information where available
* provenance records
* chain-of-custody logs
* sealed predictions
* failed predictions
* alternative explanations

New evidence should result in a versioned update rather than silent revision.

---

# Public-use and legal note

This framework is a **methodology and research protocol**.

It does not itself create:

* a plagiarism finding
* a copyright infringement finding
* a trade-secret finding
* a contractual finding
* a judicial determination

Legal conclusions depend on jurisdiction, protectable subject matter, access, copying, authorization, statutory exceptions, contractual rights, evidence admissibility, damages, and other case-specific requirements.

Structural findings and legal conclusions should remain separate.

---

# Companion framework

This project is designed to be paired with:

**Generative Continuity Audit Framework & Manual v2.0**

The two frameworks serve different but complementary purposes:

> **Generative Continuity:**
> What can the Target's own history explain?

> **Source-Lineage Forensics:**
> What source graph best explains what remains?

---

# Framework document

The complete methodology is available in:

`Source_Lineage_Forensic_Comparison_Framework_v2.0_GitHub_Public_Release.pdf`

---

# Citation

Recommended citation:

**Chuanyan Liu (Elowen), *Source-Lineage Forensic Comparison Framework & Manual v2.0*, GitHub Public Release Edition, 2026.**

---

# Closing principle

A strong source-lineage investigation does not succeed by finding the Source that looks most similar.

It asks:

**What can the Source's own history explain?
What can the Target's own history explain?
What can common prior art explain?
Could an intermediary or several sources explain the pattern better?
How common is the alleged fingerprint in the background population?
Could AI, translation, contributors, or organizational processes explain the convergence?
Are rare errors and repair paths inherited?
Are missing records actually expected to exist?
And how many of the surviving evidence streams are truly independent?**

Only evidence that continues to converge after these controls should materially increase a source-lineage conclusion.

**The goal is discrimination, not accusation.**
