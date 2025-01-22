I built this program trying to implement my CFA Level II learnings.

It implements the Ho-Lee Model, a financial model used to simulate and analyze interest rate dynamics. 

generates simulated paths to understand potential future movements in interest rates

The Ho-Lee model is a no-arbitrage interest rate model used in finance to describe the evolution of short-term interest rates over time. It is a simple yet foundational model that assumes the short rate 
𝑟
𝑡
r 
t
​
  follows a stochastic process:

𝑑
𝑟
𝑡
=
𝜃
 
𝑑
𝑡
+
𝜎
 
𝑑
𝑊
𝑡
dr 
t
​
 =θdt+σdW 
t
​
 
Components of the Model
𝑟
𝑡
r 
t
​
 : The short-term interest rate at time 
𝑡
t.
𝜃
θ: The drift term, which captures the deterministic trend or mean rate of change in the interest rate.
𝜎
σ: The volatility term, representing the magnitude of random fluctuations in the interest rate.
𝑑
𝑊
𝑡
dW 
t
​
 : A Wiener process (or Brownian motion), modeling random noise with the properties:
𝑑
𝑊
𝑡
∼
𝑁
(
0
,
𝑑
𝑡
)
dW 
t
​
 ∼N(0,dt), i.e., normally distributed with mean 
0
0 and variance 
𝑑
𝑡
dt.

drift 
𝜃
θ and volatility 
𝜎
σ are constant over time

o simulate interest rate paths, we discretize the model using a time step 
Δ
𝑡
Δt:

𝑟
𝑡
+
Δ
𝑡
=
𝑟
𝑡
+
𝜃
 
Δ
𝑡
+
𝜎
 
Δ
𝑡
 
𝑍
r 
t+Δt
​
 =r 
t
​
 +θΔt+σ 
Δt
​
 Z
Where:

𝑍
∼
𝑁
(
0
,
1
)
Z∼N(0,1) is a standard normal random variable

