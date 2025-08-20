Valorant Win Rate Prediction
📌 Overview

This project predicts match outcome (win vs. loss) in Valorant using player performance features (KD, kills, deaths, assists) plus categorical context (agent, map). The original continuous win rate was converted to a binary target using a 0.5 threshold:

win = 1 if win_rate ≥ 0.5

win = 0 otherwise

The workflow covers EDA → preprocessing → baseline Logistic Regression → hyperparameter tuning → evaluation.

🔑 Features

EDA: frequency plots (agents, maps), histograms, correlation matrix

Preprocessing: encoding categorical features (Agent Name, map_name), handling types

Models: Base Logistic Regression vs. tuned Logistic Regression

Evaluation: accuracy (train/test), side-by-side bar chart comparison

📂 Structure
Valorant-Win-Rate-Prediction/
├── README.md
└── Valorant_data_prediction_hyper_parameter.ipynb

⚙️ Installation & Run

Clone the repo and install the libraries listed below (no requirements.txt needed):

git clone https://github.com/Dr-Zero69/Valorant-Win-Rate-Prediction.git
cd Valorant-Win-Rate-Prediction

# (optional but recommended) create a virtual env
python -m venv .venv
# mac/linux
source .venv/bin/activate
# windows (powershell)
.venv\Scripts\Activate.ps1

# install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn jupyter


Launch the notebook:

jupyter notebook Valorant_data_prediction_hyper_parameter.ipynb

📦 Dependencies

Python 3.x

numpy, pandas

matplotlib, seaborn

scikit-learn

jupyter

(If you later prefer a requirements.txt, you can add one with the same list.)

🧪 Data & Target

Target: binary win label derived from win_rate using 0.5 threshold

Predictors: KD, Kills, Deaths, Assists, Agent Name, map_name (and any others present)

Notes: KD is related to Kills/Deaths; keep an eye on multicollinearity for linear models. Trees are less sensitive.

Results

Base Logistic Regression (test): 64.35% accuracy

Tuned Logistic Regression (test): 67.57% accuracy

The tuned model outperforms the base model on both train and test sets (see bar chart in the notebook).

Repro Tips

Ensure categorical encoding happens after splitting (or use pipelines) to avoid leakage.

If classes are imbalanced, report additional metrics (precision/recall, F1, ROC AUC) and/or use class weights.

Contributing

Issues and PRs are welcome—feel free to suggest features (e.g., tree models, cross-validation, confusion matrix in README).

Optional: .gitignore

Create a .gitignore to keep the repo clean:

.ipynb_checkpoints/
__pycache__/
*.pyc
.venv/
.env

License (MIT)

You can keep this section here or copy it into a new LICENSE file.

MIT License

Copyright (c) 2025 Anurodh Jha

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
