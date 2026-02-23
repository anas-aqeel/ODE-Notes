# 📝 Module 3 Practice: Orthogonal Trajectories

This section contains practice problems for finding the geometric orthogonal trajectories of a given family of curves.

---

### 📝 Question 1: Family of Circles
**Find the orthogonal trajectories of:** $x^2 + y^2 = k$

**Solution:**
1. **Differentiate to find the slope of the given family ($m_1$):**
   $2x + 2y\frac{dy}{dx} = 0$
   $2y\frac{dy}{dx} = -2x \implies \frac{dy}{dx} = -\frac{x}{y}$
   *(Note: The parameter $k$ is already eliminated).*
2. **Apply Orthogonality Condition ($m_2 = -1/m_1$):**
   Replace $\frac{dy}{dx}$ with $-\frac{dx}{dy}$:
   $-\frac{dx}{dy} = -\frac{x}{y}$
3. **Solve the new DE:**
   $\frac{dx}{dy} = \frac{x}{y}$
   Separate variables:
   $\frac{dx}{x} = \frac{dy}{y}$
   Integrate:
   $\int \frac{1}{x} dx = \int \frac{1}{y} dy$
   $\ln|x| = \ln|y| + \ln C$
   $\ln|x| - \ln|y| = \ln C \implies \ln\left(\frac{x}{y}\right) = \ln C$
   $\frac{x}{y} = C \implies x = Cy$
   **Final Answer:** $y = C'x$ (A family of straight lines passing through the origin).

---

### 📝 Question 2: Family of Parabolas
**Find the orthogonal trajectories of:** $y = cx^2$

**Solution:**
1. **Differentiate:**
   $\frac{dy}{dx} = 2cx$
2. **Eliminate parameter $c$:**
   From the original equation, $c = \frac{y}{x^2}$.
   Substitute $c$ into the derivative:
   $\frac{dy}{dx} = 2\left(\frac{y}{x^2}\right)x = \frac{2y}{x}$
3. **Apply Orthogonality Condition:**
   Replace $\frac{dy}{dx}$ with $-\frac{dx}{dy}$:
   $-\frac{dx}{dy} = \frac{2y}{x}$
4. **Solve the new DE:**
   Separate variables:
   $-x \, dx = 2y \, dy$
   Integrate:
   $-\int x \, dx = \int 2y \, dy$
   $-\frac{x^2}{2} = y^2 + K$
   Multiply by 2 to clear fractions:
   $-x^2 = 2y^2 + 2K$
   Rearrange constants:
   **Final Answer:** $x^2 + 2y^2 = C$ (A family of ellipses).

---

### 📝 Question 3: Exponential Curves
**Find the orthogonal trajectories of:** $y = ce^x$

**Solution:**
1. **Differentiate:**
   $\frac{dy}{dx} = ce^x$
2. **Eliminate parameter $c$:**
   Notice that $ce^x$ is exactly equal to $y$. Substitute it directly:
   $\frac{dy}{dx} = y$
3. **Apply Orthogonality Condition:**
   Replace $\frac{dy}{dx}$ with $-\frac{dx}{dy}$:
   $-\frac{dx}{dy} = y$
4. **Solve the new DE:**
   Separate variables:
   $-dx = y \, dy$
   Integrate:
   $-\int dx = \int y \, dy$
   $-x = \frac{y^2}{2} + K$
   Multiply by 2 and rearrange:
   $-2x = y^2 + 2K$
   **Final Answer:** $2x + y^2 = C$ (A family of parabolas opening to the left).