# 📐 Orthogonal Trajectories

In geometry and physics, we often deal with families of curves that interact with each other. One of the most common interactions is when two families of curves intersect each other at right angles ($90^\circ$). These are called **Orthogonal Trajectories**.

Common examples include:
*   **Electric Fields:** Equipotential lines and electric field lines are orthogonal trajectories of each other.
*   **Heat Flow:** Isotherms (lines of constant temperature) and lines of heat flow are orthogonal.

---

## 1. Concept Overview

> **Definition:** An **Orthogonal Trajectory** is a curve that intersects every curve of a given family at right angles.

If we have a family of curves represented by $F(x,y,c) = 0$, its "slope" at any point is given by the derivative $\frac{dy}{dx}$ (let's call this slope $m_1$).

For a second curve to be perpendicular (orthogonal) to the first, its slope ($m_2$) must be the **negative reciprocal** of $m_1$:
$$ m_1 \cdot m_2 = -1 \implies m_2 = -\frac{1}{m_1} $$

Therefore, the differential equation for the orthogonal trajectory is found by replacing $\frac{dy}{dx}$ with $-\frac{dx}{dy}$.

---

## 2. Working Rule (Step-by-Step)

To find the orthogonal trajectories of a given family of curves:

1.  **Find the Differential Equation:** Differentiate the given equation of the family of curves with respect to $x$ to find $\frac{dy}{dx}$.
2.  **Eliminate the Parameter:** If the derivative still contains the arbitrary constant (parameter $C$ or $k$), use the original equation to substitute it out. The differential equation must only contain $x, y, \frac{dy}{dx}$.
3.  **Apply Orthogonality Condition:** Replace $\frac{dy}{dx}$ with $-\frac{dx}{dy}$ in the differential equation.
    $$ \frac{dy}{dx} \longrightarrow -\frac{dx}{dy} $$
4.  **Solve the New Equation:** Solve this new differential equation (usually by Variable Separation) to find the family of orthogonal trajectories.

---

## 3. Solved Questions

Here are two examples from the lecture notes illustrating this process.

### 📝 Question 1: Hyperbolas
**Find the orthogonal trajectories of the family of curves:**
$$ x^2 - y^2 = C $$
*(This represents a family of rectangular hyperbolas).*

**Solution:**

**Step 1: Differentiate the Given Equation**
Differentiate with respect to $x$:
$$ 2x - 2y\frac{dy}{dx} = 0 $$
$$ 2y\frac{dy}{dx} = 2x $$
$$ \frac{dy}{dx} = \frac{x}{y} $$
*(Note: The constant $C$ disappeared automatically upon differentiation).*

**Step 2: Apply Orthogonality Condition**
To find the orthogonal path, replace $\frac{dy}{dx}$ with $-\frac{dx}{dy}$:
$$ -\frac{dx}{dy} = \frac{x}{y} $$

**Step 3: Solve the New Differential Equation**
Separate the variables:
$$ -\frac{dx}{x} = \frac{dy}{y} $$
Integrate both sides:
$$ -\int \frac{1}{x} dx = \int \frac{1}{y} dy $$
$$ -\ln|x| = \ln|y| + \ln K $$
*(Using $\ln K$ as the integration constant for easier simplification).*

**Step 4: Simplify**
$$ \ln|y| + \ln|x| = -\ln K $$
$$ \ln|xy| = C' $$
$$ xy = \text{Constant} $$

**Result:** The orthogonal trajectories of the hyperbolas $x^2 - y^2 = C$ are the hyperbolas $xy = K$.

---

### 📝 Question 2: Parabolas
**Find the orthogonal trajectories of the family of curves:**
$$ y = (x - k)^2 $$
*(This represents a family of parabolas shifted along the x-axis).*

**Solution:**

**Step 1: Differentiate the Given Equation**
Differentiate with respect to $x$:
$$ \frac{dy}{dx} = 2(x - k) $$

**Step 2: Eliminate the Parameter ($k$)**
Our derivative depends on $k$, which is not allowed in the final DE.
From the original equation $y = (x - k)^2$, we can say:
$$ x - k = \sqrt{y} $$
Substitute this back into the derivative:
$$ \frac{dy}{dx} = 2\sqrt{y} $$

**Step 3: Apply Orthogonality Condition**
Replace $\frac{dy}{dx}$ with $-\frac{dx}{dy}$:
$$ -\frac{dx}{dy} = 2\sqrt{y} $$

**Step 4: Solve the New Differential Equation**
Rearrange to separate variables:
$$ dx = -2\sqrt{y} \, dy $$
Integrate both sides:
$$ \int dx = -2 \int y^{1/2} \, dy $$
$$ x = -2 \left( \frac{y^{3/2}}{3/2} \right) + C $$
$$ x = -2 \left( \frac{2}{3} y^{3/2} \right) + C $$
$$ x = -\frac{4}{3} y^{3/2} + C $$

**Result:** The orthogonal trajectories are the family of semi-cubical parabolas given by $3x + 4y^{3/2} = C'$.

---

**Next Steps:** Practice finding orthogonal trajectories with the [Module 3 Practice Questions](./02-practice-questions.md).