# 🔍 1. Finding the Complementary Function ($y_c$)

When solving higher-order linear differential equations of the form $f(D)y = F(x)$, the general solution is always composed of two parts:
$$ y = y_c + y_p $$

The **Complementary Function ($y_c$)** represents the solution to the **homogeneous** version of the equation (where the right side is zero). This is the first step in solving *any* linear ODE with constant coefficients.

---

## 1. The Operator 'D'

To simplify writing derivatives, we use the differential operator $D$:
*   $Dy = \frac{dy}{dx}$
*   $D^2y = \frac{d^2y}{dx^2}$
*   $D^ny = \frac{d^ny}{dx^n}$

An equation like $\frac{d^2y}{dx^2} + 5\frac{dy}{dx} + 6y = 0$ can be written as:
$$ (D^2 + 5D + 6)y = 0 $$

---

## 2. The Auxiliary Equation (A.E.)

To find $y_c$, we assume a solution of the form $y = e^{mx}$. Substituting this into the homogeneous equation gives us the **Auxiliary Equation** (or Characteristic Equation).

Simply replace $D$ with $m$ and set the equation to zero:
$$ f(m) = 0 $$

We then solve for the roots of $m$. The nature of these roots determines the form of $y_c$.

---

## 3. Cases for Roots and Forms of $y_c$

### Case 1: Real and Distinct Roots
If the roots $m_1, m_2, \dots$ are real and different:
$$ y_c = C_1 e^{m_1 x} + C_2 e^{m_2 x} + \dots $$

### Case 2: Real and Repeated Roots
If a root $m$ is repeated $k$ times (e.g., $m, m, m$):
$$ y_c = (C_1 + C_2 x + C_3 x^2 + \dots + C_k x^{k-1}) e^{mx} $$

### Case 3: Complex Conjugate Roots
If the roots are complex ($\alpha \pm i\beta$):
$$ y_c = e^{\alpha x} (C_1 \cos \beta x + C_2 \sin \beta x) $$

---

## 4. Advanced: Finding Roots using Synthetic Division

When the auxiliary equation is a 3rd-degree or 4th-degree polynomial that cannot be easily factored, we use **Synthetic Division** to find the roots by trial and error.

### 📝 Example: 4th-Order Equation
**Find $y_c$ for:** $(D^4 + 6D^3 + 5D^2 - 24D - 36)y = 0$

**Solution:**
1. **Auxiliary Equation:**
   $m^4 + 6m^3 + 5m^2 - 24m - 36 = 0$
2. **First Root by Trial & Error:**
   Test small integers ($1, -1, 2, -2$). Let's test $m = -2$:
   $(-2)^4 + 6(-2)^3 + 5(-2)^2 - 24(-2) - 36 = 16 - 48 + 20 + 48 - 36 = 0$.
   Since the result is 0, **$m = -2$ is a root**.
3. **Synthetic Division (First Pass):**
   ```text
      -2 |  1   6   5  -24  -36
         |     -2  -8    6   36
         -----------------------
            1   4  -3  -18    0  (Remainder is 0)
   ```
   The reduced cubic equation is: $m^3 + 4m^2 - 3m - 18 = 0$
4. **Second Root by Trial & Error:**
   Test $m = -2$ again on the new cubic equation:
   $(-2)^3 + 4(-2)^2 - 3(-2) - 18 = -8 + 16 + 6 - 18 = -4 \neq 0$. (Not a root).
   Test $m = 2$:
   $(2)^3 + 4(2)^2 - 3(2) - 18 = 8 + 16 - 6 - 18 = 0$. **$m = 2$ is a root.**
5. **Synthetic Division (Second Pass):**
   ```text
       2 |  1   4  -3  -18
         |      2  12   18
         ------------------
            1   6   9    0
   ```
   The reduced quadratic equation is: $m^2 + 6m + 9 = 0$
6. **Solve the Quadratic:**
   $m^2 + 6m + 9 = 0 \implies (m+3)^2 = 0 \implies m = -3, -3$
7. **Final Roots and $y_c$:**
   The four roots are: $m = -2, 2, -3, -3$.
   Since -3 is repeated, the Complementary Function is:
   $$ y_c = C_1 e^{-2x} + C_2 e^{2x} + (C_3 + C_4 x)e^{-3x} $$

## 5. Solved Questions

Here are examples from the lecture notes demonstrating how to find $y_c$ for different types of roots.

### 📝 Question 1: Real & Distinct Roots
**Find $y_c$ for:** $y'' + 6y' + 5y = 0$

**Solution:**

1.  **Write in Operator Form:**
    $(D^2 + 6D + 5)y = 0$
2.  **Auxiliary Equation:**
    $m^2 + 6m + 5 = 0$
3.  **Solve for Roots:**
    Factor the quadratic:
    $(m+5)(m+1) = 0$
    Roots: $m_1 = -1, m_2 = -5$
4.  **Write $y_c$:**
    Since roots are real and distinct:
    $$ y_c = C_1 e^{-x} + C_2 e^{-5x} $$

---

### 📝 Question 2: Real & Repeated Roots
**Find $y_c$ for:** $y''' + 3y'' + 3y' + y = 0$

**Solution:**

1.  **Write in Operator Form:**
    $(D^3 + 3D^2 + 3D + 1)y = 0$
2.  **Auxiliary Equation:**
    $m^3 + 3m^2 + 3m + 1 = 0$
3.  **Solve for Roots:**
    Recognize this as the binomial expansion of $(m+1)^3$:
    $(m+1)^3 = 0$
    Roots: $m = -1, -1, -1$ (Repeated 3 times)
4.  **Write $y_c$:**
    Since the root $-1$ repeats 3 times, we multiply the constants by increasing powers of $x$:
    $$ y_c = (C_1 + C_2 x + C_3 x^2) e^{-x} $$

---

### 📝 Question 3: Complex Roots
**Find $y_c$ for:** $y'''' + 4y = 0$

**Solution:**

1.  **Write in Operator Form:**
    $(D^4 + 4)y = 0$
2.  **Auxiliary Equation:**
    $m^4 + 4 = 0 \implies m^4 = -4$
    $m^2 = \pm 2i$
    $m = \pm \sqrt{2i}$
    
    *Alternative Method (Factorization):*
    $m^4 + 4 = (m^2 + 2)^2 - 4m^2 = (m^2 + 2 - 2m)(m^2 + 2 + 2m) = 0$
    
    Solve $m^2 - 2m + 2 = 0$ using quadratic formula:
    $m = \frac{2 \pm \sqrt{4 - 8}}{2} = \frac{2 \pm 2i}{2} = 1 \pm i$
    
    Solve $m^2 + 2m + 2 = 0$:
    $m = \frac{-2 \pm \sqrt{4 - 8}}{2} = -1 \pm i$
    
    Roots: $1 \pm i$ and $-1 \pm i$
    ($\alpha = 1, \beta = 1$) and ($\alpha = -1, \beta = 1$)
3.  **Write $y_c$:**
    Combine the solutions for both pairs of conjugate roots:
    $$ y_c = e^x(C_1 \cos x + C_2 \sin x) + e^{-x}(C_3 \cos x + C_4 \sin x) $$

---

**Next Step:** Once $y_c$ is found, we must find the Particular Integral ($y_p$) based on the function on the right side of the equation. Proceed to [Topic 2: Particular Integral - Exponential Case](./02-yp-exponential.md).