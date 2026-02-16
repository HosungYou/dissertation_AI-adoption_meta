# Master Integration Document — AI Adoption MASEM

> Central coordination document for the AI Adoption Meta-Analytic SEM dissertation.
> All decisions, cross-references, and integration points are tracked here.

## Document Version History

| Version | Date | Changes |
|---------|------|---------|
| 0.1.0 | 2026-02-16 | Initial scaffolding |

---

## 1. Project Overview

**Title**: Meta-Analytic Structural Equation Modeling of AI Adoption: Testing TAM/UTAUT Validity and the Incremental Contribution of AI-Specific Constructs

**Scope**: Quantitative synthesis of empirical AI adoption studies (2015–2025) using MASEM to simultaneously test structural path models across pooled correlation matrices from ~200+ primary studies.

---

## 2. Construct Registry (12 Standard Constructs)

| ID | Construct | Abbr | Role in Model |
|----|-----------|------|---------------|
| 1 | Performance Expectancy | PE | Core predictor (TAM/UTAUT) |
| 2 | Effort Expectancy | EE | Core predictor (TAM/UTAUT) |
| 3 | Social Influence | SI | Core predictor (UTAUT) |
| 4 | Facilitating Conditions | FC | Core predictor (UTAUT) |
| 5 | Behavioral Intention | BI | Core mediator |
| 6 | Use Behavior | UB | Core outcome |
| 7 | Attitude | ATT | Mediator (TAM) |
| 8 | Self-Efficacy | SE | Antecedent |
| 9 | AI Trust | TRU | AI-specific predictor |
| 10 | AI Anxiety | ANX | AI-specific predictor |
| 11 | AI Transparency | TRA | AI-specific antecedent |
| 12 | Perceived AI Autonomy | AUT | AI-specific antecedent |

---

## 3. Analysis Module Cross-Reference

| Module | R Script | Input Data | Output | Dependencies |
|--------|----------|-----------|--------|-------------|
| Data Prep | `01_data_preparation.R` | `data/02_verified/` | Cleaned matrices | None |
| Stage 1 Pooling | `02_stage1_pooling.R` | Cleaned matrices | `data/03_pooled/` | Module 1 |
| Stage 2 SEM | `03_stage2_sem.R` | Pooled matrix | Path coefficients | Module 2 |
| Competing Models | `04_competing_models.R` | Pooled matrix | Model comparison | Module 2 |
| OSMASEM | `05_osmasem_moderators.R` | Raw matrices + moderators | Moderation effects | Module 1 |
| Temporal | `06_temporal_analysis.R` | Raw matrices + years | Pre/post comparison | Module 1 |
| Mediation | `07_mediation.R` | Pooled matrix | Indirect effects | Module 2 |
| Heterogeneity | `08_heterogeneity.R` | Raw correlations | I², τ², PI | Module 1 |
| Pub Bias | `09_publication_bias.R` | Raw correlations | Bias diagnostics | Module 1 |
| Sensitivity | `10_sensitivity.R` | r-only + r+β datasets | Robustness check | Module 1 |
| Bayesian MASEM | `11_bayesian_masem.R` | Pooled matrix + priors | Posteriors, BF | Module 2 |
| Network | `12_network_analysis.R` | Pooled matrix | Network metrics | Module 2 |
| Visualization | `13_visualization.R` | All outputs | Figures | All modules |

---

## 4. Key Decision Log

| Date | Decision | Rationale | Reference |
|------|----------|-----------|-----------|
| 2026-02-16 | 12 constructs (not 8 or 16) | Balance between comprehensiveness and data availability | Plan v1 |
| 2026-02-16 | Include β→r conversion | Many AI studies report only β; Peterson & Brown (2005) conversion is standard | Plan v1 |
| 2026-02-16 | 3-model comparison approach | Tests TAM/UTAUT validity, integrated model, and AI-only model | Plan v1 |
| 2026-02-16 | Sabherwal priors for Bayesian | Direct quantitative comparison: general IT vs. AI contexts | Plan v1 |
| 2026-02-16 | MAGNA network analysis | Triangulation: confirmatory (SEM) + exploratory (network) | Plan v1 |

---

## 5. Data Flow

```
PDFs → Phase 0 (RAG Index)
     → Phase 1 (AI Extraction) → Phase 2 (Construct Mapping)
     → Phase 3 (3-Model Consensus) → Phase 4 (ICR Sampling)
     → Phase 5 (Human Resolution) → Phase 6 (QA Final)
     → data/04_final/ → R Analysis Pipeline
```

---

## 6. Quality Gates

| Gate | Criterion | Script |
|------|-----------|--------|
| G1 | All correlation matrices are positive definite | `01_data_preparation.R` |
| G2 | κ ≥ .85 for categorical, ICC ≥ .95 for numerical | `phase4_sampling_icr.py` |
| G3 | TSSEM Stage 1 converges | `02_stage1_pooling.R` |
| G4 | All competing models converge | `04_competing_models.R` |
| G5 | MCMC chains converge (R̂ < 1.01) | `11_bayesian_masem.R` |
| G6 | Network stability CS > 0.50 | `12_network_analysis.R` |

---

## 7. Manuscript Mapping

| Manuscript Section | Data Source | Script |
|-------------------|------------|--------|
| Table 1: Study characteristics | `data/04_final/` | — |
| Table 2: Pooled correlation matrix | `data/03_pooled/` | `02_stage1_pooling.R` |
| Table 3: Path coefficients | `analysis/output/path_coefficients/` | `03_stage2_sem.R` |
| Table 4: Model comparison | `analysis/output/model_comparison/` | `04_competing_models.R` |
| Table 5: Moderation results | `analysis/output/` | `05_osmasem_moderators.R` |
| Figure 1: PRISMA flow diagram | `supplementary/prisma/` | `generate_prisma.py` |
| Figure 2: Path diagram | `figures/output/` | `13_visualization.R` |
| Figure 3: Forest plots | `figures/output/` | `13_visualization.R` |
| Figure 4: Bayesian posteriors | `analysis/output/bayesian_posteriors/` | `11_bayesian_masem.R` |
| Figure 5: Network graph | `analysis/output/network_graphs/` | `12_network_analysis.R` |
