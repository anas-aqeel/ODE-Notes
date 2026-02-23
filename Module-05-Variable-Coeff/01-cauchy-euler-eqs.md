# 🔄 1. Cauchy-Euler Differential Equations

In the previous module, we solved Higher-Order Linear ODEs where the coefficients were constants. Now, we will look at a special type of linear equation where the coefficients are variables—specifically, powers of $x$. 

This specific form is known as the **Cauchy-Euler Equation** (or Cauchy's Differential Equation).

---

## 1. Concept Overview

A Cauchy-Euler equation has a very recognizable signature: **the power of the independent variable $x$ exactly matches the order of the derivative it is multiplied by.**

### The Standard Form
$$ a_n x^n \frac{d^ny}{dx^n} + a_{n-1} x^{n-1} \frac{d^{n-1}y}{dx^{n-1}} + \dots + a_1 x \frac{dy}{dx} + a_0 y = F(x) $$
Where $a_0, a_1, \dots, a_n$ are constants.

Notice that $x^2$ is paired with $\frac{d^2y}{dx^2}$, $x^1$ is paired with $\frac{dy}{dx}$, and so on.

---

## 2. Working Rule (The $x = e^t$ Substitution)

We cannot solve this directly using our constant-coefficient methods. However, we can use a clever substitution to transform the independent variable from $x$ to $t$, which magically turns the variable coefficients into constant coefficients!

**Step 1: The Core Substitution**
Let $x = e^t$. This also means that $t = \ln x$.

**Step 2: Define the New Operator**
Let $D = \frac{d}{dt}$ (Notice the derivative is now with respect to $t$, not $x$).

**Step 3: Transform the Derivatives**
Using the chain rule (proof omitted for brevity), the $x$-derivatives transform into $D$-operators as follows:
*   $x \frac{dy}{dx} = Dy$
*   $x^2 \frac{d^2y}{dx^2} = D(D - 1)y = (D^2 - D)y$
*   $x^3 \frac{d^3y}{dx^3} = D(D - 1)(D - 2)y = (D^3 - 3D^2 + 2D)y$

**Step 4: Substitute and Solve**
Substitute these operators into the original equation. It will now be a standard Higher-Order Linear ODE with constant coefficients. Solve for $y(t) = y_c + y_p$ using the methods from Module 4.

**Step 5: Resubstitute back to $x$**
Once you have the final answer in terms of $t$, replace every $t$ with $\ln x$ and every $e^{kt}$ with $x^k$.

---

## 3. Solved Questions

Here are two comprehensive examples from the lecture notes demonstrating this transformation.

### 📝 Question 1: Algebraic Right-Hand Side
**Solve:** $x^2 \frac{d^2y}{dx^2} + 7x \frac{dy}{dx} + 5y = x^5$

**Solution:**

**Step 1: Apply Transformations**
Let $x = e^t$, $t = \ln x$, and $D = d/dt$.
Substitute the operators into the left side, and $e^t$ into the right side:
$$ [D(D - 1) + 7D + 5]y = (e^t)^5 $$
$$ (D^2 - D + 7D + 5)y = e^{5t} $$
$$ (D^2 + 6D + 5)y = e^{5t} $$
*(This is now a constant-coefficient equation!)*

**Step 2: Find the Complementary Function ($y_c$)**
Auxiliary Equation: $m^2 + 6m + 5 = 0$
Factor: $(m + 5)(m + 1) = 0 \implies m = -1, -5$
$$ y_c = C_1 e^{-t} + C_2 e^{-5t} $$

**Step 3: Find the Particular Integral ($y_p$)**
$$ y_p = \frac{1}{D^2 + 6D + 5} e^{5t} $$
Apply the Exponential Rule ($D \to 5$):
$$ y_p = \frac{1}{5^2 + 6(5) + 5} e^{5t} = \frac{1}{25 + 30 + 5} e^{5t} = \frac{1}{60} e^{5t} $$

**Step 4: Write General Solution in $t$**
$$ y(t) = y_c + y_p = C_1 e^{-t} + C_2 e^{-5t} + \frac{1}{60} e^{5t} $$

**Step 5: Resubstitute back to $x$**
Recall that $e^t = x$, so $e^{-t} = x^{-1}$ and $e^{5t} = x^5$.
$$ y(x) = C_1 x^{-1} + C_2 x^{-5} + \frac{x^5}{60} $$

---

### 📝 Question 2: Trigonometric & Shift Rule Combination
**Solve:** $x^2 \frac{d^2y}{dx^2} - 3x \frac{dy}{dx} + 5y = x^2 \sin(\ln x)$

**Solution:**

**Step 1: Apply Transformations**
Let $x = e^t$, $t = \ln x$, and $D = d/dt$.
Substitute into the equation:
$$ [D(D - 1) - 3D + 5]y = (e^t)^2 \sin(t) $$
$$ (D^2 - D - 3D + 5)y = e^{2t} \sin t $$
$$ (D^2 - 4D + 5)y = e^{2t} \sin t $$

**Step 2: Find the Complementary Function ($y_c$)**
Auxiliary Equation: $m^2 - 4m + 5 = 0$
Use quadratic formula: $m = \frac{4 \pm \sqrt{16 - 20}}{2} = \frac{4 \pm 2i}{2} = 2 \pm i$
Complex roots ($\alpha = 2, \beta = 1$):
$$ y_c = e^{2t} (C_1 \cos t + C_2 \sin t) $$

**Step 3: Find the Particular Integral ($y_p$)**
$$ y_p = \frac{1}{D^2 - 4D + 5} (e^{2t} \sin t) $$
Apply Exponential Shift Rule (Shift $e^{2t}$ to the front, replace $D \to D+2$):
$$ y_p = e^{2t} \frac{1}{(D+2)^2 - 4(D+2) + 5} \sin t $$
$$ y_p = e^{2t} \frac{1}{(D^2 + 4D + 4) - 4D - 8 + 5} \sin t $$
$$ y_p = e^{2t} \frac{1}{D^2 + 1} \sin t $$

**Step 4: Solve Trigonometric part (Case of Failure)**
Apply Trig Rule for $\sin(1t)$ (Replace $D^2 \to -1^2 = -1$):
Denominator becomes $-1 + 1 = 0$. This is a Case of Failure.
Multiply by $t$ (our new independent variable) and differentiate denominator ($2D$):
$$ y_p = e^{2t} \cdot t \cdot \frac{1}{2D} \sin t $$
The operator $\frac{1}{D}$ means integrate with respect to $t$:
$$ y_p = \frac{t e^{2t}}{2} \int \sin t \, dt = \frac{t e^{2t}}{2} (-\cos t) $$
$$ y_p = -\frac{t}{2} e^{2t} \cos t $$

**Step 5: Write General Solution in $t$**
$$ y(t) = e^{2t}(C_1 \cos t + C_2 \sin t) - \frac{t}{2} e^{2t} \cos t $$

**Step 6: Resubstitute back to $x$**
Substitute $t = \ln x$ and $e^{2t} = x^2$:
$$ y(x) = x^2 [C_1 \cos(\ln x) + C_2 \sin(\ln x)] - \frac{1}{2}(\ln x) x^2 \cos(\ln x) $$

---

**Next Steps:** Practice these transformations with the [Module 5 Practice Questions](./02-practice-questions.md).