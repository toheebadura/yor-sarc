---
license: cc-by-4.0
language:
- yo
tags:
- sarcasm detection
- sentiment analysis
- figurative language
- low-resource nlp
- african languages
pretty_name: yor-sarc
---

# Dataset Card for Yor-Sarc

Yor-Sarc is a gold-standard dataset for sarcasm detection in Yorùbá, a tonal and morphologically rich low-resource African language spoken by over 50 million people. The dataset was created to address the scarcity of high-quality annotated resources for figurative language understanding in African NLP.

It contains 436 manually annotated Yorùbá text instances labeled for binary sarcasm classification.

---

## Dataset Details

### Dataset Description

Yor-Sarc aims to accelerate research in Yorùbá NLP and broader low-resource African language modeling by providing a carefully curated benchmark dataset for sarcasm detection.

Unlike coarse-grained sentiment datasets, Yor-Sarc focuses on fine-grained figurative language understanding, specifically sarcasm — a pragmatically complex phenomenon that depends on tone, context, and cultural cues.

Each instance:

- Is written in Standardized Yorùbá orthography (with diacritics)
- Is annotated with a binary label such that we could eventually have:
  - `0` = non-sarcastic
  - `1` = sarcastic
- Was independently labeled by three native Yorùbá speakers
- Preserves annotator agreement for uncertainty-aware modelling

The dataset achieves substantial inter-annotator agreement:

- Fleiss’ κ = 0.7660  
- Pairwise Cohen’s κ = 0.6732–0.8743  
- 83.3% unanimous agreement  

Yor-Sarc provides a foundational benchmark for evaluating machine learning, deep learning, and large language model (LLM) approaches for sarcasm detection in low-resource settings.

---

- **Curated by:** Toheeb Aduramomi Jimoh, Tabea De Wille, Nikola S. Nikolov  
- **Language(s):** Yorùbá (yo)  
- **License:** CC-BY-4.0  

---

## Dataset Sources

- **Paper (arXiv):** https://arxiv.org/abs/2602.18964  
- **ePrint:** 2602.18964  

---

## Uses

### Direct Use

Yor-Sarc is intended for research in:

- Sarcasm detection
- Figurative language understanding
- Sentiment and emotion analysis
- Low-resource NLP
- African language modelling
- Cross-lingual transfer learning
- Uncertainty-aware and disagreement-aware modeling

It is suitable for benchmarking:

- Machine learning models
- Deep learning architectures
- Transformer-based models
- Large Language Models (LLMs)

---

### Out-of-Scope Use

This dataset should not be used for:

- Surveillance or profiling
---

## Dataset Structure

Total instances: **436**

Each record contains:

- `text`: Yorùbá sentence (with diacritics)
- `label`: Majority-vote binary sarcasm label
- (Optional) Annotator vote proportions for soft-label modeling

Agreement distribution:

- 83.26% unanimous agreement (3–0)
- 16.74% majority agreement (2–1)

---

## Dataset Creation

### Curation Rationale

Sarcasm detection research is heavily dominated by English and other high-resource languages. Yorùbá lacks publicly available gold-standard sarcasm datasets despite its linguistic richness and widespread usage.

Yor-Sarc was created to:

- Provide a culturally grounded benchmark
- Support African NLP research
- Encourage figurative language modeling in tonal languages
- Enable robust evaluation of sarcasm detection systems in low-resource settings

---

### Source Data

Data were collected from:

- Yorùbá news platforms
- Social media platforms (X, Facebook, Instagram, YouTube captions)
- Crowdsourced contributions

All texts were cleaned and standardized before annotation.

---

#### Data Collection and Processing

- Manual collection and filtering
- Standardized orthographic normalization
- Three independent native-speaker annotations
- Majority voting for final labels
- Agreement metrics computed using Cohen’s κ and Fleiss’ κ

---

### Annotations

#### Annotation Process

- Three native Yorùbá annotators
- Binary sarcasm labeling
- Iteratively refined guidelines
- Independent annotation
- Statistical agreement validation

#### Who are the annotators?

Native Yorùbá speakers with linguistic proficiency and familiarity with dialectal variation. Annotators were independent and compensated fairly.

---

#### Personal and Sensitive Information

The dataset contains publicly available and voluntarily contributed texts. Personally identifiable information has been removed where necessary. No sensitive metadata is included.

---

## Bias, Risks, and Limitations

- Relatively small dataset size (436 instances)
- Non-exhaustive domain coverage
- Cultural understanding influences sarcasm interpretation


## Citation

If you use Yor-Sarc, please cite:

**BibTeX:**

```bibtex
@misc{jimoh2026yorsarcgoldstandarddatasetsarcasm,
      title={Yor-Sarc: A gold-standard dataset for sarcasm detection in a low-resource African language}, 
      author={Toheeb Aduramomi Jimoh and Tabea De Wille and Nikola S. Nikolov},
      year={2026},
      eprint={2602.18964},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2602.18964}
}
