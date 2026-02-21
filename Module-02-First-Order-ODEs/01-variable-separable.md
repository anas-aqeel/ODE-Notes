# 🧮 1. Variable Separable Method

The simplest and most straightforward technique for solving first-order Ordinary Differential Equations is the **Variable Separable** method. Whenever you are faced with a new DE, you should always check if it can be solved using this method before attempting more complex techniques.

---

## 1. Concept Overview

> **Definition:** A first-order differential equation is considered "separable" if it can be written entirely in the form:
> $$ f(y) dy = g(x) dx $$

This means you can completely isolate all terms containing the dependent variable $y$ (including $dy$) on one side of the equals sign, and all terms containing the independent variable $x$ (including $dx$) on the other side.

---

## 2. Working Rule (Step-by-Step)

To solve a differential equation using the variable separable method, follow these steps:
1.  **Rearrange the Equation:** Use algebraic manipulation (factoring, cross-multiplying, dividing) to get all $y$-terms with $dy$ on the left side, and all $x$-terms with $dx$ on the right side.
2.  **Integrate Both Sides:** Apply the integral sign to both sides of the separated equation: $\int f(y) dy = \int g(x) dx$.
3.  **Add the Constant:** After integrating, add a single arbitrary constant of integration (usually $C$) to one side of the equation (conventionally the $x$-side).
4.  **Apply Initial Conditions (If Given):** If the problem provides specific values for $x$ and $y$ (an Initial Value Problem), plug them into your general solution to solve for the exact value of $C$.

---

## 3. Solved Questions

Here are four questions from the lecture notes, demonstrating standard separation, factoring, initial value problems, and pre-substitution.

### 📝 Question 1: Standard Separation
**Solve:** $(x+1)\frac{dy}{dx} = x(y^2+1)$

**Solution:**
1. **Separate the variables:**
   Divide by $(y^2+1)$ and divide by $(x+1)$ to move terms:
   $$ \frac{1}{y^2+1} dy = \frac{x}{x+1} dx $$
2. **Manipulate the right side for easier integration:**
   Notice that $\frac{x}{x+1} = \frac{x+1-1}{x+1} = 1 - \frac{1}{x+1}$
   $$ \frac{1}{y^2+1} dy = \left( 1 - \frac{1}{x+1} \right) dx $$
3. **Integrate both sides:**
   $$ \int \frac{1}{y^2+1} dy = \int \left( 1 - \frac{1}{x+1} \right) dx $$
   $$ \tan^{-1}(y) = x - \ln|x+1| + C $$
4. **Final General Solution:**
   $$ y = \tan(x - \ln|x+1| + C) $$

---

### 📝 Question 2: Factoring Before Separation
**Solve:** $(xy^2+x)dx + (yx^2+y)dy = 0$

**Solution:**
1. **Factor out common terms:**
   $$ x(y^2+1)dx + y(x^2+1)dy = 0 $$
2. **Move the $dy$ term to the right side:**
   $$ x(y^2+1)dx = -y(x^2+1)dy $$
3. **Separate variables:**
   Divide by $(x^2+1)$ and $(y^2+1)$:
   $$ \frac{x}{x^2+1} dx = -\frac{y}{y^2+1} dy $$
4. **Integrate both sides:**
   Multiply both sides by 2 to perfectly match the derivative of the denominators:
   $$ \frac{1}{2} \int \frac{2x}{x^2+1} dx = -\frac{1}{2} \int \frac{2y}{y^2+1} dy $$
   $$ \frac{1}{2}\ln|x^2+1| = -\frac{1}{2}\ln|y^2+1| + C $$
5. **Simplify using logarithm rules:**
   $$ \ln(x^2+1) + \ln(y^2+1) = 2C $$
   $$ \ln[(x^2+1)(y^2+1)] = C' \implies (x^2+1)(y^2+1) = e^{C'} = K $$
   *(Where $K$ is just a new arbitrary constant).*

---

### 📝 Question 3: Initial Value Problem (IVP)
**Solve:** $x\frac{dy}{dx} + \cot y = 0$ given the initial condition $y = \frac{\pi}{4}$ when $x = \sqrt{2}$.

**Solution:**
1. **Separate the variables:**
   $$ x\frac{dy}{dx} = -\cot y $$
   $$ \frac{1}{\cot y} dy = -\frac{1}{x} dx \implies \tan y \, dy = -\frac{1}{x} dx $$
2. **Integrate both sides:**
   $$ \int \tan y \, dy = -\int \frac{1}{x} dx $$
   $$ -\ln|\cos y| = -\ln|x| + \ln C $$
   *(Using $\ln C$ instead of $C$ makes simplification easier).*
3. **Simplify the General Solution:**
   Multiply by $-1$:
   $$ \ln|\cos y| = \ln|x| - \ln C \implies \ln(\cos y) = \ln\left(\frac{x}{C}\right) $$
   $$ \cos y = \frac{x}{C} \implies x = C \cos y $$
4. **Apply Initial Conditions to find $C$:**
   Substitute $x = \sqrt{2}$ and $y = \pi/4$:
   $$ \sqrt{2} = C \cos\left(\frac{\pi}{4}\right) $$
   $$ \sqrt{2} = C \left(\frac{1}{\sqrt{2}}\right) \implies C = \sqrt{2} \times \sqrt{2} = 2 $$
5. **Final Particular Solution:**
   $$ x = 2 \cos y \quad \text{or} \quad y = \cos^{-1}\left(\frac{x}{2}\right) $$

---

### 📝 Question 4: Substitution Reducing to Separable
**Solve:** $x^4 \frac{dy}{dx} + x^3y = -\sec(xy)$

**Solution:**
1. **Factor out $x^3$ on the left side:**
   $$ x^3 \left( x\frac{dy}{dx} + y \right) = -\sec(xy) $$
2. **Notice the product rule derivative:** The term $(x\frac{dy}{dx} + y)$ is exactly the derivative of the product $(xy)$. Let's use a substitution.
   *   Let $t = xy$
   *   Differentiate with respect to $x$: $\frac{dt}{dx} = x\frac{dy}{dx} + y(1) = x\frac{dy}{dx} + y$
3. **Substitute $t$ and $dt/dx$ into the equation:**
   $$ x^3 \frac{dt}{dx} = -\sec t $$
4. **Now it is Variable Separable!**
   $$ \frac{1}{\sec t} dt = -\frac{1}{x^3} dx \implies \cos t \, dt = -x^{-3} dx $$
5. **Integrate:**
   $$ \int \cos t \, dt = -\int x^{-3} dx $$
   $$ \sin t = -\left( \frac{x^{-2}}{-2} \right) + C $$
   $$ \sin t = \frac{1}{2x^2} + C $$
6. **Resubstitute $t = xy$ for the final solution:**
   $$ \sin(xy) = \frac{1}{2x^2} + C $$

---

**Next Method:** What happens if the variables *cannot* be cleanly separated? Proceed to [Method 2: Homogeneous Differential Equations](./02-homogeneous-eqs.md) to learn the next technique.