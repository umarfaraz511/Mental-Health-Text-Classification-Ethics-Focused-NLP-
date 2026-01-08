# Mental Health Text Classification (Ethics-Focused NLP)

This project fine-tunes a pretrained NLP model to classify mental-health-related signals from text (e.g., stress, anxiety, depression categories) using an ethics-first approach. It includes dataset evaluation (EDA), preprocessing, stratified splitting, 10-epoch training, and full metric reporting.

> Important: This project is for **research and educational purposes**. It is **not** a medical diagnostic system.

---

## Project Objectives

- Perform **EDA** to understand label distribution and text length patterns.
- Build a reproducible pipeline for:
  - text cleaning
  - stratified train/validation/test split
  - pretrained model fine-tuning (5 epochs)
- Evaluate using:
  - **Accuracy**
  - **Precision (weighted)**
  - **Recall (weighted)**
  - **F1-score (weighted)**
  - **Loss**
- Emphasize ethical considerations: privacy, misuse prevention, and careful interpretation.

---

## Dataset

- Source: Kaggle  
- Path used in Colab:






Running the Project (Colab)
1) Install dependencies
pip install -U transformers datasets accelerate evaluate scikit-learn pandas matplotlib

2) Train (10 epochs)
Use eval_strategy="epoch" and save_strategy="epoch"


Enable GPU in Colab for practical training times:
 Runtime → Change runtime type → GPU


3) Evaluate
Outputs:
Validation metrics per epoch


Final test metrics dictionary


Optional detailed report and confusion matrix



Recommended Training Settings
If running on CPU:


use a subset for quick experiments


reduce max_length to 128


If using BART:


start with smaller batch sizes (e.g., 4–8)


reduce max_length if you hit CUDA OOM



Ethics & Responsible Use
This classifier:
Detects linguistic patterns, not diagnoses.


Must not be used to label individuals clinically.


Should be deployed only with:


privacy protection (PII handling, anonymization)


clear disclaimers


safe user messaging (support resources, escalation guidance)




License
Choose an appropriate license (e.g., MIT) based on your intended use and dataset constraints.



