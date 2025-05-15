# Functions

A **function** $f$ from a set $D$ to a set $Y$ is a rule that assigns a **unique** element $f(x) \in Y$ to each element $x \in D$.

- **Domain:** The set $D$ is called the **domain** of the function.
- **Range:** The set of all output values $f(x)$ is called the **range**.

> **Note:**  
> The domain need not be the entire set of real numbers $\mathbb{R}$.  
> If $f(x)$ becomes infinite (i.e., $f(x) = \infty$), then the function is **undefined** at that point, because infinity is not an actual number in the real number system—just a concept of a very large quantity.

## Exponential Functions and the Natural Number $e$

The most important exponential function used for modeling natural, physical, and economic phenomena is the **natural exponential function**, whose base is the special number:

$$
e \approx 2.71828\ldots
$$

Why choose $e$?  

- The graph of $y = e^x$ has the property that the slope (rate of change) at any point equals its own height $y$.
- Specifically, the slope at $x = 0$ is exactly 1.

Thus, $e$ is deeply connected to growth processes, rates of change, and calculus.

> The slope is:
>
> - Smaller than 1 if the base $a < e$
> - Larger than 1 if the base $a > e$

## Composite Functions

### Definition

If $f$ and $g$ are functions, the **composite function** $f \circ g$ (“$f$ composed with $g$”) is defined by:

$$
(f \circ g)(x) = f(g(x))
$$

- The domain of $f \circ g$ consists of all $x$ in the domain of $g$ such that $g(x)$ lies in the domain of $f$.

### Important

- $f \circ g$ and $g \circ f$ are **usually different**.
- To evaluate $g \circ f$, you first apply $f$, then $g$.

## Radians and Arc Length

In a circle, the relationship between arc length $s$, radius $r$, and central angle $\theta$ in **radians** is:

$$
s = r\theta
$$

For a **unit circle** (radius $r = 1$):

- The angle $\theta$ in radians equals the length of the arc cut from the circle.
- One full revolution is:

$$
360^\circ = 2\pi \text{ radians}
$$

## Inverse Functions

### Definition

Suppose $f$ is a **one-to-one** function on a domain $D$ with range $R$.  
The **inverse function** $f^{-1}$ is defined by:

$$
f^{-1}(b) = a \quad \text{if and only if} \quad f(a) = b
$$

Properties:

- The domain of $f^{-1}$ is $R$.
- The range of $f^{-1}$ is $D$.
- Domains and ranges are **interchanged** between $f$ and $f^{-1}$.

> **Important:**  
> $f^{-1}(x)$ does **not** mean $\frac{1}{f(x)}$.  
> It represents the function that **reverses** the action of $f$.

---

## Quick Examples

### Composite Function Example

If:

$$
f(x) = 2x + 3, \quad g(x) = x^2
$$

then:

$$
(f \circ g)(x) = f(g(x)) = f(x^2) = 2x^2 + 3
$$
$$
(g \circ f)(x) = g(f(x)) = g(2x + 3) = (2x + 3)^2
$$

Notice how $f \circ g \neq g \circ f$!
