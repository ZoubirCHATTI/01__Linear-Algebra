# 📊 PCA Deflation Implementation (Principal Component Analysis)

This Jupyter Notebook provides a custom implementation of the **Principal Component Analysis (PCA)** algorithm, focusing on the **Deflation Method** to sequentially extract principal components. This project is designed to be educational, showing the mathematical core of PCA without relying solely on high-level libraries like `scikit-learn`.

## 🌟 Features

- **Custom PCA Implementation:** Implements PCA from scratch using fundamental linear algebra concepts.

- **Deflation Method:** Uses the deflation technique to find subsequent principal components after the first one has been identified.

- **Data Visualization:** Projects the data onto the first two principal components (PC1 and PC2) and visualizes the results using `matplotlib` and `seaborn`.

- **Application Example:** Applies the custom PCA function to a classic dataset (likely the Iris dataset) to demonstrate dimensionality reduction.

## 🛠️ Technologies Used

- **Language:** Python

- **Libraries:** `numpy`, `matplotlib`, `seaborn`

- **Environment:** Jupyter Notebook (or any environment capable of running `.ipynb` notebooks)

## 🚀 Installation and Setup

### Prerequisites

You need a Python environment with the following libraries installed:

```bash
pip install numpy matplotlib seaborn
```

### Execution

1. **Download** the `PCA_deflation.ipynb` file.

1. **Ensure Data and Functions:** This notebook relies on external files:
  - A data file (e.g., `iris.txt`) located in a `../data/` directory.
  - Custom functions (`centering`, `P_I`, `deflation`) located in a `../functions/` directory.
    **

1. **Open** the notebook in your Jupyter environment.

1. **Execute** the cells sequentially. The final cell will display the 2D scatter plot of the data projected onto PC1 and PC2.

## 💡 Key Concepts Demonstrated

| Concept | Description |
| --- | --- |
| **Centering** | Preprocessing step to shift the data so that the mean of each feature is zero. |
| **Power Iteration (P_I)** | An iterative algorithm used to find the largest eigenvalue and its corresponding eigenvector (the first principal component). |
| **Deflation** | A technique used to modify the covariance matrix after finding the first principal component, allowing the power iteration method to find the next largest component. |

## 📝 Author

- [Zoubir CHATTI]



