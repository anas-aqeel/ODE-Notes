# 📉 5. Bernoulli's Equations (Reducible to Linear)

Bernoulli's equations are a specific class of **non-linear** differential equations that can be easily transformed into a standard **Linear** differential equation using a clever substitution. This method is the final standard technique for first-order ODEs.

---

## 1. Concept Overview

A Bernoulli differential equation has the form:
$$ \frac{dy}{dx} + P(x)y = Q(x)y^n $$

Where $n$ is any real number except $0$ or $1$.
*   If $n=0$, the equation is Linear.
*   If $n=1$, the equation is Variable Separable.
*   For any other $n$, the term $y^n$ on the right side makes the equation **non-linear**.

---

## 2. Working Rule (Reduction to Linear Form)

To solve a Bernoulli equation, we must "linearize" it.

**Step 1: Divide by the non-linear term**
Divide the entire equation by $y^n$ to move the $y$ terms to the left side:
$$ y^{-n}\frac{dy}{dx} + P(x)y^{1-n} = Q(x) $$

**Step 2: Substitute**
Let $z = y^{1-n}$ (the term attached to $P(x)$).

**Step 3: Differentiate**
Differentiate $z$ with respect to $x$:
$$ \frac{dz}{dx} = (1-n)y^{-n}\frac{dy}{dx} $$
Rearrange this to match the first term of your divided equation:
$$ \frac{1}{1-n}\frac{dz}{dx} = y^{-n}\frac{dy}{dx} $$

**Step 4: Transform into Linear DE**
Substitute $z$ and $\frac{dz}{dx}$ back into the equation. It will now be a standard Linear DE in terms of $z$ and $x$:
$$ \frac{dz}{dx} + (1-n)P(x)z = (1-n)Q(x) $$

**Step 5: Solve and Resubstitute**
Solve this new linear equation for $z$ using the Integrating Factor method (see [Topic 4](./04-linear-odes.md)). Finally, replace $z$ with $y^{1-n}$ to get the general solution.

---

## 3. Solved Questions

Here are two step-by-step examples from the lecture notes.

### 📝 Question 1: Rational Powers
**Solve:** $\frac{dy}{dx} + \frac{y}{x} = \frac{y^2}{x^2}$

**Solution:**

**Step 1: Identify Form**
This matches Bernoulli's form with $P(x) = 1/x$, $Q(x) = 1/x^2$, and $n=2$.

**Step 2: Divide by $y^n$ ($y^2$)**
$$ y^{-2}\frac{dy}{dx} + \frac{1}{x}y^{-1} = \frac{1}{x^2} $$

**Step 3: Substitute**
Let $z = y^{1-2} = y^{-1}$.
Differentiate: $\frac{dz}{dx} = -1 \cdot y^{-2} \frac{dy}{dx} \implies -\frac{dz}{dx} = y^{-2}\frac{dy}{dx}$.

**Step 4: Transform**
Substitute into the equation:
$$ -\frac{dz}{dx} + \frac{1}{x}z = \frac{1}{x^2} $$
Multiply by $-1$ to standardize:
$$ \frac{dz}{dx} - \frac{1}{x}z = -\frac{1}{x^2} $$

**Step 5: Solve Linear DE**
*   **I.F.:** $e^{\int -\frac{1}{x} dx} = e^{-\ln x} = \frac{1}{x}$
*   **Solution Formula:**
    $$ z \cdot \left(\frac{1}{x}\right) = \int \left[ -\frac{1}{x^2} \cdot \frac{1}{x} \right] dx + C $$
    $$ \frac{z}{x} = -\int x^{-3} dx + C $$
    $$ \frac{z}{x} = -\left( \frac{x^{-2}}{-2} \right) + C = \frac{1}{2x^2} + C $$

**Step 6: Resubstitute ($z=1/y$)**
$$ \frac{1}{xy} = \frac{1}{2x^2} + C $$

---

### 📝 Question 2: Cubic Power
**Solve:** $\frac{dy}{dx} + 4xy = xy^3$

**Solution:**

**Step 1: Identify Form**
This is Bernoulli's form with $n=3$.

**Step 2: Divide by $y^3$**
$$ y^{-3}\frac{dy}{dx} + 4xy^{-2} = x $$

**Step 3: Substitute**
Let $z = y^{1-3} = y^{-2}$.
Differentiate: $\frac{dz}{dx} = -2y^{-3}\frac{dy}{dx} \implies -\frac{1}{2}\frac{dz}{dx} = y^{-3}\frac{dy}{dx}$.

**Step 4: Transform**
Substitute into the equation:
$$ -\frac{1}{2}\frac{dz}{dx} + 4xz = x $$
Multiply by $-2$ to standardize:
$$ \frac{dz}{dx} - 8xz = -2x $$

**Step 5: Solve Linear DE**
*   **Identify P(x):** $P(x) = -8x$
*   **I.F.:** $e^{\int -8x dx} = e^{-4x^2}$
*   **Solution Formula:**
    $$ z \cdot e^{-4x^2} = \int (-2x)e^{-4x^2} dx + C $$

**Step 6: Integrate**
To solve $\int -2x e^{-4x^2} dx$, use substitution $u = -4x^2 \implies du = -8x dx \implies \frac{1}{4}du = -2x dx$.
$$ \text{Right Side} = \int e^u (\frac{1}{4} du) = \frac{1}{4}e^u = \frac{1}{4}e^{-4x^2} $$
So the equation becomes:
$$ z e^{-4x^2} = \frac{1}{4}e^{-4x^2} + C $$

**Step 7: Resubstitute ($z=y^{-2}$)**
$$ y^{-2} e^{-4x^2} = \frac{1}{4}e^{-4x^2} + C $$
Multiply by $e^{4x^2}$:
$$ \frac{1}{y^2} = \frac{1}{4} + Ce^{4x^2} $$

---

**Next Steps:** Test your mastery of all five first-order methods with the [Module 2 Practice Questions](./06-practice-questions.md).