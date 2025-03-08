# Numerical Verification of the Spectral Approach to the Riemann Hypothesis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/PS1971/TUO_REPOSITORY_NAME/blob/main/riemann-spectral-verification.ipynb)

**Authors:** Samuel Pedrielli

## Overview

This repository provides numerical evidence supporting the spectral approach to the Riemann Hypothesis.  The core idea of this approach is to construct a self-adjoint operator whose eigenvalues correspond to the non-trivial zeros of the Riemann zeta function.  Because self-adjoint operators have real eigenvalues, this would imply the Riemann Hypothesis (that all non-trivial zeros have a real part of 1/2).

This project does *not* claim to prove the Riemann Hypothesis.  Instead, it demonstrates the key principles numerically, using a simplified model.  Specifically, we verify:

1.  **GUE Statistics of Riemann Zeros:** We show that the statistical distribution of the spacings between consecutive Riemann zeros is consistent with the Gaussian Unitary Ensemble (GUE) of random matrix theory.

2.  **GUE Statistics of Scaled GUE Matrix Eigenvalues:** We construct a random matrix from the GUE and scale its eigenvalues to approximate the Riemann zeros. We then demonstrate that the *spacings* between these scaled eigenvalues *also* follow GUE statistics.

3. **Approximation of Zeros:** We show that the scaled GUE matrix eigenvalues provide a reasonable (though not perfect) approximation to the Riemann zeros.

## Repository Structure

*   **`riemann_verification.ipynb`:**  The Jupyter Notebook containing the Python code for the numerical verification.  This is the main file.
*   **`requirements.txt`:**  A list of the Python libraries required to run the notebook.

## Instructions

The easiest way to run the code and see the results is to use Google Colab:

1.  **Click the "Open in Colab" button** at the top of this README. This will open the notebook directly in a Colab environment.
2.  **Run all cells:** In the Colab menu, select "Runtime" -> "Run all".

Alternatively, you can run the notebook locally:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/PS1971/TUO_REPOSITORY_NAME.git](https://www.google.com/search?q=https://github.com/TUO_USERNAME/TUO_REPOSITORY_NAME.git)
    cd TUO_REPOSITORY_NAME
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the notebook:**
    ```bash
    jupyter notebook riemann_verification.ipynb
    ```
    (Or use JupyterLab: `jupyter lab`)

## Results

The notebook performs the following calculations and generates corresponding plots:

*   **Calculation of Riemann zeta zeros:** The first *n* non-trivial zeros of the Riemann zeta function are computed (or pre-loaded for efficiency).
*   **GUE statistics of zeros:** The spacings between consecutive zeros are calculated, normalized, and compared to the Wigner surmise (the expected distribution for GUE). A Kolmogorov-Smirnov test and the mean level spacing ratio are used to assess the goodness of fit.
*   **Construction of a GUE matrix:** A random matrix from the Gaussian Unitary Ensemble is generated.
*   **Scaling of GUE eigenvalues:** The eigenvalues of the GUE matrix are scaled to match the mean and standard deviation of the Riemann zeros.
*   **GUE statistics of scaled eigenvalues:**  The spacings between the *scaled* eigenvalues are calculated, normalized, and compared to the Wigner surmise (Kolmogorov-Smirnov test and mean level spacing ratio).
*   **Comparison of eigenvalues and zeros:** The scaled eigenvalues are plotted against the Riemann zeros, and the Root Mean Squared Error (RMSE) is calculated.

The results consistently show:

*   **Strong evidence for GUE statistics:** Both the Riemann zeros and the scaled GUE eigenvalues exhibit statistics very close to the GUE predictions (high p-values in the K-S test and mean level spacing ratios close to the expected GUE value).
*   **Reasonable approximation:** The scaled GUE eigenvalues provide a reasonable approximation to the Riemann zeros, although the approximation becomes less accurate for larger zeros.

## Conclusion

The numerical results presented in this repository strongly support the connection between the Riemann zeros and the eigenvalues of random matrices from the Gaussian Unitary Ensemble. While this is not a proof of the Riemann Hypothesis, it provides compelling evidence for the spectral approach.

## Citation

If you use this code or the results in your research, please cite it as follows:

[Pedrielli], [Samuel], Pedrielli, S. (2024). Numerical Verification of the Spectral Approach to the Riemann Hypothesis [Jupyter Notebook]. GitHub repository. [Link al tuo repository GitHub]


## License

This project is licensed under the MIT License - see the LICENSE file for details.
