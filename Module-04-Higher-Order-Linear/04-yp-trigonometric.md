# 📉 4. Particular Integral ($y_p$): Trigonometric Case

When the right-hand side of a linear differential equation contains sine or cosine functions ($F(x) = \sin ax$ or $\cos ax$), we use a specific substitution rule involving the square of the differential operator ($D^2$).

---

## 1. The Method ($D^2 \to -a^2$)

Given a differential equation $f(D^2)y = \sin ax$ (or $\cos ax$):

The Particular Integral is:
$$ y_p = \frac{1}{f(D^2)} \sin ax $$

### 1.1 The Rule
Replace every instance of **$D^2$** with **$-a^2$**.

$$ y_p = \frac{1}{f(-a^2)} \sin ax $$

> **⚠️ Important Warning:**
> The negative sign is **outside** the square.
> *   If $a = 2$, then $D^2$ becomes $-(2^2) = -4$.
> *   It does **NOT** become $(-2)^2 = +4$.

### 1.2 Handling Remaining $D$ Terms (Rationalization)
If replacing $D^2$ leaves a $D$ term in the denominator (e.g., $D - 3$), you cannot substitute $-a^2$ for $D$ directly. Instead:
1.  Multiply the numerator and denominator by the conjugate (e.g., $D + 3$).
2.  This creates a difference of squares ($D^2 - 9$) in the denominator.
3.  Replace the new $D^2$ with $-a^2$ again.
4.  Apply the numerator operator to the function.

---

## 2. The Case of Failure ($f(-a^2) = 0$)

If replacing $D^2$ with $-a^2$ causes the denominator to become zero, the method fails. We apply the standard failure rule:

1.  Multiply the numerator by $x$.
2.  Differentiate the denominator with respect to $D$ ($f'(D)$).
3.  Try the substitution again.

$$ y_p = x \cdot \frac{1}{f'(D)} \sin ax $$

---

## 3. Solved Questions

Here are three distinct cases from the lecture notes: a standard substitution, a rationalization case, and a case of failure.

### 📝 Question 1: Standard Substitution
**Solve for $y_p$:** $(D^2 + 4)y = \sin 3x$

**Solution:**
$$ y_p = \frac{1}{D^2 + 4} \sin 3x $$

**Step 1: Identify $a$**
Here, $a = 3$. Therefore, $-a^2 = -(3^2) = -9$.

**Step 2: Substitute $D^2 = -9$**
$$ y_p = \frac{1}{-9 + 4} \sin 3x $$
$$ y_p = \frac{1}{-5} \sin 3x $$

**Final Answer:**
$$ y_p = -\frac{1}{5} \sin 3x $$

---

### 📝 Question 2: Rationalization Required
**Solve for $y_p$:** $(D^2 + D + 1)y = \cos 2x$

**Solution:**
$$ y_p = \frac{1}{D^2 + D + 1} \cos 2x $$

**Step 1: Identify $a$ and Substitute**
Here, $a = 2$. So, $D^2 \to -4$.
$$ y_p = \frac{1}{-4 + D + 1} \cos 2x $$
$$ y_p = \frac{1}{D - 3} \cos 2x $$

**Step 2: Rationalize the Denominator**
We still have a $D$ in the denominator. Multiply numerator and denominator by the conjugate $(D+3)$.
$$ y_p = \frac{D + 3}{(D - 3)(D + 3)} \cos 2x $$
$$ y_p = \frac{D + 3}{D^2 - 9} \cos 2x $$

**Step 3: Substitute $D^2$ again**
Replace $D^2$ with $-4$ again.
$$ y_p = \frac{D + 3}{-4 - 9} \cos 2x $$
$$ y_p = \frac{D + 3}{-13} \cos 2x $$

**Step 4: Operate Numerator**
Apply $(D+3)$ to $\cos 2x$:
$$ y_p = -\frac{1}{13} [ D(\cos 2x) + 3\cos 2x ] $$
*   Derivative $D(\cos 2x) = -2\sin 2x$
$$ y_p = -\frac{1}{13} [-2\sin 2x + 3\cos 2x] $$

**Final Answer:**
$$ y_p = \frac{2\sin 2x - 3\cos 2x}{13} $$

---

### 📝 Question 3: Case of Failure
**Solve for $y_p$:** $(D^2 + 4)y = \cos 2x$

**Solution:**
$$ y_p = \frac{1}{D^2 + 4} \cos 2x $$

**Step 1: Check Substitution**
Here $a = 2$, so $D^2 \to -4$.
Denominator becomes $-4 + 4 = 0$. **Method Fails.**

**Step 2: Apply Failure Rule**
Multiply by $x$ and differentiate the denominator ($D^2 + 4 \to 2D$).
$$ y_p = x \cdot \frac{1}{2D} \cos 2x $$

**Step 3: Interpret $1/D$**
The operator $\frac{1}{D}$ represents **Integration**.
$$ y_p = \frac{x}{2} \int \cos 2x \, dx $$

**Step 4: Integrate**
$$ \int \cos 2x \, dx = \frac{\sin 2x}{2} $$
$$ y_p = \frac{x}{2} \left( \frac{\sin 2x}{2} \right) $$

**Final Answer:**
$$ y_p = \frac{x \sin 2x}{4} $$

---

**Next Method:** Sometimes we have a product of two functions, like $e^x \sin x$. For this, we use the Shift Rule. Proceed to [Method 4: Shift & Product Rules](./05-yp-shift-product.md).