<div align="center">

# ⚖️ Fairness Auditing Tool for Income Prediction
### Detecting and Mitigating Bias in ML Models using the Adult Census Dataset

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

<p align="center">
  <img src="https://img.shields.io/badge/Models-8%20Classifiers-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Dataset-Adult%20Census-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Sensitive%20Attributes-Race%2C%20Sex%2C%20Education-orange?style=flat-square"/>
</p>

*A fairness auditing framework that trains, evaluates, and compares ML classifiers for income prediction through the lens of algorithmic fairness and demographic parity.*

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Models](#-models)
- [Fairness Metrics](#-fairness-metrics)
- [Results](#-results)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Future Work](#-future-work)
- [References](#-references)
- [Author](#-author)

---

## 🔬 Overview

This project builds a **fairness auditing tool** to systematically detect and mitigate biases in machine learning models trained to predict whether an individual earns more or less than $50K/year.

Using the **UCI Adult Census Income dataset**, eight classifiers are trained and evaluated not only for predictive accuracy but for **fairness across protected attributes**: race, sex, and education level.

Key questions addressed:
- Which models introduce the most demographic bias?
- Where does bias originate — in the data or the algorithm?
- Can mitigation strategies (reweighting, adversarial debiasing) reduce bias without sacrificing accuracy?

---

## 📦 Dataset

**UCI Adult Census Income Dataset** (also known as the "Adult" dataset)

🔗 [archive.ics.uci.edu/ml/datasets/adult](https://archive.ics.uci.edu/ml/datasets/adult)

| Property           | Value                              |
|--------------------|------------------------------------|
| Instances          | 48,842                             |
| Features           | 14 (age, education, occupation…)   |
| Target             | Income ≤$50K / >$50K (binary)      |
| Sensitive attributes | Race, Sex, Education             |
| Source             | 1994 US Census Bureau              |

> ⚠️ The dataset is available via `sklearn.datasets.fetch_openml('adult')` — no manual download needed.

---

## 🤖 Models

Eight classifiers are trained and compared:

| Model                  | Type                     |
|------------------------|--------------------------|
| Logistic Regression    | Linear                   |
| Decision Tree          | Tree-based               |
| Random Forest          | Ensemble (bagging)       |
| SVM                    | Kernel-based             |
| KNN                    | Instance-based           |
| AdaBoost               | Ensemble (boosting)      |
| Gradient Boosting      | Ensemble (boosting)      |
| Neural Network (MLP)   | Deep learning            |

---

## 📐 Fairness Metrics

| Metric                    | Description                                                   |
|---------------------------|---------------------------------------------------------------|
| **Demographic Parity**    | Equal positive prediction rates across demographic groups     |
| **Disparate Impact Ratio**| Ratio of positive prediction rates between groups (≥0.8 fair) |
| **Accuracy by group**     | Per-group breakdown of model accuracy                         |

Sensitive attributes evaluated: **Race**, **Sex**, **Education level**

---

## 📊 Results

Full results, confusion matrices, fairness plots, and model comparisons are in the notebook and the project report.

Key findings:
- Tree-based models (Random Forest, Gradient Boosting) achieve highest accuracy but show notable demographic parity gaps
- Logistic Regression offers a better accuracy-fairness trade-off
- Reweighting as a pre-processing mitigation step reduces disparity without large accuracy loss

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install -r requirements.txt
```

### Run

```bash
# 1. Clone the repository
git clone https://github.com/FarhadBayrami/Fairness-Auditing-Tool-for-Income-Prediction_.git
cd Fairness-Auditing-Tool-for-Income-Prediction_

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook Fairness_Auditing_Income_Prediction.ipynb
```

> 💡 The Adult dataset loads automatically via `sklearn`. No manual download needed.

---

## 📁 Project Structure
📦 Fairness-Auditing-Tool-for-Income-Prediction_
┣ 📓 Fairness_Auditing_Income_Prediction.ipynb        ← Full pipeline: data, models, fairness evaluation
┣ 📄 Fairness and Bias Detection in ML Models.docx    ← Full project report
┣ 📄 Fairness and Bias Detection Proposal.pdf         ← Project proposal
┣ 📄 requirements.txt                                 ← Python dependencies
┣ 📄 LICENSE                                          ← MIT License
┣ 📄 CITATION.cff                                     ← How to cite this work
┗ 📝 README.md
---

## 🔮 Future Work

- [ ] Implement adversarial debiasing (in-processing mitigation)
- [ ] Add equalised odds and equal opportunity metrics
- [ ] Extend to intersectional fairness (e.g. race × sex)
- [ ] Build an interactive Gradio/Streamlit fairness dashboard
- [ ] Test on additional datasets (COMPAS, German Credit)

---

## 📚 References

1. Dua, D. & Graff, C. — *UCI Machine Learning Repository*, 2019.
2. Barocas, S. & Hardt, M. — *Fairness and Machine Learning*, fairmlbook.org, 2023.
3. Bellamy, R. et al. — *AI Fairness 360: An Extensible Toolkit for Detecting and Mitigating Algorithmic Bias*, IBM Journal of R&D, 2019.
4. Mehrabi, N. et al. — *A Survey on Bias and Fairness in Machine Learning*, ACM CSUR, 2021.

---

## 👤 Author

**Farhad Bayrami**
MSc Student — University of Bologna
📧 [farhad.bayrami@studio.unibo.it](mailto:farhad.bayrami@studio.unibo.it)
🔗 [GitHub](https://github.com/FarhadBayrami)

---

<div align="center">
  <sub>Built with ❤️ as part of an Ethics in AI course project at the University of Bologna</sub>
</div>
