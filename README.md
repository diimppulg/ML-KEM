# ML-KEM
## 📂 Dataset

This project uses the Kyber side-channel dataset from:

Rezaeezade et al. *"Side-Channel Power Trace Dataset for Kyber Pair-Pointwise Multiplication on Cortex-M4."*  
Cryptology ePrint Archive, Paper 2025/811.

Due to GitHub file-size limits, the dataset is hosted externally.
the matlab files are changed to npy files and uploaded here.
👉 **Download here:**  
https://drive.google.com/drive/folders/1GUskLSzM39t7ZgY3x5HvGcYMYng2F3xm?usp=drive_link

### File Structure
kyber_sidechannel_dataset/
├── nonces.npy
├── traces.npy
├── nonces_dataset/
│ ├── noncesA0.npy
│ ├── noncesA1.npy
│ ...
│ └── noncesA9.npy
└── traces_dataset/
│ ├── tracesA0.npy
│ ├── tracesA1.npy
...
│ └── tracesA9.npy


As mentioned above, the dataset is taken from Rezaeezade et al. It was originally provided as MATLAB files and has been converted into NumPy (`.npy`) format.

`traces.npy` contains 100,000 power traces, each represented by 50,000 time samples (each time sample is 1 byte).

`nonces.npy` contains 6 values for each of the 100,000 traces, each value stored as 2-byte little-endian integers.

traces.npy is divided to tracesA0.npy ,tracesA1.npy ....tracesA9.npy ,each contains 10,000 traces .
similarly with nonces.npy.

## ✅ Running the Code

After downloading the dataset, place the datset files in the same repository of ipynb files:

—or update the dataset path in the code/notebooks accordingly.

after that You can either:
- install the required dependencies and run the notebooks yourself, or
- simply view the results already included in the notebook outputs.


## 📘 Notebooks Overview

### 🛠️ Core Analysis Notebooks
The root directory contains the primary entry-point notebooks used to run evaluations, trace feature significance, and benchmark overall metrics:

- **SCA.ipynb** — Performs ML-based side-channel analysis using  
  Random Forest, Logistic Regression, SVC, and a Single-Layer Perceptron.

- **top10.ipynb** — Identifies and displays the top 10 candidate keys with the highest log-likelihood for different poi values using random forest model.

- **rank.ipynb** — Plots key-rank vs number of traces for randomforest model.

---

### 📂 Model-Specific Performance Directories
Each folder below represents an isolated pipeline stage containing its respective implementation scripts (`.ipynb`), quantitative metric arrays (`.json`), and  subkey convergence curves (`.pdf` format for both a_0 and a_1)for diiferent poi values:



* 📁- ***RF/***- This folder contains code(ipynb files),results(json files),plots of key-rank vs no.of traces(pdf for both a0,a1) using Random Forest model for different poi values .

* 📁-  ***XGB/***- This folder contains code(ipynb files),results(json files),plots of key-rank vs no.of traces (pdf for both a0,a1)using XGboost model for different poi values .

* 📁-  ***SVC/***- This folder contains code(ipynb file),results(json files),plots of key-rank vs no.of traces (pdf for both a0,a1)using Support Vector Classifier model for different poi values .

* 📁-  ***LR/***- This folder contains code(ipynb file),results(json files),plots of key-rank vs no.of traces (pdf for both a0,a1)using Logistic Regression model for different poi values .

* 📁-  ***SLP/***- This folder contains code(ipynb file),results(json files),plots of key-rank vs no.of traces (pdf for both a0,a1)using Single Layer Perceptron model for different poi values .

* 📁-  ***CNN/***- This folder contains code(ipynb file),results(json file),plots of key-rank vs no.of traces (pdf for both a0,a1)using Convolutional Neural Network .

* 📁-  ***LSTM_RNN/***- This folder contains code(ipynb file) of Long Short-Term Memory and Recurrent Neural Network .


---

### 📄 Final Deliverables
-clg_report.pdf contains report.










