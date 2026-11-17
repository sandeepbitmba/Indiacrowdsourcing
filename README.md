# Indiacrowdsourcing-
Indiacrowdsourcing dataset
# India-Focused Crowdsourcing Research: LDA-Based Thematic Analysis

## Overview

This repository contains the research materials and computational workflow for an India-focused study examining crowdsourcing applications, with particular attention to business innovation and Micro, Small and Medium Enterprises (MSMEs).

The study uses text-based analysis and Latent Dirichlet Allocation (LDA) topic modelling to identify broad research themes in the selected India-related literature. It also examines the extent to which the identified literature directly addresses business innovation and MSME-related applications.

## Research Objectives

The study addresses three objectives:

1. Identify the major thematic areas in India-related crowdsourcing research.
2. Examine the representation of business innovation and direct SME/MSME studies in the selected literature.
3. Identify research opportunities arising from the limited direct evidence on crowdsourcing and MSME applications in India.

## Dataset and Corpus

The final analytical corpus contains **34 documents** selected from an India-related working set of 78 records.

The screening summary is:

| Screening status | Records |
|---|---:|
| Retained | 34 |
| Excluded | 25 |
| Pending verification | 19 |
| Total | 78 |

The final corpus comprises four relevance categories:

| Category | Documents |
|---|---:|
| Domain-adjacent crowdsourcing | 27 |
| Business innovation | 3 |
| Direct SME/MSME | 2 |
| Agriculture-related | 2 |
| **Total** | **34** |

The five business-focused records comprise three business innovation studies and two direct SME/MSME studies. These categories should not be interpreted as five direct MSME studies.

## Methodology

The research workflow consists of the following stages:

1. Identification and retrieval of India-related crowdsourcing records.
2. Screening and relevance classification of the retrieved records.
3. Preparation of the final 34-document corpus.
4. Text preprocessing using lowercase conversion, URL removal, tokenisation and stopword removal.
5. Construction of the document-term dictionary.
6. Estimation of candidate LDA models.
7. Comparison of topic coherence scores.
8. Interpretation of the selected topics and examination of business-focused records.

## LDA Configuration

The final LDA experiment used the following configuration:

| Parameter | Setting |
|---|---|
| Final documents | 34 |
| Vocabulary size | 729 |
| Algorithm | Latent Dirichlet Allocation |
| Implementation | Gensim 4.4.0 |
| Python | 3.13.18 |
| NumPy | 2.4.6 |
| Random seed | 42 |
| Candidate topics | 2, 3 and 4 |
| Selected topics | 4 |
| Passes | 30 |
| Iterations | 400 |
| Chunk size | 50 |
| Alpha | Symmetric |
| Eta | Auto |
| Coherence measure | C_v |

## Principal Results

The four-topic model achieved the highest coherence score among the candidate models.

| Number of topics (K) | C_v coherence |
|---:|---:|
| 2 | 0.320669 |
| 3 | 0.352714 |
| 4 | **0.382169** |

The final topic prevalence was:

| Topic | Documents | Percentage |
|---|---:|---:|
| Topic 1 | 10 | 29.41% |
| Topic 2 | 10 | 29.41% |
| Topic 3 | 6 | 17.65% |
| Topic 4 | 8 | 23.53% |
| **Total** | **34** | **100%** |

The topics broadly represent digital platforms and crowdwork, public participation and digital accountability, open innovation and collaborative development, and applied crowdsourcing in business, agriculture and technical problem-solving.

## Repository Contents

The repository is intended to contain:

- `Crowd_LDA_new_revised.ipynb` — executed notebook containing the final LDA workflow.
- `Crowdsourcing_Reports_India.txt` — India-related report and literature collection.
- `data/` — final corpus and supporting data files, where included.
- `results/` — topic modelling outputs, tables and document-level assignments.
- `figures/` — generated visualisations used in the research.
- `requirements.txt` — software dependencies and versions.

Only files actually included in the repository should be treated as available research outputs.

## Reproducibility

The notebook documents the preprocessing procedure, dictionary construction, LDA configuration, topic selection and topic interpretation. The reported final experiment uses a fixed random seed of 42.

For reproduction, use the stated Python and package versions where possible. Install the required packages using:

```bash
pip install -r requirements.txt
```

Open and execute `Crowd_LDA_new_revised.ipynb` in Jupyter Notebook or Google Colab after placing the input files in the paths specified in the notebook.

## Limitations

The corpus is a screened collection of India-related records rather than an exhaustive representation of all crowdsourcing research in India. Most retained documents are domain-adjacent, while only two are directly classified as SME/MSME studies. The LDA topics represent patterns in this selected corpus and should not be interpreted as definitive categories for the entire Indian crowdsourcing research landscape. Topic interpretations also involve qualitative judgement.

## Citation

Please cite the associated research paper when using or referring to the findings from this repository.

**Author:** Sandeep Bhattacharjee  
Assistant Professor, Amity University, Kolkata, India

**ORCID:** https://orcid.org/0000-0002-6686-3947

## Data and Code Availability

The notebook and supporting research materials are provided in this repository to support transparency and reproducibility. Please acknowledge the original authors and data sources when reusing bibliographic records or other third-party materials, and observe their applicable access and reuse conditions.
