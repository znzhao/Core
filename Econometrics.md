# Econometrics

## Content

[TOC]



## Preliminaries

### Probability

### Distribution



### Statistics

#### Random Sampling

Definition: (Random Sample) Suppose $\{X\}$ is the set of population, a subset $\{X_n\} \in \{X\}$ is called a Random Sample, where $X_i \sim f_X$ are mutually independent and have identical distribution.

Note: The joint PMF or PDF of $\{X_n\}$ is $f_{\{X_n\}} = \prod_{i = 1}^n f_X(x_i)$.

Definition: (Estimator) An estimator is a function of the sample, i.e. $\hat\theta = T(\{X_n\})$.

Definition: (Sampling Distribution) The distribution of $\hat\theta$ is called a sampling distribution.

#### Comparison of Estimators

Definition: (Unbiasedness) If $E[\hat \theta] = \theta$, then we say the estimator is unbiased.



### Point Estimation

#### Maximum Likelihood

Definition: (Likelihood Function) Likelihood Function of a sample is defined as:
$$
L_n(\theta) = \prod_{i=1}^nf(X_i, \theta)
$$
Definition: (Maximum Likelihood Estimator) Maximum Likelihood Estimator of a sample is defined as:
$$
\hat\theta = argmax[lnL_n(\theta)] = argmax[\sum_{i=1}^nlnf(X_i, \theta)]
$$

#### Method of Moments

Definition: (Method of Moments Estimator) When the population random variable $X$ have the following property:
$$
E[m(X,\theta)] = 0
$$
Then then Method of Moments Estimator of a sample is the solution to the following equation:
$$
\sum_{i=1}^n m(X_n,\hat\theta)/n = 0
$$

### Confidence Intervals

### Convergence Theory

#### Convergence

Definition: (Convergence in Probability)

Definition: (Convergence in Distribution)

Theorem: (Properties of Convergence)

#### Delta Method

Theorem: (Delta Method)

### Law of Large Number and Central Limit Theorem

### Statistical Inferences

## Ordinary Least Squares Estimation

### Regression Model

#### General Regression Model

Definition: (General Regression Model) A regression model is defined as:
$$
y = m(x)+\epsilon
$$
with $E[\epsilon|x] = 0$ and $E[\epsilon^2|x] =  \sigma^2(x)$.

#### Linear Regression Model

Definition: (Linear Regression Model) A linear regression model is defined as:
$$
y = x\beta+\epsilon
$$
with $E[\epsilon|x] = 0$ and $E[\epsilon^2|x] =  \sigma^2(x)$.

Theorem: (Linear Projection) The best linear predictor is defined as $P(y|x) = x'\beta$, where beta is defined as 

$$
\beta =E[xx']^{-1}E[xy] = argminE[(y-x'b)^2]
$$
Definition: (Sample) A sample $\{(X,Y)\}$ is drawn from the population $\{(x,y)\}$.

Definition: (Sample Regression Model) A linear regression model of the sample is defined as:
$$
Y = X\beta+e
$$
with $E[e|X] = 0$ and $E[e^2|X] =  \sigma^2(X)$.

Definition: (Least Square Estimator) A least square estimator is defined as:
$$
\hat \beta = argmin(\frac{1}{n}\sum_{i=1}^n (y_i-x_i'b)^2) = argmin(\frac{1}{n}(Y-Xb)'(Y-Xb))
$$

#### Assumption

Assumption 1: (Random sampling) Each Sample is drawn with i.i.d.

Assumption 2: (No Perfectly Collinearity) $X’X$ is invertible.

Assumption 3’: (Zero Correlation) $E[Xe] = 0$.

Assumption 3: (Zero Conditional Mean) $E[e|X] = 0$.

Note: Zero Conditional Mean is stronger than Zero Correlation.

Assumption 4’: (Heteroskedasticity) $E[e^2|X] =  \sigma^2(X)$.

Assumption 4: (Homoscedasticity) $E[e^2|X] =  \sigma^2$.

Assumption 5: (Gaussian Error) $e|X \sim N(0,\sigma^2)$.



### Estimator

#### Maximum Likelihood Estimator

Required Assumption: 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean
4. Homoscedasticity
5. Gaussian Error

Theorem: (Maximum of Likelihood Estimator of OLS) Under the required assumption, the Maximum of Likelihood Estimator of the regression model is:
$$
\hat\beta = (X'X)^{-1}X'Y = (\sum_{i=1}^nx_ix_i')^{-1}\sum_{i=1}^nx_iy_i
$$

$$
\hat\sigma^2=\hat e'\hat e/2=(Y-X\hat\beta)'(Y-X\hat\beta)/n= \sum_{i=1}^n(y_i-x_i'\hat\beta)^2/n
$$

#### Least Square Estimator

Required Assumption: 

1. Random sampling
2. No Perfectly Collinearity

Theorem: (OLS Estimator) Under the required assumption, the OLS Estimator is:
$$
\hat\beta = (X'X)^{-1}X'Y = (\sum_{i=1}^nx_ix_i')^{-1}\sum_{i=1}^nx_iy_i
$$
Definition: (Prediction) Under the required assumption, the Prediction of the dependent variable is defined as:
$$
\hat Y = X\hat\beta = X(X'X)^{-1}X'Y
$$
Definition: (Residual) Under the required assumption, the Residual of the estimation is defined as:
$$
\hat e =Y-\hat Y = Y-X\hat\beta = Y- X(X'X)^{-1}X'Y
$$
Definition: (Projection Matrix) The Projection Matrix is Defined as:
$$
P_X = X(X'X)^{-1}X'
$$
Definition: (Orthogonal Projection Matrix) The Orthogonal Projection Matrix is Defined as:
$$
M_X = I- X(X'X)^{-1}X'
$$
#### Leverage

Definition: (Leverage) The Leverage of the estimation is defined as $h_{ii} = x_i'(X'X)^{-1}x_i$.
Definition: (Influence) The predict estimator is defined as $\hat\beta_{-i} = \hat\beta - (1-h_{ii})^{-1}(X'X)^{-1}x_i\hat e_i $, and we define the prediction residual as $\tilde e_i = y_i - x_i'\hat\beta_{-i} = \hat e_i/(1-h_{ii})$.

Note: $x_i'\hat\beta - x_i'\hat\beta_{-i} = h_{ii}\tilde e_i$.



#### General Properties of the Estimation

Theorem: (Properties of the Estimator and Residual) Under Assumption 1 and 2, the OLS Estimator and the Residual has the following properties:

1. $\hat Y  = P_X Y$, and $\hat e = M _X e = M_X Y$
2. $\hat e'\hat e = e'M_Xe = Y'M_XY$
3. $X'\hat e = 0$ and $\hat Y \hat e = 0$
4. If the independent variables include constant, i.e.  $x_1 = \iota$, then $\sum_{i=1}^n\hat e = 0$, and $\bar y = \bar{\hat y}$

Theorem: (Properties of the Projection Matrix) Under Assumption 1 and 2, the Projection Matrix has the following properties:

1. $P_X$ is symmetric and idempotent, i.e. $P_X' = P_X$, and $P_X P_X = P_X$ 
2. $P_X \iota = \iota$
3. $P_X X = X$
4. $P_\iota = \iota\iota’/n$
5. $P_\iota Y = \bar y$
6. $Trace(P_X) = k$

Theorem: (Properties of the Orthogonal Projection Matrix) Under Assumption 1 and 2, the Orthogonal Projection Matrix has the following properties:

1. $M_X$ is symmetric and idempotent, i.e. $M_X' = M_X$, and $M_X M_X = M_X$ 
2. $M_X X = 0$
3. $Trace(M_X) = n-k$

Theorem: (Properties of the Leverage) Under Assumption 1 and 2, the Leverage has the following properties:

1. $h_{ii}$ is the i-th element on the diagonal of $P_X$
2. $\sum_{i=1}^n h_{ii} = k$
3. $h_{ii}\in [0,1]$

#### Special Cases

Theorem: (Special Regressor) The following statements are true:

1. When $k = 1$ and $X_1 = \iota$, $\hat\beta = \bar y$
2. When $k=1$ and $X_1 = x$, $\hat\beta = \sum_{i = 1}^nx_iy_i/\sum_{i = 1}^nx_i^2$
3. When $k=2$ and $X_1 = \iota$, $X_2 = x$, then $\hat\beta_1 = \bar y -\bar x\hat\beta_2$, and $\hat\beta_2 = \sum_{i = 1}^n(x_i-\bar x) (y_i-\bar y)/\sum_{i = 1}^nx_i^2$
4. (Transformations) When regress $Y$ on $XC$, the estimator is $\hat \beta^* = C^{-1}\hat\beta$, and $\hat Y^*  = \hat Y $
5. (Transformations) When regress $a+bY$ on $X_1$ and $ X_2 $, the estimator is $\hat\beta_1^* = a+ b \hat\beta_1$, and  $b \hat\beta_2^* = b \hat\beta_2$

### Partitioned Regression

#### Partitioned Regression

Theorem: (Partitioned Regression) Suppose we see the regression model as $Y = X_1\beta_1+X_2\beta_2+e$, then we have:
$$
\hat \beta_1 = (X_1'M_{X_2}X_1)^{-1}X_1'M_{X_2}Y,\space \hat \beta_2 = (X_2'M_{X_1}X_2)^{-1}X_2'M_{X_1}Y
$$
or
$$
\hat \beta_1 = ((M_{X_2}X_1)'M_{X_2}X_1)^{-1}(M_{X_2}X_1)'Y,\space \hat \beta_2 = ((M_{X_1}X_2)'M_{X_1}X_2)^{-1}(M_{X_1}X_2)'Y
$$
i.e. the regression of the residuals of $Y$ and $X_i$ on $X_j$.

#### Special Cases

Theorem: (Special Partitioned Regression) The following statements are true:

1. When $\hat \beta_1$ is a scaler and there is an intercept in $X_2$, then $\hat \beta_1 = X_1'M_{X_2}Y / (X_1'M_{X_2}X_1)$
2. Generally, when $X_1 = \iota$, then the regression will pass the mean of the sample, i.e.

$$
\hat\beta_1 = \bar y -\bar x'\hat\beta_2=(\iota'M_{X_2}\iota)^{-1}\iota'M_{X_2}Y
$$

$$
\hat\beta_2 = [\sum_{i = 1}^nx_ix_i']^{-1} \sum_{i = 1}^n(x_i-\bar x) (y_i-\bar y)' = (X_2M_\iota X_2)^{-1}X_2'M_\iota Y
$$



### R-Squared

#### Variation Partition

Definition:(Total Sum of Square) Total Sum of Square is defined as $SST = (Y-\iota\bar y)'(Y-\iota\bar y)$.

Definition:(Regression Sum of Square) Regression Sum of Square is defined as $SSR = (\hat Y-\iota\bar y)'(\hat Y-\iota\bar y) = \hat\beta' X'M_\iota X \hat\beta$.

Definition:(Sum of Square Error) Sum of Square Error is defined as $SSE = \hat e’ \hat e = \sum_{i=1}^n \hat e_i^2$.

Theorem: (Variation Partition) The following statements are true:

1. $Y = P_X Y +M_X Y$
2. $SST = SSR+SSE$

#### R-Squared

Definition:(R-Squared) R-Squared is defined as $R^2 = SSR/SST = 1-SSE/SST$.

Theorem: (Properties of R-Squared) The following statements are true:

1.  $R^2 = corr(Y,\hat Y)^2$
2. $R^2 \in [0,1]$
3. When k increases, R-squared will always increase.

#### Adjusted R-Squared

Definition:(Adjusted R-Squared) Adjusted R-Squared is defined as $R^2 = 1-\frac{SSE(n-1)}{SST(n-k-1)}$.



### Properties of Estimator: Small Sample Result

#### Expectation and Variance of the Estimator

Required Assumption: 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean

Theorem: (Small Sample Result) Under Assumption 1, 2 and 3, the following properties are true:

1. $\hat\beta$ is an unbiased estimator, i.e. $E[\hat \beta] = \beta$, and $E[\hat e] = 0$
2. $Var(\hat\beta|X) = (X'X)^{-1}X'\Sigma X(X'X)^{-1}$, where $\Sigma = E[ee'|X] = diag[\sigma^2(x_i)]$
3. $Var(\hat e | X) =  M_X \Sigma M_X'$

#### Expectation and Variance of the Estimator with Homoscedasticity

Required Assumption: 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean
4. Homoscedasticity

Theorem: (Small Sample Result with Homoscedasticity) Under Assumption 1, 2, 3, and 4,  the following properties are true:

1. $Var(\hat\beta|X) = \sigma^2(X'X)^{-1}$
2. $E[\hat e_i^2|X] = \sigma^2(1-h_{ii})$
3. $Var(\hat e | X) = \sigma^2 M_X$

#### Gauss Markov Theorem



Theorem: (Gauss Markov Theorem)

#### Variance Estimation

#### Distribution Result

Required Assumption: 

1. Random sampling
2. No Perfectly Collinearity
3. Zero Conditional Mean
4. Homoscedasticity
5. Gaussian Error





### Properties of Estimator: Large Sample Theory



### Basic Hypothesis Test

### Advanced Hypothesis Test

