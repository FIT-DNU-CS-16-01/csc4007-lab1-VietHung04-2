# 📊 Data Card – IMDB Movie Review Dataset

---

## 🎯 **Key Questions**

### 1️⃣ **Who are the intended readers?**

* 👨‍🎓 **NLP Students**: Understand data quality for fair model evaluation
* 🔬 **Researchers**: Assess dataset suitability for sentiment analysis tasks
* ⚙️ **ML Engineers**: Review preprocessing steps and data quality before pipeline integration
* 🕵️ **Data Auditors**: Identify risks such as data leakage, duplicates, and bias
* 🔁 **Future Lab Students**: Reuse and improve the dataset in future experiments

---

### 2️⃣ **What decisions need to be made?**

* ✅ Can this dataset be reliably used for sentiment classification?
* ✅ Are evaluation results on the test set trustworthy (e.g., no leakage)?
* ✅ What preprocessing steps are required before training?
* ✅ Are there label errors, and how significant are they?
* ✅ What potential blind spots might models trained on this dataset have?

---

### 3️⃣ **What should users be cautious about?**

* 🔴 **Label Quality**: Cleanlab detected approximately **X** potentially mislabeled samples
* 🔴 **Duplicates**: Presence of duplicate/near-duplicate samples → risk of overfitting
* 🔴 **Validation Issues**: Some records may fail validation checks (e.g., abnormal length, missing values)
* 🟡 **HTML Artifacts**: Residual HTML entities still exist in the dataset
* 🟡 **Data Distribution**: Although balanced, labels are derived from thresholds and may not reflect real-world distribution

---

## 📦 **1. Overview**

* 📚 **Dataset:** IMDB Movie Reviews
* 🎯 **Task:** Sentiment Classification
* 🏷️ **Labels:** Positive (1), Negative (0)

---

## 📊 **2. Dataset Snapshot**

* 📈 **Total Samples:** *(from `datacard_stats.json`)*
* 🔀 **Split:**

  * Train: *(from outputs/splits)*
  * Validation: *(from outputs/splits)*
  * Test: *(from outputs/splits)*

---

## 🎯 **3. Intended Use**

This dataset is intended for training and evaluating NLP models for sentiment classification.
It is particularly suitable for educational purposes and baseline model development.

---

## ⚠️ **4. Data Quality**

* 🔴 **HTML Artifacts** → Require text cleaning
* 🔴 **Duplicate Samples** → Risk of overfitting
* 🔴 **Label Noise** → Detected using Cleanlab

---

## 🧪 **5. Validation**

* 🛠️ **Tool:** Great Expectations

* 📌 **Result:** PASS / FAIL

* 📉 **Observed Issues (if any):**

  * *(e.g., missing values, invalid labels, abnormal text length)*

---

## 🏷️ **6. Labeling & Annotation**

* ✍️ Dataset is manually labeled for sentiment classification
* 🤖 Cleanlab identified several suspicious samples

**Manual Review Findings:**

* Some labels were incorrect and required correction
* Some samples were ambiguous and need further review

---

## 🔄 **7. Data Transformations**

* 🔴 **Before:**
  Raw data contained HTML artifacts, duplicate entries, and noisy labels

* 🟢 **After:**
  Data was cleaned by removing HTML tags, eliminating duplicates, and reviewing mislabeled samples

---

## ⚠️ **8. Limitations**

* Residual label noise may still exist
* Possible class imbalance in real-world scenarios
* Dataset is in English → limited applicability to other languages (e.g., Vietnamese)

---

## ⚖️ **9. Ethical Considerations**

* Potential bias due to subjective human annotations
* Caution required when deploying models trained on this dataset in real-world applications

---

## 🏷️ **10. Versioning**

* 📌 **Version:** v1.0
* 📅 **Last Updated:** 23/04/2026

---
