# Database Coverage and Characteristics

## Overview

This document details the characteristics, coverage, and expected contribution of each database to the systematic literature search for AI adoption meta-analysis.

## Database Comparison Table

| Database | Subject Coverage | Unique Strengths | Expected Hits | Overlap with Others |
|----------|------------------|------------------|---------------|---------------------|
| Web of Science | Multidisciplinary, high-impact journals | Citation tracking, quality filtering | 800-1,200 | High with Scopus (60-70%) |
| Scopus | Broader multidisciplinary | More regional journals, conference proceedings | 1,000-1,500 | High with WoS (60-70%) |
| PsycINFO | Psychology, behavioral sciences | Individual acceptance, attitudes, anxiety | 300-500 | Moderate (30-40%) |
| IEEE Xplore | Engineering, computer science | Technical AI systems, HCI | 400-600 | Moderate with ACM (50%) |
| ACM Digital Library | Computing, information systems | User experience, interaction design | 300-450 | Moderate with IEEE (50%) |
| Google Scholar | Universal | Grey literature, preprints, recent work | 2,000+ (supplementary only) | Very high (80-90%) |

## Database-Specific Details

### Web of Science (Core Collection)

**Coverage:**
- 21,000+ peer-reviewed journals
- Conference proceedings (selective)
- Strong in business, management, psychology, computer science

**Indexed Fields Searched:**
- Title (TI)
- Abstract (AB)
- Author Keywords (AK)
- Keywords Plus (WoS-assigned terms)

**Date Coverage:**
- 2015-2025 for this search
- Historical coverage varies by journal

**Export Format:**
- Plain text, BibTeX, RIS
- **Preferred:** RIS (most complete metadata)

**Expected Contribution:**
- High-quality AI adoption studies in top-tier journals
- Strong coverage of UTAUT/TAM applications
- Business and organizational AI adoption

**Search Fields Used:**
```
TS=(search string)
```
Where TS = Topic (Title + Abstract + Keywords + Keywords Plus)

**Filters Applied:**
- Document Type: Article, Proceedings Paper
- Language: English
- Timespan: 2015-2025

---

### Scopus

**Coverage:**
- 27,000+ peer-reviewed journals
- More international and regional journals than WoS
- Strong conference proceeding coverage

**Indexed Fields Searched:**
- Title
- Abstract
- Author Keywords
- Indexed Keywords

**Date Coverage:**
- 2015-2025 for this search
- Comprehensive from 1996 onwards

**Export Format:**
- CSV, RIS, BibTeX
- **Preferred:** RIS

**Expected Contribution:**
- Broader geographic coverage (Asian, European regional journals)
- AI adoption in emerging markets
- Conference proceedings with full papers

**Search Fields Used:**
```
TITLE-ABS-KEY(search string)
```

**Filters Applied:**
- Document Type: Article, Conference Paper
- Language: English
- Publication Stage: Final
- Date: 2015-2025

**Unique Value:**
- More comprehensive than WoS (27k vs 21k journals)
- Better coverage of non-US journals
- Strong in engineering and computer science

---

### PsycINFO

**Coverage:**
- 2,500+ journals in psychology and behavioral sciences
- Strong in individual behavior, attitudes, acceptance
- Unique thesaurus of psychological constructs

**Indexed Fields Searched:**
- Title
- Abstract
- Keywords (author and APA thesaurus terms)

**Date Coverage:**
- 2015-2025 for this search
- Historical coverage to 1800s (comprehensive from 1967)

**Export Format:**
- RIS, APA PsycNET format
- **Preferred:** RIS

**Expected Contribution:**
- Individual-level AI acceptance and attitudes
- AI anxiety, trust, self-efficacy constructs
- Health, education psychology applications

**Thesaurus Terms Used:**
```
Artificial Intelligence (Thesaurus)
Technology Adoption (Thesaurus)
User Attitudes (Thesaurus)
Behavioral Intention (Thesaurus)
Computer Anxiety (Thesaurus)
Self-Efficacy (Thesaurus)
```

**Filters Applied:**
- Methodology: Quantitative, Empirical Study
- Language: English
- Age Group: (no filter - all populations)
- Publication Type: Journal Article, Conference Paper

**Unique Value:**
- Best coverage of psychological constructs (anxiety, trust, self-efficacy)
- Strong in educational and healthcare AI adoption
- Rigorous behavioral science methodology

---

### IEEE Xplore

**Coverage:**
- 5+ million documents in electrical engineering, computer science, electronics
- Conference proceedings (IEEE-sponsored)
- Standards, technical reports (excluded in this search)

**Indexed Fields Searched:**
- Document Title
- Abstract
- Index Terms (IEEE controlled vocabulary)

**Date Coverage:**
- 2015-2025 for this search
- Comprehensive from 1988 onwards

**Export Format:**
- CSV, BibTeX, RIS
- **Preferred:** BibTeX (best IEEE metadata)

**Expected Contribution:**
- Technical AI systems adoption
- Human-AI interaction
- Early AI adoption studies (CS researchers adopt early)

**Search Fields Used:**
```
("Abstract": artificial intelligence) AND ("Abstract": adoption OR acceptance)
```

**Filters Applied:**
- Content Type: Journals, Conferences
- Year: 2015-2025

**Unique Value:**
- Earliest AI adoption studies (technical community)
- Explainability, transparency constructs
- Autonomous systems, robotics adoption

---

### ACM Digital Library

**Coverage:**
- 1+ million articles and proceedings in computing
- ACM-published journals and conferences
- Strong in human-computer interaction

**Indexed Fields Searched:**
- Title
- Abstract
- Keywords
- ACM Computing Classification System (CCS) categories

**Date Coverage:**
- 2015-2025 for this search
- Comprehensive from 1950s

**Export Format:**
- BibTeX, EndNote, ACM Ref
- **Preferred:** BibTeX

**Expected Contribution:**
- HCI perspective on AI adoption
- User experience with AI systems
- Interaction design, usability

**CCS Categories Filtered:**
```
Human-centered computing → Human computer interaction (HCI)
Human-centered computing → Empirical studies in HCI
Computing methodologies → Artificial intelligence
```

**Filters Applied:**
- Publication Type: Research Article, Proceedings
- Year: 2015-2025

**Unique Value:**
- HCI community's AI adoption research
- User experience and interface studies
- Explainability and transparency focus

---

### Google Scholar (Supplementary)

**Coverage:**
- Universal (journals, books, theses, preprints, reports)
- No quality filtering
- Includes grey literature

**Search Approach:**
- **NOT used for primary systematic search** (lack of reproducibility)
- Used for backward/forward citation searching only
- Used to identify recent preprints and working papers

**Citation Searching Protocol:**
1. Identify top 20 most-cited studies from database search
2. Use "Cited by" function to find forward citations
3. Review 50 most recent citations per seed paper
4. Apply same inclusion/exclusion criteria

**Expected Contribution:**
- Recent preprints (2024-2025)
- Working papers from top institutions
- Grey literature from think tanks, industry research

**Limitations:**
- No controlled vocabulary
- Duplicate detection difficult
- Quality varies widely
- Not reproducible (results change daily)

**Justification for Supplementary Use Only:**
- PRISMA guidelines recommend transparent, reproducible searches
- Google Scholar lacks advanced search operators and stable results
- Used only for citation chasing, not primary search

---

## Field Mapping Across Databases

| Concept | WoS Field | Scopus Field | PsycINFO Field | IEEE Field | ACM Field |
|---------|-----------|--------------|----------------|------------|-----------|
| AI Technology | Topic (TS) | TITLE-ABS-KEY | Title/Abstract | Abstract | Title/Abstract |
| Adoption | Topic (TS) | TITLE-ABS-KEY | Thesaurus + Text | Abstract | Title/Abstract |
| Methodology | Topic (TS) | TITLE-ABS-KEY | Methodology Filter | Full text | Full text |

## Duplicate Handling Strategy

### Expected Overlap Rates
- WoS ↔ Scopus: 60-70% (both multidisciplinary, high-quality journals)
- IEEE ↔ ACM: 40-50% (computing overlap)
- PsycINFO ↔ WoS/Scopus: 30-40% (psychology journals indexed in multidisciplinary DBs)
- Any DB ↔ Google Scholar: 80-90% (GS indexes almost everything)

### Deduplication Protocol

**Step 1: Automated Deduplication (Zotero)**
- Match on DOI (highest priority)
- Match on Title + First Author + Year
- Match on PMID, ISBN (if applicable)

**Step 2: Manual Review of Near-Duplicates**
- Same authors, similar titles, same year → likely duplicate
- **Priority rule:** Keep version with most complete data
  1. Journal article > conference paper (if both available)
  2. Final published version > preprint
  3. Version with correlation matrix > version without

**Step 3: Duplicate Sample Identification**
- Same author team + overlapping data collection period → flag as potential duplicate sample
- Review methodology sections during full-text screening
- If duplicate samples confirmed: keep most complete analysis

### Duplicate Tracking
Create `duplicates_log.csv`:
- original_id
- duplicate_id
- match_reason (DOI, title, etc.)
- resolution (kept, removed)
- kept_version_source

---

## Export Formats and Metadata Completeness

| Database | Format | DOI Coverage | Abstract Coverage | Keywords Coverage | Full-Text Link |
|----------|--------|--------------|-------------------|-------------------|----------------|
| Web of Science | RIS | 95%+ | 100% | 100% | Via library resolver |
| Scopus | RIS | 98%+ | 100% | 100% | Via library resolver |
| PsycINFO | RIS | 90%+ | 100% | 100% (Thesaurus) | Via library resolver |
| IEEE | BibTeX | 100% | 100% | 95% | Direct IEEE links |
| ACM | BibTeX | 100% | 100% | 90% (CCS codes) | Direct ACM links |

**Quality Check:**
- Verify DOI presence in ≥90% of exported records
- Verify abstract presence in 100% of exported records
- If missing, manually retrieve from publisher website

---

## Search Execution Tracking

### Log Template

```csv
database,search_date,search_time,n_results,filters_applied,exported_file
Web of Science,2026-02-16,10:30,1047,"Article|Proceedings; EN; 2015-2025",wos_export_20260216.ris
Scopus,2026-02-16,11:15,1523,"Article|ConferencePaper; EN; Final; 2015-2025",scopus_export_20260216.ris
PsycINFO,2026-02-16,14:00,412,"Quantitative; EN; 2015-2025",psycinfo_export_20260216.ris
IEEE Xplore,2026-02-16,15:30,678,"Journals|Conferences; 2015-2025",ieee_export_20260216.bib
ACM Digital Library,2026-02-16,16:45,389,"Research Article|Proceedings; 2015-2025",acm_export_20260216.bib
```

---

## Database Access and Institutional Subscriptions

**Institutional Access Required:**
- Web of Science: Yes (institutional subscription)
- Scopus: Yes (institutional subscription)
- PsycINFO: Yes (via EBSCOhost or Ovid)
- IEEE Xplore: Partial (many open access; subscription for full access)
- ACM Digital Library: Partial (ACM membership or institutional subscription)
- Google Scholar: No (free, public access)

**Access Verification:**
- Confirm institutional access to all databases before search execution
- Verify VPN access for off-campus searching
- Document subscription coverage dates

---

## Expected Study Yield

### Optimistic Scenario
- Total raw hits: 4,500-5,000
- After deduplication: 3,000-3,500
- After title/abstract screening: 400-600
- After full-text review: 150-250 included studies

### Conservative Scenario
- Total raw hits: 3,000-3,500
- After deduplication: 2,000-2,500
- After title/abstract screening: 250-350
- After full-text review: 80-120 included studies

### Target
- **k ≥ 100 studies** for stable MASEM estimates
- **N > 20,000 total participants** for adequate power
- **≥10 studies per correlation cell** for Stage 1 TSSEM

---

## Quality Indicators by Database

| Database | Peer Review | Impact Factor Filter | Methodology Filter | Citation Data |
|----------|-------------|----------------------|--------------------|---------------|
| Web of Science | Yes | Yes (JCR quartiles) | No | Yes (cited reference search) |
| Scopus | Yes | Yes (CiteScore) | No | Yes (Scopus API) |
| PsycINFO | Yes | No | Yes (Empirical/Quantitative) | Limited |
| IEEE Xplore | Yes (IEEE-sponsored) | No | No | Yes (IEEE Xplore API) |
| ACM Digital Library | Yes | No | No | Yes (ACM DL API) |

---

## References

Bramer, W. M., Rethlefsen, M. L., Kleijnen, J., & Franco, O. H. (2017). Optimal database combinations for literature searches in systematic reviews: A prospective exploratory study. *Systematic Reviews*, 6(1), 245.

Gusenbauer, M., & Haddaway, N. R. (2020). Which academic search systems are suitable for systematic reviews or meta-analyses? Evaluating retrieval qualities of Google Scholar, PubMed, and 26 other resources. *Research Synthesis Methods*, 11(2), 181-217.
