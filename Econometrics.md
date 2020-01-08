# Econometrics

## Content

[TOC]



## Preliminaries

### Probability

### Distribution



### Statistics and Convergence Theory

#### Random Sampling

**Definition: (Random Sample)** Suppose $\{X\}$ is the set of population, a subset $\{X_n\} \in \{X\}$ is called a Random Sample, where $X_i \sim f_X$ are mutually independent and have identical distribution.

**Note:** The joint PMF or PDF of $\{X_n\}$ is $f_{\{X_n\}} = \prod_{i = 1}^n f_X(x_i)$.

**Definition: (Estimator)** An estimator is a function of the sample, i.e. $\hat\theta = T(\{X_n\})$.

**Definition: (Sampling Distribution)** The distribution of $\hat\theta$ is called a sampling distribution.

#### Convergence

**Definition: (Convergence in Probability)** A sequence of Random Variables is said to converge in probability to $\mu\in \R$ if $lim_{n \to + \infty }P(|X_n-\mu|<\epsilon)=1$ for $\epsilon >0$.

**Definition: (Orders in Probability)** We write $X_n = O(n^r) $ if $X_n/n^r$ is bounded in probability, i.e. for any $\epsilon>0$, there exists $b \in \R$ and $N\in \R$ for $P(|X_n/n^r|>b)<\epsilon$.

**Definition: (Higher Orders in Probability)** We write $X_n = o(n^r) $ if $lim_PX_n/n^r = 0$.

**Definition: (Convergence in Distribution)** We say $X_n$ converges in distribution to $X$ when the CDF of $X_n$ converges to $X$, i.e. $lim_{n\to +\infty} F_{X_n}(x) = F_X(x)$ for all $x$.

**Theorem: (Continuous Mapping Theorem)** Suppose $lim_pX_n = \mu_X$, $lim_pY_n = \mu_Y$ , and $lim_dZ_n = Z$, the following statements are true:

1.  $lim_paX_n = a\mu_X$, where $a$ is a scaler
2.  $lim_pX_n+Y_n = \mu_X+\mu_Y$, $lim_pX_nY_n = \mu_X\mu_Y$, and $lim_pX_n/Y_n = \mu_X/\mu_Y$ if $\mu_Y\neq 0$
3.  If $g(.)$ is a continuous function, then  $lim_pg(X_n,Y_n) = g(\mu_X,\mu_Y)$
4.  $lim_daZ_n = aZ$, where $a$ is a scaler
5.  $lim_dX_n+Y_n Z_n = \mu_X+\mu_YZ$
6.  If $g(.)$ is a continuous function, then  $lim_dg(Z_n) = g(Z)$
7.  If $lim_pX_n = Z_n$ and $lim_dZ_n = Z$, then  $lim_dX_n = Z$

#### Law of Large Number

**Theorem: (Weak Law of Large number)** Assume that $\{X_i\}_{i=1}^N$ are $i.i.d.$ with $E[X_i] = \mu < +\infin$, and $Var(X_i)<+\infin$, then we have:
$$
lim_p \frac{1}{N}\sum_{i=1}^N X_i = \mu
$$

#### Central Limit Theorem

**Theorem: (Central Limit Theorem)**Assume that $\{X_i\}_{i=1}^N$ are $i.i.d.$ with $E[X_i] = \mu < +\infin$, and $Var(X_i) = \Sigma<+\infin$, then we have:
$$
\sqrt n(\bar X_n-\mu) = \sqrt n(\frac{1}{N}\sum_{i=1}^N X_i-\mu) =  \to^d N(0,\Sigma)
$$

#### Delta Method

**Theorem: (Delta Method)** Suppose $g(.)$ is twice continuously differentiable at $\mu$, such that $lim_p X_n = \mu$ and $\sqrt n(x_n-\mu) \to^d N(0,\Sigma)$, then:
$$
\sqrt n(g(X_n)-g(\mu)) \to^d Dg(\mu)N(0,\Sigma) = N(0,Dg(\mu)'\Sigma Dg(\mu))
$$



### Point Estimation and Confidence Intervals

#### Maximum Likelihood

**Definition: (Likelihood Function)** Likelihood Function of a sample is defined as:
$$
L_n(\theta) = \prod_{i=1}^nf(X_i, \theta)
$$
**Definition: (Maximum Likelihood Estimator)** Maximum Likelihood Estimator of a sample is defined as:
$$
\hat\theta = argmax[lnL_n(\theta)] = argmax[\sum_{i=1}^nlnf(X_i, \theta)]
$$

#### Method of Moments

**Definition: (Method of Moments Estimator)** When the population random variable $X$ have the following property:
$$
E[m(X,\theta)] = 0
$$
Then Method of Moments Estimator of a sample is the solution to the following equation:
$$
\sum_{i=1}^n m(X_n,\hat\theta)/n = 0
$$

#### Comparison of Estimators

**Definition: (Unbiasedness)** If $E[\hat \theta] = \theta$, then we say the estimator is unbiased.

**Definition: (Mean Square Error)** The mean square error of the estimation is defined by $MSE(\hat \theta)=E[(\hat\theta-\theta)^2] = (E[\hat\theta]-E[\theta])^2+var(\hat \theta)$

**Definition: (Efficiency)** Given two estimator $\hat \theta_1$ and $\hat \theta_2$, for a given sample size, if $Var(\hat\theta_1) \leq Var(\hat\theta_2)$, we say $\hat \theta_1$ is more efficient than $\hat \theta_2$.

**Definition: (Consistency)** The estimator is consistent if $lim_p\hat \theta_n = \theta$.

#### Confidence Intervals

Definition: (Confidence Interval) Given the data $\{S_n\}$ we observe, suppose $S_i\sim f(\theta)$. Let $L$ and $U$ be two statstics. We say $(L,U)$ is a $1-\alpha$ Confidence Interval for $\theta $ if $P(\theta\in (L,U)) = 1-\alpha$. 



### Statistical Inferences

#### Hypothesis Test

**Definition: (Null Hypothesis)** Suppose $\theta \in \Theta$ is a random parameter, Null Hypothesis is $H_0:\theta \in \Theta_0$.

**Definition: (Alternative Hypothesis)** Suppose $\theta \in \Theta$ is a random parameter, Alternative Hypothesis is $H_1:\theta \notin \Theta_0$.

**Definition: (Type I Error)** Type I Error is when you reject $H_0$ when it is correct.

**Definition: (Type II Error)** Type II Error is when you accept $H_0$ when it is not correct.

**Note:** Type I Error is much worse than Type II Error.

**Definition: (Decision Rule)** Given the data $\{S_n\}$ we observe, we setup a rejection region $ C $, such that if $S_n \in C$ we reject $H_0$, if $S_n \notin C$ we refuse to reject $H_0$.

**Definition: (Size)** The size of a Hypothesis Test is the probability of making type I error, i.e. $size = P(S_n\in C|\theta_0)$.

**Definition: (P-Value)** Suppose $H_0$ is true and a given rejection region $ C $, P-Value is defined as $P(C) = P(S_n\in C|\theta_0)$

**Definition: (Power)** The size of a Hypothesis Test is the probability of not making type II error, also known as the probability of rejecting a given alternative hypothesis $\theta \in \Theta \backslash\Theta_0$, i.e. $power(\theta) = P(S_n\in C|\theta \in \Theta \backslash\Theta_0)$.

**Note:** We would want the power to be high and the size to be low.

#### Comparison of Decision Rules

**Definition: (Unbiased Test)** A test is called unbiased if it is more likely to reject under Alternative Hypothesis than under then Null Hypothesis.

**Definition: (Consistent Test)** A test is called consistent if $lim_{n\to +\infty} P(S_n\in C|\theta \in \Theta \backslash\Theta_0)  =1$.



## Ordinary Least Squares Estimation

### Regression Model

#### General Regression Model

**Definition: (General Regression Model)** A regression model is defined as:
$$
y = m(x)+\epsilon
$$
with $E[\epsilon|x] = 0$ and $E[\epsilon^2|x] =  \sigma^2(x)$.

#### Linear Regression Model

**Definition: (Linear Regression Model)** A linear regression model is defined as:
$$
y = x'\beta+\epsilon
$$
with $E[\epsilon|x] = 0$ and $E[\epsilon^2|x] =  \sigma^2(x)$.

**Theorem: (Linear Projection)** The best linear predictor is defined as $P(y|x) = x'\beta$, where beta is defined as 
$$
\beta =E[xx']^{-1}E[xy] = argminE[(y-x'b)^2]
$$
**Definition: (Sample)** A sample $\{(X,Y)\}$ is drawn from the population $\{(x,y)\}$.

**Definition: (Sample Regression Model)** A linear regression model of the sample is defined as:
$$
Y = X\beta+e
$$
with $E[e|X] = 0$ and $E[e^2|X] =  \sigma^2(X)$.

**Definition: (Least Square Estimator)** A least square estimator is defined as:
$$
\hat \beta = argmin(\frac{1}{n}\sum_{i=1}^n (y_i-x_i'b)^2) = argmin(\frac{1}{n}(Y-Xb)'(Y-Xb))
$$

#### Assumption

**Assumption 1: (Random sampling)** Each Sample is drawn with i.i.d.

**Assumption 2: (No Perfectly Collinearity)** $X’X$ is invertible.

**Assumption 3’: (Zero Correlation)** $E[Xe] = 0$.

**Assumption 3: (Zero Conditional Mean)** $E[e|X] = 0$.

**Note:** Zero Conditional Mean is stronger than Zero Correlation.

**Assumption 4’: (Heteroskedasticity)** $E[e^2|X] =  \sigma^2(X)$.

**Assumption 4: (Homoscedasticity)** $E[e^2|X] =  \sigma^2$.

**Assumption 5: (Gaussian Error)** $e|X \sim N(0,\sigma^2)$.



### Estimator

#### Maximum Likelihood Estimator

**Assumption: (MLE Estimator)** 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean
4. Homoscedasticity
5. Gaussian Error

**Theorem: (Maximum of Likelihood Estimator of OLS)** Under the required assumption, the Maximum of Likelihood Estimator of the regression model is:
$$
\hat\beta = (X'X)^{-1}X'Y = (\sum_{i=1}^nx_ix_i')^{-1}\sum_{i=1}^nx_iy_i
$$

$$
\hat\sigma^2=\hat e'\hat e/n=(Y-X\hat\beta)'(Y-X\hat\beta)/n= \sum_{i=1}^n(y_i-x_i'\hat\beta)^2/n
$$

#### Least Square Estimator

**Assumption: (OLS Estimator)** 

1. Random sampling
2. No Perfectly Collinearity

**Theorem: (OLS Estimator)** Under the required assumption, the OLS Estimator is:
$$
\hat\beta = (X'X)^{-1}X'Y = (\sum_{i=1}^nx_ix_i')^{-1}\sum_{i=1}^nx_iy_i
$$
**Definition: (Prediction)** Under the required assumption, the Prediction of the dependent variable is defined as:
$$
\hat Y = X\hat\beta = X(X'X)^{-1}X'Y
$$
**Definition: (Residual)** Under the required assumption, the Residual of the estimation is defined as:
$$
\hat e =Y-\hat Y = Y-X\hat\beta = Y- X(X'X)^{-1}X'Y
$$
**Definition: (Projection Matrix)** The Projection Matrix is Defined as:
$$
P_X = X(X'X)^{-1}X'
$$
**Definition: (Orthogonal Projection Matrix)** The Orthogonal Projection Matrix is Defined as:
$$
M_X = I- X(X'X)^{-1}X'
$$
#### Leverage

**Definition: (Leverage)** The Leverage of the estimation is defined as $h_{ii} = x_i'(X'X)^{-1}x_i$.
**Definition: (Influence)** The predict estimator is defined as $\hat\beta_{-i} = \hat\beta - (1-h_{ii})^{-1}(X'X)^{-1}x_i\hat e_i $, and we define the prediction residual as $\tilde e_i = y_i - x_i'\hat\beta_{-i} = \hat e_i/(1-h_{ii})$.

**Note:** $x_i'\hat\beta - x_i'\hat\beta_{-i} = h_{ii}\tilde e_i$.

#### General Properties of the Estimation

**Theorem: (Properties of the Estimator and Residual)** Under Assumption 1 and 2, the OLS Estimator and the Residual has the following properties:

1. $\hat Y  = P_X Y$, and $\hat e = M _X e = M_X Y$
2. $\hat e'\hat e = e'M_Xe = Y'M_XY$
3. $X'\hat e = 0$ and $\hat Y \hat e = 0$
4. If the independent variables include constant, i.e.  $x_1 = \iota$, then $\sum_{i=1}^n\hat e = 0$, and $\bar y = \bar{\hat y}$

**Theorem: (Properties of the Projection Matrix)** Under Assumption 1 and 2, the Projection Matrix has the following properties:

1. $P_X$ is symmetric and idempotent, i.e. $P_X' = P_X$, and $P_X P_X = P_X$ 
2. $P_X \iota = \iota$
3. $P_X X = X$
4. $P_\iota = \iota\iota’/n$
5. $P_\iota Y = \bar y$
6. $Trace(P_X) = k$

**Theorem: (Properties of the Orthogonal Projection Matrix)** Under Assumption 1 and 2, the Orthogonal Projection Matrix has the following properties:

1. $M_X$ is symmetric and idempotent, i.e. $M_X' = M_X$, and $M_X M_X = M_X$ 
2. $M_X X = 0$
3. $M_\iota = I-\iota\iota’/n$
4. $Trace(M_X) = n-k$

**Theorem: (Properties of the Leverage)** Under Assumption 1 and 2, the Leverage has the following properties:

1. $h_{ii}$ is the i-th element on the diagonal of $P_X$
2. $\sum_{i=1}^n h_{ii} = k$
3. $h_{ii}\in [0,1]$

#### Special Cases

**Theorem: (Special Regressor)** The following statements are true:

1. When $k = 1$ and $X_1 = \iota$, $\hat\beta = \bar y$
2. When $k=1$ and $X_1 = x$, $\hat\beta = \sum_{i = 1}^nx_iy_i/\sum_{i = 1}^nx_i^2$
3. When $k=2$ and $X_1 = \iota$, $X_2 = x$, then $\hat\beta_1 = \bar y -\bar x\hat\beta_2$, and $\hat\beta_2 = \sum_{i = 1}^n(x_i-\bar x) (y_i-\bar y)/\sum_{i = 1}^n(x_i-\bar x)^2$
4. (Transformations) When regress $Y$ on $XC$, the estimator is $\hat \beta^* = C^{-1}\hat\beta$, and $\hat Y^*  = \hat Y $
5. (Transformations) When regress $a+bY$ on $X_1$ and $ X_2 $, the estimator is $\hat\beta_1^* = a+ b \hat\beta_1$, and  $ \hat\beta_2^* = b \hat\beta_2$



### Partitioned Regression

#### Partitioned Regression

**Theorem: (Partitioned Regression)** Suppose we see the regression model as $Y = X_1\beta_1+X_2\beta_2+e$, then we have:
$$
\hat \beta_1 = (X_1'M_{X_2}X_1)^{-1}X_1'M_{X_2}Y,\space \hat \beta_2 = (X_2'M_{X_1}X_2)^{-1}X_2'M_{X_1}Y
$$
or
$$
\hat \beta_1 = ((M_{X_2}X_1)'M_{X_2}X_1)^{-1}(M_{X_2}X_1)'Y,\space \hat \beta_2 = ((M_{X_1}X_2)'M_{X_1}X_2)^{-1}(M_{X_1}X_2)'Y
$$
i.e. the regression of the residuals of $Y$ and $X_i$ on $X_j$.

#### Special Cases

**Theorem: (Special Partitioned Regression)** The following statements are true:

1. When $\hat \beta_1$ is a scaler and there is an intercept in $X_2$, then $\hat \beta_1 = X_1'M_{X_2}Y / (X_1'M_{X_2}X_1)$
2. Generally, when $X_1 = \iota$, then the regression will pass the mean of the sample, i.e.

$$
\hat\beta_1 = \bar y -\bar x'\hat\beta_2=(\iota'M_{X_2}\iota)^{-1}\iota'M_{X_2}Y
$$

$$
\hat\beta_2 = [\sum_{i = 1}^n(x_i-\bar x)(x_i-\bar x)']^{-1} \sum_{i = 1}^n(x_i-\bar x) (y_i-\bar y)' = (X_2'M_\iota X_2)^{-1}X_2'M_\iota Y
$$



### R-Squared

#### Variation Partition

**Definition:(Total Sum of Square)** Total Sum of Square is defined as $SST = (Y-\iota\bar y)'(Y-\iota\bar y)$.

**Definition:(Regression Sum of Square)** Regression Sum of Square is defined as $SSR = (\hat Y-\iota\bar y)'(\hat Y-\iota\bar y) = \hat\beta' X'M_\iota X \hat\beta$.

**Definition:(Sum of Square Error)** Sum of Square Error is defined as $SSE = \hat e’ \hat e = \sum_{i=1}^n \hat e_i^2$.

**Theorem: (Variation Partition)** The following statements are true:

1. $Y = P_X Y +M_X Y$
2. $SST = SSR+SSE$

#### R-Squared

**Definition:(R-Squared)** R-Squared is defined as $R^2 = SSR/SST = 1-SSE/SST$.

**Theorem: (Properties of R-Squared)** The following statements are true:

1.  $R^2 = corr(Y,\hat Y)^2$
2. $R^2 \in [0,1]$
3. When k increases, R-squared will always increase.

#### Adjusted R-Squared

**Definition:(Adjusted R-Squared)** Adjusted R-Squared is defined as:
$$
R^2 = 1-\frac{SSE/(n-k-1)}{SST/(n-1)}
$$



## Properties of Estimator and Applications

### General Small Sample Result

**Assumption: (Small Sample Assumption)** 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean, i.e. $E[e_i|x_i] = 0$

**Theorem: (Small Sample Result)** Under Assumption 1, 2 and 3, the following properties are true:

1. $\hat\beta$ is an unbiased estimator, i.e. $E[\hat \beta] = \beta$, and $E[\hat e] = 0$

2. $Var(\hat\beta|X) = (X'X)^{-1}X'\Sigma X(X'X)^{-1}$, where $\Sigma = E[ee'|X] = diag[\sigma^2(x_i)]$

3. $Var(\hat e | X) =  M_X \Sigma M_X'$

   And when Homoscedasticity is true, we have:

4. $Var(\hat\beta|X) = \sigma^2(X'X)^{-1}$

5. $Var(\hat e | X) = \sigma^2 M_X$

6. $E[\hat e_i^2|X] = \sigma^2(1-h_{ii})$



### Variance Estimation

**Definition: (Heteroskedasticity variance estimator)** When Assumption 1-3 are true and Heteroskedasticity is true, define the estimator of the variance of $\hat\beta$ as:
$$
\hat V(\hat\beta|X) = (X'X)^{-1}X'S X(X'X)^{-1}
$$
where $S = \hat\Sigma = diag[\hat e_i^2]$

**Definition: (Homoscedasticity variance estimator)** When Assumption 1-3 are true and Homoscedasticity is true, define the estimator of the variance of $\hat e$ as:
$$
s^2 = \frac{\hat e'\hat e}{n-k}
$$
**Definition: (Standardized Residual)** When Homoscedasticity is true, define the Standardized Residual as:
$$
\bar e_i = \frac{\hat e}{\sqrt{1-h_{ii}}}
$$
**Definition: (Homoscedasticity variance estimator)** When Homoscedasticity is true, define the estimator of the variance of $e$ as:
$$
\tilde\sigma^2 = \frac{\sum_{i=1}^n\bar e_i^2}{n}
$$
**Note:** Under Homoscedasticity, $\hat\sigma^2$, $s^2$, and $\tilde\sigma^2$ are all estimators of $\sigma^2$, where the first is the MLE estimator, and the second and the third are generated because they are unbiased.

**Definition: (Homoscedasticity variance estimator)** When Homoscedasticity is true, define the estimator of the variance of $\hat\beta$ as:
$$
\hat V(\hat\beta|X) = s^2(X'X)^{-1}
$$
**Theorem: (Expectation of the variance estimator)** Under Assumption 1, 2, and 3, the following properties are true:

1. $E[\hat V(\hat\beta|X)] = Var(\hat\beta|X)$

   And when Homoscedasticity is true, we have:

2. $E[s^2] = E[\tilde\sigma^2] = \sigma^2$, but $E[\hat \sigma^2] = (n-k)\sigma^2$



### Gauss Markov Theorem

#### Efficient Estimator

**Assumption: (Gauss Markov Assumption)** 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean, i.e. $E[e_i|x_i] = 0$
4. Homoscedasticity
5. Gaussian Error

**Theorem: (Gauss Markov Theorem)** Under Assumption 1-5, OLS estimator is Best Linear Unbiased Estimator(BLUE).

**Theorem: (WLS Theorem)** Under Assumption 1, 2, 3, and Heteroskedasticity,  OLS estimator is not the Best Linear Unbiased Estimator(BLUE), instead, The BLUE is:
$$
\hat\beta_W = (X'\Sigma^{-1}X)^{-1}X'\Sigma^{-1}Y
$$

#### Small Sample Distribution Result

**Assumption: (Small Sample Distribution Assumption)** 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean, i.e. $E[e_i|x_i] = 0$
4. Homoscedasticity
5. Gaussian Error

**Theorem: (Conditional Distribution)** Under Assumption 1-5, the following statement are true:

1. $\hat \beta |X \sim N(\beta ,\sigma^2(X'X)^{-1})$
2. $\hat e |X \sim N(0,\sigma^2M_X)$
3. $\hat \beta$ is independent to $\hat e$
4. $(n-k)s^2/\sigma^2 \sim \chi^2(n-k)$
5. $\hat \beta$ is independent to $s^2$
6. $T_j|X=\frac{\hat \beta_j -\beta_j}{\sqrt{\sigma^2[(X'X)^{-1}]_{jj}}}|X \sim N(0,1)$
7. $\hat T_j|X=\frac{\hat \beta_j -\beta_j}{\sqrt{s^2[(X'X)^{-1}]_{jj}}}|X \sim T(n-k)$
8. When $C$ is a $1\times k$ vector, we have $\hat T'|X=\frac{C\hat \beta -C\beta}{\sqrt{s^2C(X'X)^{-1}C'}}|X \sim T(n-k)$
9. When $R$ is a $J \times k$ matrix, we have $F|X=\frac{(R(\hat \beta-\beta ))'(R(X'X)^{-1}R')^{-1}(R(\hat\beta - \beta))/J}{\sigma^2}|X \sim \chi^2(J)/J$
10. When $R$ is a $J \times k$ matrix, we have $\hat F|X=\frac{(R(\hat \beta-\beta ))'(R(X'X)^{-1}R')^{-1}(R(\hat\beta - \beta))/J}{s^2}|X \sim F(J,n-k)$

Theorem: (Partitioned Regression) Suppose we see the regression model as $Y = X_1\beta_1+X_2\beta_2+e$. Under Assumption 1-5, we have:

1. $\hat \beta_1 |X \sim N(\beta_1 ,\sigma^2(X_1'X_1 - X_1'X_2(X_2'X_2)^{-1}X_2'X_1)^{-1})$
2. $\hat \beta_2 |X \sim N(\beta_2 ,\sigma^2(X_2'X_2 - X_2'X_1(X_1'X_1)^{-1}X_1'X_2)^{-1})$



### Large Sample Theory

#### Theory Under Heteroscedasticity

**Assumption: (Large Sample Distribution Assumption with Heteroscedasticity)** 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Correlation, i.e. $E[x_ie_i] = 0$
4. $E[x_ix_i'e_i^2] = \Omega < +\infin$
5. $E[x_ix_i'] = Q_{xx} < +\infin$ and it is positive definite

**Theorem: (Consistency)** Under Assumption 1-5, suppose we have large sample, then the OLS estimator is consistent.

**Theorem: (Asymptotic Result)** Under Assumption 1-5, suppose we have large sample, then the following results are true:

1. $\sqrt n (\hat \beta - \beta)|X \to^d N(0,Q_{xx}^{-1}\Omega Q_{xx}^{-1})$
2. $lim_p n V(\hat\beta|X) = Q_{xx}^{-1}\Omega Q_{xx}^{-1}$
3. $lim_p n\hat V(\hat\beta|X) = Q_{xx}^{-1}\Omega Q_{xx}^{-1}$
4. $\hat T_j|X=\frac{\hat \beta_j -\beta_j}{\sqrt{\hat V(\hat\beta|X)_{jj}}}|X \to^d N(0,1)$
5. When $C$ is a $1\times k$ vector, we have $\hat T'|X=\frac{C\hat \beta -C\beta}{\sqrt{C\hat V(\hat\beta|X)C'}}|X \to^d N(0,1)$
6. When $R$ is a $J \times k$ matrix, we have $F|X=(R(\hat \beta-\beta ))'(R V(\hat\beta|X)R')^{-1}(R(\hat\beta - \beta))/J|X \to^d \chi^2(J)/J$
7. When $R$ is a $J \times k$ matrix, we have $\hat F|X=(R(\hat \beta-\beta ))'(R \hat V(\hat\beta|X)R')^{-1}(R(\hat\beta - \beta))/J|X \to^d \chi^2(J)/J$
8. Generally, suppose $g(.)$ is a function system with $J$ equations, $\sqrt n (g(\hat \beta)-g(\beta)) \to^d N(0,G'Q_{xx}^{-1}\Omega Q_{xx}^{-1}G)$, where $G = \partial g(\beta)/\partial \beta|_\hat\beta$
9. Generally, suppose $g(.)$ is a function system with $J$ equations, $\hat W = (g(\hat \beta)-g(\beta))'(G'\hat V(\hat\beta|X)G)^{-1}(g(\hat \beta)-g(\beta))/J \to^d \chi^2(J)/J$, where $G = \partial g(\beta)/\partial \beta|_\hat\beta$

#### Theory Under Homoscedasticity

**Assumption: (Large Sample Distribution Assumption with Homoscedasticity)** 

1. Random sampling

2. No Perfectly Collinearity

3. Zero Correlation, i.e. $E[x_ie_i] = 0$

4. $E[x_ix_i'e_i^2] = \Omega < +\infin$

5. $E[x_ix_i'] = Q_{xx} < +\infin$ and it is positive definite

6. Homoscedasticity

**Theorem: (Asymptotic Result with Homoscedasticity)** Under Assumption 1-6, suppose we have large sample and  Homoscedasticity is true, we have:

1. $\sqrt n (\hat \beta - \beta) |X \to^d N(0,\sigma^2Q_{xx}^{-1})$
2. $lim_p n \sigma^2(X'X)^{-1} = \sigma^2Q_{xx}^{-1}$
3. $lim_p n s^2(X'X)^{-1} = \sigma^2Q_{xx}^{-1}$
4. $\hat T_j|X=\frac{\hat \beta_j -\beta_j}{\sqrt{s^2[(X'X)^{-1}]_{jj}}}|X \to^d N(0,1)$
5. When $C$ is a $1\times k$ vector, we have $\hat T'|X=\frac{C\hat \beta -C\beta}{\sqrt{s^2[C(X'X)^{-1}C']}}|X \to^d N(0,1)$
6. When $R$ is a $J \times k$ matrix, we have $F|X=\frac{(R(\hat \beta-\beta ))'(R(X'X)^{-1}R')^{-1}(R(\hat\beta - \beta))/J}{\sigma^2}|X \to^d \chi^2(J)/J$
7. When $R$ is a $J \times k$ matrix, we have $\hat F|X=\frac{(R(\hat \beta-\beta ))'(R(X'X)^{-1}R')^{-1}(R(\hat\beta - \beta))/J}{s^2}|X \to^d \chi^2(J)/J$
8. Generally, suppose $g(.)$ is a function system with $J$ equations, $\sqrt n (g(\hat \beta)-g(\beta)) \to^d N(0,\sigma^2G'Q_{xx}^{-1}G)$, where $G = \partial g(\beta)/\partial \beta|_\hat\beta$
9. Generally, suppose $g(.)$ is a function system with $J$ equations,  $\hat W = \frac{(g(\hat \beta)-g(\beta))'(G'(X'X)^{-1}G)^{-1}(g(\hat \beta)-g(\beta))/J}{s^2} \to^d \chi^2(J)/J$, where $G = \partial g(\beta)/\partial \beta|_\hat\beta$

Theorem: (Partitioned Regression) Suppose we see the regression model as $Y = X_1\beta_1+X_2\beta_2+e$. Under Assumption 1-6, suppose we have large sample and  Homoscedasticity is true, we have:

1. $\sqrt n (\hat\beta_1 - \beta_1) |X \to^d N(0 ,\sigma^2 (Q_{11} - Q_{12}Q_{22} ^{-1} Q_{21})^{-1})$
2. $\sqrt n (\hat\beta_2 - \beta_2) |X \to^d N(0 ,\sigma^2 (Q_{22} - Q_{21}Q_{11} ^{-1} Q_{12})^{-1})$



### Hypothesis Test

#### Assumption

**Assumption: (Small Sample)**

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean, i.e. $E[e_i|x_i] = 0$
4. Homoscedasticity
5. Gaussian Error

**Assumption: (Large Sample)** 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Correlation, i.e. $E[x_ie_i] = 0$
4. $E[x_ix_i'e_i^2] = \Omega < +\infin$
5. $E[x_ix_i'] = Q_{xx} < +\infin$ and it is positive definite

**Assumption: (Large Sample with Homoscedasticity)** 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Correlation, i.e. $E[x_ie_i] = 0$
4. $E[x_ix_i'e_i^2] = \Omega < +\infin$
5. $E[x_ix_i'] = Q_{xx} < +\infin$ and it is positive definite
6. Homoscedasticity

#### T test

**Definition: (Test with Small Sample)** Under the Assumption about small sample, we use the T estimator to do Hypothesis Test for $H_0: \beta =0$, and $H_1:\beta \neq 0$, i.e. reject if $\hat T \notin [-T_{\alpha/2},T_{\alpha/2}]$, where $\hat T$ is defined as:
$$
\hat T_j|X=\frac{\hat \beta_j -\beta_j}{\sqrt{s^2[(X'X)^{-1}]_{jj}}}|X \sim T(n-k)
$$
**Definition: (Test with Large Sample)** Under the Assumption about large sample and heteroskedasticity, we use the T estimator to do Hypothesis Test for $H_0: \beta =0$, and $H_1:\beta \neq 0$, i.e. reject if $\hat T \notin [-T_{\alpha/2},T_{\alpha/2}]$, where $\hat T$ is defined as:
$$
\hat T_j|X=\frac{\hat \beta_j -\beta_j}{\sqrt{\hat V(\hat\beta|X)_{jj}}}|X \to^d N(0,1)
$$
**Definition: (Test with Large Sample and Homoscedasticity)** Under the Assumption about large sample and homoscedasticity, we use the T estimator to do Hypothesis Test for $H_0: \beta =0$, and $H_1:\beta \neq 0$, i.e. reject if $\hat T \notin [-T_{\alpha/2},T_{\alpha/2}]$, where $\hat T$ is defined as:
$$
\hat T_j|X=\frac{\hat \beta_j -\beta_j}{\sqrt{s^2[(X'X)^{-1}]_{jj}}}|X \to^d N(0,1)
$$
**Theorem: (Unbiased and Consistent T-Test)** The T-Test described above is unbiased under small sample assumption, and consistent under large sample assumption.

#### T Test with General Linear Restriction

**Definition: (Test with Small Sample)** Under the Assumption about small sample, we use the linear combined T estimator to do Hypothesis Test for $H_0: C\beta -r =0$, and $H_1:C\beta -r\neq 0$, where $C$ is a $1\times k$ vector, i.e. reject if $\hat T' \notin [-T_{\alpha/2},T_{\alpha/2}]$, where $\hat T'$ is defined as:
$$
\hat T'|X=\frac{C\hat \beta -r}{\sqrt{s^2C(X'X)^{-1}C'}}|X \sim T(n-k)
$$
**Definition: (Test with Large Sample)** Under the Assumption about large sample and heteroscedasticity, we use the linear combined T estimator to do Hypothesis Test for $H_0: C\beta -r =0$, and $H_1:C\beta -r\neq 0$, where $C$ is a $1\times k$ vector, i.e. reject if $\hat T' \notin [-N_{\alpha/2},N_{\alpha/2}]$, where $\hat T'$ is defined as:
$$
\hat T'|X=\frac{C\hat \beta -r}{\sqrt{C\hat V(\hat\beta|X)C'}}|X \to^d N(0,1)
$$
**Definition: (Test with Large Sample and Homoscedasticity)** Under the Assumption about large sample and homoscedasticity, we use the linear combined T estimator to do Hypothesis Test for $H_0: C\beta -r =0$, and $H_1:C\beta -r\neq 0$, where $C$ is a $1\times k$ vector, i.e. reject if $\hat T' \notin [-N_{\alpha/2},N_{\alpha/2}]$, where $\hat T'$ is defined as:
$$
\hat T'|X=\frac{C\hat \beta -r}{\sqrt{s^2[C(X'X)^{-1}C']}}|X \to^d N(0,1)
$$

#### F test

**Definition: (Test with Small Sample)** Under the Assumption about small sample, we use the F estimator to do Hypothesis Test for $H_0: R\beta -r =0$, and $H_1:R\beta -r\neq 0$, where $R$ is a $J\times k$ vector, i.e. reject if $\hat F \in [F_{\alpha},+\infty]$, where $\hat F$ is defined as:
$$
\hat F|X=\frac{(R\hat \beta-r )'(R(X'X)^{-1}R')^{-1}(R\hat \beta-r ))/J}{s^2}|X \sim F(J,n-k)
$$
**Theorem: (Alternative Derivation of F Statistic)** Under the small sample assumptions, suppose we have $SSE_U = (Y-X\hat\beta)'(Y-X\hat\beta)$, and $SSE_R = (Y-X\tilde\beta)'(Y-X\tilde\beta)$ where $\tilde \beta = \hat \beta -(X'X)^{-1}R'(R(X'X)^{-1}R')^{-1}(R\hat \beta-r)$, then we have:
$$
\hat F = \frac{(SSE_R-SSE_U)/J}{SSE_U/(n-k)}
$$
**Definition: (Test with Large Sample)** Under the Assumption about large sample and heteroscedasticity, we use the  F estimator to do Hypothesis Test for $H_0: R\beta -r =0$, and $H_1:R\beta -r\neq 0$, where $R$ is a $J\times k$ vector, i.e. reject if $\hat F \in [\chi^2_{\alpha},+\infty]$, where $\hat F$ is defined as:
$$
\hat F|X=(R\hat \beta-r )'(R \hat V(\hat\beta|X)R')^{-1}(R\hat \beta-r )/J|X \to^d \chi^2(J)/J
$$
**Definition: (Test with Large Sample and Homoscedasticity)** Under the Assumption about large sample and homoscedasticity, we use the F estimator to do Hypothesis Test for $H_0: R\beta -r =0$, and $H_1:R\beta -r\neq 0$, where $R$ is a $J\times k$ vector, i.e. reject if $\hat F \in [\chi^2_{\alpha},+\infty]$, where $\hat F$ is defined as:
$$
\hat F|X=\frac{(R\hat \beta-r )'(R(X'X)^{-1}R')^{-1}(R\hat \beta-r )/J}{s^2}|X \to^d \chi^2(J)/J
$$
**Theorem: (Unbiased and Consistent F-Test)** The F-Test described above is unbiased under small sample assumption, and consistent under large sample assumption.

#### Wald Test for General Non-linear Restriction

**Definition: (Test with Large Sample)** Under the Assumption about large sample and heteroscedasticity, we use the Wald estimator to do Hypothesis Test for $H_0: g(\beta) =0$, and $H_1:g(\beta) \neq 0$, i.e. reject if $\hat W \in [\chi^2_{\alpha},+\infty]$, where $\hat W$ is defined as:
$$
\hat W = g(\hat \beta)'(G'\hat V(\hat\beta|X)G)^{-1}g(\hat \beta)/J \to^d \chi^2(J)/J
$$
, where $G = \partial g(\beta)/\partial \beta|_\hat\beta$

**Definition: (Test with Large Sample and Homoscedasticity)** Under the Assumption about large sample and homoscedasticity, we use the Wald estimator to do Hypothesis Test for $H_0: g(\beta) =0$, and $H_1:g(\beta) \neq 0$, i.e. reject if $\hat W \in [\chi^2_{\alpha},+\infty]$, where $\hat W$ is defined as:
$$
\hat W = \frac{g(\hat \beta)'(G'(X'X)^{-1}G)^{-1}g(\hat \beta)/J}{s^2} \to^d \chi^2(J)/J
$$
, where $G = \partial g(\beta)/\partial \beta|_\hat\beta$

**Theorem: (Consistent Wald Test)** The Wald Test described above is consistent under large sample assumption.



### Restricted Estimation

#### Restricted Estimation

**Definition: (Restricted Estimation)** Suppose the restriction $R\beta = r$ is true, then the restricted regressor is:
$$
\tilde \beta = \hat \beta - (X'X)^{-1}R'(R(X'X)^{-1}R')^{-1}(R\hat \beta-r)
$$
**Theorem: (Properties of Restricted Estimation)** When the restriction is correct we have:

1. the restricted estimator is consistent

2. $\sqrt n (\tilde \beta -\beta) \to^d N(0,AQ_{XX}^{-1}\Omega Q_{XX}^{-1}A')$, where $A = I-Q_{XX}^{-1}R'(RQ_{XX}^{-1}R')^{-1}R$. 

   Furthermore, if homoscedasticity is true, we have

3. The restricted estimator is more efficient than the OLS Estimator
   
4. $\sqrt n (\tilde \beta -\beta) \to^d N(0,\sigma ^2 A Q_{XX}^{-1}A')$, where $\sigma ^2 A Q_{XX}^{-1}A' = \sigma ^2 Q_{XX}^{-1} - \sigma ^2 Q_{XX}^{-1}R'(RQ_{XX}^{-1}R')^{-1}RQ_{XX}^{-1} < \sigma ^2 Q_{XX}^{-1}$.

**Note:** When the restriction is incorrect the restricted estimator is inconsistent.

#### Special Case

**Definition: (Special Case)** For a linear regression model $Y = X_1\beta_1+X_2\beta_2+e$, suppose we impose the constraint $\beta_2 = 0$, then we have $\tilde \beta_1 = (X_1'X_1)^{-1}X_1y$.

**Theorem: (Properties of the Special Case)** When the restriction is correct and if homoscedasticity is true, we have

1. the estimator is consistent
2. $\sqrt n (\tilde \beta_1 -\beta_1) \to^d N(0, \sigma^2 Q_{11}^{-1})$, where  $\sigma^2 Q_{11}^{-1} \leq \sigma^2 (Q_{11} - Q_{12}Q_{22} ^{-1} Q_{21})^{-1}$, i.e. the restricted estimator is more efficient than the original OLS estimator

**Definition: (Special Case Efficient Estimator)**  For a linear regression model $Y = X_1\beta_1+X_2\beta_2+e$, suppose we impose the constraint $\beta_2 = 0$, the most efficient estimator is $\tilde \beta_1^* = (X_1'X(X'\Sigma X)^{-1}X'X_1)^{-1}X_1'X(X'\Sigma X)^{-1}X'y$, where $\Sigma = diag(\sigma^2(x_i))$.

**Theorem: (Omitted Variables)** When the restriction is incorrect, i.e. $\beta_2 \neq 0$, we have

1. Under small sample assumption, the restricted estimator is biased, and $E[\tilde \beta_1|X] = \beta_1+(X_1'X_1)^{-1}(X_1X_2)\beta_2$
2. Under large sample assumption, the restricted estimator is inconsistent, and $lim_p \tilde \beta_1|X = \beta_1+Q_{11}^{-1}Q_{12}\beta_2$



### Trinity of Tests

#### Lagrange Multiplier Test

**Definition: (LM Estimator)** Define the Lagrange Multiplier Estimator of the restricted estimation as $\tilde \lambda = (R(X'X)^{-1}R')^{-1}(R\hat \beta-r)$.

**Theorem: (Properties of LM Estimator)** Under large sample assumption, we have:
$$
\frac{\tilde \lambda}{\sqrt n} \to^d N(0,(RQ_{xx}^{-1}R')^{-1}(R Q_{xx}^{-1}\Omega Q_{xx}^{-1}R')(RQ_{xx}^{-1}R')^{-1})
$$
Furthermore, under the Assumption about large sample and homoscedasticity, we have:
$$
\frac{\tilde \lambda}{\sqrt n} \to^d N(0,\sigma^2(R(X'X)^{-1}R')^{-1})
$$
**Definition: (Lagrange Multiplier Test)** Under the Assumption about large sample and heteroscedasticity, we use the LM statistic to do Hypothesis Test for $H_0: R\beta -r =0$, and $H_1:R\beta -r\neq 0$, where $R$ is a $J\times k$ vector, i.e. reject if $\hat {LM} \in [\chi^2_{\alpha},+\infty]$, where $\hat {LM}$ is defined as:
$$
\hat {LM} = \frac{\tilde \lambda'\hat V_\lambda^{-1}\tilde \lambda/J}{n} \to^d \chi^2(J)/J
$$
where $\hat V_\lambda = (R(X'X)^{-1}R')^{-1}(R \hat V(\tilde \beta|X)R')(R(X'X)^{-1}R')^{-1}/n$ is the variance estimator of the restricted regression.

**Definition: (Lagrange Multiplier Test with Homoscedasticity)** Under the Assumption about large sample and homoscedasticity, we use the LM statistic to do Hypothesis Test for $H_0: R\beta -r =0$, and $H_1:R\beta -r\neq 0$, where $R$ is a $J\times k$ vector, i.e. reject if $\hat {LM} \in [\chi^2_{\alpha},+\infty]$, where $\hat {LM}$ is defined as:
$$
\hat {LM} = \frac{\tilde \lambda'\hat V_\lambda^{-1}\tilde \lambda/J}{n}  = \frac{(R\hat \beta-r)'(R(X'X)^{-1}R')^{-1}(R\hat \beta-r)/J}{\tilde s^2}\to^d \chi^2(J)/J
$$
where $\tilde s^2 = SSE_R/n-(k-J)$ is the variance of the residual of the restricted estimation.

#### Likelihood Ratio Test

**Definition: (LR Estimator)** Under homoscedasticity and gaussian error assumption, define the Likelihood Ratio Estimator of the restricted estimation as $LR = 2(logL(\hat \beta, \hat \sigma^2)-logL(\tilde \beta, \tilde \sigma^2))$.

**Theorem: (LR Estimator and F Statistic)** We have $LR = nlog(1+JF/(n-k))$.

**Definition: (Likelihood Ratio Test with Homoscedasticity and Gaussian Error)** Under the Assumption about large sample and homoscedasticity and Gaussian Error, we use the LR statistic to do Hypothesis Test for $H_0: R\beta -r =0$, and $H_1:R\beta -r\neq 0$, where $R$ is a $J\times k$ vector, i.e. reject if $\hat {LR} \in [\chi^2_{\alpha},+\infty]$, where $\hat {LM}$ is defined as:
$$
\hat {LR} = \frac{(R\hat \beta-r)'(R(X'X)^{-1}R')^{-1}(R\hat \beta-r)/J}{\hat \sigma^2}\to^d \chi^2(J)/J
$$
where $\hat \sigma^2$ is the variance of the MLE of $\sigma^2$ under the unrestricted estimation.

**Note:** As n increases, $s^2$, $\tilde s^2$ and $\hat \sigma^2$ are all consistent estimator of $\sigma^2$. Hence Wald Test, LM Test and LR Test are all consistent and are similar to each other.



### Confidence Interval

Definition: (Confidence Interval) Given the data $\{S_n\}$ we observe, suppose $S_i\sim f(\theta)$. Let $L$ and $U$ be two statistics. We say $(L,U)$ is a $1-\alpha$ Confidence Interval for $g(\theta) $ if $P(g(\theta)\in (L,U)) = 1-\alpha$. 



## Specification Issues in OLS

### Dummy Variables

#### Difference in Difference



### Bootstrapping

Method: (Bootstrapping)

1. From the original sample $\{X_1,...,X_n\}$ generate an estimator $\hat \theta  = h(X_1,...X_n)$
2. Take a random sample of the same size n from the original sample with replacement, and form a new sample $\{X_1^1,...,X_n^1\}$, get an estimator $\hat \theta^1  = h(X_1^1,...X_n^1)$
3. Repeat step 2 and form a new sample $\{X_1^k,...,X_n^k\}$, get estimators $\hat \theta^k  = h(X_1^k,...X_n^k)$
4. Compute the distribution with the estimators $\theta^k$
5. Use the distribution calculated above to do Hypothesis Test or give the Confidence Interval



### Quantile Regression

### Further Issues

#### Predictions

#### Clustering

#### Multicollinearity

#### Testing for Heteroskedasticity

#### Testing for Functional Form

## Endogeneity

### Source of Endogeneity

#### Omitted Variables

**Definition: (Omitted Variables)** For a linear regression model $Y = X_1\beta_1+X_2\beta_2+e$, suppose we omitted $X_2$ from the OLS. The OLS Estimator is called having Omitted Variable issue.

**Theorem: (Omitted Variables Issues)** Suppose we have $X_2 = X_1\delta+\mu$, the OLS estimator have the following properties:

1. Under small sample assumption, the estimator is biased, and $E[\hat \beta_1|X_1] = \beta _1 + \delta \beta_2$
2. Under large sample assumption, the estimator is inconsistent, and $lim_p \hat \beta_1|X_1 = \beta _1 + \delta \beta_2$

#### Errors in Variables

**Definition: (Errors in Variables)** For a linear regression model $Y = X\beta+e$, suppose we can only observe a noisy signal $S$ of $X$. The OLS Estimator of regression $Y$ on $S$ is called having Errors in Variables issue.

**Theorem: (Errors in Variables Issues)** Suppose we have that $S = X+u$, the OLS estimator have the following properties:

1. Under small sample assumption, the estimator is biased, and $E[\hat \beta|S] =\beta\frac{\sigma ^2_X}{\sigma ^2_X+\sigma ^2_u}$
2. Under large sample assumption, the estimator is inconsistent, and $lim_p \hat \beta|S = \beta\frac{\sigma ^2_X}{\sigma ^2_X+\sigma ^2_u}$

#### Simultaneity

**Definition: (Simultaneity)** For a linear regression system $Q = P\beta_1+e_1$ and $Q = P\beta_2+e_2$, suppose we omitted $X_2$ from the OLS. The OLS Estimator is called having simultaneity issue.

**Note:** When we have Simultaneity issues, we cannot run OLS.



### Instrument Variable

**Definition: (Instrument Variable)** Consider a linear regression model $Y = X_1\beta_1+X_2\beta_2+e$, with $E[e|X_2] \neq 0$ and $\beta_2$ is $k\times 1$. Suppose we have another set of data $Z$, which is $J\times 1$ and $J\geq k$, and we have $E[Ze] = 0$, but $E[ZX_{2k}] \neq0$, then $Z$ is called an Instrument Variable. Furthermore, suppose we have $X_2 = X_1\Gamma_1+Z\Gamma_2+u$ then we have the following linear regression $Y = X_1(\beta_1+\Gamma_1\beta_2)+Z\Gamma_2\beta_2+(e+\beta_2u) = X_1\gamma_1+Z\gamma_2+v$.

**Definition: (Identification)** Let $\Gamma_2$ be a $J\times k$ metrics. Suppose the following conditions are satisfied:

1. Order Condition: $J\geq k$
2. Rank Condition: $rank(\Gamma_2) = k$

We say the endogenous variable $X_2$ is identified.

**Definition: (IV Estimator)** When the endogenous variable is identified, we can define the IV Estimator as:

1. if $J=k$, define $\hat \beta_2^{IV} = \hat \Gamma_2^{-1}\hat\gamma_2$
2.  if $J>k$, define $\hat \beta_2^{IV} = (\hat \Gamma_2' A\hat \Gamma_2)^{-1}\hat \Gamma_2'A\gamma_2$, where $A$ is a symmetric and positive definite



### General Method of Moments

#### GMM Estimator

**Definition: (General Method of Moments)** Suppose we have $\frac{1}{n}\sum_{i=1}^nz_i(y_i-x_i'\beta) = 0$. Let $W_n$ be a symmetric positive definite matrix,  General Method of Moments estimator is defined as:
$$
\bar \beta = argmin_\beta \{(Y-X\beta)'ZW_nZ'(Y-X\beta)\}
$$
Note: We only derive the GMM Estimator under the large sample assumptions.

**Assumption: (Large Sample Assumption of General Method of Moments)**

1. $W_n \to W$ and $W$ is symmetric and positive definite
2. $E[z_ie_i] = 0$
3. $E[z_ix_i'] = Q_{zx}$ exists
4. $E[z_iz_i'e_i^2] = \Omega < +\infin$

**Theorem: (GMM Estimator)** Under the Assumption of General Method of Moments, the GMM estimator is
$$
\bar \beta = (X'ZW_nZ'X)^{-1}X'ZW_nZ'Y
$$
**Theorem: (GMM Estimator Property)** Under the Large Sample Assumption of General Method of Moments, we have

1. $\sqrt n (\bar \beta-\beta) \to^dN(0,(Q_{zx}'WQ_{zx})^{-1}Q_{zx}'W\Omega W Q_{zx}(Q_{zx}'WQ_{zx})^{-1})$
2. $lim_p \hat Q_{zx} = lim_p Z'X/n = Q_{zx}$
3. $lim_p \hat \Omega = lim_p \sum_{i=1}^n\hat e_i^2 z_iz_i'/n = \Omega$, where $\hat e = Y-X\bar\beta$

**Note:** From 2 and 3 generate a consistent estimator of the asymptotic variance of the estimator $\bar \beta$.

#### Special Case

**Theorem: (Special Case)** Under the Assumption of General Method of Moments, if $J=K$, the GMM estimator is
$$
\bar \beta = (Z'X)^{-1}Z'Y
$$
**Theorem: (Special Case Property)** Under the Large Sample Assumption of General Method of Moments, if $J=K$, we have

1. $\sqrt n (\bar \beta-\beta) \to^dN(0,(Q_{zx}'\Omega^{-1} Q_{zx})^{-1})$
2. $lim_p \hat Q_{zx} = lim_p Z'X/n = Q_{zx}$
3. $lim_p \hat \Omega = lim_p \sum_{i=1}^n\hat e_i^2 z_iz_i'/n = \Omega$, where $\hat e = Y-X\bar\beta$

**Note:** From 2 and 3 generate a consistent estimator of the asymptotic variance of the estimator $\bar \beta$.

#### Efficient GMM Estimator

**Theorem: (Optimal Weight Matrix)** We have that for any $W$,
$$
(Q_{zx}'WQ_{zx})^{-1}Q_{zx}'W\Omega W Q_{zx}(Q_{zx}'WQ_{zx})^{-1} \geq (Q_{zx}'\Omega^{-1} Q_{zx})^{-1}
$$
**Definition: (Feasible Efficient GMM Estimator)** The feasible efficient estimator is $\bar \beta = (X'Z\hat\Omega^{-1}Z'X)^{-1}X'Z\hat\Omega^{-1}Z'Y$.

**Theorem: (Efficient GMM Estimator Property)** Under the Large Sample Assumption of GMM Estimator we have

1. $\sqrt n (\bar \beta-\beta) \to^dN(0,(Q_{zx}'\Omega^{-1} Q_{zx})^{-1})$
2. $lim_p \hat Q_{zx} = lim_p Z'X/n = Q_{zx}$
3. $lim_p \hat \Omega = lim_p \sum_{i=1}^n\hat e_i^2 z_iz_i'/n = \Omega$, where $\hat e = Y-X\bar\beta$

**Note:** From 2 and 3 generate a consistent estimator of the asymptotic variance of the estimator $\bar \beta$.

**Note:** The Optimal Weight Matrix is such that $W_n \to \Omega^{-1}$.

#### 2SLS Estimator

**Definition: (2SLS Estimator)** the 2 Stage Least Square Estimator is defined as
$$
\hat \beta^{2SLS} = (X'Z(Z'Z)^{-1}Z'X)^{-1}X'Z(Z'Z)^{-1}Z'Y
$$
**Theorem: (2SLS and GMM)** 2SLS Estimator is GMM Estimator with $W_n = (Z'Z/n)^{-1}$, which is optimal if Homoscedasticity is true, i.e. $E[z_iz_i'e_i^2] = \sigma^2E[z_iz_i']$.



### Identification Issues

#### Weak IV

**Definition: (Weak Identification)** When the rank condition is not satisfied, i.e. $rank(\Gamma_2)<k$, we say that the IVs are weak.

**Theorem: (Weak IV Problem)** When $\Gamma_2 = 0$, the GMM Estimator is inconsistent.

**Definition: (Weak IV Test)** To test if the IVs are weak, we can take the regression $X_2 = X_1\Gamma_1+Z\Gamma_2+u$, and do a Wald Test or F test with $H_0: \Gamma_2 = 0$.

#### Hansen’s J Test

**Definition: (Over Identification)** When we have more IVs than the endogenous variables, i.e. $J>k$, we say that the endogenous variables are over identified.

**Definition: (Hansen’s J)** Define Hansen’s J statistic as $J = n(Y-X\bar \beta)'Z\hat \Omega^{-1}Z'(Y-X\bar \beta)$.

**Theorem: (Hansen’s J Property)** Under the large sample assumption of General Method of Moments, we have $J \to^d \chi^2(J-k)$.

**Definition: (Hansen’s J Test)** Under the large sample assumption of General Method of Moments, we use the J estimator to do Hypothesis Test for $H_0: E[z_ie_i] = 0$, and $H_1:E[z_ie_i] \neq 0$, i.e. reject if $\hat J \in [\chi^2_{\alpha},+\infty]$, where $\hat J$ is defined as:
$$
\hat J = n(Y-X\bar \beta)'Z\hat \Omega^{-1}Z'(Y-X\bar \beta) \to^d \chi^2(J-k)
$$

#### Hausman Test

**Definition: (Hausman Test)** Under the large sample assumption of General Method of Moments, we do a Hypothesis Test for $H_0:\hat \beta = \bar \beta$, and $H_1:\hat \beta \neq \bar \beta$, i.e. if there are endogeneity or not, we define a Hausman statistic:
$$
H = n(\hat \beta-\bar \beta)'V^{+}(\hat \beta-\bar \beta) \to^d \chi^2(k)
$$
where $V^{+} = V(\hat\beta-\bar \beta)^{+} = (V(\hat\beta)-V(\bar \beta))^{+}$ is the G-inverse of V.

**Definition: (Alternative Hausman Test)** Under the large sample assumption of General Method of Moments, we do a Hypothesis Test for $H_0:E[z_ie_i] = 0$, and $H_1:E[x_ie_i] \neq 0$, i.e. if there are endogeneity or not, by doing OLS on $Y = X_1\beta_1+X_2\beta_2+\hat u\rho+\epsilon$, where $\hat u$ is the OLS residual from regressing $X_2 = X_1\Gamma_1+Z\Gamma_2+u$, and do a F Test with $\rho$.

**Theorem: (Relationship Between Alternative Hausman Test and 2SLS)** If we do the regression of $Y = X_1\beta_1+X_2\beta_2+\hat u\rho+\epsilon$, the estimator $\hat \beta$ will be the 2SLS estimator.