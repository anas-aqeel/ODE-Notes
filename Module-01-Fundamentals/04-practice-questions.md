# 📝 Module 1 Practice: Formation of Differential Equations

This section contains homework and practice problems to test your understanding of forming differential equations by eliminating arbitrary constants.

---

### 📝 Question 1: Polynomial Function
**Form the differential equation for:** $y = ax + bx^2 + cx^3$

**Solution:**
1. **Identify constants:** There are 3 constants ($a, b, c$), so we must differentiate 3 times.
2. **Differentiate successively:**
   * $y' = a + 2bx + 3cx^2$
   * $y'' = 2b + 6cx$
   * $y''' = 6c \implies c = \frac{y'''}{6}$
3. **Back-substitute to eliminate constants:**
   Substitute $c$ into the $y''$ equation to find $b$:
   $y'' = 2b + 6(\frac{y'''}{6})x \implies y'' = 2b + x y''' \implies b = \frac{1}{2}y'' - \frac{1}{2}x y'''$
   
   Substitute $b$ and $c$ into the $y'$ equation to find $a$:
   $y' = a + 2(\frac{1}{2}y'' - \frac{1}{2}x y''')x + 3(\frac{y'''}{6})x^2$
   $y' = a + x y'' - x^2 y''' + \frac{1}{2}x^2 y''' \implies a = y' - x y'' + \frac{1}{2}x^2 y'''$

4. **Substitute $a, b, c$ into the original equation:**
   $y = \left(y' - x y'' + \frac{1}{2}x^2 y'''\right)x + \left(\frac{1}{2}y'' - \frac{1}{2}x y'''\right)x^2 + \left(\frac{y'''}{6}\right)x^3$
   $y = x y' - x^2 y'' + \frac{1}{2}x^3 y''' + \frac{1}{2}x^2 y'' - \frac{1}{2}x^3 y''' + \frac{1}{6}x^3 y'''$
   $y = x y' - \frac{1}{2}x^2 y'' + \frac{1}{6}x^3 y'''$

5. **Simplify (Multiply by 6):**
   $6y = 6x y' - 3x^2 y'' + x^3 y'''$
   **Final Answer:** $x^3 y''' - 3x^2 y'' + 6xy' - 6y = 0$

---

### 📝 Question 2: Trigonometric Function
**Form the differential equation for:** $y = A \cos 2t + B \sin 2t$

**Solution:**
1. **Identify constants:** There are 2 constants ($A, B$), so we differentiate 2 times.
2. **First derivative (with respect to $t$):**
   $y' = -2A \sin 2t + 2B \cos 2t$
3. **Second derivative:**
   $y'' = -4A \cos 2t - 4B \sin 2t$
4. **Eliminate constants:** Notice that we can factor out a $-4$:
   $y'' = -4(A \cos 2t + B \sin 2t)$
   The expression in the parentheses is exactly our original $y$.
   $y'' = -4y$
   **Final Answer:** $y'' + 4y = 0$

---

### 📝 Question 3: Exponential Function
**Form the differential equation for:** $y = ae^x + be^{2x} + ce^{3x}$

**Solution:**
*Advanced Tip:* Instead of tedious substitution, we can use the reverse of the auxiliary equation method. 
1. **Identify roots:** The terms $e^{1x}, e^{2x}, e^{3x}$ indicate that the roots of the characteristic equation are $m_1 = 1$, $m_2 = 2$, and $m_3 = 3$.
2. **Form the characteristic equation:**
   $(m - 1)(m - 2)(m - 3) = 0$
3. **Expand the equation:**
   $(m^2 - 3m + 2)(m - 3) = 0$
   $m^3 - 3m^2 - 3m^2 + 9m + 2m - 6 = 0$
   $m^3 - 6m^2 + 11m - 6 = 0$
4. **Convert back to derivatives ($m^n \to y^{(n)}$):**
   **Final Answer:** $y''' - 6y'' + 11y' - 6y = 0$

---

### 📝 Question 4: Mixed Function
**Form the differential equation for:** $y = ae^x + be^{-x} + c \cos x + d \sin x$

**Solution:**
1. **Identify roots:** We have 4 constants, so order is 4. 
   * $e^x$ and $e^{-x}$ give roots $m = 1$ and $m = -1$.
   * $\cos 1x$ and $\sin 1x$ give complex conjugate roots $m = 0 \pm 1i \implies m = i$ and $m = -i$.
2. **Form the characteristic equation:**
   $(m - 1)(m + 1)(m - i)(m + i) = 0$
3. **Expand the equation (using difference of squares):**
   $(m^2 - 1)(m^2 - i^2) = 0$
   Since $i^2 = -1$:
   $(m^2 - 1)(m^2 + 1) = 0$
   $m^4 - 1 = 0$
4. **Convert back to derivatives:**
   **Final Answer:** $y'''' - y = 0$ (or $\frac{d^4y}{dx^4} - y = 0$)

---

**Next Module:** You have successfully completed Module 1! You are now ready to begin solving equations. Proceed to [Module 2: Solving First-Order ODEs](../Module-02-First-Order-ODEs/README.md).