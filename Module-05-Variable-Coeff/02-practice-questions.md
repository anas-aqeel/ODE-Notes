# 📝 Module 5 Practice: Cauchy-Euler Equations

This section contains all the comprehensive homework and practice problems for variable-coefficient linear differential equations (Cauchy-Euler equations). 

**Core Substitution Rule Reminder:**
Let $x = e^t$, which means $t = \ln x$.
Let $D = \frac{d}{dt}$.
Transformations:
*   $x\frac{dy}{dx} = Dy$
*   $x^2\frac{d^2y}{dx^2} = D(D-1)y = (D^2 - D)y$
*   $x^3\frac{d^3y}{dx^3} = D(D-1)(D-2)y = (D^3 - 3D^2 + 2D)y$
*   $x^4\frac{d^4y}{dx^4} = D(D-1)(D-2)(D-3)y = (D^4 - 6D^3 + 11D^2 - 6D)y$

---

### 📝 Question 1 (From Whiteboard Q1)
**Solve:** $x^2 \frac{d^2y}{dx^2} - 2x \frac{dy}{dx} - 4y = x^2$

**Solution:**
1. **Apply Transformations:**
   Substitute $x^2\frac{d^2y}{dx^2} = (D^2 - D)y$, $x\frac{dy}{dx} = Dy$, and $x^2 = (e^t)^2 = e^{2t}$.
   $$ (D^2 - D)y - 2Dy - 4y = e^{2t} $$
   $$ (D^2 - 3D - 4)y = e^{2t} $$
2. **Find Complementary Function ($y_c$):**
   Auxiliary Equation: $m^2 - 3m - 4 = 0$
   Factorizing: $(m - 4)(m + 1) = 0 \implies m = 4, -1$
   $$ y_c(t) = C_1e^{4t} + C_2e^{-t} $$
3. **Find Particular Integral ($y_p$):**
   $$ y_p(t) = \frac{1}{D^2 - 3D - 4} e^{2t} $$
   Substitute $D = 2$:
   $$ y_p(t) = \frac{1}{(2)^2 - 3(2) - 4} e^{2t} = \frac{1}{4 - 6 - 4} e^{2t} = -\frac{1}{6}e^{2t} $$
4. **General Solution in terms of $t$:**
   $$ y(t) = C_1e^{4t} + C_2e^{-t} - \frac{1}{6}e^{2t} $$
5. **Resubstitute back to $x$ ($e^t = x$):**
   $$ y(x) = C_1x^4 + C_2x^{-1} - \frac{1}{6}x^2 $$

---

### 📝 Question 2 (From Whiteboard Q2)
**Solve:** $x^2 \frac{d^2y}{dx^2} - 2x \frac{dy}{dx} + 2y = x^3$

**Solution:**
1. **Apply Transformations:**
   $$ (D^2 - D)y - 2Dy + 2y = (e^t)^3 $$
   $$ (D^2 - 3D + 2)y = e^{3t} $$
2. **Find Complementary Function ($y_c$):**
   Auxiliary Equation: $m^2 - 3m + 2 = 0$
   Factorizing: $(m - 1)(m - 2) = 0 \implies m = 1, 2$
   $$ y_c(t) = C_1e^t + C_2e^{2t} $$
3. **Find Particular Integral ($y_p$):**
   $$ y_p(t) = \frac{1}{D^2 - 3D + 2} e^{3t} $$
   Substitute $D = 3$:
   $$ y_p(t) = \frac{1}{(3)^2 - 3(3) + 2} e^{3t} = \frac{1}{9 - 9 + 2} e^{3t} = \frac{1}{2}e^{3t} $$
4. **General Solution in terms of $t$:**
   $$ y(t) = C_1e^t + C_2e^{2t} + \frac{1}{2}e^{3t} $$
5. **Resubstitute back to $x$ ($e^t = x$):**
   $$ y(x) = C_1x + C_2x^2 + \frac{1}{2}x^3 $$

---

### 📝 Question 3 (From Whiteboard Q3 - 4th Order)
**Solve:** $x^4 \frac{d^4y}{dx^4} + 6x^3 \frac{d^3y}{dx^3} + 9x^2 \frac{d^2y}{dx^2} + 3x \frac{dy}{dx} + y = (1 + \ln x)^2$

**Solution:**
1. **Apply Transformations:**
   Let $x = e^t \implies t = \ln x$. The right side becomes $(1 + t)^2 = t^2 + 2t + 1$.
   Substitute the operator equivalents into the left side:
   $[(D^4 - 6D^3 + 11D^2 - 6D) + 6(D^3 - 3D^2 + 2D) + 9(D^2 - D) + 3D + 1]y = t^2 + 2t + 1$
   Expand the brackets:
   $(D^4 - 6D^3 + 11D^2 - 6D + 6D^3 - 18D^2 + 12D + 9D^2 - 9D + 3D + 1)y$
   Group like terms:
   $D^4 + (-6+6)D^3 + (11-18+9)D^2 + (-6+12-9+3)D + 1$
   $(D^4 + 2D^2 + 1)y = t^2 + 2t + 1$
   Notice that $(D^4 + 2D^2 + 1)$ is a perfect square: $(D^2 + 1)^2$.
   $$ (D^2 + 1)^2 y = t^2 + 2t + 1 $$
2. **Find Complementary Function ($y_c$):**
   Auxiliary Eq: $(m^2 + 1)^2 = 0 \implies m^2 = -1 \implies m = \pm i$ (Repeated twice)
   $$ y_c(t) = (C_1 + C_2t)\cos t + (C_3 + C_4t)\sin t $$
3. **Find Particular Integral ($y_p$):**
   Because the RHS is algebraic, we use binomial expansion.
   $$ y_p(t) = \frac{1}{(1 + D^2)^2} (t^2 + 2t + 1) = (1 + D^2)^{-2} (t^2 + 2t + 1) $$
   Expand $(1 + x)^{-2} = 1 - 2x + 3x^2 - \dots$
   $$ y_p(t) = (1 - 2D^2 + 3D^4 - \dots) (t^2 + 2t + 1) $$
   Apply the operator (derivatives higher than $D^2$ on a $t^2$ polynomial will be 0):
   $$ y_p(t) = 1(t^2 + 2t + 1) - 2D^2(t^2 + 2t + 1) $$
   First derivative: $2t + 2$. Second derivative ($D^2$): $2$.
   $$ y_p(t) = (t^2 + 2t + 1) - 2(2) = t^2 + 2t + 1 - 4 = t^2 + 2t - 3 $$
4. **General Solution in terms of $t$:**
   $$ y(t) = (C_1 + C_2t)\cos t + (C_3 + C_4t)\sin t + t^2 + 2t - 3 $$
5. **Resubstitute back to $x$ ($t = \ln x$):**
   $$ y(x) = (C_1 + C_2\ln x)\cos(\ln x) + (C_3 + C_4\ln x)\sin(\ln x) + (\ln x)^2 + 2\ln x - 3 $$

---

### 📝 Question 4 (From Notes - Logarithmic RHS)
**Solve:** $x^2 \frac{d^2y}{dx^2} - x \frac{dy}{dx} + y = \ln x$

**Solution:**
1. **Apply Transformations:**
   $$ [D(D - 1) - D + 1]y = t $$
   $$ (D^2 - 2D + 1)y = t \implies (D - 1)^2 y = t $$
2. **Find Complementary Function ($y_c$):**
   Auxiliary Eq: $(m - 1)^2 = 0 \implies m = 1, 1$
   $$ y_c(t) = (C_1 + C_2t)e^t $$
3. **Find Particular Integral ($y_p$):**
   $$ y_p(t) = \frac{1}{D^2 - 2D + 1} t = \frac{1}{1 - (2D - D^2)} t $$
   Binomial Expansion: $[1 - (2D - D^2)]^{-1} t \approx (1 + 2D)t$
   $$ y_p(t) = t + 2D(t) = t + 2(1) = t + 2 $$
4. **General Solution in terms of $t$:**
   $$ y(t) = (C_1 + C_2t)e^t + t + 2 $$
5. **Resubstitute back to $x$ ($e^t = x, t = \ln x$):**
   $$ y(x) = x(C_1 + C_2\ln x) + \ln x + 2 $$

---

### 📝 Question 5 (From Notes - Complex Roots)
**Solve:** $x^2 y'' + y = 3x^2$

**Solution:**
1. **Apply Transformations:**
   $$ (D^2 - D)y + y = 3e^{2t} $$
   $$ (D^2 - D + 1)y = 3e^{2t} $$
2. **Find Complementary Function ($y_c$):**
   Auxiliary Eq: $m^2 - m + 1 = 0$
   Quadratic Formula: $m = \frac{1 \pm \sqrt{1 - 4}}{2} = \frac{1 \pm i\sqrt{3}}{2} = \frac{1}{2} \pm i\frac{\sqrt{3}}{2}$
   $$ y_c(t) = e^{t/2} \left( C_1\cos\left(\frac{\sqrt{3}}{2}t\right) + C_2\sin\left(\frac{\sqrt{3}}{2}t\right) \right) $$
3. **Find Particular Integral ($y_p$):**
   $$ y_p(t) = \frac{1}{D^2 - D + 1} 3e^{2t} $$
   Substitute $D = 2$:
   $$ y_p(t) = 3 \frac{1}{2^2 - 2 + 1} e^{2t} = 3 \frac{1}{4 - 2 + 1} e^{2t} = 3 \left(\frac{1}{3}\right) e^{2t} = e^{2t} $$
4. **General Solution in terms of $t$:**
   $$ y(t) = e^{t/2} \left( C_1\cos\left(\frac{\sqrt{3}}{2}t\right) + C_2\sin\left(\frac{\sqrt{3}}{2}t\right) \right) + e^{2t} $$
5. **Resubstitute back to $x$ ($e^t = x, e^{t/2} = x^{1/2} = \sqrt{x}$):**
   $$ y(x) = \sqrt{x} \left( C_1\cos\left(\frac{\sqrt{3}}{2}\ln x\right) + C_2\sin\left(\frac{\sqrt{3}}{2}\ln x\right) \right) + x^2 $$

---

### 📝 Question 6 (From Notes - Double Failure Case)
**Solve:** $x^2 y'' - 3xy' + 4y = 2x^2$

**Solution:**
1. **Apply Transformations:**
   $$ [D(D - 1) - 3D + 4]y = 2e^{2t} $$
   $$ (D^2 - 4D + 4)y = 2e^{2t} \implies (D - 2)^2 y = 2e^{2t} $$
2. **Find Complementary Function ($y_c$):**
   Auxiliary Eq: $(m - 2)^2 = 0 \implies m = 2, 2$
   $$ y_c(t) = (C_1 + C_2t)e^{2t} $$
3. **Find Particular Integral ($y_p$):**
   $$ y_p(t) = \frac{1}{(D - 2)^2} 2e^{2t} $$
   Substitute $D=2 \implies$ Denominator is 0 (Failure).
   *Fix 1:* Multiply by $t$, diff denominator: $y_p(t) = t \frac{1}{2(D-2)} 2e^{2t}$. Sub $D=2 \implies$ Failure again.
   *Fix 2:* Multiply by $t$ again ($t^2$), diff denominator again: $y_p(t) = t^2 \frac{1}{2(1)} 2e^{2t} = t^2 e^{2t}$.
4. **General Solution in terms of $t$:**
   $$ y(t) = (C_1 + C_2t)e^{2t} + t^2 e^{2t} $$
5. **Resubstitute back to $x$:**
   $$ y(x) = (C_1 + C_2\ln x)x^2 + (\ln x)^2 x^2 $$

---

**🎉 Congratulations!** You have completed the structured course notes for Ordinary Differential Equations based on your provided material.