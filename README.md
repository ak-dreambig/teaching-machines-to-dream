# Teaching Machines to Dream

### A Practical Engineer's Handbook on Synthetic Data

**Authors:** Aimal Khan · Hamza Raziq Khan  
**Peshawar, Pakistan · 2026**

---

> *"Build what you need. Simulate what you don't have. Measure everything."*

---

## About This Repository

This is the official companion repository for the handbook **Teaching Machines to Dream: A Practical Engineer's Handbook on Synthetic Data**.

The handbook covers synthetic data generation across four domains: tabular data, text, images, and document workflows. This repository contains all runnable notebooks, pipeline configs, and utility references so you can experiment with every concept from the book immediately.

---

## The Handbook

The book is available as a PDF on the releases page of this repository.

**Topics covered:**

- Synthetic tabular data generation (SDV, CTGAN, GaussianCopula)
- Synthetic text generation (LLMs, templates, back-translation)
- Synthetic image and video data (Stable Diffusion, ControlNet, Albumentations)
- Building production synthetic data pipelines with quality gates
- Training ML models on synthetic data (curriculum learning, domain adaptation)
- Complete evaluation suite (KS test, TSTR, TRTS, UMAP, FID, privacy audit)

---

## Notebook Series: TMD

All notebooks are available here and on Kaggle. Each one is self-contained and runnable without any local setup.

| Notebook | Topic | GPU | Dataset |
|----------|-------|-----|---------|
| [TMD-01](notebooks/TMD-01-Tabular-Quickstart.ipynb) | Tabular Data Quickstart | No | adult-census-income |
| [TMD-02](notebooks/TMD-02-CTGAN-Fraud-Detection.ipynb) | CTGAN for Fraud Detection | Yes T4 | creditcardfraud |
| [TMD-03](notebooks/TMD-03-Synthetic-Text-LLM.ipynb) | Synthetic Text with LLMs | Yes T4 | None |
| [TMD-04](notebooks/TMD-04-Image-Augmentation.ipynb) | Image Augmentation Pipeline | No | intel-image-classification |
| [TMD-05](notebooks/TMD-05-Diffusion-Generation.ipynb) | Diffusion Model Generation | Yes T4 | None |
| [TMD-06](notebooks/TMD-06-Pipeline-Quality-Gates.ipynb) | Pipeline Quality Gates | No | adult-census-income |
| [TMD-07](notebooks/TMD-07-Evaluation-Suite.ipynb) | Complete Evaluation Suite | No | adult-census-income |

**Run on Kaggle (free GPU included):**  
[kaggle.com/work/collections/18158089](https://www.kaggle.com/work/collections/18158089)

---

## Quick Start

### Option 1: Run on Kaggle (recommended)

1. Go to the Kaggle collection link above
2. Open any notebook
3. Click Copy and Edit
4. Add the required dataset from the Add Data panel
5. Click Run All

No local setup needed. Kaggle provides free GPU for T4 notebooks.

### Option 2: Run locally

```bash
git clone https://github.com/ak-dreambig/teaching-machines-to-dream.git
cd teaching-machines-to-dream

# CPU notebooks
pip install -r requirements.txt

# GPU notebooks
pip install -r requirements-gpu.txt

jupyter notebook
```

---

## Requirements

**CPU (`requirements.txt`):**

```
sdv>=1.9.0
faker>=25.0.0
pandas>=2.0.0
numpy>=1.24.0
scikit-learn>=1.3.0
scipy>=1.11.0
umap-learn>=0.5.3
imbalanced-learn>=0.11.0
matplotlib>=3.7.0
seaborn>=0.13.0
albumentations>=1.3.1
opencv-python>=4.8.0
Pillow>=10.0.0
pyyaml>=6.0
tqdm>=4.65.0
jupyter>=1.0.0
```

**GPU (`requirements-gpu.txt`):**

```
torch>=2.1.0
torchvision>=0.16.0
diffusers>=0.24.0
transformers>=4.36.0
accelerate>=0.25.0
bitsandbytes>=0.41.0
torch-fidelity>=0.3.0
```

---

## Datasets Used

All datasets are publicly available on Kaggle.

| Dataset | Used In | Kaggle Link |
|---------|---------|-------------|
| Adult Census Income | TMD-01, TMD-06, TMD-07 | [uciml/adult-census-income](https://www.kaggle.com/datasets/uciml/adult-census-income) |
| Credit Card Fraud | TMD-02 | [mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) |
| Intel Image Classification | TMD-04 | [puneet6060/intel-image-classification](https://www.kaggle.com/datasets/puneet6060/intel-image-classification) |

---

## Repository Structure

```
teaching-machines-to-dream/
├── notebooks/
│   ├── TMD-01-Tabular-Quickstart.ipynb
│   ├── TMD-02-CTGAN-Fraud-Detection.ipynb
│   ├── TMD-03-Synthetic-Text-LLM.ipynb
│   ├── TMD-04-Image-Augmentation.ipynb
│   ├── TMD-05-Diffusion-Generation.ipynb
│   ├── TMD-06-Pipeline-Quality-Gates.ipynb
│   └── TMD-07-Evaluation-Suite.ipynb
├── configs/
│   └── pipeline_config.yaml
├── data/
│   └── README.md
├── README.md
├── requirements.txt
├── requirements-gpu.txt
├── LICENSE
└── .gitignore
```

---

## Key Concepts

**What is synthetic data?**  
Data that is artificially generated rather than collected from real-world events. It can mimic the statistical properties of real data, represent rare scenarios, or encode domain knowledge in a structured form.

**Why does it matter?**  
Real data is expensive, slow to collect, privacy-sensitive, and uneven in its coverage of edge cases. Synthetic data solves all of these problems when used correctly.

**What is TSTR?**  
Train on Synthetic, Test on Real. The most important metric for synthetic data quality. A TSTR ratio above 0.95 means your synthetic data is genuinely useful for ML training.

---

## Citation

If you use this handbook or notebooks in your work please cite:

```
@book{khan2026tmd,
  title     = {Teaching Machines to Dream: A Practical Engineer's Handbook on Synthetic Data},
  author    = {Khan, Aimal and Khan, Hamza Raziq},
  year      = {2026},
  publisher = {Self-published},
  url       = {https://github.com/ak-dreambig/teaching-machines-to-dream}
}
```

---

## License

MIT License. See [LICENSE](LICENSE) for details.

Code is provided as-is for educational purposes. Adapt everything to your own environment before production use.

---

## Connect

**GitHub:** [github.com/ak-dreambig](https://github.com/ak-dreambig)  
**Kaggle Collection:** [kaggle.com/work/collections/18158089](https://www.kaggle.com/work/collections/18158089)

---

*Teaching Machines to Dream · Aimal Khan · Hamza Raziq Khan · Peshawar, 2026*
