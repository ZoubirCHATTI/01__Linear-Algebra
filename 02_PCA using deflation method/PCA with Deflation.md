# PCA with Deflation

This repository contains a Python implementation of Principal Component Analysis (PCA) using the deflation method. The provided Jupyter Notebook `PCA_deflation.ipynb` demonstrates how to apply PCA to a dataset, specifically the Iris dataset, to reduce dimensionality and visualize the principal components.




## Features

- **PCA Implementation**: Core PCA algorithm implemented from scratch.
- **Deflation Method**: Utilizes the deflation method for extracting principal components sequentially.
- **Data Centering**: Includes a function to center the data before PCA application.
- **Power Iteration**: Employs power iteration for efficient eigenvalue and eigenvector computation.
- **Iris Dataset Example**: Demonstrates PCA on the classic Iris dataset.
- **2D Visualization**: Projects and visualizes data onto the first two principal components using `matplotlib` and `seaborn`.




## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Make sure you have the following installed:

- Python 3.x
- Jupyter Notebook
- `numpy`
- `matplotlib`
- `seaborn`

You can install the required Python libraries using pip:

```bash
pip install numpy matplotlib seaborn
```

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/PCA_deflation.git
   cd PCA_deflation
   ```

2. Ensure the `functions` directory is correctly set up (as indicated by `sys.path.append(path)` in the notebook). You might need to create a `functions` directory in the root of your project and place the `deflation.py` (or similar) file containing `centering`, `P_I`, and `deflation` functions there.

   A placeholder for `deflation.py` might look like this:

   ```python
   # functions/deflation.py
   import numpy as np

   def centering(A):
       # Implementation for centering matrix A and returning covariance
       mean = np.mean(A, axis=0)
       A_centred = A - mean
       cov = np.cov(A_centred, rowvar=False)
       return A_centred, cov

   def P_I(matrix, n_iter, epsilon):
       # Implementation for power iteration
       b_k = np.random.rand(matrix.shape[0])
       for _ in range(n_iter):
           b_k1 = np.dot(matrix, b_k)
           b_k1_norm = np.linalg.norm(b_k1)
           b_k = b_k1 / b_k1_norm
       eigenvalue = np.dot(b_k.T, np.dot(matrix, b_k)) / np.dot(b_k.T, b_k)
       return eigenvalue, b_k

   def deflation(cov_matrix, n_iter, epsilon):
       # Implementation for deflation method to find multiple eigenvalues and eigenvectors
       eigenvalues = []
       eigenvectors = []
       B = np.copy(cov_matrix)
       for _ in range(cov_matrix.shape[0]): # Assuming we want all components
           eigenval, eigenvec = P_I(B, n_iter, epsilon)
           eigenvalues.append(eigenval)
           eigenvectors.append(eigenvec)
           B = B - eigenval * np.outer(eigenvec, eigenvec)
       return np.array(eigenvalues), np.array(eigenvectors).T
   ```

3. The notebook also expects a `data` directory with `iris.txt`. Create a `data` directory and place the Iris dataset there. A sample `iris.txt` can be found from various online sources or created manually with comma-separated values (sepal length, sepal width, petal length, petal width, species).

   Example `iris.txt` format (first few lines):
   ```
   5.1,3.5,1.4,0.2,Iris-setosa
   4.9,3.0,1.4,0.2,Iris-setosa
   4.7,3.2,1.3,0.2,Iris-setosa
   ...
   ```




## Usage

1. Open the Jupyter Notebook:

   ```bash
   jupyter notebook PCA_deflation.ipynb
   ```

2. Run all cells in the notebook. The notebook will:
   - Load the Iris dataset from `../data/iris.txt`.
   - Apply the custom PCA function to the dataset.
   - Project the data onto the first two principal components.
   - Generate a scatter plot visualizing the projected data, with different colors for each Iris species, and showing the directions of the first two principal components.

### PCA Function Details

The `pca` function defined in the notebook takes the following arguments:

- `A`: The input data matrix (e.g., `variables` from the Iris dataset).
- `n_iter`: Number of iterations for the power iteration method.
- `epsilon`: Tolerance for convergence in the power iteration method.

It returns:

- `p1`: Projections of the data onto the first principal component.
- `p2`: Projections of the data onto the second principal component.
- `PC1`: The first principal component (eigenvector).
- `PC2`: The second principal component (eigenvector).




## Contributing

Contributions are welcome! If you have suggestions for improvements, bug fixes, or new features, please open an issue or submit a pull request.



