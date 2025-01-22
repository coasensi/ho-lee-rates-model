I created this python program to implement my CFA Level II learnings.

Here focus on the **Ho-Lee Model**, a foundational no-arbitrage model to simulate and analyze interest rate dynamics. 

simulate paths to explore potential future movements of short-term interest rates

### Overview of the Ho-Lee Model
The Ho-Lee model assumes that the short-term interest rate \( r_t \) evolves according to the following stochastic process:

```
dr_t = θ * dt + σ * dW_t
```

#### Key Components
1. **r_t**: The short-term interest rate at time \( t \).
2. **θ**: The drift term, representing the deterministic trend or average rate of change in the interest rate.
3. **σ**: The volatility term, quantifying the magnitude of random fluctuations.
4. **dW_t**: A Wiener process (Brownian motion) that introduces random noise:
   - \( dW_t ~ N(0, dt) \), i.e., normally distributed with mean \( 0 \) and variance \( dt \).

### Discretization for Simulation
The model can be discretized for simulation purposes as follows:

```
r(t + Δt) = r(t) + θ * Δt + σ * sqrt(Δt) * Z
```

Where:

Δt : Time step size.

Z ~ N(0, 1): A standard normal random variable.

This program leverages the Ho-Lee model to simulate interest rate paths and generate insights into potential rate movements. It also provides a practical way to explore the theoretical foundations of stochastic interest rate modeling.
