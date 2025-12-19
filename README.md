# Semantic Segmentation of Medicinal Flower Images

This repository contains the implementation and experimental results for a **semantic segmentation project on medicinal flower images** under a **limited-label setting**. The goal of this work is to evaluate how **semi-supervised learning (SSL)** methods can improve segmentation performance when only a small portion of the data is labeled.

---

## 🔍 Project Summary

- **Task:** Binary semantic segmentation (flower vs background)
- **Dataset size:** ~7,397 images
- **Label setting:** 20% labeled, 80% unlabeled
- **Annotation:** Automatically generated segmentation masks
- **Backbone models:** U-Net, DeepLabV3+
- **Semi-supervised methods:** Pseudo-Labeling, Mean Teacher, FixMatch

---

## 🚀 Key Contributions

- Implemented supervised and semi-supervised segmentation pipelines
- Compared two supervised baselines with three SSL methods
- Demonstrated the effectiveness of consistency-based SSL
- Built a label-efficient, fully automated segmentation workflow
- Provided both quantitative metrics and qualitative visual results

---

## 📂 Repository Structure

Semantic-Segmentation-of-medicinal-flower/
├── baseline_model_training/

│ ├── unet/

│ └── deeplabv3plus/

├── semi_supervised_models/

│ ├── pseudo_labeling/

│ ├── mean_teacher/

│ └── fixmatch/

├── dataset/

│ ├── images/

│ └── masks/

├── results/

│ ├── metrics/

│ └── plots/

├── appendix_visuals/

│ └── qualitative_results/

├── requirements.txt

└── README.md


---

## 📊 Dataset & Split

- **Total images:** ~7,397
- **Train / Validation / Test:** 80% / 10% / 10%
- **Training split:**
  - 20% labeled
  - 80% unlabeled

This setup simulates a realistic low-annotation scenario.

---

## 🏗️ Models

### Supervised Baselines
- U-Net
- DeepLabV3+

### Semi-Supervised Models
- Pseudo-Labeling
- Mean Teacher
- FixMatch

All SSL methods use **DeepLabV3+** as the backbone for fair comparison.

---

## 🏆 Best Results

- **Best supervised model:**  
  DeepLabV3+  
  - Dice: **0.7656**  
  - IoU: **0.6321**

- **Best semi-supervised performance:**  
  - FixMatch: Highest Dice / F1-score (**0.748**) with high specificity  
  - Mean Teacher: Most stable and robust SSL behavior  
  - Pseudo-Labeling: Modest but consistent improvement  

Consistency-based SSL methods outperform naive self-training.

---

## 📈 Evaluation Metrics

- Dice coefficient (F1-score)
- Intersection over Union (IoU)
- Precision, Recall, Specificity (FixMatch)
- Pixel-level confusion statistics

All results are reported on the **held-out test set**.

---

## ⚙️ Setup & Installation

```bash
pip install -r requirements.txt

Requirements:

Python 3.8+

PyTorch

torchvision

NumPy, Matplotlib

CUDA (optional)

▶️ Running the Code

Train supervised baselines:

python train_unet.py
python train_deeplabv3plus.py

Train semi-supervised models:

python train_pseudo_labeling.py
python train_mean_teacher.py
python train_fixmatch.py

🖼️ Qualitative Results

Visual segmentation outputs for all models are available in the
appendix_visuals/qualitative_results/ directory.
These examples complement quantitative evaluation and illustrate model behavior.

⚠️ Limitations

Performance depends on automatic mask quality

SSL gains are moderate but consistent

Experiments focus on binary segmentation only

🔮 Future Work

Extend to multi-class segmentation

Evaluate on larger and more diverse datasets

Incorporate uncertainty-aware learning

Optimize models for real-time deployment

👤 Author

Mohammad Mehedi Hasan Munna
Department of Computer Science and Engineering
East West University

📄 License

This project is intended for academic and educational use.


---

### ✅ What to Do Next on GitHub
1. Paste the content
2. Click **Preview** (to check formatting)
3. Click **Commit changes**
4. Use commit message:
