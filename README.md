# IoT ARP Spoofing Detection using Deep Learning

A lightweight Deep Learning-based Intrusion Detection System (IDS) for detecting **ARP Spoofing attacks** in IoT networks using packet-level traffic analysis and SHAP explainability.

## Features

- Detects ARP Spoofing / MITM attacks
- Deep Neural Network (DNN) classifier
- SHAP Explainable AI visualization
- Packet-level traffic analysis
- High accuracy with low false positive rate

---

## Model

- Input: 21 network traffic features
- Architecture: `24 → 16 → 16 → 8 → 1`
- Activation: ReLU + Sigmoid
- Optimizer: Nadam

Important features:

- `tcp.dstport`
- `tcp.srcport`
- `frame.len`
- `tcp.len`
- `tcp.flags.syn`

---

## Results

| Metric | Score |
|---|---|
| Accuracy | 96.79% |
| Precision | 93.52% |
| Recall | 99.34% |
| F1-Score | 0.96.34% |

---

## Visualizations
- Confusion Matrix
![Confusion Matrix](plots/confmatrix.jpg)
- Training Loss Curve
![Loss](plots/loss.jpg)
- SHAP Summary Plot
![Shap](plots/shap.jpg)


---

## Installation

```bash
git clone https://github.com/MINHDANGab/iot-arp-spoofing-detection.git
cd iot-arp-spoofing-detection
pip install -r requirements.txt
```

---

## Usage

Train model:

```bash
python train.py
```

Evaluate model:

```bash
python evaluate.py
```

---

## Technologies

- Python
- Pytorch
- Scikit-learn
- SHAP
- Pandas
- NumPy

---

## Author

**Minh Dang**

GitHub: https://github.com/MINHDANGab