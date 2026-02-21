# 📏 Order and Degree of a Differential Equation

Once you have identified an equation as a Differential Equation (DE), the next critical step is to classify it by its **Order** and **Degree**. These two properties determine the complexity of the equation and dictate which mathematical methods you will need to use to solve it.

---

## 1. Concept Overview

### 1.1 The Order of a Differential Equation
> **Definition:** The **Order** of a differential equation is the order of the highest differential coefficient (derivative) present in the equation.

*   If the highest derivative is $\frac{dy}{dx}$ (or $y'$), it is a **1st-order** DE.
*   If the highest derivative is $\frac{d^2y}{dx^2}$ (or $y''$), it is a **2nd-order** DE.
*   If the highest derivative is $\frac{d^ny}{dx^n}$ (or $y^{(n)}$), it is an **n-th order** DE.

### 1.2 The Degree of a Differential Equation
> **Definition:** The **Degree** of a differential equation is the highest power (exponent) of the highest-order derivative present in the equation.

---

## 2. Important Working Rule
To accurately find the degree of a differential equation, the equation **must be made free from radicals and fractions** as far as the derivatives are concerned. 

If a derivative is inside a square root or raised to a fractional power (e.g., $3/2$), you must use algebraic manipulation (like squaring or cubing both sides) to clear those fractional powers before determining the degree.

---

## 3. Solved Questions

Here are step-by-step examples from the lecture notes demonstrating how to find the order and degree.

### 📝 Question 1
Determine the order and degree of the following Differential Equation:
$$ \cos x \frac{d^2y}{dx^2} + \sin x \left( \frac{dy}{dx} \right)^3 + 8y = \tan x $$

**Solution:**
1. **Find the Order:** Look for the highest derivative in the equation.
   * We have a first derivative: $\frac{dy}{dx}$
   * We have a second derivative: $\frac{d^2y}{dx^2}$
   * The highest derivative is the second derivative. Therefore, the **Order is 2**.
2. **Find the Degree:** Look at the power of the *highest* derivative.
   * The highest derivative is $\frac{d^2y}{dx^2}$.
   * It is not raised to any explicitly written power, which means its power is $1$.
   * *(Note: Do not be tricked by the $\left( \frac{dy}{dx} \right)^3$ term. Even though it has a higher power of 3, it is not the highest-order derivative).*
3. **Final Answer:**
   * **Order:** $2$
   * **Degree:** $1$

---

### 📝 Question 2
Determine the order and degree of the following Differential Equation:
$$ \left[ 1 + \left( \frac{dy}{dx} \right)^2 \right]^{3/2} = K \frac{d^2y}{dx^2} $$

**Solution:**
1. **Apply the Working Rule (Clear Radicals):** We notice that the derivatives on the left side are raised to a fractional power ($3/2$). We cannot determine the degree until this fraction is removed.
2. **Algebraic Manipulation:** To eliminate the denominator of the fraction ($/2$), we square both sides of the equation.
   $$ \left( \left[ 1 + \left( \frac{dy}{dx} \right)^2 \right]^{3/2} \right)^2 = \left( K \frac{d^2y}{dx^2} \right)^2 $$
   $$ \left[ 1 + \left( \frac{dy}{dx} \right)^2 \right]^3 = K^2 \left( \frac{d^2y}{dx^2} \right)^2 $$
3. **Find the Order:** Now look at the manipulated equation. The highest derivative present is $\frac{d^2y}{dx^2}$. 
   * Therefore, the **Order is 2**.
4. **Find the Degree:** Look at the power of that highest derivative. 
   * The term $\left( \frac{d^2y}{dx^2} \right)$ is raised to the power of $2$. 
   * Therefore, the **Degree is 2**.
5. **Final Answer:**
   * **Order:** $2$
   * **Degree:** $2$

---

**Next Topic:** Now that you know how to classify DEs, proceed to [Topic 1.3: Formation of Differential Equations](./03-formation-of-odes.md) to learn how these equations are originally constructed.