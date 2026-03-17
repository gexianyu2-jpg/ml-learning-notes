# ML Learning Notes

## Learning Goal
- Understand machine learning fundamentals (based on Li Hongyi's course)
- Explore applications in medical imaging

---

## 1. Machine Learning Basics

### What is Machine Learning
Machine learning aims to learn a function that maps input to output.

Core components:
- Model
- Loss function
- Optimization

---

### Tasks
- Classification (e.g., cancer detection)
- Regression

---

## 2. Medical AI Pipeline

From reading the papers, I summarize:

1. Data:
- CT images (3D)
- Imbalanced dataset

2. Task:
- Classification
- Report generation

3. Model:
- CNN / Transformer
- Vision-Language Models (VLM)

4. Evaluation:
- AUC is commonly used

---

## 3. Paper Insights

### AI-based gastric cancer screening (Nat Med 2025)
- Task: classification
- Data: CT images
- Metric: AUC

### LLaVA-Med
- Multimodal model (image + text)
- Used for biomedical tasks

---

## 4. Thoughts

- I find AUC important because medical data is imbalanced
- Medical imaging tasks can be framed as ML problems
- I am interested in combining ML with biology

---

## 5. Next Steps

- Learn PyTorch
- Understand deep learning models
