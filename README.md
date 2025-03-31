
# QR Code Authentication

This project focuses on distinguishing between **first print** and **second print** QR codes using a combination of traditional machine learning, custom CNN models, and transfer learning with MobileNetV2.

---

## Project Structure

```
qr_auth_project/
├── data/                  # Dataset and preprocessed arrays
├── models/                # Saved model files
├── notebooks/             # Jupyter notebook with complete code
├── results/               # Evaluation plots and metrics
├── report/                # Final project report
├── README.md              # Project overview
└── requirements.txt       # Python dependencies
```

---

## Approach

1. **Data Preparation**
   - Extracted QR codes from two folders (`first_print`, `second_print`)
   - Resized and normalized grayscale images to 224x224
   - Computed brightness feature for ML baseline

2. **Modeling Techniques**
   - **Logistic Regression** using brightness as a single feature
   - **CNN from scratch** trained on raw images
   - **CNN with data augmentation** to improve generalization
   - **MobileNetV2 Transfer Learning** for high-accuracy classification

3. **Evaluation**
   - Accuracy, confusion matrix, precision, recall, F1-score
   - Training vs validation loss curves
   - Side-by-side comparison of all models

---

## Requirements

All dependencies are listed in `requirements.txt`. To install:

```bash
pip install -r requirements.txt
```

---

## Usage

1. Clone the repository or download the files
2. Navigate to the project directory
3. Open and run the Jupyter notebook:
   ```
   notebooks/qr_auth_classification.ipynb
   ```

---

## Results Summary

| Model                   | Accuracy | Notes                         |
|------------------------|----------|-------------------------------|
| Logistic Regression     | ~90%     | Brightness-only baseline      |
| CNN                    | ~95%+    | Custom architecture           |
| CNN + Augmentation     | ~98%+    | Improved generalization       |
| MobileNetV2 (Transfer) | ~100%    | Best overall performance      |

---



