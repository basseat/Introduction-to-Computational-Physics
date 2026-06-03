# Exercise 4 – Period of an Anharmonic Oscillator

## Topic
Numerical integration of a singular integral to compute the period of an anharmonic oscillator with potential $V(x) = \frac{1}{2}x^2 + \frac{\lambda}{4}x^4$.

## Parts

### Part 1 – Singularity Analysis
Identifies the $\frac{1}{\sqrt{A-x}}$ integrable singularity at the turning point via Taylor expansion of $V(x)$ around $x = A$.

### Part 2 – Open Newton–Cotes Rules
Applies midpoint, two-point, and three-point open rules to the original singular integral. All three converge at $O(N^{-1/2})$ instead of their formal orders — the singularity in the integrand's derivatives dominates the error.

### Part 3 – Change of Variables
Substitutes $x = A\sin\theta$ to analytically remove the singularity. The $\cos\theta$ factors cancel exactly, leaving a smooth integrand $g(\theta)$ on $[0, \pi/2]$ with a finite, computable endpoint value $g(\pi/2) = 1/\sqrt{1 + \lambda A^2}$.

### Part 4 – Closed Newton–Cotes on Transformed Integral
Applies trapezoidal and Simpson's rules to $g(\theta)$. Both achieve near machine precision ($\sim 10^{-13}$) at $N = 10$, demonstrating the dramatic benefit of singularity removal.

## Key Result
$T \approx 3.17972332$ s for $A = 2$, $\lambda = 1$.

## Dependencies
`numpy`, `scipy`, `matplotlib`
