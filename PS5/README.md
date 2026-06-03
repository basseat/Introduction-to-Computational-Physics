# Problem Set 5 – Cosmic Ray Transport

## Topic
Simulating cosmic-ray transport as a stochastic pitch-angle scattering process and connecting the microscopic Monte Carlo model to macroscopic diffusion theory.

## Parts

### Part 1 – Exponential Waiting Times
Derives and implements the inverse-CDF method to sample exponential inter-scattering times $\Delta t \sim \text{Exp}(1/\tau)$. Validated against the analytic PDF with $N = 10^5$ samples.

### Part 2 – Isotropic Pitch Angles
Shows that $\mu = \cos\theta$ is uniformly distributed on $[-1, 1]$ for an isotropic 3D distribution, and verifies $\langle\mu\rangle = 0$, $\langle\mu^2\rangle = 1/3$.

### Part 3 – Monte Carlo Particle Trajectories
Simulates individual cosmic-ray paths: each particle starts at $x = 0$, draws a random $\mu$, then alternates between ballistic segments and pitch-angle resamples. Five trajectories are plotted.

### Part 4 – Ensemble Diffusion
Runs $N_p = 10^4$ particles and tracks $\langle x \rangle(t)$, $\sigma^2_x(t)$, and the running diffusion coefficient $\kappa_\text{MC}(t) = \sigma^2_x / 2t$, converging to the theoretical value $\kappa = \frac{1}{3}v^2\tau \approx 0.333$.

### Part 5 – Incorrect Sampling (Fixed $\Delta t$)
Demonstrates that replacing exponential waiting times with a fixed $\Delta t = \tau$ suppresses fluctuations and yields $\kappa_\text{MC} \approx \kappa_\text{th}/2$, illustrating the importance of correct microscopic sampling.

### Part 6 – Momentum-Dependent Scattering
Extends the model to $\tau(p) = \tau_0 (p/p_0)^{1/3}$, recovering $\kappa(p) \propto p^{1/3}$ across four momentum values on a log–log plot.

## Dependencies
`numpy`, `scipy`, `matplotlib`
