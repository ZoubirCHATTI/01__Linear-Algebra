# 🖼️ SVD for Image Denoising/Compression (Singular Value Decomposition)

This Jupyter Notebook demonstrates a powerful application of the **Singular Value Decomposition (SVD)** algorithm for **image processing**, specifically for **denoising** and **compression**. By treating the image as a matrix and leveraging the low-rank approximation property of SVD, we can effectively reduce noise and significantly compress the image data while retaining most of the visual information.

## 🌟 Features

- **Image Loading and Preprocessing:** Loads an image (e.g., the GitHub logo) and converts it to a grayscale matrix for SVD application.

- **SVD Application:** Decomposes the image matrix into its singular values, which represent the importance of each component.

- **Optimal Rank Selection:** Uses the **Elbow Method** (via the `kneed` library) on the singular values to determine the optimal number of components to retain for reconstruction.

- **Image Reconstruction:** Reconstructs the image using only the most significant singular values, achieving compression and noise reduction.

- **Visual Comparison:** Compares the original image with the compressed/denoised image.

## 🛠️ Technologies Used

- **Language:** Python

- **Libraries:** `numpy`, `matplotlib`, `scikit-image` (`skimage`), `kneed`

- **Environment:** Jupyter Notebook (or any environment capable of running `.ipynb` notebooks)

## 🚀 Installation and Setup

### Prerequisites

You need a Python environment with the following libraries installed:

```bash
pip install numpy matplotlib scikit-image kneed
```

### Execution

1. **Download** the `simple_SVD_code_for_denoising_github_image.ipynb` file.

1. **Ensure Image File:** The notebook expects an image file (e.g., `GitHub.png`) to be available at the specified path (`.../data/GitHub.png`). You must adjust the `path` variable in the notebook to point to your image file.

1. **Open** the notebook in your Jupyter environment.

1. **Execute** the cells sequentially to see the image processing and reconstruction in action.

## 💡 Key Concepts Demonstrated

| Concept | Description |
| --- | --- |
| **Image as a Matrix** | A grayscale image is represented as a matrix where each pixel's intensity is an entry. SVD is applied directly to this matrix. |
| **Low-Rank Approximation** | By keeping only the top $k$ singular values, the image is approximated by a lower-rank matrix, which is the core principle of SVD-based compression. |
| **Elbow Method** | A heuristic used to find the "knee" or bend in the plot of singular values, indicating the point where the remaining values contribute mostly to noise or minor details. |

## 📝 Author

- [Zoubir CHATTI]

