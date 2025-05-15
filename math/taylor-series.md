# Taylor Series

## The power series

The power series is a series of the form
$$\sum_{n=0}^{\infty} c_n (x - a)^n = c_0 + c_1(x-a) + c_2(x-a)^2 + c_3(x-a)^3 + \cdots$$
where $c\_n$ are constants and $a$ is a constant called the center of the series.  

Power series have a radius of convergence where they converge to a finite value. This can be found using ratio and root test

We know that within the interval of convergence the sum of a power series is a continuous function so taylor thought what about the other way around. If a function has derivatives of all orders on an interval I can it be expressed as a power series?

Enter the taylor series.

## The taylor series

The Taylor series of a function $f(x)$ that is infinitely differentiable at a point $a$ is given by:
$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x - a)^n = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \cdots$$
where $f^{(n)}(a)$ is the $n$-th derivative of $f(x)$ evaluated at $a$, and $n!$ is the factorial of $n$.
![Taylor series](/public/images/Taylor%20series.svg)
You can see in the figure above how as we add more terms we get closer and closer to the the actual function near x=2.

Taylor series have a radius of convergence as they are a power series. The radius of convergence above is 2. so the series can only correctly approximate the function when $0\lt x \lt4$. Though we see below that the actual interval of may be smaller than the radius of convergence.

Taylor series are continuous i.e if the function is undefined at some point like at x=0 above the taylor series approximation will naturally be limited by this. (Visually you can think that there will be no hops in the taylor series graph like 2/x at x=0).

For every point outside the radius the series diverges or is undefined/infinite.

You can't make a taylor series approximation of 2/x at x=0 as the function itself is undefined at that point.

## The taylor polynomial

In real life we cannot take infinite terms so we take the first $n+1$ terms of the series which is a polynomial of $n$-th degree called a taylor polynomial. The $n$-th degree Taylor polynomial of a function $f(x)$ centered at $a$ is given by:
$$T_n(x) = \sum_{k=0}^{n} \frac{f^{(k)}(a)}{k!}(x - a)^k = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \cdots + \frac{f^{(n)}(a)}{n!}(x-a)^n$$
So we approximate functions by an $n$-th order polynomial (within radius of convergence of course) using the Taylor polynomial.

## The Remainder Term and Convergence to the Function

When we approximate $f(x)$ with $T_n(x)$, there is an error or difference between the actual function value and the polynomial approximation. This difference is called the remainder term, denoted by $R_n(x)$.
$$R_n(x) = f(x) - T_n(x)$$
This means the function can be written as $f(x) = T_n(x) + R_n(x)$.
where $R_n(x) = \frac{f^{(n+1)}{(c)}}{n+1!}(x-a)^{(n+1)}$ for some c between a and x. See thomas calulas for the derivation of $R_n$

For the infinite Taylor series to accurately represent the function $f(x)$ within its radius of convergence, it is necessary and sufficient that the remainder term goes to zero as the degree of the polynomial $n$ approaches infinity:
$$\lim_{n \to \infty} R_n(x) = 0$$

Functions for which the Taylor series converges to the function itself on an interval are called **analytic functions** on that interval.

    The radius of convergence of the taylor series and i.e its interval of convergence is not necessarily the interval where it converges f(x) for this we have to calulate $R_n$ and get the interval. See the example below.

### Notes about convergence

We are not only interested in where the taylor series converges we also want to know where it converges to the function it is approximating.

The classic example of a function which converges everywhere but not to the function we are approximating:

$$f(x) = \begin{cases} e^{-1/x^2} & \text{if } x \neq 0 \\ 0 & \text{if } x = 0 \end{cases}$$

Let's analyze this function around the point $a=0$ (i.e., find its Maclaurin series):

1. **Check differentiability at x=0:** This function is infinitely differentiable at $x=0$, and remarkably, all of its derivatives at $x=0$ are exactly zero.
    * $f(0) = 0$ (by definition)
    * $f'(0) = \lim_{h \to 0} \frac{f(h) - f(0)}{h} = \lim_{h \to 0} \frac{e^{-1/h^2}}{h}$. This limit evaluates to 0 (the exponential term goes to zero faster than any power of $h$).
    * For all higher derivatives $f^{(n)}(0)$, it can be proven (though it's a somewhat involved proof) that $f^{(n)}(0) = 0$ for all $n \ge 0$.

2. **Convergence of the series:** This series clearly converges for all values of $x$, and its sum is always 0. Its radius of convergence is infinite ($R=\infty$).

3. **Compare series sum to the function:**
    * The sum of the Taylor series is $S(x) = 0$ for all $x$.
    * The function is $f(x) = e^{-1/x^2}$ for $x \neq 0$ and $f(0)=0$.

The Taylor series converges everywhere to the value 0. However, the original function $f(x)$ is equal to 0 *only* at $x=0$. For any $x \neq 0$, $e^{-1/x^2}$ is a positive value (e.g., $f(1) = e^{-1}$, $f(2) = e^{-1/4}$).

Therefore, for this function, the Taylor series centered at 0 converges for all $x$ to the value 0, but it *does not* converge to the function $f(x)$ for any $x \neq 0$.

This is a classic example of a function that is infinitely differentiable but not "analytic" at $x=0$, because it is not equal to its Taylor series in any open interval containing 0. The remainder term $R_n(x) = f(x) - T_n(x) = f(x) - 0 = f(x)$ does not go to 0 as $n \to \infty$ for $x \neq 0$.
