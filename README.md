Calibration Collapse: On the Disconnect Between Predictive Probability and Ground Truth in Deep Neural Networks
https://img.shields.io/badge/License-MIT-yellow.svg
https://img.shields.io/badge/python-3.8+-blue.svg
https://img.shields.io/badge/PyTorch-2.0+-red.svg
https://img.shields.io/badge/Colab-F9AB00?logo=googlecolab&logoColor=white

Calibration Collapse is a technical paper and a experimental project investigating miscalibration and overconfidence in deep neural networks. This repository contains the full code, experimental results, and the accompanying research paper.

## 📄 Paper

Read the complete paper here:

[Calibration_Collapse.pdf](paper/Calibration_Collapse.pdf)

📌 Overview
Modern deep neural networks often produce high‑confidence predictions that are incorrect — a phenomenon known as miscalibration or overconfidence. This project explores the causes of calibration collapse, demonstrates the confidence‑accuracy gap empirically on MNIST, and discusses implications for AI safety.

Key contributions:

✅ Conceptual framework for understanding calibration in deep learning

✅ Empirical demonstration on MNIST using a simple feedforward network

✅ Reliability diagrams and Expected Calibration Error (ECE) reporting

✅ AI safety analysis linking overconfidence to real‑world risks

✅ Survey of mitigation strategies (temperature scaling, ensembles, Bayesian methods)

📁 Repository Structure
text
calibration-collapse-mnist/
│
├── paper/                        # Research paper (PDF)
│   └── Calibration_Collapse.pdf
│
├── notebook/                     # Jupyter notebook (Google Colab ready)
│   └── MNIST.ipynb
│
├── src/                          # Python source code
│   └── mnist.py                  # Full experiment script
│
├── figures/                      # All generated figures
│   ├── figure1_confidence_distribution.png
│   ├── figure2_reliability_diagram.png
│   └── figure3_confidently_wrong.png
│
├── models/                       # Trained model weights
│   └── mnist_model.pth
│
├── results/                      # Experimental results
│   └── table1_summary.csv
│
├── README.md                     # This file
├── requirements.txt              # Python dependencies
└── LICENSE                       # MIT License

🚀 Getting Started
Option 1: Run in Google Colab (Recommended)
https://colab.research.google.com/assets/colab-badge.svg

Click the badge above to open the notebook in Colab.

Run all cells to train the model and generate figures.

Download the figures from the Colab file browser.

Option 2: Run Locally
Clone the repository:

bash
git clone https://github.com/Priyanshu-Technologies/calibration-collapse-mnist.git
cd calibration-collapse-mnist
Create a virtual environment (optional but recommended):

bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:

bash
pip install -r requirements.txt
Run the experiment:

bash
python src/mnist.py
All figures will be saved in the figures/ directory.

📊 Results
1. Confidence Distribution
Figure 1: Distribution of confidence scores on the MNIST test set.
Most predictions fall in the high‑confidence regime (>90%), typical of modern neural networks.

2. Reliability Diagram
Figure 2: Accuracy vs. confidence.
The model exhibits significant overconfidence — accuracy falls below confidence across all bins.

3. Confidently Wrong Examples
Figure 3: Examples of predictions with >90% confidence that are incorrect.
The model is wrong with complete certainty — a safety‑critical failure mode.

4. Calibration Metrics
Metric	Value
Test Accuracy	97.8%
Expected Calibration Error (ECE)	4.2%
Maximum Calibration Error (MCE)	6.1%
Confidently Wrong (>90%)	64 examples
% of Wrong Predictions >90%	30.5%

🔬 Why This Matters
Calibration is a safety requirement, not a nice‑to‑have.

In high‑stakes domains — healthcare, autonomous vehicles, criminal justice — AI systems that are overconfident can cause catastrophic harm. This project demonstrates that even simple models exhibit calibration collapse, highlighting the urgency of developing better uncertainty estimation techniques.

"The ability to say 'I don't know' is as important as the ability to be correct."

📚 Citation
If you use this work, please cite:

bibtex
@techreport{sharma2026calibration,
  title     = {Calibration Collapse: On the Disconnect Between Predictive Probability and Ground Truth in Deep Neural Networks},
  author    = {Priyanshu Sharma},
  year      = {2026},
  note      = {The Approach Papers — Volume 2},
  url       = {https://github.com/Priyanshu-Technologies/calibration-collapse-mnist}
}
📝 References
Guo, C., Pleiss, G., Sun, Y., & Weinberger, K. Q. (2017). On Calibration of Modern Neural Networks. ICML.

Hendrycks, D., & Gimpel, K. (2016). A Baseline for Detecting Misclassified and Out-of-Distribution Examples in Neural Networks. arXiv.

Ovadia, Y., et al. (2019). Can You Trust Your Model's Uncertainty? Evaluating Predictive Uncertainty Under Dataset Shift. NeurIPS.

Lakshminarayanan, B., Pritzel, A., & Blundell, C. (2017). Simple and Scalable Predictive Uncertainty Estimation using Deep Ensembles. NeurIPS.

Gal, Y., & Ghahramani, Z. (2016). Dropout as a Bayesian Approximation: Representing Model Uncertainty in Deep Learning. ICML.

Full references in the paper.

🤝 Contributing
This is an open‑source research project. Contributions are welcome!

🐛 Report bugs — Open an issue

💡 Suggest improvements — Open an issue or discussion

🔧 Submit code — Fork, make your changes, and open a pull request
📄 License
This project is licensed under the MIT License — see the LICENSE file for details.

Acknowledgements
Special thanks to the AI safety research community for highlighting the importance of uncertainty quantification in deep learning. This work is part of The Approach Papers series — dedicated to exploring the reasoning behind scientific concepts.

📬 Contact
Priyanshu Sharma
GitHub: @Priyanshu-Technologies
Linkedin: https://www.linkedin.com/in/priyanshu-sharma-646233394/

✨ Keep asking why. ✨
