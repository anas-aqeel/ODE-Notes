# 📉 3. Equations Reducible to Homogeneous Form

Sometimes, a differential equation looks almost homogeneous but contains constant terms that break the symmetry. These equations usually describe the intersection of non-homogeneous lines. We can "reduce" them to a homogeneous form (or directly to variable separable form) using specific substitutions.

---

## 1. Concept Overview

This method applies to differential equations of the form:
$$ \frac{dy}{dx} = \frac{ax + by + c}{Ax + By + C} $$

Here, the constants $c$ and $C$ prevent the equation from being homogeneous. To solve this, we compare the ratios of the coefficients of $x$ and $y$.

There are two distinct cases:

### 🔍 Case 1: Intersecting Lines ($\frac{a}{A} \neq \frac{b}{B}$)
If the ratios are **not equal**, the lines represented by the numerator and denominator intersect at a specific point $(h, k)$.
*   **Substitution:** We shift the origin to that intersection point.
    *   $x = X + h$
    *   $y = Y + k$
    *   $dy = dY, dx = dX$
*   We find $h$ and $k$ by solving the system of equations $ax+by+c=0$ and $Ax+By+C=0$.
*   This removes the constants $c$ and $C$, resulting in a standard Homogeneous DE in variables $X$ and $Y$.

### 🔍 Case 2: Parallel Lines ($\frac{a}{A} = \frac{b}{B}$)
If the ratios **are equal**, the lines are parallel. This means the terms $(ax+by)$ and $(Ax+By)$ are scalar multiples of each other.
*   **Substitution:** We substitute the common linear expression with a new variable $z$.
    *   Let $z = ax + by$
    *   Differentiate with respect to $x$ to find $\frac{dz}{dx}$.
*   This immediately reduces the DE to a **Variable Separable** form.

---

## 2. Solved Questions

Here is a step-by-step solution for a **Case 2** problem found in the lecture notes.

### 📝 Question 1 (Case 2: Equal Ratios)
**Solve:** $(x + 2y)(dx - dy) = dx + dy$

**Solution:**

**Step 1: Rewrite in Standard Form**
First, rearrange the equation to isolate $\frac{dy}{dx}$.
Expand the terms:
$$ x\,dx - x\,dy + 2y\,dx - 2y\,dy = dx + dy $$
Group $dx$ and $dy$ terms:
$$ (x + 2y)\,dx - dx = (x + 2y)\,dy + dy $$
$$ (x + 2y - 1)\,dx = (x + 2y + 1)\,dy $$
$$ \frac{dy}{dx} = \frac{x + 2y - 1}{x + 2y + 1} $$

**Step 2: Check Ratios**
Compare coefficients of $x$ and $y$ in the numerator ($a=1, b=2$) and denominator ($A=1, B=2$).
$$ \frac{a}{A} = \frac{1}{1} = 1, \quad \frac{b}{B} = \frac{2}{2} = 1 $$
Since $\frac{a}{A} = \frac{b}{B}$, this is **Case 2**.

**Step 3: Apply Substitution**
Let the common term be $z$.
$$ z = x + 2y $$
Differentiate with respect to $x$:
$$ \frac{dz}{dx} = 1 + 2\frac{dy}{dx} \implies \frac{dy}{dx} = \frac{1}{2}\left(\frac{dz}{dx} - 1\right) $$

**Step 4: Substitute into the DE**
Replace $\frac{dy}{dx}$ and $(x+2y)$ in the standard form equation:
$$ \frac{1}{2}\left(\frac{dz}{dx} - 1\right) = \frac{z - 1}{z + 1} $$
Multiply by 2:
$$ \frac{dz}{dx} - 1 = \frac{2(z - 1)}{z + 1} = \frac{2z - 2}{z + 1} $$
Add 1 to both sides:
$$ \frac{dz}{dx} = \frac{2z - 2}{z + 1} + 1 $$
Find common denominator:
$$ \frac{dz}{dx} = \frac{2z - 2 + (z + 1)}{z + 1} = \frac{3z - 1}{z + 1} $$

**Step 5: Separate Variables and Integrate**
$$ \frac{z + 1}{3z - 1} dz = dx $$
Integrate both sides:
$$ \int \frac{z + 1}{3z - 1} dz = \int dx $$

*Integration Tip:* To integrate the left side, make the numerator resemble the derivative of the denominator or perform long division.
Multiply and divide by 3 inside the integral for easier manipulation:
$$ \frac{1}{3} \int \frac{3z + 3}{3z - 1} dz = x + C $$
$$ \frac{1}{3} \int \frac{(3z - 1) + 4}{3z - 1} dz = x + C $$
$$ \frac{1}{3} \int \left( 1 + \frac{4}{3z - 1} \right) dz = x + C $$
$$ \frac{1}{3} \left[ z + 4 \cdot \frac{\ln|3z - 1|}{3} \right] = x + C $$

**Step 6: Final Substitution**
Multiply by 3 to clear the fraction:
$$ z + \frac{4}{3}\ln|3z - 1| = 3x + 3C $$
Substitute $z = x + 2y$ back:
$$ (x + 2y) + \frac{4}{3}\ln|3(x + 2y) - 1| = 3x + C' $$
Rearrange for the final implicit solution:
$$ 2y - 2x + \frac{4}{3}\ln|3x + 6y - 1| = C' $$

---

**Next Method:** While Homogeneous and Reducible methods deal with ratios, many physical systems are modeled by **Linear Differential Equations**. Proceed to [Method 4: Linear ODEs](./04-linear-odes.md).