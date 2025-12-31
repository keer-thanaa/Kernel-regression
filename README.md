## Kernel Regression

In many real-world regression problems, the relationship between input features and the target variable is **not strictly linear**. Linear regression assumes a straight-line relationship, which often leads to **underfitting** when the data follows a more complex pattern. To address this limitation, **kernel-based methods** are used.

---

## Kernel Intuition
A **kernel** allows the model to capture non-linear relationships by implicitly mapping the input data into a **higher-dimensional feature space**, where a linear model can better fit the data. This transformation is performed **implicitly** using the *kernel trick*, without explicitly computing the high-dimensional mapping.

---

## Kernel Ridge Regression
In this project, **Kernel Ridge Regression** from scikit-learn is used. Kernel Ridge Regression combines:

- **Ridge Regression**, which applies **L2 regularization** to prevent overfitting by penalizing large model coefficients, and  
- **Kernel methods**, which enable non-linear regression through kernel functions such as the **RBF (Gaussian) kernel**.

---

## Hyperparameters

### Alpha (α)
Alpha controls the **regularization strength**.  
A higher alpha increases the penalty on large coefficients, resulting in a **simpler and more stable model**.

### Gamma (γ)
Gamma is specific to the **RBF kernel** and controls the **smoothness of the regression curve**:
- Small gamma → smoother curve (higher bias, lower variance)
- Large gamma → more flexible curve (lower bias, higher variance)

---

## Dataset and Experiment Setup
To ensure a fair comparison, the **same dataset used for linear regression** is reused. However, only **one feature** is selected for this experiment to simplify visualization and clearly demonstrate the non-linear behavior captured by kernel regression.

---

## Results
After applying kernel regression, the model is able to better capture the underlying **non-linear patterns** in the data. This improvement is reflected in a **lower Mean Squared Error (MSE)** compared to linear regression, demonstrating the advantage of kernel-based methods when the linearity assumption does not hold.
