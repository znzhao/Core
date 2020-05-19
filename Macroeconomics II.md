# Macroeconomics II

## Consumption Theory

### Permanent Income Hypothesis

#### Consumer Problem

**Assumption: (Setup)**

- Stochastic model
- Partial equilibrium, with no production and one asset with a given price
- Income is exogenous and random

**Definition: (Consumer Problem)** Consider the following Consumer’s problem:
$$
max\space E_t[\sum_{j=0}^{+\infty}\beta^jU(c_{t+j})] \\
s.t. \space c_t+a_t = R_ta_{t-1}+ y_t \space \forall t \\
lim_{s\to +\infty} E_t[a_{t+s}/R_{t+s}] = 0
$$
where normally the second restriction is called the weak No-Ponzi condition.

**Solution: (Necessary Condition)**

Using the Lagrangian method, we have $L = E_t\sum_{j=0}^{+\infty}\beta^jU(c_{t+j})+\lambda_{t+j}[R_{t+j}a_{t+j-1}+y_{t+j}-c_{t+j}-a_{t+j}]$. Then we have the first order conditions:
$$
U'(c_t) = \lambda_t \\
\lambda_t = E_t[\beta\lambda_{t+1}R_{t+1}]
$$
Along with the transitivity condition:
$$
lim_{s\to \infty}E_t[\beta^sU'(c_{t+s})a_{t+s}] = 0
$$
From the first order conditions we could derive the Euler’s Equation:
$$
U'(c_t) = E_tU'(\beta c_{t+1}R_{t+1})
$$

#### Consumption Martingale

**Assumption: (Simplification Assumption)** $R_t = (1+r) = 1/\beta$.

**Claim: (Marginal Utility Martingale)** With the assumption $R_t = R = 1/\beta$, we have $U'(c_t) = E_tU'(c_{t+1})$, i.e. $U'(c_t)$ is a martingale.

**Note:** We have the following explanation for the marginal utility martingale:

- $U'(c_t)$ is the best ex ante prediction of tomorrow’s marginal utility $U'(c_{t+1})$
- Changes in $U'(c_{t+1})$ are unpredictable based only on past information

**Assumption: (Quadratic Utility)** $U(c_t) = -\frac{1}{2}(c_t-\gamma)^2$.

**Claim: (Consumption Martingale)** With the assumption $U(c_t) = -\frac{1}{2}(c_t-\gamma)^2$, we have $c_t = E_t[c_{t+1}]$, i.e. $c_t$ is a martingale.

**Note:** We have the following explanation for the consumption martingale:

- $c_t$ is the best ex ante prediction of tomorrow’s marginal utility $c_{t+1}$
- Changes in $c_{t+1}$ are unpredictable based only on past information

**Definition: (Consumption Prediction Error)** The Consumption Prediction Error is defined as $c_{t+1} = c_t+\epsilon_{t+1}$, i.e. $\Delta c_{t+1} =  c_{t+1} - c_t=\epsilon_{t+1}$. Note that $\epsilon_{t+1} = c_{t+1}-E_t[c_{t+1}]$.

**Note:** This implies that there is no present or earlier variable should be correlated with the change in consumption. Empirically, we could test the given model $\Delta c_{t+1} = \sum_{j=0}^J \beta_jX_{t-j}+ \epsilon_{t+1}$, with null hypothesis $\beta_j=0\space \forall j$. To be more specific, we mostly care about the case when $X = E_t[\Delta y_{t+1}] = E_t[y_{t+1} - y_{t}]$ and we want to show that when $\Delta c_{t+1} = \beta\Delta y_{t+1}+ \epsilon_{t+1}$, we have $\beta= 0$.

#### Permanent Income Hypothesis

**Solution: (Lifetime Budget Constraint)**

Take the period-by-period budget constraint $c_t+a_t = R_ta_{t-1}+ y_t$, discount and sum up, we end up with:
$$
(1+r)a_{t-1} = lim_{s\to\infty}a_{t+s}/(1+r)^s-\sum_{j=0}^s\frac{y_{t+j}-c_{t+j}}{(1+r)^j}
$$
where according to  the weak No-Ponzi condition $lim_{s\to\infty}E_t a_{t+s}/(1+r)^s=0$, we have $(1+r)a_{t-1} = -E_t[\sum_{j=0}^s\frac{y_{t+j}-c_{t+j}}{(1+r)^j}]$. We call this equation the Lifetime Budget Constraint.

**Solution: (Permanent Income Hypothesis)**

Combine the Euler’s equation and the lifetime budget constraint, we can get the closed form solution. First, by the law of iterated expectation, $c_t = E_t[c_{t+1}] = E_t[c_{t+j}]$. So the lifetime budget constraint can be written as:
$$
(1+r)a_{t-1} = -E_t[\sum_{j=0}^s\frac{y_{t+j}-c_{t+j}}{(1+r)^j}] = -E_t[\sum_{j=0}^s\frac{y_{t+j}}{(1+r)^j}]+\frac{1+r}{r}c_t \\
c_t = ra_{t-1}+\frac{r}{1+r}E_t[\sum_{j=0}^{+\infty}\frac{y_{t+j}}{(1+r)^j}]
$$
**Note:** The closed form solution of the consumption suggests the following:

- This is the result of Permanent Income Hypothesis
- Consumption is smoothed over the expected present value
- Ricardian Equivalence holds, i.e. the timing of the lump-sum tax is irrelevant
- Certainty Equilvance holds, i.e. only the conditional means of $y_t$ matters, but not the conditional variance
- however, there is no precautionary savings

**Solution: (Closed Form Solution)**

From the closed form solution of consumption, we can also solve for the following variables:

1. Asset level: $a_t = (1+r)a_{t-1}+(y_t-c_t) = a_{t-1}+y_t-(c_t-ra_{t-1}) = a_{t-1}+y_t-\frac{r}{1+r}E_t[\sum_{j=0}^{+\infty}\frac{y_{t+j}}{(1+r)^j}]$
2. Saving: $s_t = a_t-a_{t-1} = y_t-\frac{r}{1+r}E_t[\sum_{j=0}^{+\infty}\frac{y_{t+j}}{(1+r)^j}]$. Or, we could also write saving as $s_t = -E_t[\sum_{j=1}^{+\infty}\frac{\Delta y_{t+j}}{(1+r)^j}]$, i.e. the saving is negative expected present value of income decline.
3. Change in consumption: $\epsilon_{t+1} = \Delta c_{t+1} = c_{t+1}-c_t = \frac{r}{1+r}\sum_{j=0}^{+\infty}\frac{(E_{t+1}-E_{t})y_{t+j+1}}{(1+r)^j}$, i.e. the change in consumption is the revision of expectations of income.

**Assumption: (AR1 Process)** $y_t = \rho y_{t-1}+e_t$.

**Solution: (AR1 Solution)**

When we assume $y_t = \rho y_{t-1}+e_t$, we have the following solutions:

|    Variables     |          $\rho=0$           |           $\rho\in (0,1)$            |    $\rho=1$    |
| :--------------: | :-------------------------: | :----------------------------------: | :------------: |
|      $c_t$       | $ra_{t-1}+\frac{r}{1+r}y_t$ |   $ra_{t-1}+\frac{r}{1+r-\rho}y_t$   | $ra_{t-1}+y_t$ |
|      $a_t$       | $a_{t-1}+\frac{1}{1+r}y_t$  | $a_{t-1}+\frac{1-\rho}{1+r-\rho}y_t$ |   $a_{t-1}$    |
|      $s_t$       |     $\frac{1}{1+r}y_t$      |     $\frac{1-\rho}{1+r-\rho}y_t$     |      $0$       |
| $\epsilon_{t+1}$ |     $\frac{r}{1+r}y_t$      |       $\frac{r}{1+r-\rho}y_t$        |     $y_t$      |



### Precautionary Savings

**Definition: (Prudence)** A utility function is Prudent if $U'''(.)>0$.

**Assumption: (2 Period Model)** 

- 2 period model
- One asset with $R_t = (1+r) = 1/\beta$
- Shocks in $y_1$, where $E[y_1] = 0$ and $Var(y_1) = \sigma^2$

**Definition: (Consumer’s Problem)** Consider the following consumer’s problem:
$$
max\space U(c_0)+\beta E_0[U(c_1)] \\
s.t. \space c_0+a_1 = y_0, \space c_1 = y_1 + R a_1
$$
**Solution: (Euler’s Equation)**

Solving the Euler’s Equation, we will have $U'(y_0-a_1) = E[U'(Ra_1+y_1)]$.

**Theorem: (Precautionary Savings)** If the utility function of a consumer is prudent, then we can observe precautionary savings, i.e. when there is a mean preserving spread in the shock the saving would increase.

Proof:

From the Euler’s equation we have $U'(y_0-a_1) = E[U'(Ra_1+y_1)]$. Define the left hand side and right hand side to be $LHS(a_1) = U'(y_0-a_1)$ and $RHS(a_1) = E[U'(Ra_1+y_1)]$.

First, suppose the variance of the shock is 0. Since $U(.)$ is strictly increasing and strictly concave, we can show that $LHS(.)>0$, $LHS'(.)>0$ and $RHS(.)>0$, $RHS'(.)<0$. Hence there exists $a_1^\star$ such that $LHS(a_1^\star) = RHS(a_1^\star)$

Second, try to get a mean preserving spreading transformation. As $\sigma^2$ increases, we want to show that the solution increases. This requires $RHS(.)$ to move upward, since the left hand side will not be affected, i.e. we requires that $E[U'(Ra_1+y_1)]>U'(E[Ra_1+y_1])$, by Jensen’s inequality, this means $U'(.)$ is a convex function, which is true since $U'''(.)>0$. $\square$ 



## Consumption Asset Pricing Model

### Lucas Tree Asset Pricing

**Assumption: (Setup)**

- One agent general equilibrium
- No idiosyncratic risk
- One stock asset and bond asset

**Definition: (Sequential Market Equilibrium)** A Sequential Market Equilibrium is defined as a set of endogenous variables $\{C_t, A_t, B_t\}$ and a set of price $\{P_t,Q_t\}$, such that

1. Given the price the consumer solves the following problem:
   $$
   max \space E_0[\sum_{t=0}^\infty \beta ^t U (C_t) ] \\
   s.t. \space C_t+ P_t A_{t} + Q_t B_t = (P_t+d_t) A_{t-1} +B_{t-1} \\
   B_t \geq -\bar B, \space A_t\geq -\bar A, \space A_{-1} = 1, \space B_{-1}=0
   $$

2. Markets clear, i.e.
   $$
   C_t = d_t,\space A_t=1, \space B_t=0
   $$

**Note:** Note that since there is only one representative agent in the model, there is no idiosyncratic risk, hence as long as there is a asset, then it is a complete market.

**Solution: (Lucas Tree Model)**

By the first order conditions of the consumer’s problem, we have
$$
Q_t U'(C_t) = \beta E_t[U'(C_{t+1})] \\
P_t U'(C_t) = \beta E_t[U'(C_{t+1}) (P_{t+1}+d_{t+1})] 
$$
and the transversality conditions:
$$
lim_{k\to \infty} E_t[\beta^kU'(C_{t+k})Q_{t+k}B_{t+k}] = 0, \space lim_{k\to \infty} E_t[\beta^kU'(C_{t+k})P_{t+k}A_{t+k}] = 0
$$
By market clearing conditions we have 
$$
Q_t  = \beta E_t[\frac {U'(d_{t+1})}{U'(d_t)}] \\
P_t  = \beta E_t[\frac {U'(d_{t+1})}{U'(d_t)}(P_{t+1}+d_{t+1})]
$$

**Definition: (Stochastic Discount Factor)** Define the Stochastic Discount Factor to be $M_{t,t+1} = \beta\frac{U'(C_{t+1})}{U'(C_{t})}$.

**Definition: (Pricing Kernel)** Define the Pricing Kernel to be $P_{t,t+1}(S_{t+1}) = \beta\frac{U'(C_{t+1})}{U'(C_{t})}\pi(S_{t+1}|S_t)$.

### Term Structure

#### Sequential Market Equilibrium

**Assumption: (Setup)**

- One agent general equilibrium
- No idiosyncratic risk
- One stock asset
- Two bonds with different terms

**Definition: (Sequential Market Equilibrium with Term Structure)** A Sequential Market Equilibrium is defined as a set of endogenous variables $\{C_t, A_t, B_{1t}, B_{2t}\}$ and a set of price $\{P_t,Q_{1t},Q_{2t}\}$, such that

1. Given the price the consumer solves the following problem:
   $$
   max \space E_0[\sum_{t=0}^\infty \beta ^t U (C_t) ] \\
   s.t. \space C_t+ P_t A_{t} + Q_{1,t} B_{1,t} + Q_{2,t} B_{2,t} = (P_t+d_t) A_{t-1} +  B_{1,t-1} + Q_{1,t} B_{2,t-1} \\
   B_t \geq -\bar B, \space A_t\geq -\bar A, \space A_{-1} = 1, \space B_{1,-1}=0, \space B_{2,-1}=0
   $$

2. Markets clear, i.e.
   $$
   C_t = d_t,\space A_t=1, \space B_{1,-1}=0, \space B_{2,-1}=0
   $$

**Note:** Note that Since there is only one representative agent in the model, there is no idiosyncratic risk, hence as long as there is a asset, then it is a complete market.

**Solution: (Lucas Tree Model with Term Structure)**

By the first order conditions of the consumer’s problem, we have
$$
Q_{1t} U'(C_t) = \beta E_t[U'(C_{t+1})] \\
Q_{2t} U'(C_t) = \beta E_t[U'(C_{t+1})Q_{1t+1}] \\
P_t U'(C_t) = \beta E_t[U'(C_{t+1}) (P_{t+1}+d_{t+1})]
$$
and the transversality conditions:
$$
lim_{k\to \infty} E_t[\beta^kU'(C_{t+k})Q_{1,t+k}B_{1,t+k}] = 0\\
lim_{k\to \infty} E_t[\beta^kU'(C_{t+k})Q_{2,t+k}B_{2,t+k}] = 0\\
lim_{k\to \infty} E_t[\beta^kU'(C_{t+k})P_{t+k}A_{t+k}] = 0
$$
By market clearing conditions we have 
$$
Q_{1t}  = \beta E_t[\frac {U'(d_{t+1})}{U'(d_t)}] \\
Q_{2t}  = \beta^2 E_t[\frac {U'(d_{t+2})}{U'(d_t)}] \\
P_t  = \beta E_t[\frac {U'(d_{t+1})}{U'(d_t)}(P_{t+1}+d_{t+1})]
$$

#### Term Structure

**Definition: (Holding Period Return)** The Holding Period Return is defined as $R_{t, t+j} = \frac{P_{t+j}+d_{t+j}}{P_t}$.

**Definition: (Yield To Maturity)** The Yield To Maturity is defined as $YTM_j = R_{t,t+j}^{\frac{1}{j}}$.

**Definition: (Expectation Hypothesis)** The Expectation Hypothesis says $Q_{2t} = Q_{1t}E_t[Q_{1t+1}]$.

**Note:** The Expectation Hypothesis generally is not true.

**Solution: (Term Structure)**

The YTM of different bonds are defined as:
$$
YTM_1 = R_{1,t} = \frac{1}{Q_{1t}} =\frac{1}{\beta} E_t[\frac {U'(d_{t+1})}{U'(d_t)}]^{-1} \\
YTM_2 = R_{2,t}^{\frac12} = (\frac{1}{Q_{2t}})^\frac{1}{2} =\frac{1}{\beta} E_t[\frac {U'(d_{t+2})}{U'(d_t)}]^{-\frac{1}{2}}
$$
Normally we have $YTM_j< YTM_{j'}$ if $j< j'$. When the YTM inverse, normally we would expect an upcoming recession.



### Consumption Asset Pricing Model

**Definition: (Risk Neutral Probabilities)** Define the risk neutral probabilities as $\pi^r(S^{t+1}|S^t) = \pi(S^{t+1}|S^t)M_{t+1}(S^{t+1}) / \sum_{S'}M_{t+1}(S')$.

**Theorem: (Risk Neutral Expectations)** We have $P(S^{t+1}|S^t) = E_t[M_{t+1}(S^{t+1})] E_t^r[P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1})]$.

Proof:

We can rewrite $P_t(S^t) = \sum_{S'}M_{t+1}(S') \sum_{S'}\beta \frac{U'(Y_{t+1}(S^t,S'))}{U'(Y_{t}(S^t))\sum_{S'}M_{t+1}(S')}\pi(S'|S^t)(P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1}))$, i.e.  $P(S^{t+1}|S^t) = E_t[M_{t+1}(S^{t+1})] E_t^r[P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1})]$. $\square$

**Definition: (Risk Free Interest Rate)** Define the Risk Free Interest Rate to be $\bar R_{t+1} = 1/E_t[M_{t,t+1}]$.

**Theorem: (CAPM)** The expected return of an asset can be decomposed as:
$$
E_t[R_{t+1}] -\bar R_{t+1} = -\bar R_{t+1}cov(M_{t,t+1},R_{t+1} )
$$
Proof:

From the asset pricing equation, we get $E_t[M_{t,t+1} R_{t+1}] =1$, which can be rewrite as
$$
cov(M_{t,t+1},R_{t+1} ) + E_t[M_{t,t+1}] E_t[R_{t+1}] = 1
$$
Time both side with risk free rate, and then we get the formula. $\square$

**Note:** Suppose the asset would deliver higher return in the next period when the consumption in the next period is low, then the agent must see this asset as a more valuable one. Hence the price today of this asset should be higher than the risk neutral bond, leading to a lower average return. 

**Definition: (Sharp Ratio)** The Sharp Ratio of an asset is defined as $\frac{E[R_{t+1}-\bar R_{t+1}]}{\sigma_R}$.

**Theorem: (Bound of Sharp Ratio)** We have $|\frac{E[R_{t+1}-\bar R_{t+1}]}{\sigma_R} | \leq |\frac{\sigma(M_{t,t+1})}{E[M_{t,t+1}]}|$.

Proof:

From CAPM we have $E_t[R_{t+1}] -\bar R_{t+1} = -\bar R_{t+1} \sigma(M_{t,t+1})  \sigma(R_{t+1})  cov(M_{t,t+1},R_{t+1} )$. So $(E_t[R_{t+1}] -\bar R_{t+1}) / \sigma(R_{t+1}) = - \sigma(M_{t,t+1})/E[M_{t,t+1}] corr(M_{t,t+1},R_{t+1} )$. By the fact $|corr(M_{t,t+1},R_{t+1} )|\leq 1$ we can get the inequality. $\square$

### Risk Premium Puzzle

**Assumption: (Setup)**

- $\frac{C_{t+1}}{C_t} = \bar C_\Delta exp(\epsilon_{c,t+1}-\sigma_c^2/2)$
- ${1+r_{t+1}} = (1+\bar r)exp(\epsilon_{r,t+1}+\sigma_r^2/2)$
- $\epsilon_{c,t+1}, \epsilon_{r,t+1}$ are jointly distributed with mean zero and variance $\sigma_c^2$ and $\sigma_r^2$
- Utility function is $U(c) = c^{1-\gamma}/(1-\gamma)$

**Solution: (Risk Premium Puzzle)** By CAPM, we have
$$
1 = \beta E[(1+r_{t+1})(\frac{C_{t+1}}{C_t})^{-\gamma}] \\
1 = \beta(1+\bar r) \bar C_0^{-\gamma}E[exp(\epsilon_{r,t+1}-\sigma_r^2/2 - \gamma(\epsilon_{c,t+1} - \sigma_c^2/2 ))] \\
1 = \beta(1+\bar r) \bar C_0^{-\gamma}exp(-\sigma_r^2/2 + \gamma \sigma_c^2/2 + \sigma_r^2/2 + \gamma^2 \sigma_c^2/2 + \gamma cov(\epsilon_c, \epsilon_r )) \\
1 = \beta(1+\bar r) \bar C_0^{-\gamma}exp(\gamma(1+\gamma) \sigma_c^2/2 + \gamma cov(\epsilon_c, \epsilon_r )) \\
log(1+\bar r) = -log(\beta) + \gamma log(\bar C_\Delta) - (1+\gamma)\gamma \sigma_c^2/2 + \gamma cov(\epsilon_r, \epsilon_c)
$$
Then minus the log of risk free interest rate from both sides, we have $log(1+\bar r) - log(1+\bar r^f)= \gamma cov(\epsilon _c,\epsilon _r)$.

**Note:** From data the risk premium is about 6%, the covariance of the asset and the consumption is about 0.00203, which will given us a risk aversion of about 30, which is too high to reasonably believe.



## Log Linearization

### Log Linearization

**Definition: (Log Linearization)** Suppose we have $F(x_1,...,x_n) = 0$. At the steady state we have $F(\bar x) = 0$. So The log linearization of the equation is defined as
$$
0 = F(x) = F(\bar x) + \sum_{j=1}^n \bar x_jF_j(\bar x)(x_j-\bar x_j)/\bar x_j\\
\sum_{j=1}^n \bar x_jF_j(\bar x)\hat x_j = 0
$$
**Solution: (Cheat Sheet of Log Linearization)**

The log linearization of following function is listed in the table below.

|              Level              |                      Log Linearization                       |
| :-----------------------------: | :----------------------------------------------------------: |
| $f(x_t)$ with $f(\bar x)\neq 0$ |        $\frac{\bar xf’(\bar x)}{f(\bar x)} \hat x_t$         |
|           ${x_ty_t}$            |                     $\hat x_t+\hat y_t$                      |
|            $x_t+y_t$            | $\frac{\bar x}{\bar x+\bar y}\hat x_t+\frac{\bar y}{\bar x+\bar y} \hat y_t$ |
|             $ax_t$              |                          $\hat x_t$                          |
|             $x_t^a$             |                         $a\hat x_t$                          |
|           $log(x_t)$            |                    $\hat x_t/log(\bar x)$                    |
|            $E[x_t]$             |                        $E[\hat x_t]$                         |



### Blanchard-Kuhn Method

**Definition: (State Space Form)** A State Space Form stochastic linear dynamic system is defined as:
$$
A \left[
 \begin{matrix}
   E_t[y_{t+1}] \\
   x_{t+1}
  \end{matrix}
  \right] =
  B \left[
 \begin{matrix}
   y_t \\
   x_t
  \end{matrix}
  \right]+
  G\epsilon_t
$$
where $y_t$ is a $n\times 1$ vector and $x_t$ is a $m\times 1$ vector. Here $y_t$ is forward looking, also known as the jump variables, and $x_t$ is the predetermined variables, also known as the state variables.

**Assumption: (Blanchard-Kuhn Condition)**

- $A$ is inversible
- $A^{-1}B$ can be decomposed as $V^{-1}\Lambda V$, where $\Lambda$ is the diagonal matrix with eigenvalues on its diagonal
- Suppose $\lambda_1,...,\lambda_{n+m}$ are the eigenvalues of the matrix $A^{-1}B$, suppose $|\lambda_i|>1$ for $i = 1,2,...,k$, then assume $k=n$

**Solution: (Blanchard-Kuhn Method)**

Under the assumption above, we have
$$
\left[
 \begin{matrix}
   E_t[y_{t+1}] \\
   x_{t+1}
  \end{matrix}
  \right] =
  V^{-1}\Lambda V \left[
 \begin{matrix}
   y_t \\
   x_t
  \end{matrix}
  \right]+
  A^{-1}G\epsilon_t
 \\
 V\left[
 \begin{matrix}
   E_t[y_{t+1}] \\
   x_{t+1}
  \end{matrix}
  \right] =
 \Lambda V \left[
 \begin{matrix}
   y_t \\
   x_t
  \end{matrix}
  \right]+
  VA^{-1}G\epsilon_t
$$
Now take a partition of the matrix $\Lambda, V$ and $VA^{-1}G$, we have:
$$
\Lambda =\left[
 \begin{matrix}
   D_{nn} & 0_{nm} \\
   0_{mn} & D_{mm} 
  \end{matrix}
  \right]
,
V =\left[
 \begin{matrix}
   V_{nn} & V_{nm} \\
   V_{mn} & V_{mm} 
  \end{matrix}
  \right], 
  VA^{-1}G = \left[
 \begin{matrix}
   C_{n} \\
   C_{m}  
  \end{matrix}
  \right]
$$
Then the state space form can be rewritten as
$$
V_{nn}E_t[y_{t+1}] + V_{nm}x_{t+1} = D_{nn}( V_{nn}y_t + V_{nm}x_t) + C_n \epsilon_t \\
V_{mn}E_t[y_{t+1}] + V_{mm}x_{t+1} = D_{mm}( V_{mn}y_t + V_{mm}x_t) + C_m \epsilon_t
$$
Consider the first equation. Define $T_{t} = V_{nn}y_t + V_{nm}x_t$, then $E_tT_{t+1} = D_{nn}T_t+C_n\epsilon_t$.  Iterate this equation to infinity, we have:
$$
T_t = D_{nn}^{-1}E_tT_{t+1} - D_{nn}^{-1} C_n\epsilon_t \\
T_t = lim_{N\to\infty}[(D_{nn}^{N})^{-1}E_tT_{t+1} - \sum_ {i=0}^{N} (D_{nn}^i)^{-1}D_{nn}^{-1} C_nE_t[\epsilon_{t+i}]]
$$
Note that since $D_{nn}$ is a diagonal matrix with each element on its diagonal to be greater than 1, then $lim_{N\to\infty}(D_{nn}^{N})^{-1}E_tT_{t+1} = 0$. Notice this is the transversality condition. So we have the policy function of the linear system:
$$
y_t =- V_{nn}^{-1}V_{nm}x_t  - V_{nn}^{-1} \sum_ {i=0}^{+\infty} (D_{nn}^i)^{-1}D_{nn}^{-1} C_nE_t[\epsilon_{t+i}]
$$
**Claim: (Blanchard Kuhn Theorem)** Suppose $k=n$, then there is a unique solution to the state space form. If $k<n$, then there are multiple solutions to the state space form. If $k>n$, then there is no solution to the state space form.



### Example: Neoclassical Growth Model

**Definition: (Social Planner’s Problem)** The Neoclassical Social Planner solves the following problem:
$$
max_{\{c_tk_{t+1}\}} E_0[\sum_{t=0}^\infty\beta log (c_t)] \\
s.t. \space c_t+(k_{t+1}-\delta k_t) = a_tk_t^\alpha \\
log (a_{t+1}) = \rho log(a_t)+e_{t+1}
$$
**Solution: (Log Linearization)**

By first order conditions we have the Euler’s equation:
$$
\frac{1}{c_t} = E_t[\beta \frac{1}{c_{t+1}} (\alpha a_{t+1}k_{t+1}^{\alpha-1}+1-\delta)] \\
c_t+k_{t+1} = a_tk_t^\alpha + (1-\delta)k_t
$$
and the transversality condition:
$$
lim_{T\to \infty} E_t[\beta^T\frac{1}{c_T}k_{T+1}]  =0
$$
Then solve the steady state. We have
$$
\alpha\bar k^{\alpha-1} = \frac{1}{\beta} +\delta -1 \\
\bar c =\bar k^\alpha -\delta \bar k
$$
Lastly we use log-linearization and the state space form of the system is:
$$
\left[
 \begin{matrix}
   1 & (1-\alpha)(1-\beta +\beta\delta) \\
   0 & 1
  \end{matrix}
  \right]
 \left[
 \begin{matrix}
   E_t[\hat c_{t+1}] \\
   \hat k_{t+1}
  \end{matrix}
  \right] =
 \left[
 \begin{matrix}
   1 & 0 \\
   \delta-\frac{1}{\alpha}(\frac{1}{\beta}+\delta-1) & \frac{1}{\beta}
  \end{matrix}
  \right]
  \left[
 \begin{matrix}
   c_t \\
   k_t
  \end{matrix}
  \right]+
  \left[
 \begin{matrix}
   \rho (1+\beta\delta -\beta) \\
   \frac{1}{\alpha}(\frac{1}{\beta}+\delta-1)
  \end{matrix}
  \right]
  a_t
$$



## Real Business Cycle

### Social Planner RBC Model

#### Setup

**Assumption: (Social Planner RBC)**

- Social planner’s problem
- Separable utility function: $U(c,n) = lnc+ \theta ln(1-n)$
-  Technology: $Y = A k^\alpha (X n)^{1-\alpha}$, where $X$ has a growth rate of $\gamma$
- Variable labor input
- Capital Accumulation

#### Model

**Definition: (Social Planner’s Model)** The Social Planner’s Problem is to solve the following problem:
$$
max \space E_0\sum_{t=0}^\infty b^t U(C_t,L_t)\\
s.t. \space C_t+ K_{t+1} = A_t K_t^ \alpha (X_t N_t)^{1-\alpha} + (1-\delta)K_t \\
N_t+ L_t=1
$$
**Definition: (Detrend Model)** The Detrended Social Planner’s Problem is to solve the following problem
$$
max \space E_0\sum_{t=0}^\infty \beta^t lnc_t+ ln(L_t)\\
s.t. \space c_t+ \gamma k_{t+1} = a_t k_t^ \alpha N_t^{1-\alpha} + (1-\delta)k_t \\
N_t+ L_t=1, log (a_t) = \rho log (a_{t-1})+e_t
$$
where $\beta = b$, $c_t = C_t/X_t$,  $k_t = K_t/X_t$ and $y_t = Y_t/X_t$.

**Solution: (Social Planner RBC)**

1. Solving the FOCs for the social planner’s problem, we have the following equations:
   $$
   \lambda_t = \frac{1}{c_t} \\
   \lambda_t (1-\alpha)a_t k_t^\alpha N_t^{-\alpha}= \frac{1}{1-N_t} \\
   \lambda_t \gamma  = E_t[\beta \lambda_{t+1}(\alpha a_tk_t^{\alpha-1}N_t^{1-\alpha}+1-\delta)] \\
   c_t+ \gamma k_{t+1} = a_t k_t^ \alpha N_t^{1-\alpha} + (1-\delta)k_t
   $$
   
2. Solve for the steady state, we have $\frac{\gamma}{\beta} -1+\delta =  \alpha (\frac{k}{n})^{\alpha -1}$, so we can solve for the ratio of capital and labor. By this we have
   $$
   \frac{k}{N} = [\alpha/(\frac{\gamma}{\beta} -1+\delta)] ^{\frac{1}{1-\alpha}} \\
   c/k =  k^ {\alpha-1} N^{1-\alpha} + (1-\delta)- \gamma = 1-\delta+\frac{1}{\alpha}(\frac{\gamma}{\beta} -1+\delta)- \gamma = (1-\delta)\frac{\alpha-1}{\alpha} + (\frac{1}{\alpha \beta}-1)\gamma \\
   \lambda = 1/c \\
   1-N = c(k/N)^{-\alpha}/(1-\alpha)
   $$
   From this system we can solve for steady state variables.

3. Log-linearization:
   $$
   \hat \lambda_t = -\hat c_t \\
   \frac{N}{1-N} \hat N_t = \hat \lambda_t +\hat a_t+\alpha (\hat k_t -\hat N_t)\\
   \hat \lambda_t -E_t[\hat \lambda_{t+1}] =[1- \frac{\beta}{\gamma}(1-\delta)] (\rho a_t+ (1-\alpha)(E_t[\hat N_{t+1}]-K_{t+1})) \\
   \frac{c}{k^\alpha N^{1-\alpha}}\hat c_t + \frac{\gamma k}{k^\alpha N^{1-\alpha}}\hat k_{t+1}- 
   \frac{(1-\delta) k}{k^\alpha N^{1-\alpha}}\hat k_{t}  = \hat a_t +\alpha \hat k_t +(1-\alpha)\hat h_t
   $$
   



### Decentralization

#### Household Owning Capital

**Definition: (Competitive Equilibrium)** A Competitive Equilibrium with Household Owning Capital is defined as:

1. The household solves the following problem:
   $$
   max \space E_0\sum_{t=0}^\infty \beta^t lnc_t+ ln(L_t)\\
   s.t. \space c_t+ I_t = w_tN_t +R_t k_t +\pi_t \\
   I_t = \gamma k_{t+1} - (1-\delta)k_t \\
   N_t+ L_t=1
   $$

2. The firm solves the following problem:
   $$
   max \space a_t k_t^\alpha N_t^{1-\alpha} - w_t N_t - R_t k_t\\
   s.t. \space log (a_t) = \rho log (a_{t-1})+e_t
   $$

3. Market clearing condition holds:
   $$
   c_t+I_t = Y_t = a_t k_t^\alpha N_t^{1-\alpha}
   $$

**Definition: (Tobin’s Q)** Suppose $\lambda_t, \mu_t$ are the shadow price of consumption and investment. The Tobin’s Q is defined as $q_t = \mu_t/\lambda_t$.

**Note:** the household would want to invest when $q_t>1$.

#### Firm Owing Capital

**Definition: (Competitive Equilibrium)** A Competitive Equilibrium with Firm Owing Capital is defined as:

1. The household solves the following problem:
   $$
   max \space E_0\sum_{t=0}^\infty \beta^t lnc_t+ ln(L_t)\\
   s.t. \space c_t+ p_tS_{t+1} = w_tN_t +(p_t + \pi_t)S_t \\
   $$

2. The firm solves the following problem:
   $$
   max \space E_t[m_{t,t+1}\pi_t] \\
   s.t. \space \pi_t  = a_t k_t^\alpha N_t^{1-\alpha} - w_t N_t - I_t\\
   I_t = \gamma K_{t+1} - (1-\delta)K_t ,  m_{t,t+1} = \beta^t U_c(c_{t+1},L_{t+1})/U_c(c_{t},L_{t})\\
   log (a_t) = \rho log (a_{t-1})+e_t
   $$

3. Market clearing condition holds:
   $$
   c_t+I_t = Y_t = a_t k_t^\alpha N_t^{1-\alpha} \\
   S_t = 1
   $$

**Note:** When the technology is homogenous, both types of decentralization have the solutions that coincide the social planner’s solution.



## Classical Dichotomy Model

### Catan Model

#### Dichotomy Model

**Definition: (Catan Model Equilibrium)** The Equilibrium is defined as the following parts:

1. Household’s Problem:
   $$
   Max \space E_0\sum_{t=0}^{\infty} \beta^t U(C_t, N_t) \\
   s.t. \space P_t C_t + Q_t B_t = B_{t-1} + W_t N_t +\Pi_t
   $$

2. Firm’s Problem:
   $$
   Max \space P_tY_t - W_tN_t^d \\
   s.t. \space A_t(N^d_t)^{1-\alpha}
   $$

3. Market Clearing:
   $$
   Y_t = C_t \\
   N_t = N^d_t \\
   B_t = 0
   $$

**Solution: (First Order Condition)**

1. Household’s Problem:
   $$
   \lambda_t P_t = U_C(C_t, N_t) \\
   \lambda_t W_t + U_N(C_t, N_t) = 0 \\
   \lambda_t Q_t = \beta E_t[\lambda_{t+1}]
   $$

2. Firm’s Problem:
   $$
   (1-\alpha)P_tA_tN_t^{-\alpha} = W_t \\
   Y_t = \space A_t(N_t)^{1-\alpha} \\
   $$

3. Market Clearing:
   $$
   Y_t = C_t \\
   B_t = 0
   $$

From these 7 equations we solve $\{C_t, Y_t, B_t, N_t, \lambda_t, P_t, Q_t, W_t\}$, which is impossible. So we need another one equation, which is the monetary policy function.

**Assumption: (Utility Function Form)** Suppose the Utility Function is $U = C_t^{1-\sigma}/(1-\sigma) - N_t^{1+\phi}/(1+\phi)$.

**Solution: (Log-Linearization)**

We could define $i_t = 1/Q_t$, and take the form of the utility. Do the log-linearization and we will have the following equation system:
$$
\hat \lambda_t + \hat p_t = -\sigma \hat c_t \\
\hat \lambda_t + \hat w_t = \phi \hat n_t \\
\hat \lambda_t - \hat i_t = E_t[\hat \lambda_{t+1}] \\
\hat p_t + a_t -\alpha \hat  n_t  = \hat w_t \\
\hat y_t = a_t +(1-\alpha) \hat  n_t \\
\hat y_t =\hat  c_t \\
\hat b_t = 0
$$
From which we solve for $\{\hat c_t, \hat y_t, \hat b_t, \hat n_t, \hat \lambda_t, \hat p_t, \hat i_t, \hat w_t\}$. There are 7 equations but 8 unknowns. So we need another one equation, which is the monetary policy function.

**Solution: (Dichotomy Model)**

Now consider the real variables in the system, we have:
$$
\hat w_t - \hat p_t= \phi \hat n_t + \sigma \hat c_t\\
\hat w_t - \hat p_t = a_t -\alpha \hat  n_t\\
\hat y_t = a_t +(1-\alpha) \hat  n_t \\
\hat y_t =\hat  c_t \\
\hat b_t = 0
$$
from which $\{\hat w_t - \hat p_t, \hat n_t, \hat y_t , \hat c_t, \hat b_t\}$ is determined. It is not related to the nominal side of the model, which will give us:
$$
\hat y_t  = \frac{1 +\phi}{\alpha +\phi + \sigma(1-\alpha)}a_t
$$

#### Monetary Policy

**Definition: (Fisher Equation)**

From the Euler’s equation we have:
$$
- \hat i_t = E_t[-\sigma \hat y_{t+1}- \hat p_{t+1}] + \sigma \hat y_t+ \hat p_t
$$
Define $\hat \pi_{t+1} = \hat p_{t+1} - \hat p_{t}$ and $\hat r_t = \sigma E[\hat y_{t+1}-\hat y_t]$, so this equation becomes $\hat i_t =\hat r_t +  E_t[\hat \pi_{t+1}]$. This equation is called Fisher Equation.

**Definition: (Exogenous Feedback Interest Rate Rule)** The Exogenous Feedback Interest Rate Rule is taking the interest rate as given i.e. $\hat i_t$ is an exogenous stationary process.

**Note:** When then EFIR rule is used, we have $E_t[\hat \pi_{t+1}]= \hat i_t -\hat r_t$, so the expected nominal price level is pinned down, but the actually price level cannot be pinned down, leading to indeterminacy.

**Definition: (Endogenous Feedback Interest Rate Rule)** If we have $\hat i_t = \phi_\pi \hat \pi_t+\epsilon_t$ with $\phi_\pi>0$, we call this an Endogenous Feedback Interest Rate Rule.

**Theorem: (Taylor’s Rule)** When $\phi_\pi>1$, there is a determined path for the nominal price level. On the other hand, if $\phi_\pi\leq 1$, there is again indeterminacy.

Proof:

Combine the monetary policy and the Fisher equation, we have $\hat \pi_t=\frac{1}{\phi_\pi} E_t[\hat \pi_{t+1}] - \frac{1}{\phi_\pi}\epsilon_t +\frac{1}{\phi_\pi}\hat r_t$. So when $\phi_\pi>1$, by Blanchard Kahn theorem, there is a determined path for the nominal price level. On the other hand, if $\phi_\pi\leq 1$, there is again indeterminacy. $\square$ 



### Money in Utility

#### Money in Utility Model

**Definition: (Money in Utility)** The Equilibrium is defined as the following parts:

1. Household’s Problem:
   $$
   Max \space E_0\sum_{t=0}^{\infty} \beta^t U(C_t, N_t, \frac{M_t}{P_t}) \\s.t. \space P_t C_t + Q_t B_t + M_t= B_{t-1} + W_t N_t + M_{t-1} + \Pi_t + P_tT_t
   $$

2. Firm’s Problem:
   $$
   Max \space \Pi_t =  P_tY_t - W_tN_t^d \\s.t. \space A_t(N^d_t)^{1-\alpha}
   $$

3. Government:
   $$
   T_t  = \frac{M_t-M_{t-1}}{P_t}
   $$
   
4. Market Clearing:
   $$
   Y_t = C_t \\N_t = N^d_t \\B_t = 0
   $$

**Solution: (First Order Condition)**

1. Household’s Problem:
   $$
   \lambda_t P_t = U_C(C_t, N_t, \frac{M_t}{P_t}) \\
   \lambda_t W_t + U_N(C_t, N_t, \frac{M_t}{P_t}) = 0 \\
   \lambda_t Q_t = \beta E_t[\lambda_{t+1}] \\
    \beta E_t[\lambda_{t+1}] - \lambda_t + \frac{1}{P_t}U_M(C_t, N_t, \frac{M_t}{P_t}) = 0
   $$

2. Firm’s Problem:
   $$
   (1-\alpha)P_tA_tN_t^{-\alpha} = W_t \\
   Y_t = \space A_t(N_t)^{1-\alpha} \\
   $$

3. Market Clearing:
   $$
   Y_t = C_t \\
   B_t = 0
   $$

From these 8 equations we solve $\{C_t, Y_t, B_t, N_t, \lambda_t, P_t, Q_t, W_t, M_t\}$, which is impossible. So we need another one equation, which is the monetary policy function.

**Note:** The budget of the household can also be written as $P_tC_t + Q_t S_t + (1-Q_t)M_t = S_{t-1} + W_tN_t+\Pi_t +P_tT_t$, where $S_t = B_t+M_t$ denote all the asset that the consumer is holding. From this we can see $(1-Q_t)$ is the implicit price of buying a unit of cash. It has the same identity as the consumption or labor.

**Assumption: (Utility Function Form)** Suppose the Utility Function is $U = C_t^{1-\sigma}/(1-\sigma) - N_t^{1+\phi}/(1+\phi) + (\frac{M_t}{P_t})^{1-v}/(1-v)$.

**Solution: (Log-Linearization)**

We could define $i_t = 1/Q_t$, and take the form of the utility. Do the log-linearization and we will have the following equation system:
$$
\hat \lambda_t + \hat p_t = -\sigma \hat c_t \\
\hat \lambda_t + \hat w_t = \phi \hat n_t \\
\hat \lambda_t - \hat i_t = E_t[\hat \lambda_{t+1}] \\
-v(\hat m_t-\hat p_t) = \frac{\beta}{1-\beta} \hat i_t + (\hat \lambda_t + \hat p_t)  \\
 
\hat p_t + a_t -\alpha \hat  n_t  = \hat w_t \\
\hat y_t = a_t +(1-\alpha) \hat  n_t \\
\hat y_t =\hat  c_t \\
\hat b_t = 0
$$
From which we solve for $\{\hat c_t, \hat m_t, \hat y_t, \hat b_t, \hat n_t, \hat \lambda_t, \hat p_t, \hat i_t, \hat w_t\}$. There are 8 equations and 9 variables to solve, so we need the monetary policy function.

**Solution: (Dichotomy Model)**

Note that the following equations are still true:
$$
\hat w_t - \hat p_t= \phi \hat n_t + \sigma \hat c_t\\\hat w_t - \hat p_t = a_t -\alpha \hat  n_t\\\hat y_t = a_t +(1-\alpha) \hat  n_t \\\hat y_t =\hat  c_t \\\hat b_t = 0
$$
from which $\{\hat w_t - \hat p_t, \hat n_t, \hat y_t , \hat c_t, \hat b_t\}$ is determined.  So all the real variables are the same. We have
$$
\hat y_t  = \frac{1 +\phi}{\alpha +\phi + \sigma(1-\alpha)}a_t
$$
**Solution: (Nominal Side of the Model)**

From the Euler’s equation we have:
$$
- \hat i_t = E_t[-\sigma \hat y_{t+1}- \hat p_{t+1}] + \sigma \hat y_t+ \hat p_t
$$
Define $\hat \pi_{t+1} = \hat p_{t+1} - \hat p_{t}$ and $\hat r_t = \sigma E[\hat y_{t+1}-\hat y_t]$, so this equation becomes $\hat i_t =\hat r_t +  E_t[\hat \pi_{t+1}]$. So Fisher equation is still true. Then from the monetary demand equation we have
$$
\hat m_t-\hat p_t= \frac{\sigma}{v} \hat y_t  -\frac{1}{v(1-\beta)} \hat i_t
$$
This is called the monetary demand function.

#### Optimal Monetary Policy Rule

**Assumption: (Local Satiation of Money)** We assume that the utility function satisfies that there is a $\bar M$ such that $U_M(C_t, \frac{M_t}{P_t}, N_t) = 0$.

**Definition: (Social Planner’s Problem)** The social planner solves the following problem:
$$
Max\space U(C_t, \frac{M_t}{P_t}, N_t) \\
s.t. \space C_t = A_t N_t^{1-\alpha}
$$
**Solution: (First Best Solution)**

Taking the first order conditions we have:
$$
\frac{U_N(C_t, \frac{M_t}{P_t}, N_t)}{U_C(C_t, \frac{M_t}{P_t}, N_t)} = -(1-\alpha)A_tN_t^{-\alpha} \\
U_M(C_t, \frac{M_t}{P_t}, N_t) = 0
$$
This implies that the optimal monetary policy is to set $U_M = 0$. Note that is and the first order conditions implies that
$$
\lambda_t Q_t = \beta E_t[\lambda_{t+1}] \\
 \beta E_t[\lambda_{t+1}] - \lambda_t  = 0
$$
So we have $i_t^\star = 0$ as the optimal monetary policy rule.

**Corollary: (Friedman’s Rule)** The Friedman’s Rule implies that the optimal monetary rule should set the nominal interest rate to be 0 and let the inflation rate be negative. Remember that $\hat i_t =\hat r_t +  E_t[\hat \pi_{t+1}] = 0$ implies that $E_t[\hat \pi_{t+1}]=-\hat r_t<0$. 

## New Keynesian Model

### Monopolistic Competition

**Assumption: (Setup)**

- Price is flexible
- There are continuum of different firms producing different products
- firm’s technology is $Y_t = Z_tN_t$
- Each firm is a monopolist in its own industry
- Identical consumer aggregates the consumptions with Dixit-Stiglitz Form

**Definition: (Dixit-Stiglitz Form)** The consumer aggregates the consumptions with Dixit-Stiglitz Form for $\theta>1$
$$
C_t = [\int_0^1C_{jt}^{\frac{\theta-1}{\theta}}dj]^{\frac{\theta}{\theta-1}}
$$
**Definition: (Consumer’s Cost Minimization Problem)** Given the aggregate consumption level, the Consumer’s Cost Minimization Problem is
$$
min \int_0^1 P_{jt}C_{jt}dj \\
s.t.\space  [\int_0^1C_{jt}^{\frac{\theta-1}{\theta}}dj]^{\frac{\theta}{\theta-1}}\geq C_t
$$
**Solution: (Consumer’s Cost Minimization Problem)**

By first order condition, we have $P_{jt} = \psi_t ({C_{jt}}/{C_t})^{-\frac{1}{\theta}}$, where $\psi_t$ denote the Lagrange multiplier. Economically it is the shadow price of consumption, which means we could define the price index as $P_t = \psi_t$, and it will give us:
$$
\frac{P_{jt} }{\psi_t }= (\frac{C_{jt}}{C_t})^{-\frac{1}{\theta}} \\
C_{jt} =( \frac{P_{jt} }{\psi_t })^{-{\theta}} C_t \\
\int _0^1 (( \frac{P_{jt} }{\psi_t })^{-{\theta}} C_t)^{\frac{\theta-1}{\theta}}dj]^{\frac{\theta}{\theta-1}} = C_t \\
\psi_t^{-\theta} = \int _0^1 (( P_{jt})^{-{\theta}})^{\frac{\theta-1}{\theta}}dj]^{\frac{\theta}{\theta-1}} \\
P_t = \psi_t= \int _0^1 ( P_{jt})^{1-\theta}dj^{\frac{1}{1-\theta}}
$$
Note that according to this definition, we have $P_t C_t = \int_0^1 P_{jt}C_{jt}dj$.

**Definition: (Consumer’s Problem)** The Consumer’s Problem is
$$
Max \space E_0\sum_{t=0}^{\infty} \beta^t U = C_t^{1-\sigma}/(1-\sigma) - \chi N_t^{1+\eta }/(1+\eta ) \\
s.t. \space P_t C_t + Q_t B_t = B_{t-1} + W_t N_t  + \Pi_t
$$
**Solution: (Consumer’s Problem and Log Linearization)**

By first order condition we have 
$$
\lambda_t P_t = C_t^{-\sigma} \\
\lambda_t W_t = \chi N_t^\eta  \\
\lambda_t Q_t = \beta E_t[\lambda_{t+1}]
$$
Log linearize the model we have 
$$
\hat w_t-\hat p_t = \eta \hat n_t + \sigma \hat c_t \\
-\sigma \hat c_t-\hat p_t - \hat i_t = E_t[-\sigma\hat  c_{t+1}-\hat p_{t+1}]
$$
where $i_t = 1/Q_t$ and define $\pi_t = p_t-p_{t-1}$. Then we will have the following result:
$$
\hat w_t-\hat p_t = \eta \hat n_t + \sigma\hat  c_t \\
\hat c_t =  E_t[\hat c_{t+1}]  -\frac{1}{\sigma} (\hat i_t-E_t[\hat \pi_{t+1}])
$$
**Definition: (Firm’s Problem)** The Firm’s Problem is
$$
max \space \frac{P_{jt} }{P_t }( \frac{P_{jt} }{P_t })^{-{\theta}} Y_t - \frac{W_t}{P_tZ_t} ( \frac{P_{jt} }{P_t })^{-{\theta}} Y_t
$$
**Note:** When we have government expenditure, the Dixit-Stiglitz Form consumption and government expenditure ensures that $y_t(i) = c_t(i)+ g_t(i)= ( \frac{P_{jt} }{P_t })^{-{\theta}} C_t+( \frac{P_{jt} }{P_t })^{-{\theta}} G_t = ( \frac{P_{jt} }{P_t })^{-{\theta}} Y_t$.

**Solution: (Firm’s Problem)**

The first order condition gives us that
$$
(1-{\theta})( \frac{P_{jt} }{P_t })^{-\theta} +\theta \frac{W_t}{P_tZ_t} ( \frac{P_{jt} }{P_t })^{-{\theta}-1}  = 0
$$
Define $\frac{W_t}{P_tZ_t} = \varphi_t$ as the marginal cost, then take the log linearization, use symmetry and we will get
$$
\hat p_{jt}-\hat p_t = \hat \varphi_t = \hat w_t-\hat p_t-\hat z_t = 0
$$
**Definition: (Flexible Price Equilibrium)** A Equilibrium  is defined as a set of endogenous variables such that they solves the consumer’s problem and the firm’s problem and market clearing condition holds: $C_t = Y_t$.

**Solution: (Flexible Price Equilibrium)**

The Flexible Price Equilibrium is given by the following equations:
$$
\hat w^f_t-\hat p^f_t = \eta \hat n^f_t + \sigma \hat c^f_t \\
\hat c^f_t =  E_t[\hat c^f_{t+1}]  -\frac{1}{\sigma} (\hat i_t-E_t[\hat \pi^f_{t+1}]) \\
\hat w^f_t-\hat p^f_t=\hat z_t \\
\hat c^f_t = \hat y^f_t = \hat z_t + \hat n^f_t
$$
It will give us the solution to the equilibrium: $\eta (\hat y_t-\hat z_t) - \sigma \hat y_t = \hat z_t$, i.e. $\hat y_t = \frac{1+\eta}{\eta+\sigma}\hat z_t$.



### Sticky Price Model

**Assumption: (Setup)**

- Price is sticky
- There are continuum of different firms producing different products, each period only $1-w$ of them can change prices

**Definition: (Firm’s Problem)** The Firm’s Problem is
$$
max \space \sum_{i=0}^{+\infty}(w\beta)^i m_{t,t+i}[\frac{P_{jt} }{P_{t+i}}( \frac{P_{jt} }{P_{t+i} })^{-{\theta}} C_{t+i} - \frac{W_{t+i}}{P_{t+i}Z_{t+1}} ( \frac{P_{jt} }{P_{t+i} })^{-{\theta}} C_{t+i}] \\
m_{t,t+i} = \frac{U_c(C_{t+i})}{U_c(C_{t})}
$$
**Solution: (Firm’s Problem)**

The first order condition gives us that
$$
\sum_{i=0}^{+\infty}(w\beta)^im_{t,t+i}[(1-{\theta})( \frac{P_{jt} }{P_{t+i}}) +\theta \frac{W_{t+i}}{P_{t+i}Z_{t+i}} ]( \frac{P_{jt} }{P_{t+i}})^{-\theta}\frac{1}{P_{jt}} C_{t+i}  = 0
$$
Define $\frac{W_t}{P_tZ_t} = \varphi_t$ as the marginal cost, then take the log linearization, use symmetry and we will get
$$
\sum_{i=0}^{+\infty}(w\beta)^i (\hat p_{jt} -\hat  p_{t+i} - \hat \varphi_{t+i})= 0\\
\hat \varphi_t = \hat w_t-\hat p_t-\hat z_t \\
\hat p_{jt}  =(1-w\beta) \sum_{i=0}^{+\infty}(w\beta)^i (\hat  p_{t+i} + \hat \varphi_{t+i}) \\
\hat p_{jt}  =(1-w\beta)(\hat  p_{t} + \hat \varphi_t)+ w\beta \hat p_{jt+1}
$$
Now since only $(1-w)$ of the firm can change the price, we have the following relationship:
$$
P_t^{1-\theta} = (1-w) P_{jt}^{1-\theta}+wP_{t-1}^{1-\theta}
$$
After log linearization we have:
$$
\hat p_t = (1-w)\hat p_{jt}+w\hat p_{t-1} \\
\hat p_t - \hat p_{t-1}  = (1-w)(\hat p_{jt}-\hat p_{t-1})\\
\hat p_{jt} -\hat p_{t-1} =(1-w\beta)(\hat  p_{t} + \hat \varphi_t)+ w\beta \hat p_{jt+1}-\hat p_{t-1}+w\beta\hat p_t-w\beta\hat p_t \\
\frac{1}{1-w}(\hat p_t - \hat p_{t-1}) = (1-w\beta)(\varphi_t)+ w\beta \frac{1}{1-w}(\hat E_t\hat p_{t+1} - \hat p_{t})+\hat p_t -\hat p_{t-1}\\
\hat\pi_t =(1-w)(1-w\beta)\hat\varphi_t+w\beta E_t[\hat\pi_{t+1}]+(1-w)\hat\pi_t \\
\hat \pi_t = \beta  E_t[\hat\pi_{t+1}]+\frac{(1-w)(1-w\beta)}{w}\hat \varphi_t
$$
**Definition: (Flexible Price Equilibrium)** A Equilibrium  is defined as a set of endogenous variables such that they solve the consumer’s problem and the firm’s problem, and marketing clearing condition holds, i.e. $C_t = Y_t \neq Y'_t= Z_t N_t$.

**Note:** Notice that here we need to be careful about the aggregation: $Y_t\neq Y'_t$, however, after the log-linearization they are the same.

**Solution: (Flexible Price Equilibrium)**

The Flexible Price Equilibrium is given by the following equations:
$$
\hat w_t-\hat p_t = \eta \hat n_t + \sigma \hat c_t \\
\hat c_t =  E_t[\hat c_{t+1}]  -\frac{1}{\sigma} (\hat i_t-E_t[\hat \pi_{t+1}]) \\
\hat \pi_t = \beta  E_t[\hat\pi_{t+1}]+\frac{(1-w)(1-w\beta)}{w}\hat \varphi_t\\
\hat \varphi_t = \hat w_t-\hat p_t -\hat z_t\\
\hat c_t = \hat y_t = \hat z_t + \hat n_t
$$
It will give us the solution to the equilibrium: $\hat \varphi_t = \hat w_t-\hat p_t -\hat z_t = \eta \hat n_t + \sigma \hat c_t - \hat z_t = \eta(\hat y_t-\hat z_t) + \sigma\hat y_t-\hat z_t$. Note that $\hat \varphi_t^f = 0$, so we have $\hat \varphi_t = (\eta+\sigma)(\hat y_t-\hat y^f_t)$. Define the output gap as $\hat x_t = (\hat y_t-\hat y^f_t)$. So we have
$$
\hat \pi_t = \beta  E_t[\hat\pi_{t+1}]+\frac{(1-w)(1-w\beta)}{w}(\eta+\sigma)\hat x_t
$$
This is called the Dynamic IS Curve.

Now from the Euler equation we have 
$$
\hat y_t =  E_t[\hat y_{t+1}]  -\frac{1}{\sigma} (\hat i_t-E_t[\hat \pi_{t+1}]) \\
\hat y_t - \hat y^f_t =  E_t[\hat y_{t+1}- \hat y^f_{t+1}]  -\frac{1}{\sigma} (\hat i_t-E_t[\hat \pi_{t+1}]) +E_t[\hat y^f_{t+1}]- \hat y^f_t\\
$$
note that the flexible real interest rate is defined as $\hat r_t^f =\sigma (E_t[\hat y^f_{t+1}]- \hat y^f_t)$. Hence we will have
$$
\hat x_t =  E_t[\hat x_{t+1}]  -\frac{1}{\sigma} (\hat i_t-E_t[\hat \pi_{t+1}] - \hat r^f_t)
$$
This is called the New Keynesian Phillips Curve.

Combine DIS and NKPC and the monetary policy function we can solve the model.

**Definition: (Taylor’s Rule)** Define $\hat i_t = \phi_\pi \hat \pi_t + \phi_x x_t$. Taylor’s Rule tells us that $\phi_\pi>1$ and $\phi_x>0$ to get a unique solution.



## Optimal Monetary Policy

### Optimal Monetary Policy

#### Optimal Monetary Policy with No Cost Push Shock

**Claim: (Taylor’s Rule)** The Taylor’s rule indicates that given the DIS and the NKPC, the following statement is true:

- If $i_t = e_t$, then we have indeterminacy
- If $i_t = \phi_\pi\pi_t+ e_t$ and $\phi_\pi>1$, we have determinacy
- If $i_t = \phi_\pi\pi_t+\phi_x x_t+ e_t$ and $\phi_\pi+ \phi_x\frac{(1-\beta)}{\kappa}>1$, we have determinacy

**Theorem: (Divine Coincidence)** Notice that with no Cost Push Shock, the Optimal Monetary Policy is to set the interest rate according to: $i_t = r_t^f+\phi_\pi \pi_t$ with $\phi >1$.

Proof:

According to the DIS and the NKPC, $\pi_t = \chi \sum_{i = 0}^\infty \beta^i E_t[x_{t+i}]$. Hence the stable monetary policy rule such that $i_t = r_t^f$ would lead to zero output gap. $\square$ 

**Definition: (Wicksellian Interest Rate)** The Wicksellian Interest Rate is defined as $i_t = r_t^f$.

#### Optimal Monetary Policy with No Cost Push Shock

**Definition: (Markov Perfect Equilibrium)** The government decide the optimal monetary policy with the following mechanism:
$$
max -\Omega E_t[\sum_{i=0}^\infty  \beta^i (\pi_{t+i}^2 +\lambda (x_{t+i}-x^\star)^2)] \\
s.t. \space \pi_t = \beta E_t[\pi_{t+1}] +\kappa x_t+e_t
$$
where $e_t$ denote the cost push shock, and since the economy is aiming at the efficient level, we have $x^\star = 0$.

**Solution: (Optimal Monetary Policy with Commitment)**

The government solves 
$$
max -\frac{\Omega}2 E_t[\sum_{i=0}^\infty  \beta^i (\pi_{t+i}^2 +\lambda (x_{t+i})^2)] \\
s.t. \space \pi_t = \beta E_t[\pi_{t+1}] +\kappa x_t+e_t
$$
Taking first order conditions we have
$$
\pi_{t+i} +\psi_{t+i} - \psi_{t+i-1} = 0 \\
\lambda x_{t+i} - \kappa \psi_{t+i} = 0
$$
with $\psi_{t-1 }= 0$ given. Notice this means the policy will be time inconsistent. From a timeless perspective, we have the targeting rule as
$$
\pi_{t} = - {\frac{\lambda} {\kappa}} (x_{t} - x_{t-1}) \\
\pi_t = \beta E_t[\pi_{t+1}] +\kappa x_t+e_t \\
x_t =  E_t[x_{t+1}]  -\frac{1}{\sigma} (i_t-E_t[\pi_{t+1}] - r^f_t)
$$
**Solution: (Discretion Optimal Monetary Policy)**

The government solves 
$$
max -\frac{\Omega}2 E_t[\sum_{i=0}^\infty  \beta^i (\pi_{t+i}^2 +\lambda (x_{t+i})^2)] \\s.t. \space \pi_t = \beta E_t[\pi_{t+1}] +\kappa x_t+e_t
$$
where $E_t[\pi_{t+1}]$ is given. Taking first order conditions we have
$$
\pi_t+\psi_t = 0 \\
\lambda x_t-\kappa \psi_t = 0
$$
combine them we have the targeting rule under the Markov Perfect Equilibrium: $\pi_t = -\frac{\lambda}{\kappa} x_t$. To get a closed form of the implement of the monetary policy, combine the targeting rule with the DIS and the NKPC:
$$
\pi_t = -\frac{\lambda}{\kappa} x_t \\
\pi_t = \beta E_t[\pi_{t+1}] +\kappa x_t+e_t
$$
will give us that $x_t = \beta (\frac{\lambda}{\lambda + \kappa^2})E_[x_{t+1} ] - (\frac{\kappa}{\lambda + \kappa^2})e_{t}$. We assume that $e_t$ is independent, so $x_t = -\frac{\kappa}{\lambda +\kappa^2}e_t$ and $\pi_t = \frac{\lambda }{\lambda+\kappa^2}e_t$ 
$$
x_t =  E_t[x_{t+1}]  -\frac{1}{\sigma} (i_t-E_t[\pi_{t+1}] - r^f_t) \\
i_t  = \sigma(E_t[x_{t+1}]- x_t) + E_t[\pi_{t+1}] + r^f_t \\
i_t  = \frac{\sigma\kappa}{\lambda +\kappa^2}e_t + r^f_t +\phi_\pi (\pi_t-\pi_t) \\
i_t  = (\frac{\sigma\kappa}{\lambda +\kappa^2} - \phi_\pi\frac{\lambda }{\lambda+\kappa^2}) e_t + r^f_t +\phi_\pi \pi_t \\
$$
where $\phi_\pi>1$.



### Optimal Monetary Policy Extensions

**Solution: (Optimal Monetary Policy with Commitment)**
$$
max -\frac{\Omega}2 E_t[\sum_{i=0}^\infty  \beta^i (\pi_{t+i}^2 +\lambda (x_{t+i})^2)] \\
s.t. \space \pi_t = \beta (1-\phi)E_t[\pi_{t+1}] + \phi \pi_{t-1}+ \kappa x_t+e_t
$$
The first order conditions gives us that 
$$
\pi_{t} -\psi_{t} + (1-\phi) \psi_{t-1} + \phi \beta E_t\psi_{t+1} = 0 \\
\lambda x_{t} + \kappa \psi_{t} = 0
$$
with $\psi_{-1} = 0$. So we still have the inconsistency.

**Solution: (Discretion Optimal Monetary Policy)**

The government solves 
$$
V(\pi_{t-1}, e_t) = min \frac{1}2  (\pi_{t}^2 +\lambda (x_{t})^2) + \beta E_t[ V(\pi_t, e_{t+1}) ]\\
s.t. \space \pi_t = \beta (1-\phi)E_t[\pi_{t+1}] + \phi \pi_{t-1}+ \kappa x_t+e_t
$$
Guess and verify. Suppose $\pi_t = A_1 \pi_{t-1}+A_2 e_t$ and $x_t = B_1 \pi_{t-1}+B_2 e_t$. Then use the standard method to solve for the Euler’s Equation, we have
$$
\pi_t + \beta E_t[V_\pi(\pi_t, e_{t+1})] + (\beta (1-\phi)A_1 - 1) \theta_t = 0 \\
\lambda x_t + \kappa \theta_t = 0 \\
V_\pi(\pi_{t-1}, e_t) = \phi \theta _t
$$
We could also guess $\theta_t = C_1 \pi_{t-1}+C_2 e_t$. Plug it back into the above equations and we could guess and verify the final solution:
$$
\pi_t - \beta\phi \lambda/ \kappa E_t[ x_{t+1}  ] = (\beta (1-\phi)A_1 - 1) \lambda  / \kappa x_t \\
\pi_t = \beta (1-\phi)E_t[\pi_{t+1}] + \phi \pi_{t-1}+ \kappa x_t+e_t
$$
combine these two equations to get $A_1,A_2,B_1,B_2$, or
$$
\lambda x_t + \kappa \theta_t = 0 \\
\pi_t - \beta\phi \lambda/ \kappa E_t[ x_{t+1}  ] = (\beta (1-\phi)A_1 - 1) \lambda  / \kappa x_t \\
\pi_t = \beta (1-\phi)E_t[\pi_{t+1}] + \phi \pi_{t-1}+ \kappa x_t+e_t
$$
and combine these three equations to get $A_1,A_2,B_1,B_2, C_1, C_2$.