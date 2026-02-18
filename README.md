# Advanced Mathematics - Assignment 1

**Name:** Naman Bansal  
**Roll Number:** 102303496  

## Results (Estimated Parameters)

Based on the assignment formulation, here are the final calculated parameters for the probability density function $\hat{p}(z) = c * e^{-\lambda(z-\mu)^2}$:

*   **$\mu$**: `25.810230670014192`
*   **$\lambda$**: `0.0014604852717727988`
*   **$c$**: `0.02156123606454654`

---

## Assignment Details

### 1. Feature Extraction
The feature **NO2** (as $x$) is extracted from the `data.csv` dataset. Rows with missing (`NA`) NO2 values are removed from the computation to ensure accurate results.

### 2. Transformation Function
Each value of $x$ is transformed into $z$ using the transformation function:
$$z = x + a_r \cdot \sin(b_r \cdot x)$$

Using Roll No **102303496**, we derived the constants:
*   $a_r = 0.05 \cdot (102303496 \pmod 7) = 0.05$
*   $b_r = 0.3 \cdot ((102303496 \pmod 5) + 1) = 0.6$

### 3. Probability Density Function Estimation
Using Maximum Likelihood Estimation (MLE) on the premise of a Gaussian distribution, the target parameters were learned:
*   **Mean ($\mu$)** is calculated as the sample mean of the transformed variable $z$.
*   **Lambda ($\lambda$)** is calculated as $\frac{1}{2\sigma^2}$, where $\sigma$ is the sample standard deviation of $z$.
*   **Constant ($c$)** is calculated as $\frac{1}{\sigma \sqrt{2\pi}}$.

## Files in this Directory
*   `solution.py`: Python script used to parse the dataset, perform the transformation, and compute the mathematical parameters.
*   `output_parameters.txt`: Raw text output log containing the final calculated values.
*   `data.csv`: The primary India air quality dataset (downloaded from Kaggle).
