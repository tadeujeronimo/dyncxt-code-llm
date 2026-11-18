# DynCxt-Code-LLM

**Replication package** for the paper *Dynamic Context Management in Code LLMs: A Literature Review* (IEEE Access, submitted). The review analyzes, at the repository level, the effect of dynamic context management strategies on functional correctness and structural code quality, compared with static baselines.

The package supports the verification of the search, the selection, and the quality assessment reported in the paper (PRISMA 2020 flow: 605 records identified, 28 duplicates removed, 577 screened, 42 read in full, 31 assessed for quality, 26 included).

## Repository contents

| Path | Content | Paper reference |
| :--- | :--- | :--- |
| `search/search_queries.md` | Search string, database-specific settings, execution date, and record counts | Section III-F, Table 3 |
| `search/raw/` | Unfiltered exports of the four databases: `acm.bib` (456), `scopus.bib` (106), `wos.ris` (36), `ieee.bib` (7) | Section III-E |
| `data/quality_assessment.csv` | Quality assessment matrix (QA1 to QA5) of the 31 studies assessed: S1 to S26 (included) and D1 to D5 (disqualified, score below 3.0) | Section III-I, Section IV-C, Appendix B |
| `primary_studies.bib` | BibTeX records of the 26 included studies (S1 to S26) | Appendix A |
| `protocol/protocol_parsifal.pdf` | Review protocol (planning and conducting) in English, following the structure of the Parsifal export and the wording of the manuscript | Section III |

## Identifiers

- `S1` to `S26`: the 26 included studies, in the order of Appendix A of the paper (publication year, first author, and title).
- `D1` to `D5`: the five studies disqualified in the quality assessment (Appendix B, Group B), in the order of that appendix.
- The `BibTeX key` column of `quality_assessment.csv` links each row to `primary_studies.bib` for the included studies.

## Quality assessment matrix

Each criterion is scored 0, 0.5, or 1.0, and the total ranges from 0.0 to 5.0. Studies with a total below 3.0 were disqualified.

| Column | Criterion |
| :--- | :--- |
| `QA1 Reproducibility` | Availability of source code, scripts, prompts, seeds, and replication artifacts |
| `QA2 Soundness and scope` | Identification of models and static baselines, repository-level experiments, and statistical hypothesis tests |
| `QA3 Biases and stability` | Prevention of temporal data contamination and stability across multiple runs or seeds |
| `QA4 Functional correctness` | Validation of the generated code through executable test suites |
| `QA5 Quality and efficiency` | Analysis of nonfunctional or structural code attributes and/or computational efficiency, cost, or latency |

For the 26 included studies, the mean total is 3.81 (median 3.75), with 13 studies of high rigor (4.0 to 5.0) and 13 of medium rigor (3.0 to 3.5).

## Protocol and management

The protocol and the selection were managed on the [Parsifal](https://parsif.al/) platform. The protocol in `protocol/protocol_parsifal.pdf` follows the structure of the Parsifal export (planning and conducting). Its text is in English and uses the wording of the manuscript, in particular for the objectives, the research questions (RQ1 to RQ4), the eligibility criteria, and the quality criteria.

## How to cite

Use the metadata in `CITATION.cff` (GitHub shows a "Cite this repository" button) or the Zenodo record: <https://doi.org/10.5281/zenodo.23824626>.

## License

This package is shared under the [CC-BY 4.0](LICENSE) license.
