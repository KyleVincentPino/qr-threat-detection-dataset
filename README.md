---

## 📄 **Dataset for “A Machine Learning-based Framework for Detecting Suspicious QR Codes through Combined Image Analysis and URL Threat Assessment”**

This repository contains the dataset used in the research study:

***A Machine Learning-based Framework for Detecting Suspicious QR Codes through Combined Image Analysis and URL Threat Assessment.***

The dataset includes QR code images and their corresponding URL threat labels used to develop and evaluate the machine learning framework consisting of a CNN-based QR image classifier, an XGBoost URL threat assessment model, and an ensemble decision mechanism.

---

## 📁 **Repository Structure**

```
/dataset
   /train
      /benign
      /malicious
      /tampered
   /val
      /benign
      /malicious
      /tampered
   /test
      /benign
      /malicious
      /tampered
   url_data.csv
   image_labels.csv
README.md
```

---

## 📦 **Dataset Contents**

### **1. QR Code Images**

Three classes of QR images are included:

| Class         | Folder       | Description                                                   |
| ------------- | ------------ | ------------------------------------------------------------- |
| **Benign**    | `benign/`    | Standard QR codes linking to safe, verified URLs              |
| **Malicious** | `malicious/` | QR codes containing phishing, deceptive, or harmful URLs      |
| **Tampered**  | `tampered/`  | Visually altered QR images (noise, distortions, obfuscations) |

Images across all splits (`train/`, `val/`, `test/`) follow the naming scheme:

```
qr_<split>_<label>_XXXX.ext
```

Examples:

* `qr_train_benign_0001.png`
* `qr_val_mal_0032.jpg`
* `qr_test_tamp_0148.png`

---

### **2. URL Dataset**

The file **`url_data.csv`** contains URLs extracted from QR codes along with engineered features used for the URL threat assessment model.

Typical columns include:

| Column              | Description                                 |
| ------------------- | ------------------------------------------- |
| `url`               | Raw extracted URL                           |
| `label`             | 0 = benign, 1 = suspicious/malicious        |
| `length`            | Total URL character length                  |
| `num_digits`        | Count of numeric characters                 |
| `num_special_chars` | Symbols such as %, ?, &, /, =, etc.         |
| `entropy`           | Shannon entropy score                       |
| `tld`               | Extracted domain extension                  |
| `is_shortened`      | Whether the URL uses a shortening service   |
| `...`               | Additional extracted or engineered features |

---

### **3. Image Label File**

**`image_labels.csv`** maps each image filename to its corresponding class label:

| image_name               | label |
| ------------------------ | ----- |
| qr_train_benign_0001.png | 0     |
| qr_train_mal_0004.jpg    | 1     |
| qr_val_tamp_0012.png     | 2     |

*(Label mapping may vary depending on your model; update as needed.)*

---

## 🎯 **Dataset Purpose**

This dataset supports research in:

* QR code threat detection
* Image-based malicious pattern recognition
* URL-based phishing and threat analysis
* Ensemble learning for cybersecurity
* Real-world mobile QR-code safety systems

It was specifically used to train and evaluate:

* A **Convolutional Neural Network (CNN)** for QR image classification
* An **XGBoost model** for URL threat assessment
* A **hybrid ensemble model** combining both predictions

---

## 📊 **Dataset Statistics**

Update with your actual counts:

* **Total QR images:** *insert number*
* **Benign:** *insert number*
* **Malicious:** *insert number*
* **Tampered:** *insert number*
* **URL entries:** *insert number*

---

## 🧪 **Methodology Overview**

The dataset enables training of a three-stage detection framework:

1. **QR Image Processing (CNN)**

   * Identifies tampering patterns
   * Detects visually suspicious QR generation behavior

2. **URL Threat Assessment (XGBoost)**

   * Evaluates URL structure and threat indicators
   * Flags phishing or malicious link patterns

3. **Ensemble Decision Layer**

   * Fuses outputs from both models
   * Produces the final threat score
   * Improves precision and robustness

---

## 📌 **Citation**

If you use this dataset, please cite the corresponding paper:

## P.S. Replace later
```
K. V. Pino et al.,
"A Machine Learning-based Framework for Detecting Suspicious QR Codes through Combined Image Analysis and URL Threat Assessment,"
2025.
```

---

## ⚠️ **Disclaimer**

This dataset contains malicious URLs strictly for research purposes.
**Do not click or visit any suspicious URL directly.**
Always use safe, isolated environments when inspecting URL data.

---

## 🤝 **Contributions**

This dataset is intended for research and educational purposes.
Contributions are welcome via pull request or issue submission.

---
