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

- **SCA.ipynb** — Performs ML-based side-channel analysis using  
  Random Forest, Logistic Regression, SVC, and a Single-Layer Perceptron.

- **top10.ipynb** — Identifies and displays the top 10 candidate keys with the highest log-likelihood.

- **rank.ipynb** — Plots key-rank vs number of traces.

-report.pdf contains report.









