# 📈 2. Particular Integral ($y_p$): Exponential Case

After finding the Complementary Function ($y_c$), the next step is to find the **Particular Integral ($y_p$)**. This part of the solution depends entirely on the function $F(x)$ on the right-hand side of the differential equation.

This file covers **Method 1**, which is used when $F(x)$ is an exponential function of the form $e^{ax}$.

---

## 1. The Method

Given a differential equation $f(D)y = e^{ax}$:

The Particular Integral is written as:
$$ y_p = \frac{1}{f(D)} e^{ax} $$

### 1.1 The Rule ($D \to a$)
To solve this, simply replace the differential operator $D$ with the coefficient $a$ from the exponent.

$$ y_p = \frac{1}{f(a)} e^{ax}, \quad \text{provided } f(a) \neq 0 $$

---

## 2. The Case of Failure ($f(a) = 0$)

If replacing $D$ with $a$ results in a zero in the denominator ($f(a) = 0$), the method fails. To fix this, we apply the following rule:

1.  Multiply the numerator by $x$.
2.  Differentiate the denominator with respect to $D$ ($f'(D)$).
3.  Try substituting $D = a$ again.

$$ y_p = x \cdot \frac{1}{f'(D)} e^{ax} $$

If the denominator is still zero, repeat the process (multiply by $x$ again to get $x^2$, and differentiate the denominator again to get $f''(D)$).

---

## 3. Solved Questions

Here are step-by-step examples from the lecture notes, covering both the standard case and the case of failure.

### 📝 Question 1: Standard Case & Constants
**Solve for $y_p$:** $(D^2 - 6D + 9)y = 6e^{3x} + 7e^{-2x} - \ln 2$

**Solution:**
We can split this into three separate parts for linearity:
$$ y_p = y_{p1} + y_{p2} + y_{p3} $$
$$ y_p = \frac{1}{(D-3)^2} (6e^{3x}) + \frac{1}{(D-3)^2} (7e^{-2x}) - \frac{1}{(D-3)^2} (\ln 2) $$

**Part 1: $6e^{3x}$ ($a=3$)**
Substitute $D=3$ into $(D-3)^2$:
$(3-3)^2 = 0$. **Case of Failure!**
*   Multiply by $x$, differentiate denominator $2(D-3)$:
    $$ x \cdot \frac{1}{2(D-3)} 6e^{3x} $$
*   Substitute $D=3$ again: $2(3-3) = 0$. **Failure again!**
*   Multiply by $x$ again ($x^2$), differentiate denominator again ($2$):
    $$ x^2 \cdot \frac{1}{2} 6e^{3x} = 3x^2 e^{3x} $$

**Part 2: $7e^{-2x}$ ($a=-2$)**
Substitute $D=-2$:
$$ \frac{1}{(-2-3)^2} 7e^{-2x} = \frac{1}{(-5)^2} 7e^{-2x} = \frac{7}{25} e^{-2x} $$

**Part 3: Constant Term $\ln 2$ ($a=0$)**
A constant can be written as $(\ln 2) \cdot e^{0x}$. Here, $a=0$.
Substitute $D=0$:
$$ \frac{1}{(0-3)^2} (\ln 2) = \frac{1}{9} \ln 2 $$

**Total $y_p$:**
$$ y_p = 3x^2 e^{3x} + \frac{7}{25} e^{-2x} - \frac{\ln 2}{9} $$

---

### 📝 Question 2: Higher Order Failure
**Solve for $y_p$:** $(D^3 - 3D^2 + 3D - 1)y = e^x$

**Solution:**
1.  **Identify Form:**
    The operator $(D^3 - 3D^2 + 3D - 1)$ is the expansion of $(D-1)^3$.
    $$ y_p = \frac{1}{(D-1)^3} e^x $$
2.  **Apply Rule ($D \to 1$):**
    Substitute $D=1$: $(1-1)^3 = 0$. **Case of Failure.**
3.  **Fix 1:** Multiply by $x$, differentiate denominator ($3(D-1)^2$).
    $$ x \cdot \frac{1}{3(D-1)^2} e^x $$
    Substitute $D=1$: Still 0.
4.  **Fix 2:** Multiply by $x$ again ($x^2$), differentiate denominator ($6(D-1)$).
    $$ x^2 \cdot \frac{1}{6(D-1)} e^x $$
    Substitute $D=1$: Still 0.
5.  **Fix 3:** Multiply by $x$ again ($x^3$), differentiate denominator ($6$).
    $$ x^3 \cdot \frac{1}{6} e^x $$
    Now the denominator is constant (6), which is not zero.
    
**Final Answer:**
$$ y_p = \frac{x^3 e^x}{6} $$

---

**Next Method:** What if $F(x)$ is not exponential, but a polynomial like $x^2$ or $x^3$? Proceed to [Method 2: Algebraic Case](./03-yp-algebraic.md).