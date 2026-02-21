# 📏 4. Linear Differential Equations

Linear Differential Equations are among the most important types of ODEs because they appear frequently in physics and engineering (e.g., circuits, mixing problems, cooling laws). Unlike previous methods where we manipulated variables, here we follow a strict algorithmic formula.

---

## 1. Concept Overview

A first-order differential equation is **Linear** if:
1.  The dependent variable ($y$) and its derivative ($\frac{dy}{dx}$) occur only in the **first degree** (power is 1).
2.  There are **no products** of the dependent variable and its derivative (e.g., no $y \cdot \frac{dy}{dx}$ terms).
3.  There are no transcendental functions of $y$ (like $\sin y$, $e^y$, $\ln y$).

### The Standard Form
A linear differential equation in $y$ is written as:
$$ \frac{dy}{dx} + P(x)y = Q(x) $$

Where $P(x)$ and $Q(x)$ are functions of $x$ alone (or constants).

---

## 2. Working Rule (Integrating Factor Method)

To solve a linear equation, we use an **Integrating Factor (I.F.)**, which transforms the left side of the equation into a perfect product derivative.

**Step 1: Standardize**
Ensure the coefficient of $\frac{dy}{dx}$ is **1**. If there is a term multiplied by $\frac{dy}{dx}$, divide the entire equation by that term.

**Step 2: Identify P and Q**
Compare your equation to the standard form and identify $P(x)$ and $Q(x)$.

**Step 3: Find the Integrating Factor (I.F.)**
Calculate the exponential integral of $P(x)$:
$$ I.F. = e^{\int P(x) dx} $$

**Step 4: Write the General Solution**
The solution is given by the formula:
$$ y \cdot (I.F.) = \int [Q(x) \cdot (I.F.)] dx + C $$

**Step 5: Evaluate the Integral**
Solve the integral on the right-hand side to find the final answer.

---

## 3. Solved Questions

Here are two step-by-step examples from the lecture notes.

### 📝 Question 1: Algebraic P(x)
**Solve:** $(x-1)^3 \frac{dy}{dx} + 4(x-1)^2 y = x+1$

**Solution:**

**Step 1: Standardize**
The coefficient of $\frac{dy}{dx}$ is $(x-1)^3$. We must divide the entire equation by $(x-1)^3$ to isolate $\frac{dy}{dx}$.
$$ \frac{dy}{dx} + \frac{4(x-1)^2}{(x-1)^3} y = \frac{x+1}{(x-1)^3} $$
$$ \frac{dy}{dx} + \frac{4}{x-1} y = \frac{x+1}{(x-1)^3} $$

**Step 2: Identify P and Q**
Comparing to $\frac{dy}{dx} + Py = Q$:
*   $P(x) = \frac{4}{x-1}$
*   $Q(x) = \frac{x+1}{(x-1)^3}$

**Step 3: Calculate I.F.**
$$ I.F. = e^{\int \frac{4}{x-1} dx} = e^{4 \ln(x-1)} $$
Using logarithm laws ($a \ln b = \ln b^a$):
$$ I.F. = e^{\ln((x-1)^4)} = (x-1)^4 $$

**Step 4: Apply General Solution Formula**
$$ y \cdot (x-1)^4 = \int \left[ \frac{x+1}{(x-1)^3} \cdot (x-1)^4 \right] dx + C $$

**Step 5: Integrate**
Simplify the term inside the integral:
$$ y(x-1)^4 = \int (x+1)(x-1) dx + C $$
Using difference of squares $(a+b)(a-b) = a^2 - b^2$:
$$ y(x-1)^4 = \int (x^2 - 1) dx + C $$
$$ y(x-1)^4 = \frac{x^3}{3} - x + C $$

---

### 📝 Question 2: Trigonometric P(x)
**Solve:** $\frac{dy}{dx} + y \tan x = \cos^2 x$

**Solution:**

**Step 1: Standardize**
The coefficient of $\frac{dy}{dx}$ is already 1. No division needed.

**Step 2: Identify P and Q**
*   $P(x) = \tan x$
*   $Q(x) = \cos^2 x$

**Step 3: Calculate I.F.**
$$ I.F. = e^{\int \tan x dx} $$
Recall standard integral: $\int \tan x dx = \ln|\sec x|$.
$$ I.F. = e^{\ln(\sec x)} = \sec x $$

**Step 4: Apply General Solution Formula**
$$ y \cdot (\sec x) = \int [\cos^2 x \cdot \sec x] dx + C $$

**Step 5: Integrate**
Simplify the term inside the integral (since $\sec x = 1/\cos x$):
$$ y \sec x = \int \left(\cos^2 x \cdot \frac{1}{\cos x}\right) dx + C $$
$$ y \sec x = \int \cos x dx + C $$
$$ y \sec x = \sin x + C $$

**Final Answer:**
You can leave it as is, or multiply by $\cos x$:
$$ y = \sin x \cos x + C \cos x $$

---

**Next Method:** Sometimes an equation is *almost* linear but has a pesky $y^n$ term on the right side. This is called a **Bernoulli Equation**. Proceed to [Method 5: Bernoulli's Equations](./05-bernoulli-eqs.md).