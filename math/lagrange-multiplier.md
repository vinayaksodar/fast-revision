# Constrained Optimization Using Lagrange Multipliers

Suppose that $f(x, y, z)$ and $g(x, y, z)$ are differentiable functions, and that

$$
\nabla g \ne \vec{0} \text{ when } g(x, y, z) = 0.
$$

To find the **local maximum and minimum values** of $f$ subject to the constraint $g(x, y, z) = 0$ (if they exist), we find the values of $x, y, z, \lambda$ that simultaneously satisfy the equations:

$$
\nabla f = \lambda \nabla g \quad \text{and} \quad g(x, y, z) = 0 \tag{1}
$$

![lagrange-multiplier](/public/images/lagrange-multiplier.png)

---

Many problems require us to find the extreme values of a differentiable function $f(x, y, z)$ whose variables are subject to **two constraints**.
If the constraints are $g_1(x, y, z) = 0$ and $g_2(x, y, z) = 0$, and both $g_1$ and $g_2$ are differentiable with

$$
\nabla g_1 \not\parallel \nabla g_2,
$$

we find the constrained local maxima and minima of $f$ by introducing **two Lagrange multipliers** $\lambda$ and $\mu$ .

That is, we locate the points $P(x, y, z)$ where $f$ takes on its constrained extreme values by finding the values of $x, y, z, \lambda, \mu$ that simultaneously satisfy the equations:

$$
\nabla f = \lambda \nabla g_1 + \mu \nabla g_2, \quad g_1(x, y, z) = 0, \quad g_2(x, y, z) = 0 \tag{2}
$$

![lagrange-multiplier-2](/public/images/lagrange-multiplier2.png)

Since $\nabla g_1 \nabla g_2$ and $\nabla f$ lie in the same plane, they can be expressed as a vector combination of each other.

## **Example: Maximize/Minimize**

$$
f(x, y) = xy \quad \text{subject to the constraint} \quad g(x, y) = \frac{x^2}{8} + \frac{y^2}{2} - 1 = 0
$$

### Step 1: Use Lagrange Multipliers

To find the **extreme values** of $f(x, y) = xy$ subject to $g(x, y) = 0$, we solve:

$$
\nabla f = \lambda \nabla g, \quad g(x, y) = 0
$$

### Compute the gradients:

$$
\nabla f = \left\langle y, x \right\rangle, \quad \nabla g = \left\langle \frac{x}{4}, y \right\rangle
$$

Set up the **Lagrange system**:

$$
\begin{aligned}
y &= \lambda \cdot \frac{x}{4} \quad &\text{(1)} \\
x &= \lambda \cdot y \quad &\text{(2)} \\
\frac{x^2}{8} + \frac{y^2}{2} &= 1 \quad &\text{(3)}
\end{aligned}
$$

> ✅ **Note:**
> We have **3 equations**: two from matching vector gradients (1 and 2), and one constraint (3).
> We are solving for **3 unknowns**: $x, y, \lambda$.
> This always works out: if you have 1 constraint and a function in 2 variables, you get 3 equations from this method.

---

### Step 2: Solve the system

From (1):

$$
y = \lambda \cdot \frac{x}{4} \Rightarrow \lambda = \frac{4y}{x}
$$

From (2):

$$
x = \lambda \cdot y = \left(\frac{4y}{x}\right) y = \frac{4y^2}{x}
$$

Multiply both sides by $x$:

$$
x^2 = 4y^2 \Rightarrow \frac{x^2}{4} = y^2 \tag{4}
$$

Substitute (4) into the constraint (3):

$$
\frac{x^2}{8} + \frac{y^2}{2} = 1 \Rightarrow \frac{x^2}{8} + \frac{1}{2} \cdot \frac{x^2}{4} = 1
$$

$$
\frac{x^2}{8} + \frac{x^2}{8} = 1 \Rightarrow \frac{2x^2}{8} = 1 \Rightarrow \frac{x^2}{4} = 1 \Rightarrow x^2 = 4
\Rightarrow x = \pm 2
$$

From (4):

$$
y^2 = \frac{x^2}{4} = 1 \Rightarrow y = \pm 1
$$

---

### Step 3: Identify the points and evaluate $f(x, y) = xy$

* $(x, y) = (2, 1) \Rightarrow f = 2$
* $(x, y) = (2, -1) \Rightarrow f = -2$
* $(x, y) = (-2, 1) \Rightarrow f = -2$
* $(x, y) = (-2, -1) \Rightarrow f = 2$

---

###  Final Answer:

* **Maximum**: $f = 2$ at $(2, 1)$ and $(-2, -1)$
* **Minimum**: $f = -2$ at $(2, -1)$ and $(-2, 1)$

---

###  **Quick Reminder**:

> When using Lagrange multipliers:
>
> * You get **as many scalar equations** as unknowns:
>
>   * Each component of the gradient equation gives one equation
>   * Each constraint gives one more
> * Don’t forget to **count equations and unknowns**—it ensures your system is solvable.

Let me know if you want this formatted for a worksheet or as LaTeX!
