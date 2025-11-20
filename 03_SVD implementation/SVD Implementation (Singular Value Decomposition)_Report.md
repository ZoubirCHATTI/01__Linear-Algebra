# 🔢 SVD Implementation (Singular Value Decomposition)

This Jupyter Notebook provides a step-by-step, manual implementation of the **Singular Value Decomposition (SVD)** algorithm in Python. The primary goal is to understand the mathematical process behind SVD and compare the custom implementation with the highly optimized function provided by `numpy.linalg.svd`.

## 🌟 Features

- **Manual SVD Implementation:** The notebook contains two custom functions for SVD:
    1. `basic_SVD`: A fundamental implementation that works for full-rank matrices.
    1. `red_SVD`: A more robust implementation that handles the problem of **null singular values** (reduced-rank matrices).

- **Comparison with NumPy:** The custom results are compared against the output of `numpy.linalg.svd` to validate the manual implementation.

- **Educational Focus:** Clearly demonstrates the use of the Gram matrix and the relationship between SVD and Eigen Decomposition.

## 🛠️ Technologies Used

- **Language:** Python

- **Libraries:** `numpy` (for matrix operations and comparison)

- **Environment:** Jupyter Notebook (or any environment capable of running `.ipynb` notebooks)

## 🚀 Installation and Setup

### Prerequisites

You need a Python environment with the `numpy` library installed:

```bash
pip install numpy
```

### Execution

1. **Download** the `Singular_value_decomposition_implementation(1).ipynb` file.

1. **Open** the notebook in your Jupyter environment.

1. **Execute** the cells sequentially. The notebook generates a random matrix and then tests the three different SVD methods (basic, NumPy, and reduced) to show that they all successfully reconstruct the original matrix.

## 💡 Key Concepts Demonstrated

| Function | Purpose | Key Mathematical Step |
| --- | --- | --- |
| **`basic_SVD`** | Implements SVD assuming no null singular values. | Uses Eigen Decomposition of the Gram matrix ($A^T A$). |
| **`red_SVD`** | Implements SVD while handling null singular values. | Filters out near-zero eigenvalues to compute the reduced SVD. |
| **Comparison** | Reconstructs the original matrix $A$ from $U \Sigma V^T$ for all methods. | Validates the correctness of the manual implementations. |

## 📝 Author

- [Zoubir CHATTI]

