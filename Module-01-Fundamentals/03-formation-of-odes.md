# 🏗️ Formation of Differential Equations

Before learning the various techniques to solve Differential Equations (DEs), it is important to understand where they come from. A differential equation is typically formed by taking a standard mathematical equation (which represents a family of curves) and eliminating its arbitrary constants.

---

## 1. Concept Overview

> **Definition:** A differential equation is formed by differentiating an ordinary equation and eliminating its arbitrary constants.

When you have an equation representing a family of curves, it will contain one or more unknown parameters, known as **arbitrary constants** (e.g., $A, B, C, k$). Your goal is to create a new equation that describes the *rate of change* of that family of curves without relying on those specific constants.

---

## 2. The Golden Rule of Formation

To know exactly how many times you need to differentiate the original equation, use this fundamental rule:

> **The Rule:** The number of arbitrary constants in the given general equation is exactly equal to the **Order** of the differential equation you need to form. 
> 
> *   If the equation has **1** arbitrary constant, differentiate **only once**.
> *   If the equation has **2** arbitrary constants, differentiate **twice**.
> *   If the equation has **$n$** arbitrary constants, differentiate **$n$ times**.

---

## 3. Solved Questions

Here are step-by-step examples from the lecture notes demonstrating how to form differential equations.

### 📝 Question 1
Form the differential equation for the given equation by eliminating the arbitrary constant. Also, write its order and degree.
$$ y = Ax + A^2 $$

**Solution:**
1. **Identify the number of arbitrary constants:** 
   There is only **1** arbitrary constant in this equation, which is $A$. Therefore, we must differentiate the equation only **once**.
2. **Differentiate with respect to $x$:**
   $$ \frac{dy}{dx} = A(1) + 0 $$
   Let's denote $\frac{dy}{dx}$ as $y'$. So, $y' = A$.
3. **Eliminate the constant:**
   Now, substitute the value of $A$ ($A = y'$) back into the original equation $y = Ax + A^2$.
   $$ y = x(y') + (y')^2 $$
   Writing this in standard fractional notation:
   $$ y = x \frac{dy}{dx} + \left(\frac{dy}{dx}\right)^2 $$
   *(This is the required differential equation, free of the constant $A$.)*
4. **Determine Order and Degree:**
   *   **Order:** The highest derivative is $\frac{dy}{dx}$, so the Order is **1**.
   *   **Degree:** The highest power of $\frac{dy}{dx}$ is $2$, so the Degree is **2**.

---

### 📝 Question 2
Form the differential equation for the given equation by eliminating the arbitrary constants.
$$ y = A\cos x + B\sin x $$

**Solution:**
1. **Identify the number of arbitrary constants:** 
   There are **2** arbitrary constants in this equation: $A$ and $B$. Therefore, we must differentiate the equation **twice**.
2. **First Differentiation:**
   Differentiate $y$ with respect to $x$:
   $$ y' = -A\sin x + B\cos x $$
3. **Second Differentiation:**
   Differentiate $y'$ with respect to $x$ to get the second derivative:
   $$ y'' = -A\cos x - B\sin x $$
4. **Eliminate the constants:**
   Notice that in the second derivative, we can factor out a negative sign:
   $$ y'' = -(A\cos x + B\sin x) $$
   Look closely at the expression inside the parentheses; it is exactly our original equation for $y$!
   Substitute $y$ back in:
   $$ y'' = -y $$
   Rearranging to standard form gives us the final differential equation:
   $$ y'' + y = 0 $$
5. **Determine Order and Degree (Bonus):**
   *   **Order:** The highest derivative is $y''$ ($\frac{d^2y}{dx^2}$), so the Order is **2**.
   *   **Degree:** The power of $y''$ is $1$, so the Degree is **1**.

---

**Next Steps:** Test your understanding of these concepts with the [Module 1 Practice Questions](./04-practice-questions.md).