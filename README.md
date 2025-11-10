# AiR Project Template (Tutor Guidance)
This is the repo. for the projects offered at our special edition of the AI in Radiology Seminar with the German University in Cairo 

## 1. Project Overview
This exercise introduces students to **medical image classification** using **deep learning** on **Chest X-ray datasets**.  
Students will explore model performance, generalization, and robustness by training models on a subset of X-rays and evaluating them under controlled challenges such as **class imbalance** and **out-of-distribution (OOD)** testing.

**Learning goals:**
- Understand the deep learning workflow for medical image classification.  
- Use pre-trained **foundation models** (e.g., ResNet, DenseNet, or ViT from `torchvision` or `timm`) for **feature extraction**.  
- Handle **imbalanced data** and evaluate **OOD performance**.  
- Develop critical insight into model reliability in medical contexts.

---

## 2. Dataset
- Use the following **publicly available Chest X-ray dataset** (e.g., NIH ChestX-ray14, CheXpert, or COVIDx). *Provide the link and source of the dataset*.   
- Tutors should prepare or provide a **small, balanced subset** suitable for Google Colab (≈1–2 GB).  
- Optionally, create an **OOD dataset** by introducing images from a different source (e.g., COVIDx for pneumonia detection trained on CheXpert).  
- Optionally, **undersample or perturb** one class manually to simulate **data shift** or **class imbalance**.

**Tutor tip:** Provide pre-organized folders (`train/`, `test/`) with labels, or a CSV with file paths and diagnosis labels to ensure fair evaluation among the groups. 

---

## 3. Task Outline
1. **Problem Definition:** Predict a medical condition (e.g., pneumonia vs. normal).  
2. **Data Preparation:**  
   - Load the dataset subset.  
   - Visualize and summarize class balance.  
3. **Feature Extraction:**  
   - Use a pre-trained CNN or ViT as a frozen feature extractor.  
   - Optionally fine-tune the final layers.  
4. **Model Training:**  
   - Train a simple classifier (e.g., Linear, MLP) on extracted embeddings.
   - Fine-tune a CNN or ViT as well   
5. **Evaluation:**  
   - Compute the clinically relevant performance metrics: accuracy, sensitivity, specificity, and AUC, among others.   
   - Compare performance on the **main** and **OOD** datasets or different sub-groups; male vs. female, adults vs. children.  
   - Analyze the effect of **class imbalance** and discuss mitigation strategies (reweighting, augmentation, oversampling).  
6. **Reflection:**  
   - Encourage discussion on fairness, uncertainty, and ethical implications of AI in healthcare.

---

## 4. Deliverables
- Jupyter notebook (Colab-compatible) with:  
  - Code and clear commentary  
  - Model training and evaluation steps  
  - Plots (ROC curves, confusion matrix, feature embeddings if possible)  
- Short written summary (max 1 page) on findings and OOD analysis.
- Oral Presentation
  
---

## 5. Assessment Criteria
| Criteria | Description |
|-----------|-------------|
| Reproducibility | Runs cleanly on Colab using small data subset |
| Methodology | Correct use of pre-trained models and evaluation methods |
| Analysis | Insightful handling of OOD and class imbalance |
| Communication | Clear explanations, medical AI awareness |

---

## 6. Extensions (Optional)
- Add noise or domain shifts to simulate hospital-to-hospital variation.  
- Experiment with different foundation models or fine-tuning depths.  
- Visualize attention maps (e.g., Grad-CAM) to interpret predictions.  
- Compare model calibration between in-distribution and OOD data.

---

**Note for Tutors:**  
Keep datasets lightweight and publicly accessible (≤2 GB).  
Encourage reproducibility and conceptual understanding over high accuracy.  
The goal is to **teach responsible and practical use of deep learning in medical imaging**, not to build a production-ready diagnostic model.

---


