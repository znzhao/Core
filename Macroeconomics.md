# MACRO ECONOMICS

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

### Sequential Market Equilibrium

### Social Planner’s Problem

### Welfare Theorem

### Asset Pricing

### Consumption Asset Pricing Model

### Asset Pricing with Endogenous Growth

## Rational Expectation

### Neoclassical Growth Model

### Rational Expectation

## Incomplete Market and Heterogeneity

### Huggett Model

#### Setup

Assumption: (The Household)

- Endowment economy
- A continuum of households
- Heterogenetic household with no aggregate risk
- Households have access to only risk-free bond
- With borrowing constraint

Assumption: (The Market)

- Perfect Competition
- Focus on Steay State
- $Prob(n_{t+1}| n_t) = \pi(n_{t+1}|n_t)$

#### Competitive Equilibrium

Definition: (Recurive Competitive Equilbrium) The Recurive Competitive Equilbrium at the Steady State in this problem is defined as a set of price of the bond $\{q\}$, a set of individual decisions $\{c^i, a^i\}$ and a set of aggregate variables $\{C, \mu\}$, where $\mu(a, y)$ is the joint distribution of $a$ and $y$, such that:

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
Note: Since we are solving the Steady State Equilbrium, the bond price does not change, the consumer in the model would just use $q' = q$ to forecast the bond price in next period. 

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

Solution: (Quantative Method)

1. Pick the initial value of $\{q^0\}$
2. For value  $q^j$, and solve for the consumer’s recursive problem, and it will give back policy functions $'a = g(a, y, q^j)$ and  $c = g_c(a, y, q^j)$

Note: The consumer has a borrowing constraint, which means the solution goes in the following way:
$$
L = U(a+y-q^0a')+\beta\sum_{y'}V(a',y',q^0)\pi(y'|y)+\lambda(a'+\bar A)
$$
Derive the Eular Equation:
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

3. Use the true law of motion $\mu(a',y') = 1_{a'=g(a,y,q^j)}\pi(y'|y)\mu(a,y)$  and try to culculate a steady distribution $\mu(a,y|r^j)$
4. Get the excess aggregate asset position by $z(r^j) = \sum_a\sum_yg(a,y,q^j)\mu(a,y|q^j)$
6. If $z(q^j)>0$, it means the aggregate demand of bond is too high, which means there are too many people trying to buy the bonds in the market, so the bond price should goes up, which means we should set $q^{j+1} <q^j$, and vice versa
7. Iterate from step 2, until $|zq(^j)-z(q^{j+1})| < \epsilon$



### Aiyagari Model

#### Setup

Assumption: (The Household)

- A continuum of households
- Heterogenetic household with no aggregate risk
- Different in labor endowment
- Households have access to capital and risk-free bond

Assumption: (The Firm)

- Representative firm
- Technology: $Y_t = K_t ^\alpha N_t ^{1-\alpha}$
- Stochastic shock in productivity, following a Markov Chain

Assumption: (The Market)

- Perfect Competition
- Focus on Steay State
- $Prob(n_{t+1}| n_t) = \pi(n_{t+1}|n_t)$

#### Competitive Equilibrium

Definition: (Recurive Competitive Equilbrium) The Recurive Competitive Equilbrium at the Steady State in this problem is defined as a set of price $\{r, w\}$, a set of individual decisions $\{c^i, k^i\}$ and a set of aggregate variables $\{C, K, \mu\}$, where $\mu(k, n)$ is the joint distribution of $k$ and $n$, such that:

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
Note: Since we are solving the Steady State Equilbrium, the interest rate of capital does not change, the consumer in the model would just use $r' = r$ to forecast the interest rate in next period. 

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

Solution: (Quantative Method)

1. Pick the initial value of $\{r^0\}$
2. For value  $r^j$, and solve for the consumer’s recursive problem, and combine the solution to the firm’s first order conditions will give back policy functions $k' = g(k, n, r^j)$ and  $c = g_c(k, n, r^j)$
3. Use the true law of motion $\mu(k',n') = 1_{k'=g(k,n,r^j)}\pi(n'|n)\mu(k,n)$  and try to culculate a steady distribution $\mu(k,n|r^j)$
4. Get the aggregate capital by $K(r^j) = \sum_k\sum_ng(k,n,r^j)\mu(k,n|r^j)$ , calculate all the other aggregate variables similarly
5. Calculate the excess supply, $z(r^j) = K(r^j)^\alpha N^{1-\alpha} -\sum_k\sum_ng_c(k, n, r^j)\mu(k,n) - \delta K(r^j)$
6. If $z(r^j)>0$, it means the excess aggregate supply is too high, which means the firm will produce less in the next period, so the demand of capital will decrease, which means we should set $r^{j+1} <r^j$, and vice versa
7. Iterate from step 2, until $|z(r^j)-z(r^{j+1})| < \epsilon$

### Krusell-Smith Model

#### Setup

Assumption: (The Household)

- A continuum of households
- Heterogenetic household
- Different in labor endowment
- Households have access to only one asset, which is capital

Assumption: (The Firm)

- Representative firm
- Technology: $Y_t = z_t K_t ^\alpha N_t ^{1-\alpha}$
- Stochastic shock in productivity, following a Markov Chain, generating aggregate shocks

Assumption: (The Market)

- Perfect Competition
- $Prob(z_{t+1}| z_t) = \pi(z_{t+1}|z_t)$
- $Prob(n_{t}| z_t) = \pi(n_t|z_t)$

#### Competitive Equilibrium

Definition: (Recurive Competitive Equilbrium) The Recurive Competitive Equilbrium in this problem is defined as a set of price $\{r_t, w_t\}$, a set of individual decisions $\{c_t^i, k_t^i\}$ for each individual consumer $i \in I$, and a set of aggregate variables $\{C_t, K_t, \mu(k_t, n_t)\}$, where $\mu(k_t, n_t)$ is the joint distribution of $K_t$ and $n_t$, such that:

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

4. The true law of motion of the distribution is consistant with the solution to the consumer’s problem.

Note: The consumers need to forcast the distribution of the the capital in the next period only because they need to predict the aggregate capital in the next period.

Note: One way to solve this problem is instead of forcasting the full distribution, forcasting the moments of the distribution. One simple approximation of the forcasting model is to use only the frist order of moments to approximate, i.e. $ln K_{t+1} = a_z+b_zlogK_t$.

#### Solution

Solution: (Quantative Method)

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

Note: This is equivalent to slove the consumer’s problem.

Solving this recursive problem, and combine the solution to the firm’s first order conditions will give back policy functions $k_{t+1}^i = g(k_t^i, n_t^i, z_t, K_t )$

3. Starting from a set of initial points $\{ k_0^i, n_0^i, z_0, K_0 \}$, use the individual decesion rules, simulate a panel of technology shock and labor endowment, and use that to generate a panel of individual capital stocks $\{k_{t+1}^i\}_{t=0}^T$, and use the panel to generate $K_t = \frac{1}{I}\sum_i k_t^i$

4. Run a regression of $lnK_{t+1} = a_z'+b_z'lnK_t+e_t$, and get $\{a_z^j, b_z^j\}$

5. Set $a_z^{j+1} = a_z' $, and $b_z^{j+1} = b_z' $, and iterate from step 2, until $||(a_z^j,b_z^j) - (a_z^{j+1},b_z^{j+1})|| < \epsilon$

