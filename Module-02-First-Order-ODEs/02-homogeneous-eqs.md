# 🧬 2. Homogeneous Differential Equations

When the variables in a first-order differential equation cannot be separated directly (i.e., you cannot get all $x$'s on one side and $y$'s on the other), the next method to check is whether the equation is **Homogeneous**.

---

## 1. Concept Overview

### 1.1 What is a Homogeneous Function?
A function $F(x,y)$ is called homogeneous of degree $n$ if, when you replace $x$ with $\lambda x$ and $y$ with $\lambda y$, the parameter $\lambda$ can be factored out completely as $\lambda^n$.

$$ F(\lambda x, \lambda y) = \lambda^n F(x, y) $$

### 1.2 What is a Homogeneous Differential Equation?
A first-order differential equation $\frac{dy}{dx} = f(x,y)$ is homogeneous if the function $f(x,y)$ can be expressed as a ratio of two homogeneous functions of the **same degree**.

Alternatively, if you can write the differential equation in the form:
$$ \frac{dy}{dx} = F\left(\frac{y}{x}\right) $$
then it is a Homogeneous Differential Equation.

---

## 2. Working Rule (The Substitution Method)

To solve a homogeneous differential equation, we use a specific substitution to transform it into a **Variable Separable** equation.

1.  **Identify Homogeneity:** Check that every term in the numerator and denominator has the same total power of variables.
2.  **Substitute:** 
    *   Let $y = vx$
    *   Differentiate with respect to $x$ (using the product rule):
        $$ \frac{dy}{dx} = v + x\frac{dv}{dx} $$
3.  **Transform:** Replace $y$ and $\frac{dy}{dx}$ in the original equation. The $x$ terms will typically cancel out, leaving an equation in terms of $v$ and $x$.
4.  **Separate and Integrate:** The new equation will be Variable Separable. Separate $v$ and $x$, then integrate both sides.
5.  **Resubstitute:** Finally, replace $v$ with $\frac{y}{x}$ to get the general solution in terms of $x$ and $y$.

---

## 3. Solved Questions

Here are questions from the lecture notes demonstrating the homogeneity check and the solution process.

### 📝 Question 1: Checking for Homogeneity
**Determine if the function $F(x,y) = \frac{2x^2y}{x^2+y^2}$ is homogeneous.**

**Solution:**
1.  **Test:** Replace $x \to \lambda x$ and $y \to \lambda y$.
    $$ F(\lambda x, \lambda y) = \frac{2(\lambda x)^2(\lambda y)}{(\lambda x)^2 + (\lambda y)^2} $$
2.  **Simplify:**
    $$ = \frac{2\lambda^2 x^2 \cdot \lambda y}{\lambda^2 x^2 + \lambda^2 y^2} $$
    $$ = \frac{\lambda^3 (2x^2y)}{\lambda^2 (x^2+y^2)} $$
3.  **Factor:**
    $$ = \lambda^{3-2} \left( \frac{2x^2y}{x^2+y^2} \right) = \lambda^1 F(x,y) $$
4.  **Conclusion:** Yes, it is a homogeneous function of degree **1**.

---

### 📝 Question 2: Solving a Homogeneous DE
**Solve:** $(2xy + x^2) \frac{dy}{dx} = 3y^2 + 2xy$

**Solution:**
1.  **Rewrite in standard form:**
    $$ \frac{dy}{dx} = \frac{3y^2 + 2xy}{2xy + x^2} $$
    *Observation: Every term ($y^2, xy, x^2$) is of degree 2. Thus, it is Homogeneous.*
2.  **Apply Substitution:**
    Let $y = vx$, so $\frac{dy}{dx} = v + x\frac{dv}{dx}$.
    Substitute into the equation:
    $$ v + x\frac{dv}{dx} = \frac{3(vx)^2 + 2x(vx)}{2x(vx) + x^2} $$
3.  **Simplify the Fraction:**
    $$ v + x\frac{dv}{dx} = \frac{x^2(3v^2 + 2v)}{x^2(2v + 1)} $$
    $$ v + x\frac{dv}{dx} = \frac{3v^2 + 2v}{2v + 1} $$
4.  **Separate Variables:**
    Move $v$ to the right side:
    $$ x\frac{dv}{dx} = \frac{3v^2 + 2v}{2v + 1} - v $$
    Find a common denominator:
    $$ x\frac{dv}{dx} = \frac{3v^2 + 2v - v(2v+1)}{2v + 1} $$
    $$ x\frac{dv}{dx} = \frac{3v^2 + 2v - 2v^2 - v}{2v + 1} = \frac{v^2 + v}{2v + 1} $$
    Now, separate $v$ and $x$:
    $$ \frac{2v + 1}{v^2 + v} dv = \frac{1}{x} dx $$
5.  **Integrate:**
    $$ \int \frac{2v + 1}{v^2 + v} dv = \int \frac{1}{x} dx $$
    *Notice: The numerator $(2v+1)$ is the exact derivative of the denominator $(v^2+v)$.*
    $$ \ln|v^2 + v| = \ln|x| + \ln C $$
    $$ v^2 + v = Cx $$
6.  **Resubstitute $v = y/x$:**
    $$ \left(\frac{y}{x}\right)^2 + \frac{y}{x} = Cx $$
    $$ \frac{y^2 + xy}{x^2} = Cx \implies y^2 + xy = Cx^3 $$

---

### 📝 Question 3: Trigonometric Homogeneous DE
**Solve:** $x \sin\left(\frac{y}{x}\right) dy = \left[ y \sin\left(\frac{y}{x}\right) - x \right] dx$

**Solution:**
1.  **Rewrite in standard form:**
    $$ \frac{dy}{dx} = \frac{y \sin(y/x) - x}{x \sin(y/x)} $$
    $$ \frac{dy}{dx} = \frac{y}{x} - \frac{x}{x \sin(y/x)} = \frac{y}{x} - \frac{1}{\sin(y/x)} $$
    *Observation: The equation is a function of $(y/x)$, so it is Homogeneous.*
2.  **Apply Substitution:**
    Let $y = vx$, so $\frac{dy}{dx} = v + x\frac{dv}{dx}$.
    $$ v + x\frac{dv}{dx} = v - \frac{1}{\sin v} $$
3.  **Simplify:**
    Subtract $v$ from both sides:
    $$ x\frac{dv}{dx} = -\frac{1}{\sin v} = -\csc v $$
4.  **Separate Variables:**
    $$ \sin v \, dv = -\frac{1}{x} dx $$
5.  **Integrate:**
    $$ \int \sin v \, dv = -\int \frac{1}{x} dx $$
    $$ -\cos v = -\ln|x| + C $$
    Multiply by $-1$:
    $$ \cos v = \ln|x| - C $$
6.  **Resubstitute $v = y/x$:**
    $$ \cos\left(\frac{y}{x}\right) = \ln|x| + C' $$

---

**Next Method:** What if the equation looks homogeneous but has constant terms interfering? Proceed to [Method 3: Equations Reducible to Homogeneous Form](./03-reducible-to-homo.md).