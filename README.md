# Beyond-the-Prototype-A-Systematic-Review-of-One-Dimensional-Learned-Indexes
Beyond the Prototype: A Systematic Review of One-Dimensional Learned Indexes with Emphasis on Dynamic Updates, String Keys, and Evidence Quality
<img width="511" height="561" alt="15 searching_flow_diagram drawio" src="https://github.com/user-attachments/assets/a0222fa2-f10c-4087-907f-ec952d441ff7" />

This project is the first PRISMA 2020-compliant systematic review of one-dimensional ordered learned indexes, covering the period from January 2018 to January 2026.

Purpose:
Since the introduction of the Recursive Model Index (RMI) by Kraska et al. in 2018, more than 65 learned index designs have been proposed. These structures aim to replace or augment traditional indexes (such as B-trees) by using machine learning models to learn the underlying data distribution and predict record positions, often delivering significant improvements in lookup speed and memory efficiency. Learned indexes are now being integrated into production storage engines and cloud database systems (e.g., Google Bigtable). However, no independent, systematic scrutiny of the benchmarking practices, reproducibility, robustness, or real-world readiness of these claims had been conducted prior to this work.

The primary purposes of this systematic review are:
To comprehensively map the design landscape of one-dimensional learned indexes, with particular emphasis on dynamic update mechanisms, string-key support, concurrency, crash-consistency (especially on persistent memory), and LSM-tree / key-value store integration.
To critically evaluate the methodological quality and credibility of the performance evidence presented in the literature using a purpose-built seven-domain methodological quality framework specifically designed for systems benchmarking studies.
To assess the overall certainty of evidence for key performance outcomes using an adapted GRADE approach.

Objectives and Research Questions:
The review addresses five main research questions (RQ1–RQ5) concerning architectural families, update mechanisms and trade-offs, string-key handling and failure modes, concurrency/crash-recovery/production readiness, and LSM-tree integration under realistic workloads.
Methods:
Seven major databases (ACM DL, IEEE Xplore, ScienceDirect, SpringerLink, MDPI, arXiv, Google Scholar) were searched on 10 January 2026, yielding 746 records after deduplication. Studies were included if they proposed or significantly extended a 1D ordered learned index with bounded error correction for exact match, range, or predecessor queries. A total of 65 studies met the eligibility criteria. Each study was assessed using the novel seven-domain risk-of-bias framework (covering baseline fairness, dataset realism, implementation transparency, experimental execution, reporting completeness, performance measurement rigour, and selective reporting). Evidence certainty was graded across five pre-specified outcomes.

Expected Outcomes / Key Contributions:
Structured taxonomies for dynamic update mechanisms (4 families) and string-key encoding strategies (3 main approaches).
A reusable seven-domain methodological quality framework and GRADE adaptation for future systems benchmarking reviews.
Regime-stratified synthesis of performance claims (point lookup, space efficiency, updates, range queries, concurrency) across six hardware-deployment regimes.
Clear identification of persistent gaps: adversarial robustness for string keys, fragmentation in NVM crash-consistency mechanisms, lack of external/independent validation, and weak performance measurement practices (especially variance reporting and confidence intervals).
Overall evidence certainty rating: LOW across all five pre-specified outcomes, despite generally positive directional findings.

This review both explains and embodies a rigorous, transparent approach to evaluating systems research. It provides actionable insights for practitioners considering adoption of learned indexes and offers clear priorities for future research (standardized string-key benchmarks, crash-consistency standardization, and more independent replication studies).
All materials (full extraction spreadsheet, risk-of-bias assessments, search strings, PRISMA diagram, etc.) are available in the associated OSF repository and GitHub.
This systematic review aims to move the field “Beyond the Prototype” by providing a sober, evidence-based assessment of where learned indexes stand in terms of technical maturity and evidential credibility as of early 2026.
