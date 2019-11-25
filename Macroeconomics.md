# MACROECONOMICS

## Content

[TOC]

## Growth Model

### Solow Growth Model

### Krueger Growth Model

### Log-Linearization

### Stochastic Growth Model

## Dynamic Programming Theory

### Deterministic Dynamic Programming

### Stochastic Dynamic Programming

### Example: Tree Cutting Problem

## Labor Market Model

### McCall’s Job Searching Model

### Diamond-Mortenson-Pissarides Model

### Mutation of Searching and Matching Model

## Complete Market and Exchange Economy

### Arrow-Deberu Equilibrium

#### Setup

**Assumption: (Arrow-Deberu)**

- There are $I$ numbers of consumers in total
- The state of the economy is denoted as $S_t$, and the history is denoted as $S^t = \{S_\tau\}_{\tau=0}^t$ 
- Stochastic Endowment Economy, person i’s endowment is denoted as $e_t^i(S^t)$
- Identical utility function $U$ among the consumers
- Complete market, meaning there are contingent claims for each state
- The consumers trade with each other at the beginning of the economy, then they will never trade again
- $Prob(S_{t+1}| S_t) = \pi(S_{t+1}|S_t)$ is a Markov process

#### Arrow-Deberu Equilibrium

**Definition: (Arrow-Deberu Equilibrium)** The Arrow-Deberu Equilibrium is defined as a set of price $\{\tilde p^0_t\}$ of consumption, a set of individual decisions $\{C^i_t(S^t)\}$, such that:

1. Given the set of price, the individual decision variables solves the following consumer’s problem:
   $$
   max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^tU(C_t^i(S^t))\pi(S^t)
   $$
   subject to the budget constraint:
   $$
   \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)C_t^i(S^t) \leq \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)e_t^i(S^t)
   $$
2. Markets clears, or the feasible condition holds which means:
   $$
   \sum_{i\in I}C_t^i(S^t) = \sum_{i\in I}e_t^i(S^t) \space for \space each \space t \space and \space S^t
   $$

#### Solution

**Solution: (Tractable Method)**

1. Solve the Consumer’s problem with Lagrange method:
   $$
   L =\sum_{t=0}^{+\infty}\sum_{S^t}\{\beta^tU(C_t^i(S^t))\pi(S^t) + \mu^ip_t^0(S^t)(e_t^i(S^t)-C_t^i(S^t))\}
   $$
   The First Order Conditions are:
   $$
   \beta^tU'(C_t^i(S^t))\pi(S^t) = \mu^i p_t^0(S^t)
   $$
   This is true for any individual. Hence if we take person i First Order Conditions and divided with person j’s equation, we will get:
   $$
   \frac{U'(C_t^i(S^t))}{U'(C_t^i(S^t))} = \frac{\mu^i}{\mu^j}
   $$
   This is true for any time and any state. which means the ratio of the consumption between any two people is a constant for any time and any state history. Hence we could define the total endowment as $Y_t(S^t)$, and assume consumer i’s consumption is:
   $$
   C_t^i(S^t) = \tilde\mu^i\sum_{i\in I}e_t^i(S^t) = \tilde\mu^iY_t(S^t)
   $$
   where $\sum_i\tilde\mu^i = 1$.
2. Solve for the price:

   Re-write First Order Conditions as: $\beta^tU'(\tilde\mu^iY_t(S^t))\pi(S^t) = \mu^i p_t^0(S^t)$, divided by time zero First Order Conditions, we will get:
   $$
   p_t^0(S^t) = \beta^t\frac{U'(C_t^i(S^t))}{U'(C_0^i(S_0))}\pi(S^t|S_0) p_0^0
   $$
   Suppose we assume that the utility has the following property:
   $$
   \frac{U'(C_t^i(S^t))}{U'(C_0^i(S_0))} = f(\frac{C_t^i(S^t)}{C_0^i(S_0)}) = f(\frac{Y_t(S^t)}{Y_0(S_0)}) 
   $$
   Then we can find the Arrow-Deberu Price for the consumption contingents ,which is:
   $$
   p_t^0(S^t) = \beta^t\frac{U'(Y_t(S^t))}{U'(Y_0(S_0))}\pi(S^t|S_0) p_0^0
   $$

3. Solve for the consumption allocation:

   Plug the prices to the budget constraint for person i, we get:
   $$
   \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)Y_t(S^t) \tilde \mu^i = \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)e_t^i(S^t)
   $$
   and hence we can solve the ratio of the consumption:
   $$
   \tilde \mu^i = \frac{\sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)e_t^i(S^t)}{\sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)Y_t(S^t) }
   $$



### Sequential Market Equilibrium

#### Setup

Assumption: (Sequential Market)**

- There are $I$ numbers of consumers in total
- The state of the economy is denoted as $S_t$, and the history is denoted as $S^t = \{S_\tau\}_{\tau=0}^t$ 
- Stochastic Endowment Economy, person i’s endowment is denoted as $e_t^i(S^t)$
- Identical utility function $U$ among the consumers
- Complete market, meaning there are some arrow securities for each state in next period
- The consumers trade with each other at each period
- $Prob(S_{t+1}| S_t) = \pi(S_{t+1}|S_t)$ is a Markov process

#### Sequential Market Equilibrium

**Definition: (Sequential Market Equilibrium)** The Sequential Market Equilibrium is defined as a set of price $\{\tilde q_t(S^t,S')\}$ of consumption, a set of individual decisions $\{C^i_t(S^t), a_t^i(S^t)\}$, such that:

1. Given the set of price, the individual decision variables solves the following consumer’s problem:
   $$
   max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^tU(C_t^i(S^t))\pi(S^t)
   $$
   subject to the budget constraint:
   $$
   C_t^i(S^t) +\sum_{S'}\tilde q_t(S^t,S') a_{t+1}^i(S^t,S') \leq e_t^i(S^t)+a_{t}^i(S^{t-1},S_t) \space for \space each \space t \space and \space S^t
   $$
   and the No-Ponzi Condition:
   $$
   a_{t+1}^i(S^{t+1}) \geq -\bar A
   $$
   
2. Markets clears, or the feasible condition holds which means:
   $$
   \sum_{i\in I}C_t^i(S^t) = \sum_{i\in I}e_t^i(S^t) \space for \space each \space t \space and \space S^t
   $$
   
#### Solution

**Solution: (Tractable Method)**

1. Solve the Consumer’s problem with Lagrange method:
   $$
   L =\sum_{t=0}^{+\infty}\sum_{S^t}\{\beta^tU(C_t^i(S^t))\pi(S^t) + \mu_t^i(S^t) [e_t^i(S^t)+a_{t}^i(S^{t-1},S_t) - C_t^i(S^t)\\
   -\sum_{S'}\tilde q_t(S^t,S') a_{t+1}^i(S^t,S')]\}
   $$
   The First Order Conditions are:
   $$
   \beta^tU'(C_t^i(S^t))\pi(S^t) = \mu_t^i(S^t) \\
   \mu_{t}^i(S^t)\tilde q_t(S^t,S') = \mu_{t+1}^i(S^t,S')
   $$
   Combine the First Order Conditions we get the Euler’s Equation:
   $$
   \tilde q_t(S^t,S') = \beta \frac{U'(C_{t+1}^i(S^t,S'))}{U'(C_t^i(S^t))}\pi(S'|S^t)
   $$
   
2. Solve for the price:

   Note that from the Euler’s Equation, if the Sequential Market and the Arrow Debreu Market have the same solution then the price of the Arrow securities can be denoted as:
   $$
   \tilde q_t(S^t,S') = p_{t+1}^0(S^t,S')/p_t^0(S^t)
   $$

#### Relationship between Two Economies

 **Theorem: (Duality)** The Solution of the Arrow Debreu Equilibrium and the Sequential Market Equilibrium are the same.

Proof:

First We proof that the solution of the Sequential Market Equilibrium is the solution of the Arrow-Debreu Equilibrium, by adding up all the discounted sequential budget constraints:
$$
lim_{T\to+\infty}\sum_{t=0}^{T} \sum_{S'} (\prod_{j=0}^{t-1}\tilde q_j(S^j,S^{j+1})) C_t^i(S^t) + lim_{T\to+\infty}\sum_{S'}(\prod_{j=0}^{T-1} \tilde q_t(S^j,S^{j+1})) \tilde q_T(S^T,S') a_{T+1}^i(S^T,S')\\
 = lim_{T\to+\infty}\sum_{t=0}^{T-1} \sum_{S'}  (\prod_{j=0}^{t-1}\tilde q_j(S^j,S^{j+1})) e_t^i(S^t)
$$
Since we have the No Ponzi Condition, we have $lim_{T\to+\infty}\sum_{S'}(\prod_{j=0}^{T-1} \tilde q_t(S^j,S^{j+1})) \tilde q_T(S^T,S') a_{T+1}^i(S^T,S') = 0$, and we can define $P^0_t(S^t) = \prod_{j=0}^{t-1}\tilde q_j(S^j,S^{j+1})$, and the lifetime budget constraint becomes:
$$
\sum_{t=0}^{+\infty}\sum_{S^t}P_t^0(S^t)C_t^i(S^t) \leq \sum_{t=0}^{+\infty}\sum_{S^t}P_t^0(S^t)e_t^i(S^t)
$$
Since we have exactly the same budget constraint, and all the other equations are also the same, we will get the exact same solution, i.e. the solution to the Sequential Market Equilibrium is the solution to the Arrow Deberu Equilibrium.

However, we have already shown that the Arrow Deberu Equilibrium have an unique solution. Since we know that the Sequential Market Equilibrium has a solution, the solution has to be the same. $\square $



### Social Planner’s Problem

#### Setup

**Assumption: (Arrow-Deberu)**

- There are $I$ numbers of consumers in total
- The state of the economy is denoted as $S_t$, and the history is denoted as $S^t = \{S_\tau\}_{\tau=0}^t$ 
- Stochastic Endowment Economy, person i’s endowment is denoted as $e_t^i(S^t)$
- Identical utility function $U$ among the consumers
- Social Planner’s problem
- $Prob(S_{t+1}| S_t) = \pi(S_{t+1}|S_t)$ is a Markov process

#### Social Planner’s Problem

**Definition: (Social Planner’s Problem)** The Social Planner’s Problem is defined as a set of allocation $\{C^i_t(S^t)\}$, such that the social welfare function is maximized: 
$$
max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^t\lambda^i U(C_t^i(S^t))\pi(S^t)
$$
subject to the feasible condition:
$$
\sum_{i\in I}C_t^i(S^t) = \sum_{i\in I}e_t^i(S^t) \space for \space each \space t \space and \space S^t
$$
**Note:** Note that the weight $\lambda^i$ is exogenous.

#### Solution

**Solution: (Tractable Method)**

Solve the Social Planner’s problem with Lagrange method:
$$
L =\sum_{t=0}^{+\infty}\sum_{S^t}\{\beta^t \lambda^i U(C_t^i(S^t))\pi(S^t) + \phi_t(S^t)(e_t^i(S^t)-C_t^i(S^t))\}
$$
The First Order Conditions are:
$$
\beta^t \lambda^i U'(C_t^i(S^t))\pi(S^t) = \phi_t(S^t)
$$
This is true for any individual. Hence if we take person i First Order Conditions and divided with person j’s equation, we will get:
$$
\frac{U'(C_t^i(S^t))}{U'(C_t^i(S^t))} = \frac{\lambda^j}{\lambda^i}
$$
Just like in the ADE model, this is true for any time and any state. which means the ratio of the consumption between any two people is a constant for any time and any state history. Hence we could define the total endowment as $Y_t(S^t)$, and assume consumer i’s consumption is:
$$
C_t^i(S^t) = \tilde\lambda^i\sum_{i\in I}e_t^i(S^t) = \tilde\lambda^iY_t(S^t)
$$
 where $\sum_i\tilde\lambda^i = 1$, and $\tilde\lambda^i$ is determined already.



### Welfare Theorem

#### Pareto Efficiency



#### Duality

**Theorem: (Duality between ADE and Social Planner’s Problem)** We can solve the Arrow-Debreu Equilibrium by solving the social planer’s problem.

Proof:

Define Total Tax of consumer i as $T_i = \sum_t \sum_{S^t} (e^i_t(S^t)-C^i_t(S^t))\phi_t(S^t)/\lambda_i$. When we set $T_i = 0$, the solution to Social Planner’s problem and the Arrow Debreu Equilibrium is the same. $\square $



### Asset Pricing and Lucas Tree

#### Arrow-Debreu Asset Pricing

**Assumption: (Arrow-Deberu)**

- Basic Arrow-Debreu Equilibrium Setup
- Complete market, with one asset to be priced, which is also called Lucas Tree

**Definition: (Arrow-Deberu Equilibrium)** The Arrow-Deberu Equilibrium is defined as a set of price $\{\tilde q_t, P_t\}$ of consumption, a set of individual decisions $\{C^i_t(S^t), b_{t}^i(S^t)\}$, such that:

1. Given the set of price, the individual decision variables solves the following consumer’s problem:
   $$
   max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^tU(C_t^i(S^t))\pi(S^t)
   $$
   subject to the budget constraint:
   $$
   \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)(C_t^i(S^t)+P_t(S^t)b_{t+1}^i(S^t))\\\leq \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)(e_t^i(S^t)+(P_t(S^t)+d_t(S^t))b_{t}^i(S^{t-1}))
   $$

2. Markets clears, or the feasible condition holds which means:
   $$
   \sum_{i\in I}C_t^i(S^t) = \sum_{i\in I}e_t^i(S^t) \space for \space each \space t \space and \space S^t
   $$
   And asset market clears, i.e.
$$
   \sum_{i\in I}b_{t+1}^i(S^t) = B
$$

**Solution: (Asset Pricing)**

Solving this problem will give us the same First Order Conditions for the contingent claims. However, it will also give us the following Asset Pricing Equation:
$$
P_t(S^t) = \sum_{S'}\beta \frac{U'(C_{t+1}(S^t,S'))}{U'(C_{t}(S^t))}\pi(S'|S^t)(P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1})) \\ 
P_t(S^t) = \sum_{S'} \frac {\tilde p_{t+1}^0(S^{t+1})}{\tilde p_t^0(S^t)}(P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1})
$$
which can also be rewrite as:
$$
P_t(S^t) = \sum_{\tau =t+1}^{+\infty} E_t[ \beta^{\tau-t}\frac{U'(C_{\tau}(S^\tau))}{U'(C_{t}(S^t))}d_\tau(S^\tau)]+lim_{T\to+\infty}E_t[\beta^T\frac{U'(C_{T+1}(S^T,S'))}{U'(C_{T}(S^T))}P_{T+1}(S^{T+1})]
$$
Because of no arbitrage condition, we have $lim_{T\to+\infty}E_t[\beta^T\frac{U'(C_{t+1}(S^t,S'))}{U'(C_{t}(S^t))}P_{T+1}(S^{T+1})] = 0$.

#### Sequential Asset Pricing

**Assumption: (Sequential Market)**

- Basic Sequential Market
- Complete market, with one asset to be priced, which is also called Lucas Tree

**Definition: (Sequential Market Equilibrium)** The Sequential Market Equilibrium is defined as a set of price $\{\tilde p^0_t, P_t\}$ of consumption, a set of individual decisions $\{C^i_t(S^t), a_t^i(S^t),  b_t^i(S^t)\}$, such that:

1. Given the set of price, the individual decision variables solves the following consumer’s problem:
   $$
   max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^tU(C_t^i(S^t))\pi(S^t)
   $$
   subject to the budget constraint:
   $$
   C_t^i(S^t)+P_t(S^t)b_{t+1}^i(S^t) +\sum_{S'}\tilde q_t(S^t,S') a_{t+1}^i(S^t,S') \\
   \leq e_t^i(S^t)+a_{t}^i(S^{t-1},S_t)+(P_t(S^t)+d_t(S^t))b_{t}^i(S^{t-1})
   $$
   And the No-Ponzi Condition: $a_{t+1}^i(S^{t+1}) \geq -\bar A$.

2. Markets clears, or the feasible condition holds which means:
   $$
   \sum_{i\in I}C_t^i(S^t) = \sum_{i\in I}e_t^i(S^t) \space for \space each \space t \space and \space S^t
   $$
   And asset market clears, i.e.
   $$
   \sum_{i\in I}b_{t+1}^i(S^t) = B
   $$

**Solution: (Asset Pricing)**

Solving this problem will give us the same Asset Pricing Equation, which can be rewrite as:
$$
P_t(S^t) = \sum_{S'} \tilde q_t(S^t,S')(P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1})\\
P_t(S^t) = \sum_{\tau =t+1}^{+\infty}E_t[\beta^{\tau-t}\frac{U'(C_{\tau}(S^\tau))}{U'(C_{t}(S^t))}d_\tau(S^\tau)] + lim_{T\to+\infty}E_t[\beta^T\frac{U'(C_{T+1}(S^T,S'))}{U'(C_{T}(S^T))}P_{T+1}(S^{T+1})]
$$
Because of no arbitrage condition, we have $lim_{T\to+\infty}E_t[\beta^T\frac{U'(C_{t+1}(S^t,S'))}{U'(C_{t}(S^t))}P_{T+1}(S^{T+1})] = 0$.

### Consumption Asset Pricing Model (CAPM)

#### Definition

#### CAPM

**Definition: (Returns)** Define the return of the asset to be $R_{t}(S^t,S_{t+1}) = (P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1}))/P_t(S^t)$.

**Definition: (Pricing Kernel)** Define the Pricing Kernel to be $M_{t}(S^{t+1}) = \beta\frac{U'(C_{t+1}(S^t,S'))}{U'(C_{t}(S^t))}$.

**Definition: (Risk Free Interest Rate)** Define the Risk Free Interest Rate to be $\bar R_{t} = 1/E_t[M_{t}(S^{t+1})]$.

**Theorem: (CAPM)** The expected return of an asset can be decomposed as:
$$
E_t[R_{t}(S^{t+1})] -\bar R_{t} = -\bar R_{t}cov(M_{t}(S^{t+1}),R_{t}(S^{t+1}) )
$$
Proof:

From the asset pricing equation, we get $E_t[M_{t}(S^{t+1}) R_t(S^{t+1})] =1$, which can be rewrite as
$$
cov(M_{t}(S^{t+1}),R_{t}(S^{t+1}) ) + E_t[M_{t}(S^{t+1})] E_t[R_{t}(S^{t+1})] = 1 
$$
Divide both side with risk free rate, and then we get the formula. $\square$

### Asset Pricing with Endogenous Growth

## Rational Expectation

### Neoclassical Growth Model

### Rational Expectation

## Incomplete Market and Heterogeneity

### Huggett Model

#### Setup

**Assumption: (The Household)**

- Endowment economy
- A continuum of households
- Heterogenetic household with no aggregate risk
- Households have access to only risk-free bond
- With borrowing constraint

**Assumption: (The Market)**

- Perfect Competition
- Focus on Steady State
- $Prob(n_{t+1}| n_t) = \pi(n_{t+1}|n_t)$

#### Competitive Equilibrium

**Definition: (Recursive Competitive Equilibrium)** The Recursive Competitive Equilibrium at the Steady State in this problem is defined as a set of price of the bond $\{q\}$, a set of individual decisions $\{c^i, a^i\}$ and a set of aggregate variables $\{C, \mu\}$, where $\mu(a, y)$ is the joint distribution of $a$ and $y$, such that:

1. Given the set of price and the set of aggregate variables, the individual decision variables solves the following consumer’s problem:
   $$
   V(a^i, y^i, q ) = max\{U(c^i)+\beta\sum_{{y^{i}}'} V(a', {y^{i}}', q' ) \pi({y^{i}}'|{y^{i}})\}
   $$
   subject to the budget constraint and the borrowing constraint:
   $$
   c^i + q{a^i}' \leq a^i+y^i,\space -{a^i}'\leq\bar A
   $$
   and the perceived law of motion of the price of the bond in next period:
   $$
   q' = H(q) = q
   $$
   Since we are solving the Steady State Equilibrium, the bond price does not change, the consumer in the model would just use $q' = q$ to forecast the bond price in next period. 
2. Markets clears, which means:
   $$
   C = \sum_a\sum_yc\mu(a,y),\space A = \sum_a\sum_ya\mu(a,y)=0
   $$
3. The true law of motion of distribution:
   $$
   \mu(a',y') = \sum_a\sum_yProb(a',y'|a,y)\mu(a,y)
   $$
   where the conditional probability is calculated as:
   $$
   Prob(a',y'|a,y) = \pi(a'|a,y)\pi(y'|a,y)=1_{a'=g(a,y,q)}\pi(y'|y)
   $$
   
#### Solution

**Solution: (Quantitative Method)**

1. Pick the initial value of $\{q^0\}$
2. For value  $q^j$, and solve for the consumer’s recursive problem, and it will give back policy functions $'a = g(a, y, q^j)$ and  $c = g_c(a, y, q^j)$
   Note: The consumer has a borrowing constraint, which means the solution goes in the following way:
   $$
   L = U(a+y-q^0a')+\beta\sum_{y'}V(a',y',q^0)\pi(y'|y)+\lambda(a'+\bar A)
   $$
   Derive the Euler Equation:
   $$
   (ENV)\space V'(a,y,q^0) = U'(c)
   $$
   $$
   (FOC)\space -qU'(c)+\beta \sum_{y'}V'(a',y',q)\pi(y'|y)+\lambda
   $$
   and it will give the solution as:
   $$
   a' = -\bar A, \space and \space if \space a’>-\bar A, \space q^0 U'(c) = \beta\sum_{y'}U'(c')\pi(y'|y)
   $$
3. Use the true law of motion $\mu(a',y') = 1_{a'=g(a,y,q^j)}\pi(y'|y)\mu(a,y)$  and try to calculate a steady distribution $\mu(a,y|r^j)$
4. Get the excess aggregate asset position by $z(r^j) = \sum_a\sum_yg(a,y,q^j)\mu(a,y|q^j)$
6. If $z(q^j)>0$, it means the aggregate demand of bond is too high, which means there are too many people trying to buy the bonds in the market, so the bond price should goes up, which means we should set $q^{j+1} <q^j$, and vice versa
7. Iterate from step 2, until $|zq(^j)-z(q^{j+1})| < \epsilon$



### Aiyagari Model

#### Setup

**Assumption: (The Household)**

- A continuum of households
- Heterogenetic household with no aggregate risk
- Different in labor endowment
- Households have access to capital and risk-free bond

**Assumption: (The Firm)**

- Representative firm
- Technology: $Y_t = K_t ^\alpha N_t ^{1-\alpha}$
- Stochastic shock in productivity, following a Markov Chain

**Assumption: (The Market)**

- Perfect Competition
- Focus on Steady State
- $Prob(n_{t+1}| n_t) = \pi(n_{t+1}|n_t)$

#### Competitive Equilibrium

**Definition: (Recursive Competitive Equilibrium)** The Recursive Competitive Equilibrium at the Steady State in this problem is defined as a set of price $\{r, w\}$, a set of individual decisions $\{c^i, k^i\}$ and a set of aggregate variables $\{C, K, \mu\}$, where $\mu(k, n)$ is the joint distribution of $k$ and $n$, such that:

1. Given the set of price and the set of aggregate variables, the individual decision variables solves the following consumer’s problem:
   $$
   V(k^i, n^i, r ) = max\{U(c^i)+\beta\sum_{{n^{i}}'} V(k', {n^{i}}', r' ) \pi({n^{i}}'|{n^{i}})\}
   $$
   subject to the budget constraint:
   $$
   c^i + {k^i}' \leq (r+1-\delta)k^i+wn^i
   $$
   and the perceived law of motion of the interest rate in next period:
   $$
   r' = H(r) = r
   $$
   Note: Since we are solving the Steady State Equilibrium, the interest rate of capital does not change, the consumer in the model would just use $r' = r$ to forecast the interest rate in next period. 

2. Given the price, the aggregate variables solve the firm’s problem:
   $$
   D = max\{K^\alpha N^{1-\alpha} - rK - wN\}
   $$
3. Markets clears, which means:
   $$
   C = \sum_k\sum_nc\mu(k,n),\space K = \sum_k\sum_nk\mu(k,n),\space and\space N = \sum_k\sum_nn\mu(k,n)
   $$
4. The true law of motion of distribution:
   $$
   \mu(k',n') = \sum_k\sum_nProb(k',n'|k,n)\mu(k,n)
   $$
   where the conditional probability is calculated as:
   $$
   Prob(k',n'|k,n) = \pi(k'|k,n)\pi(n'|k,n)=1_{k'=g(k,n,r)}\pi(n'|n)
   $$

#### Solution

**Solution: (Quantitative Method)**

1. Pick the initial value of $\{r^0\}$
2. For value  $r^j$, and solve for the consumer’s recursive problem, and combine the solution to the firm’s First Order Conditions will give back policy functions $k' = g(k, n, r^j)$ and  $c = g_c(k, n, r^j)$
3. Use the true law of motion $\mu(k',n') = 1_{k'=g(k,n,r^j)}\pi(n'|n)\mu(k,n)$  and try to calculate a steady distribution $\mu(k,n|r^j)$
4. Get the aggregate capital by $K(r^j) = \sum_k\sum_ng(k,n,r^j)\mu(k,n|r^j)$ , calculate all the other aggregate variables similarly
5. Calculate the excess supply, $z(r^j) = K(r^j)^\alpha N^{1-\alpha} -\sum_k\sum_ng_c(k, n, r^j)\mu(k,n) - \delta K(r^j)$
6. If $z(r^j)>0$, it means the excess aggregate supply is too high, which means the firm will produce less in the next period, so the demand of capital will decrease, which means we should set $r^{j+1} <r^j$, and vice versa
7. Iterate from step 2, until $|z(r^j)-z(r^{j+1})| < \epsilon$

### Krusell-Smith Model

#### Setup

**Assumption: (The Household)**

- A continuum of households
- Heterogenetic household
- Different in labor endowment
- Households have access to only one asset, which is capital

**Assumption: (The Firm)**

- Representative firm
- Technology: $Y_t = z_t K_t ^\alpha N_t ^{1-\alpha}$
- Stochastic shock in productivity, following a Markov Chain, generating aggregate shocks

**Assumption: (The Market)**

- Perfect Competition
- $Prob(z_{t+1}| z_t) = \pi(z_{t+1}|z_t)$
- $Prob(n_{t}| z_t) = \pi(n_t|z_t)$

#### Competitive Equilibrium

**Definition: (Recursive Competitive Equilibrium)** The Recursive Competitive Equilibrium in this problem is defined as a set of price $\{r_t, w_t\}$, a set of individual decisions $\{c_t^i, k_t^i\}$ for each individual consumer $i \in I$, and a set of aggregate variables $\{C_t, K_t, \mu(k_t, n_t)\}$, where $\mu(k_t, n_t)$ is the joint distribution of $K_t$ and $n_t$, such that:

1. Given the set of price and the set of aggregate variables, the individual decision variables solves the following consumer’s problem:
   $$
   V(k_t^i, n_t^i, z_t, \mu_t ) = max\{U(c_t^i)+\beta\sum_{n_{t+1}^i}\sum_{z_{t+1}} V(k_{t+1}^i, n_{t+1}^i, z_{t+1}, \mu_{t+1} ) \pi(n_{t+1}^i,z_{t+1}|n_t^i, z_t)\}
   $$
   subject to the budget constraint:
   $$
   c_t^i + k_{t+1}^i \leq (r_t+1-\delta)k_t^i+w_tn_t^i
   $$
   and the perceived law of motion of the distribution of capital and labor endowment for the next period:
   $$
   \mu_{t+1} = H(\mu_t, z_t ,z_{t+1})
   $$
2. Given the price, the aggregate variables solve the firm’s problem:
   $$
   D_t = max\{z_t K_t ^\alpha N_t ^{1-\alpha} - r_t K_t - w_t N_t\}
   $$
3. Markets clears, which means:
   $$
   C_t = \int_{i \in I}c_t^idi,\space K_t = \int_{i \in I}k_t^idi,\space and\space N_t = \int_{i \in I}n_t^idi
   $$
4. The true law of motion of the distribution is consistent with the solution to the consumer’s problem.

   Note: The consumers need to forecast the distribution of the the capital in the next period only because they need to predict the aggregate capital in the next period.

   Note: One way to solve this problem is instead of forecasting the full distribution, forecasting the moments of the distribution. One simple approximation of the forecasting model is to use only the first order of moments to approximate, i.e. $ln K_{t+1} = a_z+b_zlogK_t$.

#### Solution

**Solution: (Quantitative Method)**

1. Pick the initial value of $\{a_z^0, b_z^0\}$

2. For value  $\{a_z^j, b_z^j\}$, plug into the perceived law of motion $ln K_{t+1} = a_z^0+b_z^0logK_t$, and solve for the following problem:
   $$
   V(k_t^i, n_t^i, z_t, K_t ) = max\{U(c_t^i)+\beta\sum_{n_{t+1}^i}\sum_{z_{t+1}} V(k_{t+1}^i, n_{t+1}^i, z_{t+1}, K_t ) \pi(n_{t+1}^i,z_{t+1}|n_t^i, z_t)\}
   $$
   subject to
   $$
   c_t^i + k_{t+1}^i \leq (r_t+1-\delta)k_t^i+w_tn_t^i
   $$
   $$
   ln K_{t+1} = a_z^j+b_z^jlogK_t
   $$
   This is equivalent to solve the consumer’s problem.
   
   Solving this recursive problem, and combine the solution to the firm’s First Order Conditions will give back policy functions $k_{t+1}^i = g(k_t^i, n_t^i, z_t, K_t )$
   
3. Starting from a set of initial points $\{ k_0^i, n_0^i, z_0, K_0 \}$, use the individual decision rules, simulate a panel of technology shock and labor endowment, and use that to generate a panel of individual capital stocks $\{k_{t+1}^i\}_{t=0}^T$, and use the panel to generate $K_t = \frac{1}{I}\sum_i k_t^i$

4. Run a regression of $lnK_{t+1} = a_z'+b_z'lnK_t+e_t$, and get $\{a_z^j, b_z^j\}$

5. Set $a_z^{j+1} = a_z' $, and $b_z^{j+1} = b_z' $, and iterate from step 2, until $||(a_z^j,b_z^j) - (a_z^{j+1},b_z^{j+1})|| < \epsilon$

