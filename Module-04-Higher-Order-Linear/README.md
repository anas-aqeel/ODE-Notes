# 📂 Module 4: Higher-Order Linear ODEs (Constant Coefficients)

Welcome to **Module 4**. In the previous modules, we dealt with first-order equations where the highest derivative was $\frac{dy}{dx}$. Now, we advance to **Higher-Order Linear Differential Equations**, which involve second derivatives ($\frac{d^2y}{dx^2}$), third derivatives, and beyond.

These equations are fundamental in analyzing mechanical vibrations, electrical circuits (RLC circuits), and structural engineering. This module focuses specifically on linear equations with **Constant Coefficients**.

---

## 🎯 Module Learning Objectives
By the end of this module, you will be able to:
1.  Understand the structure of the General Solution: $y = y_c + y_p$.
2.  Solve homogeneous linear equations by finding the roots of the Characteristic Equation (to find $y_c$).
3.  Apply specific methods to find the Particular Integral ($y_p$) for different types of non-homogeneous functions (Exponential, Algebraic, Trigonometric).

---

## 🗂️ Topic Index & Solution Methods

The solution to a non-homogeneous linear ODE $f(D)y = F(x)$ is always the sum of two parts:
$$ y = y_c + y_p $$

Navigate through the methods for finding these parts using the links below:

### 📄 [1. Finding the Complementary Function ($y_c$)](./01-finding-yc.md)
*   **The Concept:** Solving the homogeneous part $f(D)y = 0$.
*   **The Method:** Using the Auxiliary (Characteristic) Equation to find roots.
*   **Cases:** Real & Distinct, Real & Repeated, and Complex Conjugate roots.

### 📄 [2. Particular Integral ($y_p$): Exponential Case](./02-yp-exponential.md)
*   **Function:** $F(x) = e^{ax}$
*   **Rule:** Replace $D$ with $a$.
*   *Includes the "Case of Failure" where $f(a) = 0$.*

### 📄 [3. Particular Integral ($y_p$): Algebraic Case](./03-yp-algebraic.md)
*   **Function:** $F(x) = x^n$ (Polynomials)
*   **Rule:** Expand $[f(D)]^{-1}$ using the Binomial Theorem.
*   *Includes step-by-step solved questions.*

### 📄 [4. Particular Integral ($y_p$): Trigonometric Case](./04-yp-trigonometric.md)
*   **Function:** $F(x) = \sin(ax)$ or $\cos(ax)$
*   **Rule:** Replace $D^2$ with $-a^2$.
*   *Includes the "Case of Failure" handling.*

### 📄 [5. Particular Integral ($y_p$): Shift & Product Rules](./05-yp-shift-product.md)
*   **Function:** $F(x) = e^{ax} V(x)$ (Product of exponential and another function)
*   **Rule:** The Exponential Shift Theorem.
*   *Includes solved examples combining multiple methods.*

---

**Next Steps:** The first step in solving *any* higher-order linear equation is finding the Complementary Function. Proceed to [Topic 1: Finding $y_c$](./01-finding-yc.md).