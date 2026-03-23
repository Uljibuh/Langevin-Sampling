# Langevin-Sampling-
Langevin Sampling — Step-by-Step Calculation Walkthrough


Langevin Sampling
Langevin sampling (or Langevin dynamics / Langevin Monte Carlo) is a method for drawing samples from a probability distribution when you know (or can compute) the gradient of the log-probability. 
It comes from physics — modeling how a particle moves through a potential energy landscape while being buffeted by random noise.
The core update rule is:

x_{t+1} = x_t + ε · ∇log p(x_t) + √(2ε) · noise

where ε is the step size and the noise is standard Gaussian. There are three forces at play: the current position, 
a "drift" term that pushes the sample toward higher-probability regions (the gradient), 
and a random "diffusion" term that ensures exploration. Over many steps, the samples converge to the target distribution.

Why use it? Traditional methods like rejection sampling struggle in high dimensions. 
Langevin sampling leverages gradient information to efficiently navigate complex distributions 
— it's widely used in Bayesian inference, energy-based models, and generative AI (diffusion models are closely related).
