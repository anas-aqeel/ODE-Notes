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

## 4. Solved Questions

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