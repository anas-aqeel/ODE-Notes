# 📂 Module 5: Higher-Order Linear ODEs (Variable Coefficients)

Welcome to **Module 5**. Up until this point, we have focused exclusively on higher-order linear differential equations where the coefficients were constants (e.g., $3y'' + 2y' + y = 0$). 

However, in many advanced engineering and physics problems, the coefficients are variables—specifically, powers of $x$. In this module, we will learn how to handle a very specific and famous type of variable-coefficient equation: the **Cauchy-Euler Equation**.

---

## 🎯 Module Learning Objectives
By the end of this module, you will be able to:
1. Identify a Cauchy-Euler Differential Equation by checking if the power of the independent variable $x$ matches the order of the derivative it multiplies.
2. Apply the independent variable substitution ($x = e^t$) to transform the variable-coefficient equation into a standard constant-coefficient equation.
3. Solve the transformed equation using the techniques mastered in Module 4, and translate the final answer back into terms of $x$.

---

## 🗂️ Topic Index

Navigate to the lesson for this module using the link below:

### 📄 [1. Cauchy-Euler Differential Equations](./01-cauchy-euler-eqs.md)
*   **The Concept:** Recognizing the $x^n \frac{d^ny}{dx^n}$ structure.
*   **The Substitution Rule:** Letting $x = e^t$ and defining the new operator $D = \frac{d}{dt}$.
*   **The Transformation:** Changing $x\frac{dy}{dx}$ to $Dy$ and $x^2\frac{d^2y}{dx^2}$ to $D(D-1)y$.
*   *Includes step-by-step solved questions converting back and forth between $x$ and $t$ domains.*

### 📝 [2. Practice Questions](./02-practice-questions.md)
*   Comprehensive Cauchy-Euler problems including algebraic, logarithmic, and trigonometric right-hand sides.
*   *Includes fully worked solutions for 4th order, complex roots, and double failure cases.*

---

**Next Steps:** Proceed to [Topic 1: Cauchy-Euler Equations](./01-cauchy-euler-eqs.md) to learn how to master this transformative technique.