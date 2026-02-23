# 📂 Module 2: Solving First-Order Ordinary Differential Equations

Welcome to **Module 2**. In this module, we transition from analyzing the structure of differential equations to actually solving them. Specifically, we will focus on **First-Order, First-Degree Ordinary Differential Equations**. 

There is no single "magic formula" to solve all differential equations. Instead, you must analyze the structure of the equation and select the appropriate mathematical method. This module covers the five standard methods for solving first-order DEs.

---

## 🎯 Module Learning Objectives
By the end of this module, you will be able to:
1. Identify the specific type or form of a given first-order differential equation.
2. Apply algebraic manipulation and substitutions to transform complex equations into solvable forms.
3. Master the five standard techniques for finding the general solution to a first-order DE.

---

## 🗂️ Topic Index & Solution Methods

Navigate through the methods covered in this module using the links below. It is highly recommended to study them in this exact order, as later methods often reduce equations back down to earlier methods (e.g., Homogeneous equations reduce down to Variable Separable).

### 📄 [1. Variable Separable Method](./01-variable-separable.md)
*   **The Concept:** Grouping all $x$ terms with $dx$ and all $y$ terms with $dy$.
*   **The Standard Form:** $f(y)dy = g(x)dx$
*   *Includes 4 step-by-step solved questions.*

### 📄 [2. Homogeneous Differential Equations](./02-homogeneous-eqs.md)
*   **The Concept:** Identifying functions where every term has the same total degree.
*   **The Substitution:** Using $y = vx$ to reduce the equation to a Variable Separable form.
*   *Includes 6 step-by-step solved questions.*

### 📄 [3. Equations Reducible to Homogeneous Form](./03-reducible-to-homo.md)
*   **The Concept:** Handling linear rational equations with constant terms: $\frac{dy}{dx} = \frac{ax+by+C}{Ax+By+C}$.
*   **Case 1:** Ratios of coefficients are not equal ($\frac{a}{A} \neq \frac{b}{B}$).
*   **Case 2:** Ratios of coefficients are equal ($\frac{a}{A} = \frac{b}{B}$).
*   *Includes step-by-step solved questions.*

### 📄 [4. Linear Differential Equations](./04-linear-odes.md)
*   **The Concept:** Solving equations of the form $\frac{dy}{dx} + P(x)y = Q(x)$.
*   **The Tool:** Finding and applying the **Integrating Factor (I.F.)**.
*   *Includes 2 step-by-step solved questions.*

### 📄 [5. Bernoulli's Equations (Reducible to Linear)](./05-bernoulli-eqs.md)
*   **The Concept:** Solving non-linear equations of the form $\frac{dy}{dx} + P(x)y = Q(x)y^n$.
*   **The Substitution:** Dividing by $y^n$ and substituting $z = y^{1-n}$ to transform it into a standard Linear DE.
*   *Includes 2 step-by-step solved questions.*

### 📝 [6. Practice Questions](./06-practice-questions.md)
*   Categorized problems covering all five methods: Variable Separable, Homogeneous, Reducible to Homogeneous, Linear, and Bernoulli.
*   *Includes fully worked solutions.*

---

**Next Steps:** Start with the most fundamental solving technique: [Method 1: Variable Separable](./01-variable-separable.md).