# Linear programming

The objective function is a plane. We check for the max and min values of this within the bounds of the domain. This always occurs at corners see image below. No need to check within or on boundaries.

![Linrear programming](/public/images/Linear%20programming.svg)

## Example: Maximize Profit

An example spit out by ChatGPT

Here's a clear, step-by-step example of a **linear programming problem**, including:

* Objective function
* Constraints
* Feasible region
* Solution

---

### Objective

A company makes two products: **A** and **B**.

* Profit:

  * Product A gives \$3 profit per unit
  * Product B gives \$5 profit per unit

How many units of A and B should be made to **maximize profit**, given resource constraints?

---

### Step 1: Define Variables

Let:

* $x$ = number of units of Product A
* $y$ = number of units of Product B

---

### Step 2: Objective Function

We want to **maximize**:

$$
P = 3x + 5y
$$

(This is the **profit function**.)

---

### Step 3: Constraints

The company has limited resources:

1. **Material constraint**:
   Each unit of A uses 1 unit of material, B uses 2 units
   Total available: 8 units
   → $x + 2y \leq 8$

2. **Labor constraint**:
   Each unit of A uses 2 hours, B uses 1 hour
   Total available: 6 hours
   → $2x + y \leq 6$

3. **Non-negativity constraints**:
   Can't produce negative units:
   → $x \geq 0,\ y \geq 0$

---

### Step 4: Graph Feasible Region

Plot the inequalities:

1. $x + 2y \leq 8$
2. $2x + y \leq 6$
3. $x \geq 0$
4. $y \geq 0$

You’ll get a **convex polygon** in the first quadrant — that’s the feasible region.

---

### Step 5: Find Corner Points (Vertices)

Solve the system to find intersection points:

* A: $(0, 0)$
* B: $(0, 3)$ ← from $2x + y = 6$ and $x = 0$
* C: $(2, 2)$ ← from solving:

  $$
  \begin{cases}
  x + 2y = 8 \\
  2x + y = 6
  \end{cases}
  \Rightarrow x = 2,\ y = 2
  $$
* D: $(4, 0)$ ← from $x + 2y = 8$ and $y = 0$

---

### Step 6: Evaluate Objective Function at Each Vertex

$$
\begin{align*}
\text{At A } (0, 0): &\quad P = 3(0) + 5(0) = 0 \\
\text{At B } (0, 3): &\quad P = 3(0) + 5(3) = 15 \\
\text{At C } (2, 2): &\quad P = 3(2) + 5(2) = 6 + 10 = 16 \\
\text{At D } (4, 0): &\quad P = 3(4) + 5(0) = 12 \\
\end{align*}
$$

---

### Final Answer

* **Maximum profit = \$16**
* **Occurs at: $(2, 2)$**
  → Make 2 units of A and 2 units of B
