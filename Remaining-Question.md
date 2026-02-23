# Course Supplement: Practice Questions & Solutions
### Ordinary Differential Equations (ODEs) & Linear Algebra
This document serves as a supplementary guide to the main course PDF, capturing all additional homework and practice questions from the handwritten notes and lecture materials. 

---

## Module 2: Solving First-Order ODEs

### 2.1 Variable Separable Method

**Question 1:**
Solve: $y(1+x^2)^{1/2}dy + x\sqrt{1+y^2}dx = 0$

**Solution:**
1. **Separate Variables:** Move the $dx$ term to the right side:
   $$y(1+x^2)^{1/2}dy = -x\sqrt{1+y^2}dx$$
   Divide by $(1+x^2)^{1/2}$ and $\sqrt{1+y^2}$:
   $$\frac{y}{\sqrt{1+y^2}}dy = -\frac{x}{\sqrt{1+x^2}}dx$$
2. **Integrate both sides:**
   $$\int \frac{y}{\sqrt{1+y^2}}dy = -\int \frac{x}{\sqrt{1+x^2}}dx$$
   *(Multiply and divide by 2 on both sides to match the exact derivative of the inside of the root)*
   $$\frac{1}{2}\int (1+y^2)^{-1/2}(2y)dy = -\frac{1}{2}\int (1+x^2)^{-1/2}(2x)dx$$
   $$\frac{1}{2} \left[ \frac{(1+y^2)^{1/2}}{1/2} \right] = -\frac{1}{2} \left[ \frac{(1+x^2)^{1/2}}{1/2} \right] + C$$
   $$\sqrt{1+y^2} = -\sqrt{1+x^2} + C$$
3. **Final General Solution:**
   $$\sqrt{1+x^2} + \sqrt{1+y^2} = C$$

**Question 2:**
Solve: $\frac{dy}{dx} = (4x+y+1)^2$

**Solution:**
1. **Substitution:** This equation is not separable in its current form, but it can be reduced to separable. Let $v = 4x+y+1$.
   Differentiate with respect to $x$:
   $$\frac{dv}{dx} = 4 + \frac{dy}{dx} \implies \frac{dy}{dx} = \frac{dv}{dx} - 4$$
2. **Substitute into the equation:**
   $$\frac{dv}{dx} - 4 = v^2 \implies \frac{dv}{dx} = v^2 + 4$$
3. **Separate Variables and Integrate:**
   $$\frac{dv}{v^2+4} = dx$$
   $$\int \frac{1}{v^2+2^2}dv = \int dx$$
   $$\frac{1}{2}\tan^{-1}\left(\frac{v}{2}\right) = x + C_1$$
4. **Resubstitute $v$ and simplify:**
   $$\tan^{-1}\left(\frac{4x+y+1}{2}\right) = 2x + 2C_1$$
   **Final Answer:**
   $$4x+y+1 = 2\tan(2x+C)$$ *(where $C = 2C_1$)*

**Question 3:**
Solve: $(x+1)\frac{dy}{dx} + 1 = 2e^{-y}$

**Solution:**
1. **Rearrange:**
   $$(x+1)\frac{dy}{dx} = 2e^{-y} - 1$$
2. **Separate Variables:**
   $$\frac{dy}{2e^{-y}-1} = \frac{dx}{x+1}$$
   Multiply numerator and denominator of the LHS by $e^y$:
   $$\frac{e^y}{2-e^y}dy = \frac{dx}{x+1}$$
3. **Integrate both sides:**
   $$\int \frac{e^y}{2-e^y}dy = \int \frac{1}{x+1}dx$$
   Let $u = 2-e^y \implies du = -e^y dy$:
   $$-\int \frac{-e^y}{2-e^y}dy = \ln|x+1| + \ln C$$
   $$-\ln|2-e^y| = \ln|x+1| + \ln C$$
4. **Simplify using Log rules:**
   $$\ln|2-e^y|^{-1} = \ln|C(x+1)| \implies \frac{1}{2-e^y} = C(x+1)$$
   **Final Answer:**
   $$(x+1)(2-e^y) = K$$ *(where $K = 1/C$)*

---

### 2.2 Homogeneous Differential Equations

**Question 4:**
Solve: $\frac{dy}{dx} + \frac{x-2y}{2x-y} = 0$

**Solution:**
1. **Standard Form:** $\frac{dy}{dx} = \frac{2y-x}{2x-y}$
2. **Substitute:** Let $y=vx \implies \frac{dy}{dx} = v+x\frac{dv}{dx}$
   $$v+x\frac{dv}{dx} = \frac{2vx-x}{2x-vx} = \frac{x(2v-1)}{x(2-v)} = \frac{2v-1}{2-v}$$
3. **Separate Variables:**
   $$x\frac{dv}{dx} = \frac{2v-1}{2-v} - v = \frac{2v-1-2v+v^2}{2-v} = \frac{v^2-1}{2-v}$$
   $$\frac{2-v}{v^2-1}dv = \frac{dx}{x}$$
4. **Partial Fractions:** $\frac{2-v}{(v-1)(v+1)} = \frac{A}{v-1} + \frac{B}{v+1}$
   $2-v = A(v+1) + B(v-1) \implies A = 1/2, B = -3/2$
   $$\int \left( \frac{1/2}{v-1} - \frac{3/2}{v+1} \right)dv = \int \frac{dx}{x}$$
   $$\frac{1}{2}\ln|v-1| - \frac{3}{2}\ln|v+1| = \ln|x| + \ln C$$
   Multiply by 2:
   $$\ln|v-1| - 3\ln|v+1| = 2\ln|x| + \ln K$$
   $$\ln \left| \frac{v-1}{(v+1)^3} \right| = \ln(Kx^2) \implies \frac{v-1}{(v+1)^3} = Kx^2$$
5. **Resubstitute $v = y/x$:**
   $$\frac{y/x-1}{(y/x+1)^3} = Kx^2 \implies \frac{\frac{y-x}{x}}{\frac{(y+x)^3}{x^3}} = Kx^2 \implies \frac{x^2(y-x)}{(y+x)^3} = Kx^2$$
   **Final Answer:**
   $$y-x = K(y+x)^3$$

**Question 5:**
Solve: $(x^2+y^2)dy = xy dx$

**Solution:**
1. **Standard Form:** $\frac{dy}{dx} = \frac{xy}{x^2+y^2}$
2. **Substitute:** Let $y=vx \implies \frac{dy}{dx} = v+x\frac{dv}{dx}$
   $$v+x\frac{dv}{dx} = \frac{x(vx)}{x^2+(vx)^2} = \frac{v}{1+v^2}$$
3. **Separate Variables:**
   $$x\frac{dv}{dx} = \frac{v}{1+v^2} - v = \frac{v - v - v^3}{1+v^2} = \frac{-v^3}{1+v^2}$$
   $$\frac{1+v^2}{v^3}dv = -\frac{dx}{x} \implies \left(v^{-3} + \frac{1}{v}\right)dv = -\frac{dx}{x}$$
4. **Integrate:**
   $$-\frac{1}{2v^2} + \ln|v| = -\ln|x| + C$$
5. **Resubstitute $v = y/x$:**
   $$-\frac{x^2}{2y^2} + \ln\left|\frac{y}{x}\right| + \ln|x| = C \implies -\frac{x^2}{2y^2} + \ln|y| - \ln|x| + \ln|x| = C$$
   **Final Answer:**
   $$\ln|y| - \frac{x^2}{2y^2} = C$$

**Question 6:**
Solve: $(x^3-3xy^2)dx + (y^3-3x^2y)dy = 0$

**Solution:**
1. **Standard Form:** $\frac{dy}{dx} = \frac{3xy^2-x^3}{y^3-3x^2y}$
2. **Substitute:** Let $y=vx \implies \frac{dy}{dx} = v+x\frac{dv}{dx}$
   $$v+x\frac{dv}{dx} = \frac{3v^2-1}{v^3-3v}$$
3. **Separate Variables:**
   $$x\frac{dv}{dx} = \frac{3v^2-1}{v^3-3v} - v = \frac{3v^2-1-v^4+3v^2}{v^3-3v} = \frac{-v^4+6v^2-1}{v^3-3v}$$
   $$\frac{v^3-3v}{v^4-6v^2+1}dv = -\frac{dx}{x}$$
4. **Integrate:** Let $u = v^4-6v^2+1 \implies du = (4v^3-12v)dv = 4(v^3-3v)dv$
   $$\frac{1}{4} \int \frac{du}{u} = -\int \frac{dx}{x}$$
   $$\frac{1}{4}\ln|v^4-6v^2+1| = -\ln x + \ln C \implies \ln(v^4-6v^2+1) = \ln(C^4 x^{-4})$$
5. **Resubstitute $v = y/x$:**
   $$\left(\frac{y}{x}\right)^4 - 6\left(\frac{y}{x}\right)^2 + 1 = \frac{K}{x^4}$$
   Multiply by $x^4$:
   **Final Answer:**
   $$y^4 - 6x^2y^2 + x^4 = K$$

**Question 7:**
Solve: $\frac{dy}{dx} = \frac{3xy+y^2}{3x^2}$

**Solution:**
1. **Substitute:** Let $y=vx \implies \frac{dy}{dx} = v+x\frac{dv}{dx}$
   $$v+x\frac{dv}{dx} = \frac{3x(vx)+(vx)^2}{3x^2} = \frac{3v+v^2}{3} = v + \frac{v^2}{3}$$
2. **Separate Variables:**
   $$x\frac{dv}{dx} = \frac{v^2}{3} \implies \frac{3}{v^2}dv = \frac{dx}{x}$$
3. **Integrate:**
   $$3\left(-\frac{1}{v}\right) = \ln|x| + C$$
4. **Resubstitute $v = y/x$:**
   $$-\frac{3x}{y} = \ln|x| + C \implies -3x = y\ln|x| + Cy$$
   **Final Answer:**
   $$3x + y\ln x + Cy = 0$$

**Question 8:**
Solve: $[x\cos(\frac{y}{x}) + y\sin(\frac{y}{x})]y - [y\sin(\frac{y}{x}) - x\cos(\frac{y}{x})]x \frac{dy}{dx} = 0$

**Solution:**
1. **Standard Form:**
   $$\frac{dy}{dx} = \frac{y[x\cos(y/x) + y\sin(y/x)]}{x[y\sin(y/x) - x\cos(y/x)]}$$
2. **Substitute:** Let $y=vx \implies \frac{dy}{dx} = v+x\frac{dv}{dx}$
   $$v+x\frac{dv}{dx} = \frac{vx[x\cos v + vx\sin v]}{x[vx\sin v - x\cos v]} = \frac{v(\cos v + v\sin v)}{v\sin v - \cos v}$$
3. **Separate Variables:**
   $$x\frac{dv}{dx} = \frac{v\cos v + v^2\sin v - v^2\sin v + v\cos v}{v\sin v - \cos v} = \frac{2v\cos v}{v\sin v - \cos v}$$
   $$\frac{v\sin v - \cos v}{v\cos v}dv = \frac{2dx}{x} \implies \left(\tan v - \frac{1}{v}\right)dv = \frac{2dx}{x}$$
4. **Integrate:**
   $$\int \tan v dv - \int \frac{1}{v} dv = 2\int \frac{dx}{x}$$
   $$\ln|\sec v| - \ln|v| = 2\ln|x| + \ln C \implies -\ln|\cos v| - \ln|v| = \ln(Cx^2)$$
   $$\ln\left(\frac{1}{v\cos v}\right) = \ln(Cx^2) \implies \frac{1}{v\cos v} = Cx^2$$
5. **Resubstitute $v = y/x$:**
   $$\frac{x}{y\cos(y/x)} = Cx^2 \implies \frac{1}{xy\cos(y/x)} = C$$
   **Final Answer:**
   $$xy\cos(y/x) = K$$

**Question 9:**
Solve: $x \frac{dy}{dx} = y(\log y - \log x + 1)$

**Solution:**
1. **Standard Form:** $\frac{dy}{dx} = \frac{y}{x}\left(\ln\left(\frac{y}{x}\right) + 1\right)$
2. **Substitute:** Let $y=vx \implies \frac{dy}{dx} = v+x\frac{dv}{dx}$
   $$v+x\frac{dv}{dx} = v(\ln v + 1) = v\ln v + v$$
3. **Separate Variables:**
   $$x\frac{dv}{dx} = v\ln v \implies \frac{dv}{v\ln v} = \frac{dx}{x}$$
4. **Integrate:** Let $u = \ln v \implies du = \frac{1}{v}dv$
   $$\int \frac{1}{u}du = \int \frac{dx}{x} \implies \ln|u| = \ln|x| + \ln C$$
   $$\ln|\ln v| = \ln|Cx| \implies \ln v = Cx$$
5. **Resubstitute $v = y/x$:**
   **Final Answer:**
   $$\ln\left(\frac{y}{x}\right) = Cx \implies y = xe^{Cx}$$

---

### 2.3 Linear Differential Equations

**Question 10:**
Solve: $(2y-3x)dx + xdy = 0$

**Solution:**
1. **Standard Form:** Divide by $x dx$:
   $$\frac{dy}{dx} + \frac{2}{x}y = 3$$
2. **Identify $P(x)$ and find I.F.:** $P(x) = \frac{2}{x}$
   $$I.F. = e^{\int \frac{2}{x}dx} = e^{2\ln x} = x^2$$
3. **General Solution Formula:**
   $$y \cdot (x^2) = \int 3 \cdot x^2 dx + C$$
   $$y x^2 = x^3 + C$$
   **Final Answer:**
   $$xy = \frac{x^2}{y} \dots \text{(Simplified to: )} x^2y - x^3 = C$$

**Question 11:**
Solve: $\frac{dy}{dx} + y\cot x = \cos x$

**Solution:**
1. **Identify $P(x)$ and find I.F.:** $P(x) = \cot x$
   $$I.F. = e^{\int \cot x dx} = e^{\ln(\sin x)} = \sin x$$
2. **General Solution Formula:**
   $$y \cdot (\sin x) = \int \cos x \cdot \sin x dx + C$$
   $$y\sin x = \int \frac{\sin 2x}{2} dx + C \quad \text{OR} \quad y\sin x = \frac{\sin^2 x}{2} + C$$
   **Final Answer:**
   $$y\sin x = \frac{\sin^2 x}{2} + C$$

**Question 12:**
Solve: $\frac{dy}{dx} + 2xy = 2e^{-x^2}$

**Solution:**
1. **Identify $P(x)$ and find I.F.:** $P(x) = 2x$
   $$I.F. = e^{\int 2x dx} = e^{x^2}$$
2. **General Solution Formula:**
   $$y \cdot (e^{x^2}) = \int 2e^{-x^2} \cdot e^{x^2} dx + C$$
   $$y e^{x^2} = \int 2 dx + C$$
   $$y e^{x^2} = 2x + C$$
   **Final Answer:**
   $$y = (2x+C)e^{-x^2}$$

**Question 13:**
Solve: $\frac{dy}{dx} + y\sec x = \tan x$

**Solution:**
1. **Identify $P(x)$ and find I.F.:** $P(x) = \sec x$
   $$I.F. = e^{\int \sec x dx} = e^{\ln(\sec x + \tan x)} = \sec x + \tan x$$
2. **General Solution Formula:**
   $$y(\sec x + \tan x) = \int \tan x(\sec x + \tan x)dx + C$$
   $$y(\sec x + \tan x) = \int (\sec x \tan x + \sec^2 x - 1) dx + C$$
   **Final Answer:**
   $$y(\sec x + \tan x) = \sec x + \tan x - x + C$$

**Question 14:**
Solve: $\cos^2 x \frac{dy}{dx} + y = \tan x$

**Solution:**
1. **Standard Form:** Divide by $\cos^2 x$:
   $$\frac{dy}{dx} + \sec^2 x \cdot y = \tan x \sec^2 x$$
2. **Identify $P(x)$ and find I.F.:** $P(x) = \sec^2 x$
   $$I.F. = e^{\int \sec^2 x dx} = e^{\tan x}$$
3. **General Solution Formula:**
   $$y \cdot e^{\tan x} = \int e^{\tan x} \tan x \sec^2 x dx + C$$
   Let $u = \tan x, du = \sec^2 x dx$:
   $$\int u e^u du = ue^u - e^u = e^{\tan x}(\tan x - 1)$$
   **Final Answer:**
   $$y e^{\tan x} = e^{\tan x}(\tan x - 1) + C \implies y = \tan x - 1 + Ce^{-\tan x}$$

---

### 2.4 Bernoulli's Equations

**Question 15:**
Solve: $x\frac{dy}{dx} = \frac{y^2-1}{y}$

**Solution:**
1. **Standard Form:** 
   $$x\frac{dy}{dx} = y - y^{-1} \implies \frac{dy}{dx} - \frac{1}{x}y = -\frac{1}{x}y^{-1}$$
   *(This is Bernoulli with $n = -1$)*.
2. **Divide by $y^n$:** Multiply by $y$:
   $$y\frac{dy}{dx} - \frac{1}{x}y^2 = -\frac{1}{x}$$
3. **Substitution:** Let $z = y^2 \implies \frac{dz}{dx} = 2y\frac{dy}{dx} \implies \frac{1}{2}\frac{dz}{dx} = y\frac{dy}{dx}$.
   $$\frac{1}{2}\frac{dz}{dx} - \frac{1}{x}z = -\frac{1}{x} \implies \frac{dz}{dx} - \frac{2}{x}z = -\frac{2}{x}$$
4. **Solve Linear DE for z:**
   $$I.F. = e^{\int -\frac{2}{x} dx} = e^{-2\ln x} = x^{-2}$$
   $$z \cdot x^{-2} = \int -\frac{2}{x} \cdot x^{-2} dx + C = \int -2x^{-3} dx + C$$
   $$z x^{-2} = x^{-2} + C \implies z = 1 + Cx^2$$
5. **Resubstitute $z = y^2$:**
   **Final Answer:**
   $$y^2 = Cx^2 + 1$$

**Question 16:**
Solve: $\frac{dy}{dx} + y = xy^3$

**Solution:**
1. **Divide by $y^3$:**
   $$y^{-3}\frac{dy}{dx} + y^{-2} = x$$
2. **Substitution:** Let $z = y^{-2} \implies \frac{dz}{dx} = -2y^{-3}\frac{dy}{dx} \implies -\frac{1}{2}\frac{dz}{dx} = y^{-3}\frac{dy}{dx}$
   $$-\frac{1}{2}\frac{dz}{dx} + z = x \implies \frac{dz}{dx} - 2z = -2x$$
3. **Solve Linear DE for z:**
   $$I.F. = e^{\int -2 dx} = e^{-2x}$$
   $$z e^{-2x} = \int -2x e^{-2x} dx + C$$
   Integration by parts:
   $$-2 \left[ x\frac{e^{-2x}}{-2} - \int \frac{e^{-2x}}{-2}dx \right] = x e^{-2x} + \frac{1}{2}e^{-2x} + C$$
   $$z = x + \frac{1}{2} + Ce^{2x}$$
4. **Resubstitute $z = y^{-2}$:**
   **Final Answer:**
   $$\frac{1}{y^2} = x + \frac{1}{2} + Ce^{2x}$$

**Question 17:**
Solve: $\frac{dy}{dx} + (\frac{x}{1-x^2})y = x\sqrt{y}$

**Solution:**
1. **Divide by $y^{1/2}$:**
   $$y^{-1/2}\frac{dy}{dx} + \left(\frac{x}{1-x^2}\right)y^{1/2} = x$$
2. **Substitution:** Let $z = y^{1/2} \implies \frac{dz}{dx} = \frac{1}{2}y^{-1/2}\frac{dy}{dx} \implies 2\frac{dz}{dx} = y^{-1/2}\frac{dy}{dx}$
   $$2\frac{dz}{dx} + \left(\frac{x}{1-x^2}\right)z = x \implies \frac{dz}{dx} + \frac{x}{2(1-x^2)}z = \frac{x}{2}$$
3. **Solve Linear DE for z:**
   $$I.F. = e^{\int \frac{x}{2(1-x^2)}dx}$$
   Let $u = 1-x^2 \implies du = -2xdx \implies xdx = -du/2$.
   $$I.F. = e^{-\frac{1}{4}\int \frac{du}{u}} = e^{-\frac{1}{4}\ln(1-x^2)} = (1-x^2)^{-1/4}$$
   $$z (1-x^2)^{-1/4} = \int \frac{x}{2}(1-x^2)^{-1/4} dx + C$$
   Again, using substitution $u = 1-x^2$:
   $$= -\frac{1}{4}\int u^{-1/4} du = -\frac{1}{4} \left[ \frac{u^{3/4}}{3/4} \right] = -\frac{1}{3}u^{3/4} = -\frac{1}{3}(1-x^2)^{3/4} + C$$
   $$z = -\frac{1}{3}(1-x^2) + C(1-x^2)^{1/4}$$
4. **Resubstitute $z = \sqrt{y}$:**
   **Final Answer:**
   $$\sqrt{y} = -\frac{1}{3}(1-x^2) + C(1-x^2)^{1/4}$$

---

## Module 3: Applications of First-Order ODEs

### 3.1 Orthogonal Trajectories

**Question 18:**
Find the orthogonal trajectories of $16x^2 + y^2 = a$

**Solution:**
1. **Differentiate:** 
   $$32x + 2y\frac{dy}{dx} = 0 \implies \frac{dy}{dx} = -\frac{16x}{y}$$
2. **Apply Orthogonality Condition:** Replace $\frac{dy}{dx}$ with $-\frac{dx}{dy}$
   $$-\frac{dx}{dy} = -\frac{16x}{y} \implies \frac{dx}{x} = 16\frac{dy}{y}$$
3. **Integrate:**
   $$\ln|x| = 16\ln|y| + \ln C \implies \ln|x| = \ln(C y^{16})$$
   **Final Answer:**
   $$x = C y^{16} \quad \text{or} \quad y^{16} = Kx$$

**Question 19:**
Find the orthogonal trajectories of $y^2 = cx^3$

**Solution:**
1. **Differentiate & Eliminate c:** 
   $$2y\frac{dy}{dx} = 3cx^2$$
   From original, $c = y^2/x^3$.
   $$2y\frac{dy}{dx} = 3\left(\frac{y^2}{x^3}\right)x^2 = \frac{3y^2}{x} \implies \frac{dy}{dx} = \frac{3y}{2x}$$
2. **Apply Orthogonality Condition:** 
   $$-\frac{dx}{dy} = \frac{3y}{2x} \implies -2x dx = 3y dy$$
3. **Integrate:**
   $$-\int 2x dx = \int 3y dy \implies -x^2 = \frac{3y^2}{2} + C_1$$
   **Final Answer:**
   $$2x^2 + 3y^2 = C$$ *(A family of ellipses).*

---

## Module 4: Higher-Order Linear ODEs 

### 4.1 Particular Integral: Exponential Case

**Question 20:**
Solve: $\frac{d^2y}{dx^2} - 6\frac{dy}{dx} + 9y = e^{3x}$

**Solution:**
1. **Find $y_c$:** $m^2 - 6m + 9 = 0 \implies (m-3)^2 = 0 \implies m = 3, 3$.
   $$y_c = (C_1 + C_2x)e^{3x}$$
2. **Find $y_p$:** 
   $$y_p = \frac{1}{(D-3)^2} e^{3x}$$
   Sub $D=3$: Denominator is 0. (Failure).
   Multiply by $x$, diff denominator: $y_p = x \frac{1}{2(D-3)} e^{3x}$. Sub $D=3 \implies 0$ again.
   Multiply by $x$ again, diff denominator: $y_p = x^2 \frac{1}{2} e^{3x}$.
3. **Final General Solution:**
   $$y = y_c + y_p = (C_1 + C_2x)e^{3x} + \frac{x^2}{2}e^{3x}$$

---

### 4.2 Particular Integral: Algebraic Case

**Question 21:**
Solve: $\frac{d^2y}{dx^2} + 2\frac{dy}{dx} + y = x$

**Solution:**
1. **Find $y_c$:** $m^2 + 2m + 1 = 0 \implies (m+1)^2 = 0 \implies m = -1, -1$.
   $$y_c = (C_1 + C_2x)e^{-x}$$
2. **Find $y_p$:** 
   $$y_p = \frac{1}{1+2D+D^2} x = (1 + 2D + D^2)^{-1} x$$
   Using binomial expansion $(1+X)^{-1} \approx 1 - X$:
   $$y_p = [1 - (2D+D^2) + \dots]x = (1 - 2D)x$$
   $$y_p = x - 2D(x) = x - 2$$
3. **Final General Solution:**
   $$y = (C_1 + C_2x)e^{-x} + x - 2$$

---

### 4.3 Particular Integral: Trigonometric & Shift Cases

**Question 22:**
Solve: $\frac{d^2y}{dx^2} + 6y = \sin 4x$

**Solution:**
1. **Find $y_c$:** $m^2 + 6 = 0 \implies m = \pm i\sqrt{6}$.
   $$y_c = C_1\cos(\sqrt{6}x) + C_2\sin(\sqrt{6}x)$$
2. **Find $y_p$:** 
   $$y_p = \frac{1}{D^2+6} \sin 4x$$
   Replace $D^2$ with $-(4^2) = -16$:
   $$y_p = \frac{1}{-16+6} \sin 4x = -\frac{1}{10} \sin 4x$$
3. **Final General Solution:**
   $$y = C_1\cos(\sqrt{6}x) + C_2\sin(\sqrt{6}x) - \frac{1}{10}\sin 4x$$

**Question 23:**
Solve: $\frac{d^2x}{dt^2} + 2\frac{dx}{dt} + 3x = \sin t$

**Solution:**
1. **Find $x_c$:** $m^2 + 2m + 3 = 0 \implies m = \frac{-2 \pm \sqrt{4-12}}{2} = -1 \pm i\sqrt{2}$.
   $$x_c = e^{-t}(C_1\cos(\sqrt{2}t) + C_2\sin(\sqrt{2}t))$$
2. **Find $x_p$:** 
   $$x_p = \frac{1}{D^2+2D+3} \sin t$$
   Replace $D^2$ with $-(1^2) = -1$:
   $$x_p = \frac{1}{-1+2D+3} \sin t = \frac{1}{2D+2} \sin t$$
   Rationalize by multiplying numerator and denominator by $(D-1)$ (and extract 1/2):
   $$x_p = \frac{1}{2} \left[ \frac{D-1}{D^2-1} \right] \sin t$$
   Replace $D^2 = -1$ again:
   $$x_p = \frac{1}{2} \left[ \frac{D-1}{-1-1} \right] \sin t = -\frac{1}{4}(D-1)\sin t$$
   $$x_p = -\frac{1}{4}(\cos t - \sin t)$$
3. **Final General Solution:**
   $$x(t) = e^{-t}(C_1\cos(\sqrt{2}t) + C_2\sin(\sqrt{2}t)) - \frac{1}{4}\cos t + \frac{1}{4}\sin t$$

**Question 24:**
Solve: $\frac{d^2y}{dx^2} + 4y = x \sin 2x$

**Solution:**
1. **Find $y_c$:** $m^2 + 4 = 0 \implies m = \pm 2i$.
   $$y_c = C_1\cos 2x + C_2\sin 2x$$
2. **Find $y_p$:** Use Euler's relation $\sin 2x = \text{Im}(e^{2ix})$. We solve for $e^{2ix}$ and take the imaginary part.
   $$y_p = \text{Im} \left[ \frac{1}{D^2+4} x e^{2ix} \right]$$
   Apply Exponential Shift (Shift $e^{2ix}$ to the front, replace $D \to D+2i$):
   $$y_p = \text{Im} \left[ e^{2ix} \frac{1}{(D+2i)^2+4} x \right] = \text{Im} \left[ e^{2ix} \frac{1}{D^2+4iD-4+4} x \right]$$
   $$y_p = \text{Im} \left[ e^{2ix} \frac{1}{4iD(1+\frac{D}{4i})} x \right]$$
   Expand the binomial up to $D$: $(1+\frac{D}{4i})^{-1} \approx 1 - \frac{D}{4i}$
   $$y_p = \text{Im} \left[ e^{2ix} \frac{1}{4iD} \left(1 - \frac{D}{4i}\right) x \right] = \text{Im} \left[ e^{2ix} \frac{1}{4iD} \left(x - \frac{1}{4i}\right) \right]$$
   The operator $1/D$ means integrate with respect to $x$:
   $$y_p = \text{Im} \left[ e^{2ix} \frac{1}{4i} \left(\frac{x^2}{2} - \frac{x}{4i}\right) \right] = \text{Im} \left[ e^{2ix} \left( \frac{x^2}{8i} - \frac{x}{16i^2} \right) \right]$$
   Multiply the first term by $i/i$: $\frac{1}{i} = -i$. Since $i^2 = -1$:
   $$y_p = \text{Im} \left[ (\cos 2x + i\sin 2x) \left( \frac{x}{16} - i\frac{x^2}{8} \right) \right]$$
   Expand and collect only imaginary parts (terms with $i$):
   $$\text{Im} = -\frac{x^2}{8}\cos 2x + \frac{x}{16}\sin 2x$$
3. **Final General Solution:**
   $$y = C_1\cos 2x + C_2\sin 2x - \frac{x^2}{8}\cos 2x + \frac{x}{16}\sin 2x$$

**Question 25:**
Solve: $\frac{d^2y}{dx^2} + 4y = e^x + \sin 2x$

**Solution:**
1. **Find $y_c$:** $m^2 + 4 = 0 \implies m = \pm 2i$.
   $$y_c = C_1\cos 2x + C_2\sin 2x$$
2. **Find $y_{p1}$ (Exponential part):**
   $$y_{p1} = \frac{1}{D^2+4} e^x = \frac{1}{1^2+4} e^x = \frac{1}{5} e^x$$
3. **Find $y_{p2}$ (Trigonometric part):**
   $$y_{p2} = \frac{1}{D^2+4} \sin 2x$$
   Sub $D^2 = -4 \implies 0$. Failure.
   Multiply by $x$, differentiate denominator:
   $$y_{p2} = x \frac{1}{2D} \sin 2x = \frac{x}{2} \int \sin 2x dx = \frac{x}{2} \left(-\frac{\cos 2x}{2}\right) = -\frac{x}{4} \cos 2x$$
4. **Final General Solution:**
   $$y = C_1\cos 2x + C_2\sin 2x + \frac{1}{5}e^x - \frac{x}{4}\cos 2x$$