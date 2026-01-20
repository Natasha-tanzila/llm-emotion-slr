<p align="center">
  <img src="LLM_EMOTION_SLR.png" width="800">
</p>


# Emotion Detection with Large Language Models: Systematic Review

This repository accompanies the paper:

> **Emotion Detection with Large Language Models: A Systematic Literature Review**  
> Natasha Tanzila Monalisa, Ranesh Naha, Alistair Barros  
> (Under review / Published in [Journal Name], Year)

The repository provides **all non-proprietary materials** required to reproduce,
inspect, and extend the dataset-level and taxonomy-grounded analyses presented in
the paper.

---

## 📌 Scope of the Repository

This repository supports a **systematic literature review (SLR)** of LLM-based
emotion detection methods published between **2015–2025**, focusing on:

- Emotion taxonomy coverage (Basic, Composite, Complex)
- Dataset-centric analysis across **55 benchmark datasets**
- Length-wise performance behaviour of LLMs
- Delta-based normalization against BERT-family baselines
- Explicit extraction of technical and conceptual limitations

---

## 📂 Repository Contents

### `data/`
- **raw/**  
  Original extracted tables from reviewed studies  
  (paper metadata, datasets, emotion labels, quality appraisal)

- **processed/**  
  Cleaned and derived tables used in figures and analysis  
  (taxonomy mappings, length grouping, Δ-score computation)

### `results/`
-raw table for result section-2 (Δ normalization)
-raw table for result section-3 (challenges study-wise)

### `appendix/`
All appendix materials referenced in the paper, including:
- search strategy
- Quality Appraisal

### `figures/`
High-resolution versions of all figures used in the paper.

### `scripts/`
Python scripts used for:
- Average text-length computation

### `docs/`
Supplementary documentation (data dictionaries, variable descriptions).

---

## 🔁 Reproducibility Notes

- No proprietary datasets are redistributed.
- Dataset links and original citations are provided where applicable.
- All derived statistics are computed from publicly available sources.
- Performance values are reported exactly as stated in the original papers.

---

## 📖 Citation

If you use this repository, **please cite the paper**:

```bibtex
@article{Monalisa2025EmotionLLMSLR,
  title   = {Emotion Detection with Large Language Models: A Systematic Review},
  author  = {Monalisa, Natasha Tanzila and Naha, Ranesh and Barros, Alistair},
  journal = {TBD},
  year    = {2025}
}
