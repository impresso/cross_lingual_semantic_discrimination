# [Examining Multilingual Embedding Models Cross-Lingually Through LLM-Generated Adversarial Examples](https://arxiv.org/pdf/2502.08638) - Datasets and starter code
<img height="24" alt="emnlp2025 suzhou" src="https://github.com/user-attachments/assets/d3a426b1-a6f7-4ee7-9d42-47595b6f3f65" /> ![License: AGPLV3+](https://img.shields.io/badge/License-AGPLV3+-brightgreen.svg)

---

## Overview

This repository accompanies our [EMNLP2025 Findings paper](https://arxiv.org/pdf/2502.08638) and provides the datasets and starter code for evaluating multilingual embedding models under cross-lingual adversarial conditions.
The adversarial examples are generated via Large Language Models (LLMs) to systematically probe embedding robustness across languages.

---

## Table of Contents

- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Datasets](#datasets)
- [Citation](#citation)
- [About Impresso](#about-impresso)
- [License](#license)

---

## Repository Structure

The repository is organized as follows:

```
├── evaluation_sets
│   └── The evaluation datasets (CLSD - WMT19/21) introduced
├── experimentation_notebooks
│   └── The notebook used to compute all the experiments and analysis from the paper
├── single_token_swaps_annotations
│   └── The annotations created for performing the fine-grained similarity analysis (Section 3.3)
```

## Datasets

This repository introduces the **CLSD–WMT19** and **CLSD–WMT21** adversarial datasets used for evaluation of precise x-lingual semantic search capabilities of models.
All datasets are publicly available within this repository.

Each dataset file contains the following columns:

| Column | Description |
|:--------|:-------------|
| **French** | Original text in French |
| **German** | Original text in German |
| **de_adv1 – de_adv4** | Adversarial distractors in German (used for FR → DE evaluation) |
| **fr_adv1 – fr_adv4** | Adversarial distractors in French (used for DE → FR evaluation) |

Machine-translated versions to English are also provided.  
These files are prefixed with `MT_M2M_` and follow the same structure.

## Citation

If you use these resources, please cite our paper:

```bibtex
@inproceedings{michail-etal-2025-examining,
    title = "Examining Multilingual Embedding Models Cross-Lingually Through {LLM}-Generated Adversarial Examples",
    author = "Michail, Andrianos  and
      Clematide, Simon  and
      Sennrich, Rico",
    editor = "Christodoulopoulos, Christos  and
      Chakraborty, Tanmoy  and
      Rose, Carolyn  and
      Peng, Violet",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2025",
    month = nov,
    year = "2025",
    address = "Suzhou, China",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.findings-emnlp.115/",
    pages = "2161--2170",
    ISBN = "979-8-89176-335-7"
    "
}
```
## About Impresso

### Impresso project

[Impresso - Media Monitoring of the Past](https://impresso-project.ch) is an interdisciplinary research project that aims to develop and consolidate tools for processing and exploring large collections of media archives across modalities, time, languages and national borders. The first project (2017-2021) was funded by the Swiss National Science Foundation under grant No. [CRSII5_173719](http://p3.snf.ch/project-173719) and the second project (2023-2027) by the SNSF under grant No. [CRSII5_213585](https://data.snf.ch/grants/grant/213585) and the Luxembourg National Research Fund under grant No. 17498891.

### Copyright

Copyright (C) 2025 The Impresso team.

### License

This program is provided as open source under the [GNU Affero General Public License](https://github.com/impresso/impresso-pyindexation/blob/master/LICENSE) v3 or later.
