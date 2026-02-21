# 📖 Basic Definitions of Differential Equations

Before learning how to solve differential equations, it is crucial to understand what they are and how they are classified. This foundational knowledge will help you identify the type of equation you are dealing with, which dictates the method required to solve it.

---

## 1. What is a Differential Equation?

> **Definition:** A **Differential Equation (DE)** is a mathematical equation that relates one or more unknown functions and their derivatives. 

In simpler terms, any equation that contains a "differential coefficient" (a derivative, such as $\frac{dy}{dx}$ or $y'$) is called a differential equation. These equations are used extensively in physics, engineering, and biology to describe physical situations involving rates of change.

---

## 2. Classification of Differential Equations

Differential equations are broadly divided into two main categories based on the number of independent variables they contain:

### 2.1 Ordinary Differential Equations (ODEs)

> **Definition:** An ODE is an equation that contains one or several derivatives of an unknown function with respect to a **single independent variable**. 

Typically, we deal with an unknown function $y(x)$, where:
*   $y$ is the **dependent variable**.
*   $x$ is the **independent variable**.

#### Examples of ODEs:
Here are some standard examples of Ordinary Differential Equations:

1.  A simple first-order ODE:
    $$ \frac{dy}{dx} = \cos x $$

2.  A second-order ODE:
    $$ \frac{d^2y}{dx^2} + 9y = e^{-2x} $$

3.  An ODE involving both variables in a rational expression:
    $$ \frac{dy}{dx} = \frac{1 + x^2}{1 - y^2} $$

### 2.2 Partial Differential Equations (PDEs)

> **Definition:** A PDE is a differential equation that contains unknown multivariable functions and their partial derivatives. This means there are **two or more independent variables**.

*(Note: While PDEs are part of the broader course curriculum, the primary focus of the current study modules is on Ordinary Differential Equations).*

---

**Next Topic:** Now that you know what a differential equation is, proceed to [Topic 1.2: Order and Degree of a DE](./02-order-and-degree.md) to learn how to classify ODEs by their highest derivatives and powers.