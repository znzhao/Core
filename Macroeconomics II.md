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
2. Saving: $s_t = a_t-a_{t-1} = y_t-\frac{r}{1+r}E_t[\sum_{j=0}^{+\infty}\frac{y_{t+j}}{(1+r)^j}]$. Or, we could also write saving as $s_t = \frac{r}{1+r}E_t[\sum_{j=0}^{+\infty}\frac{\Delta y_{t+j}}{(1+r)^j}]$, where $\Delta y_{t+j} = y_{t+j}-y_{t}$, i.e. the saving is negative expected present value of income decline.
3. Change in consumption: $\epsilon_{t+1} = \Delta c_{t+1} = c_{t+1}-c_t = \frac{r}{1+r}\sum_{j=0}^{+\infty}\frac{(E_{t+1}-E_{t})y_{t+j}}{(1+r)^j}$, i.e. the change in consumption is the revision of expectations of income.

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



