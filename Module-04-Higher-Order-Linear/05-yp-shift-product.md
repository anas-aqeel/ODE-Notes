# 🔄 5. Particular Integral ($y_p$): Exponential Shift Rule

Often, the non-homogeneous term $F(x)$ on the right side of a differential equation is not a single function, but a **product** of an exponential function and another function (like a polynomial or a trigonometric function). 

To solve this, we use a powerful technique known as the **Exponential Shift Theorem**.

---

## 1. The Method (Exponential Shift Theorem)

Given a differential equation $f(D)y = e^{ax} V(x)$, where $V(x)$ is any other function (usually $\sin bx$, $\cos bx$, or $x^n$).

The Particular Integral is:
$$ y_p = \frac{1}{f(D)} [e^{ax} V(x)] $$

### 1.1 The Working Rule ($D \to D+a$)
You cannot simply substitute $D=a$ because $V(x)$ is also present. Instead, you "shift" the exponential function to the front of the operator by modifying the operator itself.

1.  **Shift:** Move $e^{ax}$ to the left of the fraction.
2.  **Replace:** Replace every $D$ in the denominator with **$(D + a)$**.
3.  **Simplify:** Expand and simplify the new denominator $f(D+a)$.
4.  **Operate:** You are now left with $e^{ax} \cdot \frac{1}{f(D+a)} V(x)$. Apply the standard rules for $V(x)$ (Trigonometric rule if $V(x)$ is $\sin/\cos$, or Binomial rule if $V(x)$ is $x^n$) to finish the problem.

$$ y_p = e^{ax} \frac{1}{f(D+a)} V(x) $$

---

## 2. Solved Questions

Here are two detailed examples from the lecture notes demonstrating how this shift reduces complex products into standard problems we already know how to solve.

### 📝 Question 1: Product with Trigonometric Function
**Solve for $y_p$:** $(D^2 + 2D + 4)y = e^x \sin 2x$

**Solution:**
$$ y_p = \frac{1}{D^2 + 2D + 4} (e^x \sin 2x) $$

**Step 1: Apply Exponential Shift**
Here, the exponential is $e^{1x}$, so $a = 1$.
We move $e^x$ to the front and replace every $D$ with **$(D + 1)$**.
$$ y_p = e^x \frac{1}{(D+1)^2 + 2(D+1) + 4} \sin 2x $$

**Step 2: Simplify the Denominator**
$$ y_p = e^x \frac{1}{(D^2 + 2D + 1) + 2D + 2 + 4} \sin 2x $$
$$ y_p = e^x \frac{1}{D^2 + 4D + 7} \sin 2x $$

**Step 3: Apply Trigonometric Rule to $V(x)$**
Now we just solve for $\sin 2x$. The rule is to replace $D^2$ with $-b^2 = -(2^2) = -4$.
$$ y_p = e^x \frac{1}{-4 + 4D + 7} \sin 2x $$
$$ y_p = e^x \frac{1}{4D + 3} \sin 2x $$

**Step 4: Rationalize and Finalize**
Multiply the numerator and denominator by the conjugate $(4D - 3)$:
$$ y_p = e^x \frac{4D - 3}{(4D + 3)(4D - 3)} \sin 2x $$
$$ y_p = e^x \frac{4D - 3}{16D^2 - 9} \sin 2x $$
Replace $D^2$ with $-4$ again:
$$ y_p = e^x \frac{4D - 3}{16(-4) - 9} \sin 2x = e^x \frac{4D - 3}{-64 - 9} \sin 2x $$
$$ y_p = e^x \frac{4D - 3}{-73} \sin 2x $$
Apply the numerator operator $(4D - 3)$ to $\sin 2x$:
*   $4D(\sin 2x) = 4(2\cos 2x) = 8\cos 2x$
*   $-3(\sin 2x) = -3\sin 2x$

**Final Answer:**
$$ y_p = -\frac{e^x}{73} (8\cos 2x - 3\sin 2x) $$

---

### 📝 Question 2: Shift Rule resulting in a Case of Failure
**Solve for $y_p$:** $(D^2 - 4D + 13)y = e^{2x} \cos 3x$

**Solution:**
$$ y_p = \frac{1}{D^2 - 4D + 13} (e^{2x} \cos 3x) $$

**Step 1: Apply Exponential Shift**
Here, $a = 2$. Move $e^{2x}$ to the front and replace $D$ with **$(D + 2)$**.
$$ y_p = e^{2x} \frac{1}{(D+2)^2 - 4(D+2) + 13} \cos 3x $$

**Step 2: Simplify the Denominator**
$$ y_p = e^{2x} \frac{1}{(D^2 + 4D + 4) - 4D - 8 + 13} \cos 3x $$
$$ y_p = e^{2x} \frac{1}{D^2 + 9} \cos 3x $$

**Step 3: Apply Trigonometric Rule to $V(x)$**
For $\cos 3x$, replace $D^2$ with $-b^2 = -(3^2) = -9$.
$$ \text{Denominator } = -9 + 9 = 0 $$
**This is a Case of Failure!**

**Step 4: Apply Failure Rule**
Multiply the numerator by $x$ and differentiate the denominator with respect to $D$.
The denominator $D^2 + 9$ differentiates to $2D$.
$$ y_p = e^{2x} \cdot x \cdot \frac{1}{2D} \cos 3x $$

**Step 5: Integrate ($1/D$)**
The operator $\frac{1}{D}$ means integration.
$$ y_p = \frac{x e^{2x}}{2} \int \cos 3x \, dx $$
$$ \int \cos 3x \, dx = \frac{\sin 3x}{3} $$

**Final Answer:**
$$ y_p = \frac{x e^{2x}}{2} \left( \frac{\sin 3x}{3} \right) = \frac{x e^{2x} \sin 3x}{6} $$

---

**Next Method:** What if $F(x)$ is a *sum* of different function types? We can split the problem into parts. Proceed to [Method 6: Principle of Superposition](./06-yp-superposition.md).