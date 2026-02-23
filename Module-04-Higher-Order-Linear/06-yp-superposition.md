## 📝 Method: Linearity / Superposition (Sum of Functions)

When the function $F(x)$ on the right side is a sum of different types of functions (e.g., an exponential plus a trigonometric function), we apply the **Principle of Superposition**. We split the Particular Integral into separate parts, solve each using its specific rule, and add them together.

### 📝 Example: Mixed Functions
**Solve:** $\frac{d^2y}{dx^2} - 2\frac{dy}{dx} - 3y = 2e^{2x} + 10\sin 3x$

**Solution:**
**1. Find $y_c$:**
   $m^2 - 2m - 3 = 0 \implies (m-3)(m+1) = 0 \implies m = 3, -1$
   $y_c = C_1 e^{3x} + C_2 e^{-x}$

**2. Set up $y_p$:**
   $y_p = \frac{1}{D^2 - 2D - 3} (2e^{2x} + 10\sin 3x)$
   Split into two parts: $y_p = y_{p1} + y_{p2}$

**3. Solve $y_{p1}$ (Exponential Rule):**
   $y_{p1} = 2 \frac{1}{D^2 - 2D - 3} e^{2x}$
   Substitute $D = 2$:
   $y_{p1} = 2 \frac{1}{(2)^2 - 2(2) - 3} e^{2x} = 2 \frac{1}{4 - 4 - 3} e^{2x} = -\frac{2}{3} e^{2x}$

**4. Solve $y_{p2}$ (Trigonometric Rule):**
   $y_{p2} = 10 \frac{1}{D^2 - 2D - 3} \sin 3x$
   Substitute $D^2 = -(3^2) = -9$:
   $y_{p2} = 10 \frac{1}{-9 - 2D - 3} \sin 3x = 10 \frac{1}{-2D - 12} \sin 3x = -5 \frac{1}{D + 6} \sin 3x$
   Rationalize the denominator by multiplying by $(D-6)$:
   $y_{p2} = -5 \frac{D - 6}{D^2 - 36} \sin 3x$
   Substitute $D^2 = -9$ again:
   $y_{p2} = -5 \frac{D - 6}{-9 - 36} \sin 3x = \frac{-5}{-45} (D - 6) \sin 3x = \frac{1}{9} [D(\sin 3x) - 6\sin 3x]$
   $y_{p2} = \frac{1}{9} (3\cos 3x - 6\sin 3x) = \frac{1}{3}\cos 3x - \frac{2}{3}\sin 3x$

**5. Final General Solution:**
   $y = y_c + y_{p1} + y_{p2}$
   $$ y = C_1 e^{3x} + C_2 e^{-x} - \frac{2}{3} e^{2x} + \frac{1}{3}\cos 3x - \frac{2}{3}\sin 3x $$

---

**Next Steps:** Put all the methods together with the [Module 4 Practice Questions](./07-practice-questions.md).