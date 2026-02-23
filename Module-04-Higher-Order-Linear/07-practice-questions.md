# 📝 Module 4 Practice: Higher-Order Linear ODEs

This section contains all the comprehensive practice problems and homework questions for solving linear differential equations with constant coefficients. Remember that the general solution is always $y = y_c + y_p$.

---

## 🔹 Part A: Homogeneous Equations (Finding $y_c$ only)
*For these problems, $F(x) = 0$, so $y_p = 0$ and the general solution is just $y = y_c$.*

### 📝 Question 1
**Solve:** $(D^4 - D^3 - 9D^2 - 11D - 4)y = 0$

**Solution:**
1. **Auxiliary Equation:** $m^4 - m^3 - 9m^2 - 11m - 4 = 0$
2. **Find roots using Synthetic Division:**
   Test $m = -1$: $1 - (-1) - 9(-1)^2 - 11(-1) - 4 = 1 + 1 - 9 + 11 - 4 = 0$. So $m=-1$ is a root.
   ```text
   -1 |  1   -1   -9   -11   -4
      |      -1    2     7    4
      ---------------------------
         1   -2   -7    -4    0
   ```
   The reduced cubic is $m^3 - 2m^2 - 7m - 4 = 0$.
   Test $m = -1$ again: $-1 - 2(1) - 7(-1) - 4 = -1 - 2 + 7 - 4 = 0$.
   ```text
   -1 |  1   -2   -7   -4
      |      -1    3    4
      ---------------------
         1   -3   -4    0
   ```
   The reduced quadratic is $m^2 - 3m - 4 = 0$.
3. **Solve Quadratic:**
   $(m - 4)(m + 1) = 0 \implies m = 4, m = -1$.
4. **Final Roots:** $-1, -1, -1, 4$.
5. **General Solution:**
   $$ y = (C_1 + C_2x + C_3x^2)e^{-x} + C_4e^{4x} $$

### 📝 Question 2
**Solve:** $(D^4 + 5D^2 - 36)y = 0$

**Solution:**
1. **Auxiliary Equation:** $m^4 + 5m^2 - 36 = 0$
2. **Factorize:** Let $k = m^2$. Then $k^2 + 5k - 36 = 0$.
   $(k + 9)(k - 4) = 0 \implies (m^2 + 9)(m^2 - 4) = 0$.
3. **Find roots:**
   $m^2 = -9 \implies m = \pm 3i$
   $m^2 = 4 \implies m = \pm 2$
4. **General Solution:**
   $$ y = C_1e^{2x} + C_2e^{-2x} + C_3\cos 3x + C_4\sin 3x $$

### 📝 Question 3
**Solve:** $(D^2 - 2D + 5)^2 y = 0$

**Solution:**
1. **Auxiliary Equation:** $(m^2 - 2m + 5)^2 = 0$
2. **Find roots of the inner quadratic:**
   $m = \frac{-(-2) \pm \sqrt{(-2)^2 - 4(1)(5)}}{2(1)} = \frac{2 \pm \sqrt{4 - 20}}{2} = \frac{2 \pm 4i}{2} = 1 \pm 2i$.
3. **Handle squared term:**
   Because the entire quadratic is squared, the complex conjugate roots are repeated twice: $1 \pm 2i, 1 \pm 2i$.
4. **General Solution:**
   $$ y = e^x \left[ (C_1 + C_2x)\cos 2x + (C_3 + C_4x)\sin 2x \right] $$

### 📝 Question 4
**Solve:** $(D^2 + 25)y = 0$

**Solution:**
1. **Auxiliary Equation:** $m^2 + 25 = 0 \implies m^2 = -25 \implies m = \pm 5i$.
2. **General Solution:**
   $$ y = C_1\cos 5x + C_2\sin 5x $$

### 📝 Question 5
**Solve:** $(D^4 + 4D^2)y = 0$

**Solution:**
1. **Auxiliary Equation:** $m^4 + 4m^2 = 0 \implies m^2(m^2 + 4) = 0$.
2. **Find roots:**
   $m^2 = 0 \implies m = 0, 0$
   $m^2 = -4 \implies m = \pm 2i$
3. **General Solution:**
   $$ y = (C_1 + C_2x)e^{0x} + C_3\cos 2x + C_4\sin 2x = C_1 + C_2x + C_3\cos 2x + C_4\sin 2x $$

### 📝 Question 6
**Solve:** $\frac{d^5y}{dx^5} + 12\frac{d^4y}{dx^4} + 36\frac{d^3y}{dx^3} = 0$

**Solution:**
1. **Auxiliary Equation:** $m^5 + 12m^4 + 36m^3 = 0$.
2. **Factorize:** $m^3(m^2 + 12m + 36) = 0 \implies m^3(m + 6)^2 = 0$.
3. **Find roots:** $m = 0, 0, 0, -6, -6$.
4. **General Solution:**
   $$ y = C_1 + C_2x + C_3x^2 + (C_4 + C_5x)e^{-6x} $$

### 📝 Question 7
**Solve:** $\frac{d^5y}{dx^5} + 5\frac{d^4y}{dx^4} - 2\frac{d^3y}{dx^3} - 10\frac{d^2y}{dx^2} + \frac{dy}{dx} + 5y = 0$

**Solution:**
1. **Auxiliary Equation:** $m^5 + 5m^4 - 2m^3 - 10m^2 + m + 5 = 0$.
2. **Factor by grouping:**
   $m^4(m + 5) - 2m^2(m + 5) + 1(m + 5) = 0$
   $(m^4 - 2m^2 + 1)(m + 5) = 0$
   $(m^2 - 1)^2 (m + 5) = 0$
   $((m-1)(m+1))^2 (m+5) = 0 \implies (m-1)^2(m+1)^2(m+5) = 0$.
3. **Find roots:** $m = 1, 1, -1, -1, -5$.
4. **General Solution:**
   $$ y = (C_1 + C_2x)e^x + (C_3 + C_4x)e^{-x} + C_5e^{-5x} $$

---

## 🔹 Part B: Particular Integral - Exponential Case

### 📝 Question 8 (Standard Case)
**Solve:** $\frac{d^2y}{dx^2} - 3\frac{dy}{dx} + 2y = e^{3x}$

**Solution:**
1. **Find $y_c$:** $m^2 - 3m + 2 = 0 \implies (m-1)(m-2) = 0 \implies m = 1, 2$.
   $y_c = C_1e^x + C_2e^{2x}$.
2. **Find $y_p$:** $y_p = \frac{1}{D^2 - 3D + 2} e^{3x}$.
   Substitute $D=3$: $y_p = \frac{1}{9 - 9 + 2} e^{3x} = \frac{1}{2}e^{3x}$.
3. **General Solution:**
   $$ y = C_1e^x + C_2e^{2x} + \frac{1}{2}e^{3x} $$

### 📝 Question 9 (Case of Failure)
**Solve:** $(D^3 + 2D^2 - D - 2)y = e^x$

**Solution:**
1. **Find $y_c$:** $m^3 + 2m^2 - m - 2 = 0 \implies m^2(m+2) - 1(m+2) = 0 \implies (m^2-1)(m+2) = 0$. Roots: $1, -1, -2$.
   $y_c = C_1e^x + C_2e^{-x} + C_3e^{-2x}$.
2. **Find $y_p$:** $y_p = \frac{1}{D^3 + 2D^2 - D - 2} e^x$.
   Substitute $D=1$: Denominator becomes $1 + 2 - 1 - 2 = 0$. Failure.
   Multiply by $x$, diff denominator: $y_p = x \frac{1}{3D^2 + 4D - 1} e^x$.
   Substitute $D=1$: $y_p = x \frac{1}{3(1) + 4(1) - 1} e^x = \frac{x}{6}e^x$.
3. **General Solution:**
   $$ y = C_1e^x + C_2e^{-x} + C_3e^{-2x} + \frac{x}{6}e^x $$

### 📝 Question 10 (Case of Failure)
**Solve:** $(D^3 - 2D^2 - 5D + 6)y = e^{3x}$

**Solution:**
1. **Find $y_c$:** $m^3 - 2m^2 - 5m + 6 = 0$. By synthetic division (root 1 works), factors to $(m-1)(m+2)(m-3) = 0$. Roots: $1, -2, 3$.
   $y_c = C_1e^x + C_2e^{-2x} + C_3e^{3x}$.
2. **Find $y_p$:** $y_p = \frac{1}{D^3 - 2D^2 - 5D + 6} e^{3x}$.
   Substitute $D=3$: Denom $= 27 - 18 - 15 + 6 = 0$. Failure.
   Multiply by $x$, diff denominator: $y_p = x \frac{1}{3D^2 - 4D - 5} e^{3x}$.
   Substitute $D=3$: $y_p = x \frac{1}{27 - 12 - 5} e^{3x} = \frac{x}{10}e^{3x}$.
3. **General Solution:**
   $$ y = C_1e^x + C_2e^{-2x} + C_3e^{3x} + \frac{x}{10}e^{3x} $$

### 📝 Question 11 (Case of Failure with Complex Roots)
**Solve:** $\frac{d^3y}{dx^3} - \frac{d^2y}{dx^2} + 4\frac{dy}{dx} - 4y = e^x$

**Solution:**
1. **Find $y_c$:** $m^3 - m^2 + 4m - 4 = 0 \implies m^2(m-1) + 4(m-1) = 0 \implies (m^2+4)(m-1) = 0$. Roots: $1, \pm 2i$.
   $y_c = C_1e^x + C_2\cos 2x + C_3\sin 2x$.
2. **Find $y_p$:** $y_p = \frac{1}{D^3 - D^2 + 4D - 4} e^x$.
   Substitute $D=1$: Denom $= 1 - 1 + 4 - 4 = 0$. Failure.
   Multiply by $x$, diff denominator: $y_p = x \frac{1}{3D^2 - 2D + 4} e^x$.
   Substitute $D=1$: $y_p = x \frac{1}{3 - 2 + 4} e^x = \frac{x}{5}e^x$.
3. **General Solution:**
   $$ y = C_1e^x + C_2\cos 2x + C_3\sin 2x + \frac{x}{5}e^x $$

### 📝 Question 12 (Triple Failure)
**Solve:** $\frac{d^3y}{dx^3} + 3\frac{d^2y}{dx^2} + 3\frac{dy}{dx} + y = e^{-x}$

**Solution:**
1. **Find $y_c$:** $m^3 + 3m^2 + 3m + 1 = 0 \implies (m+1)^3 = 0$. Roots: $-1, -1, -1$.
   $y_c = (C_1 + C_2x + C_3x^2)e^{-x}$.
2. **Find $y_p$:** $y_p = \frac{1}{(D+1)^3} e^{-x}$.
   Sub $D=-1$ fails. Diff 1: $x \frac{1}{3(D+1)^2} e^{-x}$ (fails). Diff 2: $x^2 \frac{1}{6(D+1)} e^{-x}$ (fails). Diff 3: $x^3 \frac{1}{6} e^{-x}$.
3. **General Solution:**
   $$ y = (C_1 + C_2x + C_3x^2)e^{-x} + \frac{x^3}{6}e^{-x} $$

### 📝 Question 13 (Superposition of Exponentials)
**Solve:** $(D-2)(D+1)^2 y = e^{2x} + e^{-x}$

**Solution:**
1. **Find $y_c$:** Roots are $2, -1, -1$.
   $y_c = C_1e^{2x} + (C_2 + C_3x)e^{-x}$.
2. **Find $y_p$:** Split into $y_{p1} + y_{p2}$.
   $y_{p1} = \frac{1}{(D-2)(D+1)^2} e^{2x}$. Sub $D=2$ fails. Diff denominator product rule, or just multiply by $x$ and drop the $(D-2)$ factor: $x \frac{1}{1 \cdot (2+1)^2} e^{2x} = \frac{x}{9}e^{2x}$.
   $y_{p2} = \frac{1}{(D-2)(D+1)^2} e^{-x}$. Sub $D=-1$ fails twice. Multiply by $x^2$ and drop the $(D+1)^2$ factor: $x^2 \frac{1}{2!(-1-2)} e^{-x} = -\frac{x^2}{6}e^{-x}$.
3. **General Solution:**
   $$ y = C_1e^{2x} + (C_2 + C_3x)e^{-x} + \frac{x}{9}e^{2x} - \frac{x^2}{6}e^{-x} $$

### 📝 Question 14 (Standard Case)
**Solve:** $(D-1)^3 y = 16e^{3x}$

**Solution:**
1. **Find $y_c$:** Roots $1, 1, 1$. $y_c = (C_1 + C_2x + C_3x^2)e^x$.
2. **Find $y_p$:** $y_p = \frac{1}{(D-1)^3} 16e^{3x} = 16 \frac{1}{(3-1)^3} e^{3x} = 16 \frac{1}{8} e^{3x} = 2e^{3x}$.
3. **General Solution:**
   $$ y = (C_1 + C_2x + C_3x^2)e^x + 2e^{3x} $$

---

## 🔹 Part C: Particular Integral - Algebraic Case

### 📝 Question 15
**Solve:** $(D^2 + 5D + 4)y = 3 - 2x$

**Solution:**
1. **Find $y_c$:** $m^2 + 5m + 4 = 0 \implies m = -1, -4$. $y_c = C_1e^{-x} + C_2e^{-4x}$.
2. **Find $y_p$:** $y_p = \frac{1}{4(1 + \frac{5D+D^2}{4})} (3 - 2x)$
   Expand: $y_p = \frac{1}{4} \left[ 1 - \frac{5D}{4} \right] (3 - 2x)$
   Operate: $y_p = \frac{1}{4} \left[ (3 - 2x) - \frac{5}{4}(-2) \right] = \frac{1}{4} \left[ 3 - 2x + \frac{5}{2} \right] = \frac{11 - 4x}{8}$.
3. **General Solution:**
   $$ y = C_1e^{-x} + C_2e^{-4x} + \frac{11 - 4x}{8} $$

### 📝 Question 16
**Solve:** $\frac{d^3y}{dx^3} - \frac{d^2y}{dx^2} - 6\frac{dy}{dx} = 1 + x^2$

**Solution:**
1. **Find $y_c$:** $m(m^2 - m - 6) = 0 \implies m(m-3)(m+2) = 0$. Roots: $0, 3, -2$.
   $y_c = C_1 + C_2e^{3x} + C_3e^{-2x}$.
2. **Find $y_p$:** $y_p = \frac{1}{-6D(1 + \frac{D^2-D}{-6})} (1 + x^2) = -\frac{1}{6D} \left[ 1 - \left(\frac{D-D^2}{6}\right) \right]^{-1} (1 + x^2)$.
   Expand to $D^2$: $-\frac{1}{6D} \left[ 1 + \frac{D-D^2}{6} + \frac{D^2}{36} \right] (1+x^2) = -\frac{1}{6D} \left[ 1 + \frac{D}{6} - \frac{5D^2}{36} \right] (1+x^2)$
   Operate: $-\frac{1}{6D} \left[ (1+x^2) + \frac{1}{6}(2x) - \frac{5}{36}(2) \right] = -\frac{1}{6D} \left[ x^2 + \frac{x}{3} + \frac{13}{18} \right]$.
   Integrate ($1/D$): $-\frac{1}{6} \left( \frac{x^3}{3} + \frac{x^2}{6} + \frac{13x}{18} \right)$.
3. **General Solution:**
   $$ y = C_1 + C_2e^{3x} + C_3e^{-2x} - \frac{x^3}{18} - \frac{x^2}{36} - \frac{13x}{108} $$

### 📝 Question 17
**Solve:** $\frac{d^4y}{dx^4} + 4y = x^4$

**Solution:**
1. **Find $y_c$:** $m^4 + 4 = 0 \implies$ roots $1\pm i, -1\pm i$. 
   $y_c = e^x(C_1\cos x + C_2\sin x) + e^{-x}(C_3\cos x + C_4\sin x)$.
2. **Find $y_p$:** $y_p = \frac{1}{4(1 + D^4/4)} x^4 = \frac{1}{4} (1 - D^4/4) x^4 = \frac{1}{4} (x^4 - \frac{24}{4}) = \frac{x^4}{4} - \frac{3}{2}$.
3. **General Solution:**
   $$ y = e^x(C_1\cos x + C_2\sin x) + e^{-x}(C_3\cos x + C_4\sin x) + \frac{x^4}{4} - \frac{3}{2} $$

### 📝 Question 18
**Solve:** $(2D^2 + 3D + 4)y = x^2 - 2x$

**Solution:**
1. **Find $y_c$:** $2m^2 + 3m + 4 = 0 \implies m = \frac{-3 \pm i\sqrt{23}}{4}$.
   $y_c = e^{-3x/4} \left( C_1\cos\frac{\sqrt{23}}{4}x + C_2\sin\frac{\sqrt{23}}{4}x \right)$.
2. **Find $y_p$:** $y_p = \frac{1}{4[1 + \frac{3D+2D^2}{4}]} (x^2 - 2x) = \frac{1}{4} \left[ 1 - \frac{3D+2D^2}{4} + \frac{9D^2}{16} \right] (x^2 - 2x)$.
   Simplify operator: $\frac{1}{4} \left[ 1 - \frac{3D}{4} + \frac{D^2}{16} \right] (x^2 - 2x)$.
   Operate: $\frac{1}{4} \left[ (x^2 - 2x) - \frac{3}{4}(2x - 2) + \frac{1}{16}(2) \right] = \frac{1}{4} \left( x^2 - \frac{7x}{2} + \frac{13}{8} \right)$.
3. **General Solution:**
   $$ y = y_c + \frac{x^2}{4} - \frac{7x}{8} + \frac{13}{32} $$

### 📝 Question 19
**Solve:** $(D^2 - 4D + 3)y = x^3$

**Solution:**
1. **Find $y_c$:** $m^2 - 4m + 3 = 0 \implies m=1, 3$. $y_c = C_1e^x + C_2e^{3x}$.
2. **Find $y_p$:** $y_p = \frac{1}{3(1 - \frac{4D-D^2}{3})} x^3 = \frac{1}{3} \left[ 1 + \left(\frac{4D-D^2}{3}\right) + \left(\frac{4D-D^2}{3}\right)^2 + \left(\frac{4D-D^2}{3}\right)^3 \right] x^3$.
   Expand up to $D^3$: $\frac{1}{3} \left[ 1 + \frac{4D}{3} - \frac{D^2}{3} + \frac{16D^2}{9} - \frac{8D^3}{9} + \frac{64D^3}{27} \right] = \frac{1}{3} \left[ 1 + \frac{4D}{3} + \frac{13D^2}{9} + \frac{40D^3}{27} \right]$.
   Operate on $x^3$: $\frac{1}{3} \left[ x^3 + \frac{4}{3}(3x^2) + \frac{13}{9}(6x) + \frac{40}{27}(6) \right] = \frac{1}{3} \left( x^3 + 4x^2 + \frac{26x}{3} + \frac{80}{9} \right)$.
3. **General Solution:**
   $$ y = C_1e^x + C_2e^{3x} + \frac{x^3}{3} + \frac{4x^2}{3} + \frac{26x}{9} + \frac{80}{27} $$

---

## 🔹 Part D: Mixed Cases & Superposition (Trig, Exponential, Algebraic)

### 📝 Question 20
**Solve:** $(D^2 - 4D + 4)y = 8(e^{2x} + x^2 + \sin 2x)$

**Solution:**
1. **Find $y_c$:** $(m-2)^2 = 0 \implies m=2, 2$. $y_c = (C_1 + C_2x)e^{2x}$.
2. **Find $y_p$ (Superposition):** $y_p = y_{p1} + y_{p2} + y_{p3}$.
   *   $y_{p1} = 8 \frac{1}{(D-2)^2} e^{2x}$. Double failure at $D=2$. $\implies 8 \frac{x^2}{2}e^{2x} = 4x^2e^{2x}$.
   *   $y_{p2} = 8 \frac{1}{4(1 - D + D^2/4)} x^2 = 2[1 + D + \frac{3D^2}{4}]x^2 = 2[x^2 + 2x + \frac{3}{4}(2)] = 2x^2 + 4x + 3$.
   *   $y_{p3} = 8 \frac{1}{D^2 - 4D + 4} \sin 2x$. Substitute $D^2 = -4$: $\frac{8}{-4 - 4D + 4}\sin 2x = \frac{8}{-4D}\sin 2x = -\frac{2}{D}\sin 2x = -2(-\frac{\cos 2x}{2}) = \cos 2x$.
3. **General Solution:**
   $$ y = (C_1 + C_2x)e^{2x} + 4x^2e^{2x} + 2x^2 + 4x + 3 + \cos 2x $$

### 📝 Question 21
**Solve:** $\frac{d^2y}{dx^2} - 4\frac{dy}{dx} + 3y = e^{2x} + \cos x$

**Solution:**
1. **Find $y_c$:** $m^2 - 4m + 3 = 0 \implies m=1, 3$. $y_c = C_1e^x + C_2e^{3x}$.
2. **Find $y_p$:** 
   *   $y_{p1} = \frac{1}{D^2 - 4D + 3} e^{2x}$. Sub $D=2$: $\frac{1}{4 - 8 + 3}e^{2x} = -e^{2x}$.
   *   $y_{p2} = \frac{1}{D^2 - 4D + 3} \cos x$. Sub $D^2=-1$: $\frac{1}{2 - 4D}\cos x$. Rationalize: $\frac{2 + 4D}{4 - 16D^2}\cos x$. Sub $D^2=-1$: $\frac{2 + 4D}{20}\cos x = \frac{2\cos x - 4\sin x}{20} = \frac{\cos x - 2\sin x}{10}$.
3. **General Solution:**
   $$ y = C_1e^x + C_2e^{3x} - e^{2x} + \frac{1}{10}(\cos x - 2\sin x) $$

### 📝 Question 22
**Solve:** $\frac{d^2y}{dx^2} - 2\frac{dy}{dx} + 3y = \cos x + x^2$

**Solution:**
1. **Find $y_c$:** $m^2 - 2m + 3 = 0 \implies m = \frac{2 \pm \sqrt{4-12}}{2} = 1 \pm i\sqrt{2}$.
   $y_c = e^x(C_1\cos\sqrt{2}x + C_2\sin\sqrt{2}x)$.
2. **Find $y_p$:**
   *   $y_{p1} = \frac{1}{D^2 - 2D + 3} \cos x$. Sub $D^2=-1$: $\frac{1}{2 - 2D}\cos x = \frac{2 + 2D}{4 - 4D^2}\cos x = \frac{2\cos x - 2\sin x}{8} = \frac{\cos x - \sin x}{4}$.
   *   $y_{p2} = \frac{1}{3(1 + \frac{D^2-2D}{3})} x^2 = \frac{1}{3}[1 - \frac{D^2-2D}{3} + \frac{4D^2}{9}]x^2 = \frac{1}{3}[1 + \frac{2D}{3} + \frac{D^2}{9}]x^2 = \frac{1}{3}(x^2 + \frac{4x}{3} + \frac{2}{9})$.
3. **General Solution:**
   $$ y = y_c + \frac{\cos x - \sin x}{4} + \frac{x^2}{3} + \frac{4x}{9} + \frac{2}{27} $$

---

## 🔹 Part E: Initial Value Problems

### 📝 Question 23
**Solve:** $\frac{d^2y}{dx^2} - 2\frac{dy}{dx} - 3y = 2e^{2x} + 10\sin 3x$, given that $y(0) = 2$ and $y'(0) = 4$.

**Solution:**
1. **Find $y_c$:** $m^2 - 2m - 3 = 0 \implies m = 3, -1$. $y_c = C_1e^{3x} + C_2e^{-x}$.
2. **Find $y_p$:**
   *   $y_{p1} = \frac{2}{D^2 - 2D - 3} e^{2x}$. Sub $D=2$: $\frac{2}{4 - 4 - 3} e^{2x} = -\frac{2}{3}e^{2x}$.
   *   $y_{p2} = \frac{10}{D^2 - 2D - 3} \sin 3x$. Sub $D^2=-9$: $\frac{10}{-12 - 2D}\sin 3x = \frac{-5}{D + 6}\sin 3x = \frac{-5(D-6)}{D^2 - 36}\sin 3x = \frac{-5(D-6)}{-45}\sin 3x = \frac{1}{9}(3\cos 3x - 6\sin 3x) = \frac{1}{3}\cos 3x - \frac{2}{3}\sin 3x$.
3. **General Solution:**
   $$ y = C_1e^{3x} + C_2e^{-x} - \frac{2}{3}e^{2x} + \frac{1}{3}\cos 3x - \frac{2}{3}\sin 3x $$
4. **Apply Initial Conditions:**
   First, apply $y(0) = 2$:
   $2 = C_1(1) + C_2(1) - \frac{2}{3}(1) + \frac{1}{3}(1) - 0 \implies C_1 + C_2 = \frac{7}{3}$. *(Eq. A)*
   Next, find $y'$:
   $y' = 3C_1e^{3x} - C_2e^{-x} - \frac{4}{3}e^{2x} - \sin 3x - 2\cos 3x$
   Apply $y'(0) = 4$:
   $4 = 3C_1 - C_2 - \frac{4}{3} - 0 - 2 \implies 3C_1 - C_2 = \frac{22}{3}$. *(Eq. B)*
5. **Solve for Constants:**
   Add (Eq. A) and (Eq. B): $4C_1 = \frac{29}{3} \implies C_1 = \frac{29}{12}$.
   Substitute $C_1$ into (Eq. A): $C_2 = \frac{7}{3} - \frac{29}{12} = \frac{28}{12} - \frac{29}{12} = -\frac{1}{12}$.
6. **Final Particular Solution:**
   $$ y = \frac{29}{12}e^{3x} - \frac{1}{12}e^{-x} - \frac{2}{3}e^{2x} + \frac{1}{3}\cos 3x - \frac{2}{3}\sin 3x $$
