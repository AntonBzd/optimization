# Optimization Repository

This repository contains implementations of optimization techniques, including **Quantile Regression** and **Optimal Transport Problem**, using Python and **CVXPY** for convex optimization.

## 📂 Contents

- **Quantile Regression** – Solving quantile regression as a linear programming problem.
- **Optimal Transport Problem** – Solving the optimal transport problem using linear programming and Sinkhorn algorithm.

---

## 📝 Related Articles

Check out my articles on Medium that provide deeper insights into these topics:

- [Quantile Regression with Linear Programming](https://medium.com/@antobezard/quantile-regression-with-linear-programming-2305d613cb5b) — Explore the nuances of quantile regression and see the step-by-step implementation.
- [Solving the Optimal Transport Problem with Linear Programming and the Sinkhorn Algorithm](https://medium.com/@antobezard/solving-the-optimal-transport-problem-with-linear-programming-and-the-sinkhorn-algorithm-a226a6baab6f) — Dive into the optimal transport problem, comparing different approaches.

---

## 🚀 Quantile Regression

### 📌 Overview
Quantile regression is an extension of linear regression that estimates the conditional quantile function instead of the mean. It is particularly useful when the relationship between variables is not uniform across the distribution.

### 🛠️ Implementation Details
- Uses **CVXPY** to frame the problem as a linear program.
- Reads dataset (`quantile-regression-data.csv`) containing `x` and `y` values.
- Constructs constraint matrices and optimizes for different quantiles.

### 📜 Code Highlights
- Formulation of the **constraint matrix** for quantile regression.
- Use of **absolute deviation loss** instead of mean squared error.
- Solving the optimization problem using **cvxpy**.

### 📈 Expected Output
- Regression coefficients for different quantile levels.
- Plots comparing the standard regression line with quantile regression lines.

---

## 🚀 Optimal Transport Problem

### 📌 Overview
The **Optimal Transport Problem** (Monge-Kantorovich problem) is a fundamental problem in optimization and probability theory, describing how to optimally move mass from one distribution to another with minimal cost.

### 🛠️ Implementation Details
- Two approaches:
  1. **Linear Programming (LP) Solution** – Solves via standard optimization techniques.
  2. **Sinkhorn Algorithm** – Uses entropy regularization for fast computation.

### 📜 Code Highlights
- **Linear programming approach:**
  ```python
  # Solve using linear programming (C: cost matrix, s: source distribution, d: target distribution)
  P, cost, execution_time = linear_solver(C, s, d)
  ```
- **Sinkhorn algorithm:**
  ```python
  # Solve using Sinkhorn algorithm
  P_sinkhorn, cost_sinkhorn, execution_time_sinkhorn = Sinkhorn_solver(C, s, d, epsilon=0.1, accuracy=0.01)
  ```
  
### 📈 Expected Output
- Optimal transport matrix `P`.
- Minimal transport cost.
- Computation time comparison between LP and Sinkhorn method.

---

## 📌 Dependencies

Install required libraries using:

```bash
pip install numpy pandas cvxpy matplotlib
```

---

## 🔥 Author & Contact
👤 **Antonin**  

---
