# Derivatives and Differentials

## Definition of the Derivative

The **derivative** of a function $f$ at a point $x_0$, denoted $f'(x_0)$, is defined as:

$$
f'(x_0) = \lim_{h \to 0} \frac{f(x_0 + h) - f(x_0)}{h},
$$

provided this limit exists.

**Note:**  
If the limit is infinite (i.e., $+\infty$ or $-\infty$), the derivative **does not exist** in the standard sense. Allowing infinite derivatives would violate key properties, such as the continuity of differentiable functions.

## The Derivative Rule for Inverses

Let $f$ be a function with domain $I$ (an interval) such that:

1. $f$ is differentiable on $I$,
2. $f'(x) \neq 0$ for all $x \in I$.

Then, the inverse function $f^{-1}$ is differentiable at every point in its domain (the range of $f$).  

If $b$ is in the domain of $f^{-1}$ and $a = f^{-1}(b)$, then:

$$
(f^{-1})'(b) = \frac{1}{f'(a)} = \frac{1}{f'(f^{-1}(b))}. \quad \text{(1)}
$$

In Leibniz notation:

$$
\left. \frac{d f^{-1}}{dx} \right|_{x = b} = \left. \frac{1}{\frac{d f}{dx}} \right|_{x = f^{-1}(b)}.
$$

### Connection to the Jacobian in Higher Dimensions

This rule generalizes to multivariable functions via the **Inverse Function Theorem**, where the Jacobian matrix plays the role of the derivative:

- For $f: \mathbb{R}^n \to \mathbb{R}^n$, if the Jacobian determinant $\det(J_f) \neq 0$ at a point, then $f$ is locally invertible, and the Jacobian of $f^{-1}$ is the inverse matrix of $J_f$.

**Clarifications:**

- The **gradient** ($\nabla f$) maps $\mathbb{R}^m \to \mathbb{R}$ and is not directly invertible because it is not a square matrix(think of it as 3 dim being collapsed to 1 so one one and onto properties of inverse functions do not hold).
- The **Jacobian** $J_f$ of $f: \mathbb{R}^m \to \mathbb{R}^n$ is only invertible (as a matrix) if $m = n$ and $\det(J_f) \neq 0$.

## Definition of Differentials

Let $y = f(x)$ be a differentiable function.

- The **differential $dx$** is an independent variable representing an infinitesimal change in $x$.
- The **differential $dy$** is defined as:

$$
dy = f'(x) \, dx.
$$

![Differential Visualization](/public/images/differential.png)

**Key Distinction:**  
The symbol $dy$ here is **not** the numerator in $\frac{dy}{dx}$. Instead, it represents the **linear approximation** of the change in $y$ ($\Delta y$) for a small change $dx$ in $x$.

---

### Inflection Points  and Critical Points

While some inflection points *can* be critical points, the two concepts are distinct and serve different purposes in analyzing a function's behavior.  

#### **(a) Critical Point**  

A point $x = c$ is a **critical point** of $f(x)$ if:  

1. $f'(c) = 0$ (horizontal tangent), **or**  
2. $f'(c)$ **does not exist** (sharp corner, cusp, or vertical tangent).  

**Example:**  

- $f(x) = x^2$ at $x = 0$ (critical point where $f'(0) = 0$).  
- $f(x) = |x|$ at $x = 0$ (critical point where $f'(0)$ is undefined).  

#### **(b) Inflection Point**  

A point $x = c$ is an **inflection point** if:  

1. The **concavity** of $f$ changes at $c$ (i.e., $f''(x)$ changes sign), **and**  
2. $f$ is continuous at $c$.  

An inflection point is a critical point **only if** $f'(c) = 0$ or $f'(c)$ is undefined at that point.  

#### **Case 1: Inflection Point = Critical Point**  

- **Example:** $f(x) = x^3$ at $x = 0$.  
  - $f'(0) = 0$ (critical point).  
  - $f''(0) = 0$ and concavity changes (inflection point).  

#### **Case 2: Inflection Point ≠ Critical Point**  

- **Example:** $f(x) = x^3 + x$ at $x = 0$.  
  - $f'(0) = 1 \neq 0$ (not a critical point).  
  - $f''(x) = 6x$, which changes sign at $x = 0$ (inflection point).  

---

#### **Practical Implications**  

- **Optimization (ML/Gradient Descent):**  
  - Critical points are where optimizers look for minima/maxima.  
  - Inflection points are **not** optimization targets but indicate changes in loss landscape curvature.  
- **Graphing Functions:**  
  - Critical points help locate peaks/valleys.  
  - Inflection points show where the curve switches from "bowl-up" to "bowl-down."  

---
