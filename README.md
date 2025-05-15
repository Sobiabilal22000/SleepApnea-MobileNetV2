# Sleep Apnea Detection using Easy-MobileNetV2

This project implements a lightweight 1D CNN based on the Easy-MobileNetV2 architecture for detecting sleep apnea from ECG signals. It uses the PhysioNet Apnea-ECG database and follows a simplified replication of the approach discussed in the paper:

📄 Reference: [Easy-MobileNetV2: A Lightweight CNN for Sleep Apnea Detection (arXiv:2412.19967)](https://arxiv.org/abs/2412.19967)

---

## 📊 Dataset

- Source: PhysioNet Apnea-ECG Database
- 35+ records (`a01` to `c10`)
- 60-second ECG windows labeled as apnea or normal

---

## 🧠 Model

- **Architecture**: MobileNetV2-inspired 1D CNN
- **Preprocessing**: Bandpass filtering (0.5–40Hz), z-score normalization
- **Segments**: 60-second ECG windows

---

## 📈 Results

| Metric      | Paper Result | Our Model |
|-------------|--------------|-----------|
| Accuracy    | 97.0%        | 91.4%     |
| Precision   | 97.8%        | 90.3%     |
| Recall      | 97.8%        | 91.2%     |
| F1 Score    | 97.8%        | 90.7%     |
| ROC-AUC     | 0.98         | 0.93      |

---

## 🧪 Tools

- TensorFlow / Keras
- WFDB for ECG reading
- MLflow for experiment logging
- Matplotlib & scikit-learn for evaluation

---

## 💾 Files

- `SleepApnea.ipynb` – Main notebook
- `mobilenetv2_apnea_final.h5` – Final trained model
- `mlflow_screenshot.png` – Experiment logs
- `Assignment_2.pdf` – Assignment description
- `2412.19967v2.pdf` – Reference paper

---

## 📎 How to Run

```bash
pip install wfdb mlflow tensorflow scikit-learn matplotlib
python SleepApnea.ipynb
# SleepApnea-MobileNetV2
