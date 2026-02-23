# 📝 Module 2 Practice: Solving First-Order ODEs

This section contains practice questions from your homework assignments, categorized by the specific solving technique required.

---

## 🔹 Part A: Variable Separable Method

### 📝 Question 1
**Solve:** $(1+x^2)dy - xy \, dx = 0$

**Solution:**
1. **Separate Variables:** 
   Move the $dx$ term to the right:
   $(1+x^2)dy = xy \, dx$
   Divide by $y$ and $(1+x^2)$:
   $\frac{1}{y} dy = \frac{x}{1+x^2} dx$
2. **Integrate both sides:**
   $\int \frac{1}{y} dy = \frac{1}{2} \int \frac{2x}{1+x^2} dx$ *(multiplied by 2 to match derivative of denominator)*
   $\ln|y| = \frac{1}{2} \ln(1+x^2) + \ln C$
3. **Simplify:**
   $\ln|y| = \ln\left(C\sqrt{1+x^2}\right)$
   $y = C\sqrt{1+x^2}$
   Squaring both sides gives the **Final Answer:** $y^2 = C^2(1+x^2)$

### 📝 Question 2
**Solve:** $(e^y+2)\sin x \, dx - e^y \cos x \, dy = 0$

**Solution:**
1. **Separate Variables:**
   $(e^y+2)\sin x \, dx = e^y \cos x \, dy$
   $\frac{\sin x}{\cos x} dx = \frac{e^y}{e^y+2} dy$
2. **Integrate both sides:**
   $\int \tan x \, dx = \int \frac{e^y}{e^y+2} dy$
   $-\ln|\cos x| = \ln|e^y+2| - \ln C$
3. **Simplify:**
   $\ln C = \ln|e^y+2| + \ln|\cos x| \implies \ln C = \ln((e^y+2)\cos x)$
   **Final Answer:** $(e^y+2)\cos x = C$

---

## 🔹 Part B: Homogeneous Equations

### 📝 Question 3
**Solve:** $(y^2 - xy)dx + x^2 dy = 0$

**Solution:**
1. **Standard Form:**
   $x^2 dy = -(y^2 - xy)dx \implies \frac{dy}{dx} = \frac{xy - y^2}{x^2}$
2. **Substitute:** Let $y = vx \implies \frac{dy}{dx} = v + x\frac{dv}{dx}$
   $v + x\frac{dv}{dx} = \frac{x(vx) - (vx)^2}{x^2} = \frac{x^2(v - v^2)}{x^2} = v - v^2$
3. **Separate and Integrate:**
   $x\frac{dv}{dx} = v - v^2 - v \implies x\frac{dv}{dx} = -v^2$
   $-\frac{1}{v^2} dv = \frac{1}{x} dx$
   $\int -v^{-2} dv = \int \frac{1}{x} dx \implies \frac{1}{v} = \ln|x| + C$
4. **Resubstitute $v = y/x$:**
   $\frac{x}{y} = \ln|x| + C$
   **Final Answer:** $x = y(\ln|x| + C)$

---

## 🔹 Part C: Linear Differential Equations

### 📝 Question 4
**Solve:** $\frac{dy}{dx} + \frac{1}{x} y = x^3 - 3$

**Solution:**
1. **Identify P and Q:** $P(x) = \frac{1}{x}$, $Q(x) = x^3 - 3$
2. **Find Integrating Factor (I.F):**
   $I.F. = e^{\int \frac{1}{x} dx} = e^{\ln x} = x$
3. **General Solution Formula:**
   $y \cdot (x) = \int x(x^3 - 3) dx + C$
   $xy = \int (x^4 - 3x) dx + C$
   **Final Answer:** $xy = \frac{x^5}{5} - \frac{3x^2}{2} + C$

---

## 🔹 Part D: Bernoulli's Equations

### 📝 Question 5
**Solve:** $2x \frac{dy}{dx} = 10x^3 y^5 + y$

**Solution:**
1. **Standard Form:**
   $2x \frac{dy}{dx} - y = 10x^3 y^5 \implies \frac{dy}{dx} - \frac{1}{2x}y = 5x^2 y^5$
2. **Divide by $y^5$:**
   $y^{-5}\frac{dy}{dx} - \frac{1}{2x}y^{-4} = 5x^2$
3. **Substitute:** Let $z = y^{-4} \implies \frac{dz}{dx} = -4y^{-5}\frac{dy}{dx} \implies -\frac{1}{4}\frac{dz}{dx} = y^{-5}\frac{dy}{dx}$
   $-\frac{1}{4}\frac{dz}{dx} - \frac{1}{2x}z = 5x^2$
   Multiply by $-4$: $\frac{dz}{dx} + \frac{2}{x}z = -20x^2$ (This is Linear)
4. **Solve Linear DE for z:**
   $I.F. = e^{\int \frac{2}{x} dx} = e^{2\ln x} = x^2$
   $z \cdot x^2 = \int (-20x^2 \cdot x^2) dx + C = \int -20x^4 dx + C$
   $zx^2 = -4x^5 + C$
5. **Resubstitute $z = y^{-4}$:**
   $y^{-4}x^2 = -4x^5 + C$
   **Final Answer:** $\frac{x^2}{y^4} = -4x^5 + C$