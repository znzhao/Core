# Econometrics II

## M-Estimation

### Consistency

**Assumption: (Newey McFadden)**

- $Q(\theta)$ is uniquely maximized at $\theta_0$
- The parameter space $\Theta$ is compact
- $Q(\theta)$ is continuous
- $Q_N(\theta)\to^p Q(\theta)$ uniformly over $\Theta$ 

**Definition: (M-Estimation)** Under the assumptions listed above, suppose $Q(\theta)$ is the population objective function, and $Q_N(\theta)$ is the sample objective function. Suppose $\theta_0 = argmax_{\theta\in\Theta} \space Q(\theta)$, then define the M-Estimation of $\theta_0$ as $\hat\theta_N = argmax_{\theta\in\Theta} \space Q_N(\theta)$. 

**Theorem: (Consistency)** Under the Newey McFarlan assumption, we have $\hat\theta_N\to ^p \theta_0$.

Proof:

We want to show that $P(|\hat \theta_N-\theta_0|\geq \epsilon)\to 0$ as $N\to +\infty$.

1. For any $\epsilon >0$, Since $\hat\theta_N = argmax \space Q_N(\theta)$, we have $Q_N(\hat\theta_N)\geq Q_N(\theta_0)>Q_N(\theta_0)-\epsilon/3$. Since we have $Q_N(\theta)\to^p Q(\theta)$ uniformly over $\Theta$, when $N\to \infty$, we have $P(Q(\hat\theta_N)\geq Q_N(\hat\theta_N)-\epsilon/3)\to 1$ and $P(Q_N(\theta_0)\geq Q(\theta_0)-\epsilon/3)\to 1$. Now combine these three inequalities we have $P(Q(\hat\theta_N)>Q(\theta_0)-\epsilon/3-\epsilon/3-\epsilon/3)\to 1$, i.e. $P(Q(\hat\theta_N)>Q(\theta_0)-\epsilon)\to 1$.
2. Now, denote $N(\theta_0)$ as a neighborhood of $\theta_0$. Define $\theta^\star = argmax_{\theta\in\Theta\cap N^c} \space Q(\theta)$. By assumption $Q(.)$ is continuous, $\Theta\cap N^c$ is compact, so $\theta^\star$ always exists. Now since $Q(\theta)$ is uniquely maximized at $\theta_0$ over $\Theta$, we have $Q(\theta^\star)< Q(\theta_0)$.
3. Since $Q(\theta_0)-Q(\theta^\star)>0$, we can define $Q(\theta_0)-Q(\theta^\star)= \epsilon$, plug it back to step 1 we have $P(Q(\hat\theta_N)>Q(\theta_0)-Q(\theta_0)+Q(\theta^\star))\to 1$, i.e. $P(Q(\hat\theta_N)>Q(\theta^\star))\to 1$. However, by definition $\theta^\star = argmax_{\theta\in\Theta\cap N^c} \space Q(\theta)$, so it implies that $P(\hat\theta_N\in N(\theta_0))\to 1$, which is exactly what I want to show. $\square$

**Corollary: (MLE Consistency)** Under the following conditions:

- $\{z_i\}$ are i.i.d. with PDF $f(z_i|\theta)$

- $\theta\in \Theta$, which is a compact set
- If $\theta \neq \theta_0$ then $f(z_i|\theta) \neq f(z_i|\theta_0)$
- $lnf(z_i|\theta)$ is continuous
- $E[sup_{\theta\in\Theta}|lnf(z_i|\theta)|]< +\infty$

We have $\hat \theta\to^p\theta_0$.



### Asymptotic Distribution

**Assumption: (Asymptotic Distribution)**

- $\hat \theta _N$ is a constant estimator
- $\theta_0\in int(\Theta)$
- $Q_N(\theta)$ is continuous and twice differentiable
- $\sqrt N \nabla_\theta Q_N(\theta_0) \to^d N(0,\Sigma(\theta_0))$
- $sup_\theta || \nabla_{\theta\theta} Q_N(\theta)-H(\theta_0)||\to ^p 0$
- $H(\theta_0)$ is invertible

**Theorem: (Asymptotic Distribution)** Under the above assumption, we have $\sqrt N (\hat\theta_N-\theta_0)\to^d N(0,H^{-1}\Sigma H^{-1})$.

Proof:

1. Remember by definition we have $\hat\theta_N = argmax_{\theta\in\Theta} \space Q_N(\theta)$, i.e. the first order condition implies $\nabla_\theta Q_N(\hat\theta_N) = 0$.
2. By Taylor expansion, we have $0=\nabla_\theta Q_N(\hat\theta_N) = \nabla_\theta Q_N(\theta_0)+\nabla_{\theta\theta} Q_N(\tilde\theta_N)(\hat\theta_N-\theta_0)$, where $\tilde\theta_N$ is between $\theta_0$ and $\hat\theta_N$. Hence we have $\sqrt N (\hat\theta_N-\theta_0) = -(\nabla_{\theta\theta} Q_N(\tilde\theta_N))^{-1} \sqrt N(\nabla_\theta Q_N(\theta_0))$.
3. By assumption we know that $\sqrt N  \nabla_\theta Q_N(\theta_0) \to^d N(0,\Sigma)$ and $ \nabla_{\theta\theta} Q_N(\theta)\to^p H$. By continuous mapping theorem, we have $\sqrt N (\hat\theta_N-\theta_0)\to^d N(0,H^{-1}\Sigma H^{-1})$. $\square$

**Corollary: (MLE Asymptotic Distribution)** Suppose $\hat \theta_N$ is a MLE estimator. Under the following conditions:

- $\{z_i\}$ are i.i.d. with PDF $f(z_i|\theta)$
- $\theta_0\in int(\Theta)$, which is a compact set
- $f(z_i|\theta)$ is continuous and twice differentiable, and $f(z_i|\theta)>0$ in the neighborhood of $\theta_0$ 
- $\int sup_{\theta}||\nabla_{\theta}f(z_i|\theta)||dz< +\infty$ and $\int sup_{\theta}||\nabla_{\theta\theta}f(z_i|\theta)||dz< +\infty$
- $E[sup_{\theta}||\nabla_{\theta}lnf(z_i|\theta)||]<+\infty$
- $J = E[\nabla_{\theta}f(z_i|\theta)(\nabla_{\theta}f(z_i|\theta))']< +\infty$ and invertible

We have $\sqrt N (\hat\theta_N-\theta_0)\to^d N(0,J^{-1})$.



## Binary Outcome

### Linear Index Model

#### Linear Index Model

**Definition: (Linear Index Model)** A Linear Index Model is defined as:
$$
y = 1_{\{X\beta+\epsilon \geq 0\}}
$$
where $\epsilon$ is independent of $X$. Suppose $\epsilon$ has a CDF of $G(.)$, which is continuous symmetric around zero, then we have
$$
P(y=1) = P(X\beta+\epsilon\geq 0 | X) = G(X\beta)
$$
**Definition: (Linear Probability Model)** A Linear Probability Model is to set $G(z) = z$.

**Definition: (Probit Model)** A Probit Model is to set $G(z) = \Phi (z)$.

**Definition: (Logit Model)** A Logit Model is to set $G(z) = e^z/(1+e^z)$ .

#### Marginal Effect

**Definition: (Marginal Effect)** The Marginal Effect of the independent variable is $\frac{\partial P(y=1|X)}{\partial x} = \beta g(X\beta)$.

**Claim: (Marginal Effect)** The marginal effect of linear probability model is $\beta$, the marginal effect of Probit model is $\beta\phi(X\beta)$,The marginal effect of Logit model is $\beta\gamma(X\beta)$.

**Definition: (Partial Effect at the Averages)** The Partial Effect at the Averages, known as the PEA, is defined as the partial effect evaluated at $\bar X$.

**Definition: (Average Partial Effect)** The Average Partial Effect, known as the APE, is defined as the average of the in-sample estimated partial effects.

**Note:** Since the marginal effect of the model is related to the data, we can choose to report at different points:

1. Report at an interesting $X$
2. Report at sample average $\bar X$: PEA
3.  Report the average of the marginal effect across $X$: APE



### Conditional Maximum Likelihood Estimation

**Definition: (Conditional Maximum Likelihood Estimation)** Note that $l(y,X|\theta) = l(y|X,\theta)l(X|\theta)$. Suppose $l(X|\theta)$ doesn’t depend on $\theta$, i.e. $l(X|\theta) = l(X)$ Then maximizing the log likelihood function would be the same as maximizing the conditional log likelihood function. So Conditional Maximum Likelihood Estimation is defined as:
$$
Max \space Q_N(\theta) = \frac{1}{N} \sum_{i=1}^N ln(l(y_i|X_i,\theta))
$$
For the linear index model, $Q_N(\beta) = \frac{1}{N} \sum_{i=1}^N (y_ilnG(X_i\beta)+(1-y_i)ln(1-G(X_i\beta)))$.

**Assumption: (Consistency)**

- $\theta\in \Theta$, which is a compact set
- If $\theta \neq \theta_0$ then $G(X_i\beta) \neq G(X_i\beta_0)$
- $lnG(X_i\beta)$ is continuous
- $E[sup_{\theta\in\Theta}|lnG(X_i\beta)|]< +\infty$

**Theorem: (Consistency)** Under the above assumptions, the conditional maximum likelihood estimator is consistent.

Proof:

Using M estimation consistency result for MLE. $\square$ 

**Theorem: (Asymptotic Distribution)** Suppose $\hat \theta_N$ is a MLE estimator. Under the following conditions:

- $\{z_i\}$ are i.i.d. with PDF $G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}$
- $\beta_0\in int(\Beta)$, which is a compact set
- $G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}$ is continuous and twice differentiable, and $G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}>0$ in the neighborhood of $\beta_0$ 
- $\int sup_{\beta}||\nabla_{\beta}G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}||dz< +\infty$ and $\int sup_{\beta}||\nabla_{\beta\beta}G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}||dz< +\infty$
- $E[sup_{\beta}||\nabla_{\beta}lnG(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}||]<+\infty$
- $J = E[\frac{g(x_i\beta)^2x_i'x_i}{G(x_i\beta)[1-G(x_i\beta)]}]$ is the Jacobian matrix of the regression, which is symmetric and positive semidefinite

We have $\sqrt N (\hat\beta_N-\beta)|X \to^d N(0,J^{-1})$.

Proof:

Using M estimation asymptotic distribution result for MLE. $\square$ 



### Multiple Choice Model

#### Multinomial Choice Model

**Definition: (Multinomial Choice Model)** Suppose $y_i\in \{0,1,2,...,J\}$, and $P(y_i=j|X) = \frac{exp(X_i\beta_j)}{\sum_{h=0}^Jexp(X_i\beta_h)}$. Without loss of generality, normalize $\beta_0$ to be zero, and we will have the Multinomial Choice Model:
$$
P(y_i=j|X_i) = \frac{exp(X_i\beta_j)}{1+\sum_{h=1}^Jexp(X_i\beta_h)}
$$
**Definition: (Marginal Effect)** The marginal effect of the multinomial choice model is $\partial P(y=j|X)/\partial x_k = P(y_i=j|X_i)(\beta_{jk}-\frac{\sum_{h=1}^J \beta_{hk} exp(X_i\beta_k)}{1+\sum_{h=1}^J}exp(X_i\beta_h))$.

#### Conditional Logit Model

**Definition: (Conditional Logit Model)** Suppose $y_{ij}^\star = x_{ij}\beta+e_{ij}$ is the unobserved payoff of sample $i$ choosing category $j$. Assuming that $e_{ij}$ is independent to $x_{ij}$, and assuming $e_{ij}$ independently has type 1 extreme value distribution, i.e. $e_{ij}\sim F(e) = exp(-exp(-e))$,  the probability of choosing category $j$ is given by the Conditional Logit Model:
$$
P(y_i=j|X_{ij}) = \frac{exp(X_{ij}\beta)}{\sum_{h=0}^Jexp(X_{ih}\beta)}
$$
**Claim: (Relationship between MCM and CLM)** Define $d_{jh} = 1$ if $j=h$ and $d_{jh} = 0$ if $j\neq h$.  Suppose we have 
$$
P(y_i=j|X_i) = \frac{exp(X_i\beta_j)}{1+\sum_{h=1}^Jexp(X_i\beta_h)}
$$
Then we can define it as
$$
P(y_i=j|X_{ij}) = \frac{exp(X_{ij}\beta)}{\sum_{h=0}^Jexp(X_{ih}\beta)}
$$
where $X_{ij} = (d_{0j}X_i, d_{1j}X_i, ..., d_{Jj}X_i)$ and $\beta = (\beta_0,\beta_1,..., \beta_J)$.

#### Ordered Response Model

**Definition: (Ordered Response Model)** Suppose $y\in \{1,2,...,J\}$ is in a natural order, and $y_{ij}^\star = x_{ij}\beta+e_{ij}$ is the latent variable and it satisfies $y_i=j$ if and only if $y_i^\star \in [\alpha_{j-1},\alpha_j)$. Suppose $e_{ij}$ have a CDF of $G(.)$, then the Ordered Response Model is
$$
P(y_i=j|X_i) = G(\alpha_j-X_i\beta) - G(\alpha_{j-1}-X_i\beta)
$$



## Further Issues in OLS

### Bootstrapping

**Method: (Bootstrapping)**

1. From the original sample $\{X_1,...,X_n\}$ generate an estimator $\hat \theta  = h(X_1,...X_n)$
2. Take a random sample of the same size n from the original sample with replacement, and form a new sample $\{X_1^1,...,X_n^1\}$, get an estimator $\hat \theta^1  = h(X_1^1,...X_n^1)$
3. Repeat step 2 and form a new sample $\{X_1^k,...,X_n^k\}$, get estimators $\hat \theta^k  = h(X_1^k,...X_n^k)$
4. Compute the distribution with the estimators $\theta^k$
5. Use the distribution calculated above to do Hypothesis Test or give the Confidence Interval

**Claim: (Bootstrapping Theory)** When the time bootstrapping repeats increases, the bootstrapping distribution converges to the distribution of the real estimator.



### Clustering

**Definition: (Clustering Model)** The Clustering Model is written as 
$$
y_g = X_g \beta + u_g,g = 1,2,...,G
$$
where $y_g$ and $u_g$ are $N_g\times 1$ vectors and $X_g$ is a $N_g\times K$ matrix. Write them into one column vector, we have $y=X\beta +u$. The OLS Estimator is $\hat \beta = (X'X)^{-1}(X'y) = (\sum_{g=1}^G X_g'X_g)^{-1}(\sum_{g=1}^G X_g'y_g)$.

**Definition: (Clustering Variance)** The Clustering Variance Estimator is defined as 
$$
V(\hat\beta|X) = (X'X)^{-1}X'\Omega X(X'X)^{-1}
$$
where $\Omega = Var(u|X)$ is the variance-covariance matrix of $u$, which has the following property:
$$
\Omega =  \left[\begin{matrix} \Omega_1      & 0      & \cdots & 0      \\0     & \Omega_2    & \cdots & 0      \\ \vdots & \vdots & \ddots & \vdots \\0      & 0      & \cdots & \Omega_G      \\\end{matrix}\right]
$$
Note that $X'\Omega X = \sum_{g=1}^GX'_g E[u_gu'_g|X_g]X_g = \sum_{g=1}^G \sum_{i=1}^{N_g} \sum_{j=1}^{N_g} x_{ig} E[u_{ig}u_{jg}|X_g]x'_{jg}$.

**Definition: (Clustering Variance Estimator)** The Clustering Variance Estimator is defined as 
$$
\hat V(\hat\beta|X) = (X'X)^{-1}X'\hat \Omega X(X'X)^{-1}
$$
where $X'\hat \Omega X = \sum_{g=1}^GX'_g \hat u_g\hat u'_gX_g = \sum_{g=1}^G \sum_{i=1}^{N_g} \sum_{j=1}^{N_g} X_{ig} \hat u_{ig} \hat u_{jg} x'_{jg}$, and $\hat u_{ig} = y-X\hat \beta$.

**Note:** When $X_g$ is a $N_g\times 1$ vector, the Clustering Variance Estimator becomes $\hat V(\hat\beta|X) = [(\sum_ix_i^2)^2]^{-1}(\sum_i\sum_jx_ix_j\hat u_i\hat u_j1[\exist g \in G|i\in g, j\in g])$.

**Assumption: (Clustering OLS)**

1. Conditional exogeneity: $E[u_g|X] = 0$
2. Independent and identical distribution between different group: $(y_g, X_g)$ are i.i.d. random variables
3. Rank Condition: $\sum_{g=1}^G E[X'_gX_g]$ is inversible
4. $E[X_g'\Omega_g X_g] = \Sigma$

**Claim: (Unbiasedness and Consistency)** Under assumption 1-3, the OLS estimator is still unbiased. If the clustering number is large, the OLS estimator is still consistent, i.e. $plim_{G\to \infty} \hat \beta = \beta$.

**Claim: (Asymptotic Theory for Clustering)** Under assumption 1-4, the OLS estimator has the following property:

1. $\sqrt G(\hat \beta_{OLS}-\beta)|X \to^d N(0,Q_{xx}^{-1}\Sigma Q_{xx}^{-1})|X$ as $G\to \infty$
2. $X'\hat \Omega X/G |X \to \Sigma$ as $G\to \infty$

**Note:** To use the Asymptotic theory for clustering, we need the group number to go to infinity, which in practice might be impossible. Stata uses $\sqrt c \hat u_g$ instead of only $\hat u_g$ to deal with the finite group problem, where $c = \frac{G}{G-1}\frac{N-1}{N-K}$.

**Note:** Clustering can at the same time deal with the heteroskedasticity, so there is no need to use the robust error in clustering.

**Note:** Sometimes we need to do Multiway Clustering because the data is clustered in different dimensions. This will significantly decrease the precision of the clustering regression.



### Quantile Regression

**Definition: (Quantile)** Suppose $Y$ is he dataset, the $\alpha$ th quantile of the data set is defined as $P(y<Q_\alpha) = \alpha$.

**Definition: (Quantile Regression)** Suppose we have $Q_\alpha(y) = X\beta$, or equivalently $y = X\beta + u$ where $Q_\alpha(u) = 0$.  This is called the quantile regression.

**Definition: (Loss Function)** Suppose $y$ is the true value that we want to estimate and $\theta$ is the estimator, then a loss function is defined as $L(y,\theta)$ with $\theta = argmin E[L(y,\theta)]$.

**Definition: (Linear Loss Function)** A Linear Loss Function is defined as $L_\alpha(y,\theta) = (1-\alpha)|y-\theta|$ if $y-\theta<0$ and $L_\alpha(y,\theta) = \alpha|y-\theta|$ if $y-\theta>0$.

**Claim: (Quantile Regression)** Using the linear loss function we can get the quantile regression, i.e. $\hat Q_\alpha(y) = argmin_\theta E[L(y,\theta)]$



### Censoring 

**Definition: (Top Coding)** Suppose we have a regression model $y^\star_i = X_i\beta +\epsilon_i$ and define $y_i = y_i^\star$ if $y_i^\star\leq c$ and  $y_i = c$ if $y_i^\star> c$.

**Method: (Quantile Regression with Top Coding)** When $y_i^\star\leq c$, the CDF of $y$ is the same as $y^\star$, so the quantile regression still work for $y_i^\star\leq c$. When $y_i^\star> c$, we have $P(y\leq c|X = x)\leq P(y\leq y^\star|X = x)$. So we can find a lower bound for the CDF when we cannot observe the data.

**Definition: (Belief Regression)** We can use specific questionnaire to get information of beliefs, where we can only get the CDF values of some points. So it’s a partial identification. 

## Panel Data

### Panel Data Model

#### Pooled OLS

**Definition: (Pooled OLS)** For a given data set $(y_{it}, x_{it})$, $i= 1,2,...,N$ and $t = 1,2,..., T$, we assume $y_{it} = x_{it}\beta+ u_{it}$, with $N\to +\infty$ and $T<+\infty$. This model is called the Pooled OLS.

**Assumption: (Pooled OLS)**

- Each sample is drawn with i.i.d.
- $E[x_{it}'x_{it}]^{-1}$ exists
- $E[u_{it}|x_{it}] = 0$

**Claim: (Pooled OLS)** Under the pooled OLS assumptions, the pooled OLS estimator is unbiased and consistent, and all the result from cross sectional OLS regression work.

#### Panel Data Model

**Definition: (Panel Data Model)** Suppose we have the data set $(y_{it}, x_{it})$. The Panel Data Model is
$$
y_{it} = x_{it}\beta + c_i + u_{it}
$$


### Fixed Effect Estimator

#### Fixed Effect

**Definition: (Fixed Effect Estimator)** Consider the panel data model. Take the average of the data over time t, we have $\bar y_{i} = \bar x_{i}\beta + c_i + \bar u_{i}$. Define $\ddot y_{it}  =y_{it}-\bar y_i$, $\ddot x_{it} = x_{it}-\bar x_i$, and $\ddot u_{it} = u_{it}-\bar u_i$. Then the FE transformation gives us $\ddot y_{it} = \ddot x_{it}\beta + \ddot u_{it}$. Define $\ddot X_i = [\ddot x'_{i1},...,\ddot x'_{iT}]'$ Then the FE estimator is defined as:
$$
\hat \beta_{FE} = (\sum_{i=1}^N \sum_{t=1}^T \ddot x'_{it} \ddot x_{it})^{-1}(\sum_{i=1}^N\sum_{t=1}^T\ddot x_{it}\ddot y_{it}) = (\sum_{i=1}^N \ddot X'_{i} \ddot X_{i})^{-1}(\sum_{i=1}^N \ddot X_{i}\ddot y_{i})
$$
**Definition: (Fixed Effect Residual)** Define the Fixed Effect Residual as $\hat u_{it} = \ddot y_{it}-\ddot x_{it}\hat \beta_{FE}$. Notice $\hat u_{it}$ is an estimator of $\ddot u_{it}$ instead of $u_{it}$.

**Assumption: (FE Assumption)**

1. Strictly Exogeneity: $E(u_{it}|x_{i},c_i) = 0$ for all t
2. Rank Condition: $rank(\sum_{t=1}^T E[\ddot x_{it}'\ddot x_{it}]) = rank(E[\ddot X_{i}'\ddot X_{i}])=K$
3. Serial Uncorrelation and Heterogeneity: $E[u_iu_i'|x_i,c_i] = \sigma_u^2I_T$

**Claim: (Consistency of FE Estimator)** Under FE assumption 1-2, FE estimator is consistent.

**Claim: (Asymptotic Distribution of FE Estimator)** Under FE assumption 1-3, the following is true:

1. $\sqrt N (\hat \beta_{FE}-\beta)\to^d N(0,\sigma_u^2E[\ddot X'_i\ddot X_i]^{-1})$
2. $\hat \sigma_u^2 = \sum_{i=1}^N \sum_{t=1}^T\hat u_{it}^2/(N(T-1)-K)\to^p \sigma_u^2$
3. $N\hat {AVAR}(\hat \beta_{FE}) = N\hat \sigma_u^2 [\sum_{i=1}^N\ddot X'_i\ddot X_i]^{-1} \to^p \sigma_u^2E[\ddot X'_i\ddot X_i]^{-1}$

#### Dummy Variable Regression

**Definition: (Dummy Variable Regression Model)** The Dummy Variable Regression Model is $y_{it} = x_{it}\beta + \sum_{j=1}^N dj_{i} c_i + u_{it}$, where $dj_{i} = 1$ if $j=i$ and $dj_{i} = 0$ if $j \neq i$.

**Definition: (Dummy Variable Estimator)** The Dummy Variable Estimator of $\beta$ is $\hat \beta_{DV} = \hat \beta_{FE}$, and the estimator of $\hat c_i = \bar y_i-\bar x_i\hat \beta_{FE}$.

**Theorem: (Dummy Variable Estimator)** $\hat c_i$ is unbiased yet inconsistent.

Proof:

First prove the unbiasedness. $E[\hat c_i] = E[x_i \beta + c_i - \bar x_i \hat \beta_{FE}] = c_i$.

Second prove the inconsistency. $\hat c_i = \bar y_i-\bar x_i\hat \beta_{FE} = a_i+\bar u_i +\bar x_i(\beta-\hat \beta_{FE})$. Note that $t< +\infty$, we cannot say $\hat c_i\to ^pc_i$. $\square$ 

#### Serial Correlation and Heterogeneity

**Definition: (Serial Correlation Test)** We regress a pooled OLS on $\hat u_{it} = \delta \hat u_{it}+v_{it}$, and test $H_0: \delta = -\frac{1}{T-1}$. Notice $cov(\ddot u_{it}, \ddot u_{it-1}) = cov(u_{it}-\bar u_i, u_{it-1}-\bar u_i) = \frac{1}{T}\sigma_u^2-\frac{2}{T}\sigma_u^2+\frac{1}{T^2}\sigma_u^2$, and $var(\ddot u_{it-1}) = var(u_{it-1}-\bar u_i) = (1+\frac{1}{T^2}-\frac{2}{T})\sigma_u^2$. So $\delta = (1-T)/(1-2T+T^2)=-\frac{1}{T-1}$.

**Definition: (Robust Variance Matrix Estimator)** Under serial correlation, the Robust Variance Matrix Estimator is $\hat{AVAR}(\hat \beta_{FE}) = (\sum_{i=1}^N\ddot X_i'\ddot X_i)^{-1}(\sum_{i=1}^N\ddot X_i'\hat u_i\hat u'_i\ddot X_i)(\sum_{i=1}^N\ddot X_i'\ddot X_i)^{-1}$.

**Claim: (Asymptotic Distribution of FD Estimator)** Under FE assumption 1-3, the following is true:

1. $\sqrt N (\hat \beta_{FE}-\beta)\to^d N(0,E[\ddot X'_i\ddot X_i]^{-1}\Sigma E[\ddot X'_i\ddot X_i]^{-1})$
2. $N\hat {AVAR}(\hat \beta_{FE}) = N(\sum_{i=1}^N\ddot X_i'\ddot X_i)^{-1}(\sum_{i=1}^N\ddot X_i'\hat u_i\hat u'_i\ddot X_i)(\sum_{i=1}^N\ddot X_i'\ddot X_i)^{-1} \to^p E[\ddot X'_i\ddot X_i]^{-1}\Sigma E[\ddot X'_i\ddot X_i]^{-1}$

where $\Sigma = E[\ddot X' u_iu_i'\ddot X|x_i,c_i]$.

#### FEGLS

**Method: (FEGLS Estimator)** We have $\ddot y_{it} = \ddot x_{it}\beta + \ddot u_{it}$, Suppose we drop time period T equation, and define $\Omega = E[\ddot u_i\ddot u_i']$. Notice the matrix is of size $(T-1)\times (T-1)$. The FEGLS is obtained by following steps:

1. After dropping the last time period for each i, define the $(T-1)\times 1$ residuals as $\hat u_{it}^\star = \ddot y_i-\ddot X_i \hat \beta_{FE}$, and a constant estimator of $\Omega$ is $\hat \Omega =\frac{1}{N}\sum_{i=1}^N\hat u_{it}^\star\hat u_{it}'^\star$.
2. The Fixed Effect GLS estimator is defined by $\hat \beta_{FEGLS} =(\sum_{i=1}^N \ddot X'_{i} \hat \Omega^{-1} \ddot X_{i})^{-1}(\sum_{i=1}^N \ddot X_{i} \hat\Omega^{-1} \ddot y_{i})$.

**Assumption: (FEGLS Assumption)**

1. Strictly Exogeneity: $E(u_{it}|x_{it},c_i) = 0$ for all t.
2. Rank Condition: $rank(\sum_{t=0}^T E[\ddot x_{it}' \Omega^{-1} \ddot x_{it}]) = rank(E[\ddot X_{i}' \Omega^{-1}\ddot X_{i}])=K$.
3. Robust Variance Matrix: $E[u_iu_i'|x_i,c_i] = \Lambda$, where $\Lambda$ is positive semidefinite and symmetric

**Claim: (Asymptotic Theory of FEGLS)** Under assumption 1-2, FEGLS estimator is consistent. Under assumption 1-3, we have 

1. $\sqrt N(\hat \beta_{FEGLS}-\beta) \to^d N(0,E[\ddot X_{i}' \Omega^{-1}\ddot X_{i}]^{-1})$
2. $N\hat {AVAR}(\hat \beta_{FEGLS}) = N[\sum_{i=1}^N\ddot X'_i\hat \Omega^{-1}\ddot X_i]^{-1} \to^p E[\ddot X_{i}' \Omega^{-1}\ddot X_{i}]^{-1}$



### First Difference Estimator

#### FD Estimator

**Definition: (First Difference Estimator)** Consider the panel data model. Define $\Delta y_{it}  =y_{it}-y_{it-1}$, $\Delta x_{it}  =x_{it}-x_{it-1}$, and $\Delta u_{it}  =u_{it}-u_{it-1}$. Then the FD transformation gives us $\Delta y_{it} = \Delta x_{it}\beta + \Delta u_{it}$. Define $\Delta X_i = [\Delta x'_{i2},...,\Delta x'_{iT}]'$ Then the FD estimator is defined as:
$$
\hat \beta_{FD} = (\sum_{i=1}^N \sum_{t=1}^T \Delta x'_{it} \Delta x_{it})^{-1}(\sum_{i=1}^N\sum_{t=1}^T \Delta x_{it} \Delta y_{it}) = (\sum_{i=1}^N \Delta X'_{i} \Delta X_{i})^{-1}(\sum_{i=1}^N \Delta X_{i} \Delta y_{i})
$$
**Note:** Notice that the size of the $\Delta X_i$ is $K\times (T-1)$.

**Definition: (First Difference Residual)** Define the First Difference Residual as $\hat e_{it} = \Delta y_{it}-\Delta x_{it}\hat \beta_{FD}$. Notice $\hat e_{it}$ is an estimator of $\Delta u_{it}$ instead of $u_{it}$.

**Assumption: (FD Assumption)**

1. Strictly Exogeneity: $E(u_{it}|x_{i},c_i) = 0$ for all t
2. Rank Condition: $rank(\sum_{t=2}^T E[\Delta x_{it}'\Delta x_{it}]) = rank(E[\Delta X_{i}'\Delta X_{i}])=K$
3. Serial Uncorrelation and Heterogeneity: $E[\Delta u_i\Delta u_i'|x_i,c_i] = \sigma_e^2I_{T-1}$

**Claim: (Consistency of FD Estimator)** Under FD assumption 1-2, FE estimator is consistent.

**Claim: (Asymptotic Distribution of FD Estimator)** Under FD assumption 1-3, the following is true:

1. $\sqrt N (\hat \beta_{FD}-\beta)\to^d N(0,\sigma_e^2E[\Delta X'_i\Delta X_i]^{-1})$
2. $\hat \sigma_e^2 = \sum_{i=1}^N \sum_{t=2}^T\hat e_{it}^2/(N(T-1)-K)\to^p \sigma_e^2$
3. $N\hat {AVAR}(\hat \beta_{FE}) = N\hat \sigma_u^2 [\sum_{i=1}^N\ddot X'_i\ddot X_i]^{-1} \to^p \sigma_u^2E[\ddot X'_i\ddot X_i]^{-1}$

#### Serial Correlation and Heterogeneity

**Definition: (Serial Correlation Test)** We regress a pooled OLS on $\hat e_{it} = \delta \hat e_{it}+v_{it}$, and test $H_0: \delta = -\frac{1}{2}$. Notice $cov(\Delta u_{it}, \Delta u_{it-1}) = cov(u_{it}-u_{it-1}, u_{it-1}-u_{it-2}) = -\sigma_u^2$, and $var(\Delta u_{it-1}) = var(u_{it-1}-u_{it-2}) = 2\sigma_u^2$. So $\delta = -0.5$.

**Definition: (Robust Variance Matrix Estimator)** Under serial correlation, the Robust Variance Matrix Estimator is $\hat{AVAR}(\hat \beta_{FD}) = (\sum_{i=1}^N\Delta X_i'\Delta X_i)^{-1}(\sum_{i=1}^N\Delta X_i'\hat e_i\hat e'_i\Delta X_i)(\sum_{i=1}^N\Delta X_i'\Delta X_i)^{-1}$.

**Claim: (Asymptotic Distribution of Robust FD Estimator)** Under FE assumption 1-3, the following is true:

1. $\sqrt N (\hat \beta_{FD}-\beta)\to^d N(0,E[\Delta X'_i\Delta X_i]^{-1}\Sigma E[\Delta X'_i\Delta X_i]^{-1})$
2. $N\hat {AVAR}(\hat \beta_{FD}) = N(\sum_{i=1}^N\Delta X_i'\Delta X_i)^{-1}(\sum_{i=1}^N\Delta X_i'\hat e_i\hat e'_i \Delta X_i)(\sum_{i=1}^N\Delta X_i'\Delta X_i)^{-1} \to^p E[\Delta X'_i\Delta X_i]^{-1}\Sigma E[\Delta X'_i\Delta X_i]^{-1}$

where $\Sigma = E[\Delta X' e_ie_i'\Delta X|x_i,c_i]$.

#### Comparison of Estimators

**Claim: (FE and FD)** Under FE Assumption 1-3, the FE estimator is the most efficient. Under FD Assumption 1-3, the FD estimator is the most efficient.



### Random Effect

**Definition: (Feasible GLS Estimator)** Consider the panel data model. Define Random Effect model $y_{it} = x_{it}\beta+v_{it}$ where $v_{it} = c_i+u_{it}$. Then the Feasible GLS Estimator is defined as 
$$
\hat \beta_{FD} = (\sum_{i=1}^N X'_{i} \Omega^{-1} X_{i})^{-1}(\sum_{i=1}^N  X_{i} \Omega^{-1} y_{i})
$$
where $\Omega = E[v_iv_i']$. To estimate $\Omega$, we follow the traditional GLS estimation:

1. Do OLS of $y_{it}$ on $x_{it}$ and get the estimated residual $\hat v_{i}$
2. Estimate $\Omega$ with $\hat \Omega = \sum_{i=1}^N\hat v_{i}\hat v'_{i}/N$

**Assumption: (RE Assumption)**

1. Strictly Exogeneity: $E(u_{it}|x_{i},c_i) = 0$  and $E(c_{i}|x_{i}) = E[c_i] = 0$ for all t
2. Rank Condition: $rank(\sum_{t=0}^T E[ x_{it}' \Omega^{-1}  x_{it}]) = rank(E[X_{i}' \Omega^{-1}X_{i}])=K$.
3. Robust Variance Matrix: $E[v_iv_i'|x_i,c_i] = \Omega$, where $\Lambda$ is positive semidefinite and symmetric
4. Serial Uncorrelation and Heterogeneity: $E[u_iu_i'|x_i,c_i] = \sigma_u^2I_T$ and $E[c_i^2|x_i] = \sigma_c^2$

**Claim: (Asymptotic Theory of Feasible GLS)** Under assumption 1-2, Feasible GLS estimator is consistent. Under assumption 1-3, we have 

1. $\sqrt N(\hat \beta_{GLS}-\beta) \to^d N(0,E[ X_{i}' \Omega^{-1}X_{i}]^{-1})$
2. $N\hat {AVAR}(\hat \beta_{FE}) = N[\sum_{i=1}^N X'_i\hat \Omega^{-1} X_i]^{-1} \to^p E[ X_{i}' \Omega^{-1}X_{i}]^{-1}$. Under assumption 4, we have $\Omega = \sigma_u^2 I_T+ \sigma_c^2 \iota_T\iota_T'$.



### Endogeneity in Panel Data

#### FEIV and FDIV

**Definition: (FEIV Estimation)** Suppose there is an instrument variable $z_{it}$ such that $cov(\ddot x_{it},\ddot z_{it})\neq 0$, then the FEIV estimation is defined with the normal IV estimator.

**Assumption: (FEIV Assumption)**

1. $E[u_{it}|z_i,c_i] = 0$ for all i and all t
2. $\sum_{t=0}^T E[\ddot z_{it}'\ddot z_{it}]$ and $\sum_{t=0}^T E[\ddot z_{it}'\ddot x_{it}]$ are both full rank

**Claim: (FEIV Estimation Consistency)** Under FEIV assumptions, the FEIV estimator is consistent.

**Definition: (FDIV Estimation)** Suppose there is an instrument variable $w_{it}$ such that $cov(\Delta x_{it},w_{it})\neq 0$, then the FDIV estimation is defined with the normal IV estimator.

**Assumption: (FDIV Assumption)**

1. $E[u_{it}|w_{is},c_i] = 0$ for all i and all t and $s < t$
2. $\sum_{t=0}^T E[w_{it}' w_{it}]$ and $\sum_{t=0}^T E[w_{it}'\Delta x_{it}]$ are both full rank

**Claim: (FDIV Estimation Consistency)** Under FDIV assumptions, the FDIV estimator is consistent.

#### Sequential Exogeneity

**Assumption: (Sequential Exogeneity)** $E[u_{it}|x_{is},c_i] = 0$ for all $s<t$.

**Note:** suppose we only have sequential exogeneity, the FE and FD estimator are both inconsistent. Comparing them we would prefer to use the FE estimator, since the endogeneity problem becomes smaller as $T\to \infty$.

**Claim: (Sequential Exogeneity)** Suppose Sequential Exogeneity is true, then $E[\Delta u_{it}x_{is}] = 0$.

**Note:** Suppose Sequential Exogeneity is true, then we can use the lag of $\Delta x_{is}$ or $x_{is}$ as instruments to directly run the FDIV estimation. Because the FEIV requires the instrument variable to be strictly exogenous, we cannot use the FEIV method.



### Clustering with Fixed Effect

**Definition: (Clustering with Fixed Effect Model)** The Clustering with Fixed Effect Model is $y_{jg} = x_{jg}\beta +v_g+\epsilon_{jg}$, where $v_g$ is the unobserved heterogeneity term and $\epsilon_{jg}$ is the idiosyncratic error, grouping over $g\in G$.

**Note:** When we use clustering with fixed effect models, we need to think the error that is not shared within the group, because the variation shared within the group has been captured by $v_g$.



## Counterfactuals

### Missing Data

**Assumption: (Missing Data)** Assume that the data takes the form $(x,z,yz)$. where $z$ is a dummy variable taking 1 when we observe the data and take 0 when we don’t observe the data.

**Definition: (Identification)** Suppose we want to identify the probability of $P(y\leq t|X = x)$, by total probability formula, we have $P(y\leq t|X = x) = P(y\leq t|X = x,z = 1)P(z=1|X = x)+P(y\leq t|X = x,z = 0)P(z = 0|X = x)$. The Partial Identification of the CDF is:
$$
P(y\leq t|X = x) \in [P(y\leq t|X = x,z = 1)P(z=1|X = x),P(y\leq t|X = x,z = 1)P(z=1|X = x)+P(Z = 0|X = x)]
$$
**Assumption: (Missing at Random)** $P(y\leq t|X = x,z = 1) = P(y\leq t|X = x,z = 0)$.

**Claim: (Missing at Random)** Under the Missing at Random assumption, the Partial Identification of the CDF is $P(y\leq t|X = x,z = 1)$. Under the Missing at Random assumption, the OLS estimation with only the observed data is unbiased and consistent.



### Rubin Neyman Causal Model

**Definition: (Rubin Neyman Causal Model)** Define $\Tau$ to be the set of possible treatments and define $y$ as a set of possible outcomes. Note $y_j(t):\Tau\to y$. Define $z_j$ as the actual treatment. Then $y_j = y_j(z_j)$. The Rubin Neyman Causal Model focus on anticipating $D[y_j(t')-y_j(t)]$, where $D(.)$ is a functional operator.

**Note:** The problem with the counterfactuals model is that we can never observe $y_j(t)$ for $t\neq z_j$, so we essentially encounter the missing data problem.

**Definition: (Counterfactuals)** Define Counterfactuals as $P(y_j(d)\leq t|X = x)$ for all $d\in \Tau$. By total probability formula, the Partial Identification of the CDF is:
$$
P(y_j(d)\leq t|X = x) \in [P(y_j(z_j)\leq t|X ,z = z_j)P(z=z_j|X ),P(y_j(z_j)\leq t|X ,z = 
z_j)P(z=z_j|X )+P(Z \neq  z_j|X )]
$$
**Definition: (Object of Interest)** The Object of interest of the model could be a function of the data, i.e. $D(.)$ such that the value of the functional is a real number.

**Definition: (Respect Stochastic Dominance)** Suppose we have $y_1\geq_{FOSD} y_0$, then if $D(y_1)\geq D(y_0)$, we say that functional $D(.)$ Respect Stochastic Dominance.

**Example: (Expectation)** The expectation is a functional that respect Stochastic Dominance, i.e. the partial identification of the following is:
$$
E[y_j(t)-y_j(s)]\in [0,y_{1j}(t)-y_{0j}(s)]
$$
**Assumption: (Random Assignment of Treatment)** $P(y(d)\leq t|X = x, Z =z) = P(y(d)\leq t|X = x)$ for all $z$.

**Claim: (Random Assignment of Treatment)** Under Random Assignment of Treatment, $P(y_j(d)\leq t|X = x) = P(y_j(d)\leq t|X = x,Z = z)$.

suppose the treatment $z\in \{0,1\}$, then we have:
$$
E[y(0)|z = 1] = E[y(0)|z = 0] \\
E[y(1)|z = 0] = E[y(1)|z = 1] \\
$$
**Assumption: (Treatment Choice by Optimization)** Assume that people are choosing their treatment by their best response, i.e. for all $j$, we have $y_j(d)\leq_{FOSD} y_j(Z_j)$ for all $d$. Note that here $y_j(d)$ is a random variable.

**Claim: (Treatment Choice by Optimization)** Under the assumption of Treatment Choice by Optimization, the Partial Identification of the CDF is:
$$
P(y\leq t|X = x) \in [P(y_j(d)\leq t|X ,z = z_j)P(z=z_j|X ), P(y_j(d)\leq t|X ,z = z_j)]
$$
suppose the treatment $z\in \{0,1\}$, then we have:
$$
E[y(0)|z = 1] \leq E[y(1)|z = 1] \\
E[y(1)|z = 0] \leq E[y(0)|z = 0] \\
$$
**Assumption: (Monotone Treatment Response)** Assume that if the treatments can be ordered, then for $t\geq s$, we have $y_j(t)\geq_{FOSD} y_j(s)$ for all j.

**Theorem: (Monotone Treatment Response)** Under the assumption of Monotone Treatment Response, suppose there are 2 random variables $y_0$ and $y_1$, such that $y_0\leq_{FOSD} y_j\leq_{FOSD} y_1$, then we have
$$
y_{0j}(t)\leq y_j(t)\leq y_{1j}(t)
$$
where $y_{0j}(t) = y_j$ if $ t\geq z_j$ and $y_{0j}(t) = y_0$ for other t, and $y_{1j}(t) = y_j$ if $ t\leq z_j$ and $y_{0j}(t) = y_1$ for other t.

suppose the treatment $z\in \{0,1\}$, then we have:
$$
E[y(0)|z = 1] \leq E[y(1)|z = 1] \\
E[y(1)|z = 0] \geq E[y(0)|z = 0] \\
$$
Proof:

When $t<z_j$, by Monotone Treatment Response we have $y_j(t)\leq y_j(z_j) = y_j$. Similarly, when $t>z_j$, by Monotone Treatment Response we have $y_j(t)\geq y_j(z_j) = y_j$. $\square$ 

**Assumption: (Monotone Treatment Selection)** Assume that for each t and $s'\geq s$, $E[y(t)|z  =s']\geq E[y(t)|z = s]$.

suppose the treatment $z\in \{0,1\}$, then we have:
$$
E[y(0)|z = 0] \leq E[y(0)|z = 1] \\
E[y(1)|z = 1] \geq E[y(1)|z = 0] \\
$$
**Note:** MTR and MTS are two different assumption. Take OLS model as an example, $y= X\beta+e$. MTR requires that $\beta\geq 0$, and MTS requires $E[e|z = s']\geq E[e|z = s]$ for $s'\geq s$. 

**Note:** Sometimes by introducing more assumptions we can narrow the confidence interval of the partial identification, for example assuming $y(.)$ is concave.



### Selection Model

#### Homogenous Reservation Wage

**Example: (Log Wage Regression)** Suppose we do a regression of $wage = \beta_0+\beta_1 educ+u$. Here we might run into a problem since not all of the people in the data set are working, so for people who are not working we cannot observe his or her potential wage. Intentionally we have a selection model problem.

**Definition: (Reservation Wage)** Suppose any worker in the data set will choose to work if and only if the wage in the job market for him is higher than his Reservation wage $R$. If we do observe him working, denote $z_i=1$. So we have $z_i=1$ is equivalent to  $y\geq R$.

**Assumption: (Homogenous Reservation Wage)** Suppose $R(x)$ is a function of the demographic data. And suppose the reservation wage is the same for same $X=x$.

**Definition: (Identification)** By total probability theorem, we have
$$
P(y\leq t|X = x) = P(y\leq t|X = x,z = 1)P(z=1|X = x)+P(y\leq t|X = x,z = 0)P(Z = 0|X = x)
$$
Denote $y^\star (x) = min_i (y_i(x))$. Note that under the Homogenous Reservation Wage assumption. we have that if $t\geq y^\star (x)\geq R(x)$
$$
P(y<t|X=x,z = 0) = P(y<t|X=x,y<R(x))=1
$$
Since $y<R(x)$ essentially implies that $y < t$ for $t\geq R(x)$. Hence for $t\geq y^\star$, we can pointily identify the following:
$$
P(y\leq t|X = x) = P(y\leq t|X = x,z = 1) P(z=1|X = x) + P(Z = 0|X = x)
$$

#### Heckman 2-Step Regression

**Definition: (Log Wage Regression Model)** The Log Wage Regression that we are considering here is $logy = x\beta_1+\epsilon_1 $ and $logR  =x\beta_2+\epsilon_2$, where $R$ is the reservation wage, and $\epsilon_1, \epsilon_2\sim N(0,\Sigma)$. Assume $\epsilon_1,\epsilon_2$ are independent to x. Denote $z$ as an indicator such that $z =1$ when we do observe the wage of the data.

**Method: (Heckman 2-Step Regression)**

1. Note that $P(z = 1|X = x) = P(y(x)>R(x)|X = x) = P(\epsilon_2-\epsilon _1< x(\beta_1-\beta_2)|X = x) = \Phi(\frac{x(\beta_1-\beta_2)}{\sigma})$, where $\sigma = \sqrt{\sigma_{11}^2+\sigma_{22}^2-2\sigma_{12}}$. Hence we have $x\tilde \beta = \Phi^{-1}(P(z = 1|X = x))$, where $\tilde \beta = (\beta_1-\beta_2)/\sigma$. So the estimator is $\hat {\tilde \beta}  = E[x'x]^{-1}E[x'\Phi^{-1}(P(z = 1|X = x))]$.
2. $E[log(y)|X = x,z = 1] = E[log(y)|X = x, log(y)>log(R)] = E[x\beta_1+\epsilon_1|X = x, x(\beta_2-\beta_1)>\epsilon_1-\epsilon_2]$, which equals to $ x\beta_1+ E[\epsilon_1|x(\beta_2-\beta_1)<\epsilon_1-\epsilon_2]$. By the normal distribution we have $E[log(y)|X = x,z = 1]= x\beta_1+\sigma_{1u}m(x\tilde\beta)$, where $m(z) = \phi(z)/\Phi(z)$ and $\sigma_{1u} = cov(\epsilon_1, \frac{\epsilon_2-\epsilon_1}{\sigma})$. So we could run a OLS of $log(y)$ on $x$ and $m(x\tilde \beta)$.

**Note:** Notice that the first regression can be seen as a binary outcome regression, so it is in fact doing a Probit model regression of $z$ on $x$.

## Treatment Effect

### Local Average Treatment Effect

**Setup: (Local Average Treatment Effect)** Suppose an IV estimation has the following setup:
$$
y_j = \beta_jx_j +\epsilon_j, cov(z_j,\epsilon_j) = 0,cov(z_j,x_j) \neq  0
$$
So the IV estimator is $\hat\beta_{IV} = \frac{cov(y,z)}{cov(x,z)} = \frac{E[y|z=1]-E[y|z=0]}{E[x|z=1]-E[x|z=0]}$, with the assumption that $z_j$ is independent to $y_j$.

**Definition: (Respondence Function)** We have the definition of the following respondence:

- $x_j(0) = 0, x_j(1) = 0$ is a never-taker, the fraction in the data is defined as $\pi_n$
- $x_j(0) = 0, x_j(1) = 1$ is a complier, the fraction in the data is defined as $\pi_c$
- $x_j(0) = 1, x_j(1) = 0$ is a deifier, the fraction in the data is defined as $\pi_d$
- $x_j(0) = 1, x_j(1) = 1$ is a always-taker, the fraction in the data is defined as $\pi_a$

**Assumption: (Monotonicity Assumption)** We have $x_j(1)\geq x_j(0)$ for all j, i.e. there is no deifier in the dataset or $\pi_d=0$.

**Solution: (Local Average Treatment Effect)**

Note that $E[x |z = 0] = P(x = 1|z = 0) = P(x(0) = 1) = \pi_a$, given the monotonicity assumption. Similarly we have $E[x |z = 1] = P(x = 1|z = 1) = P(x(1) = 1) = \pi_a+\pi_c$, so $E[x|z = 1]-E[x|z = 0] = \pi_c$.

Now check the nominator: $ E[y|z = 1] = E[y|z = 1,C]\pi_C+E[y|z = 1,N]\pi_N+E[y|z = 1,A]\pi_A$. Plugging in $x(z)$ we have $ E[y|z = 1] = E[y(1)|C]\pi_C+E[y(0)|N]\pi_N+E[y(1)|A]\pi_A$. Similarly we have $ E[y|z = 0] = E[y(0)|C]\pi_C+E[y(0)|N]\pi_N+E[y(1)|A]\pi_A$. So the difference between them is $E[y|z = 1] - E[y|z = 0] = E[y(1)-y(0)|C]\pi_C$.

So the IV estimator is $E[y(1)-y(0)|C]$.

**Note:** The IV estimator is only telling us the LATE, instead of the ATE overall. In practice, the portion of the compliers in the group might be very small.

**Solution: (Local Average Treatment Effect)**

Under the assumption that Monotonicity is true, we have that $E[y|x = 0, z = 1] = E[y(0)|N]$, and $E[y|x = 1, z = 0] = E[y(1)|A]$. Now note that by the law of iterated expectation, we have 
$$
E[y|x = 1, z = 1] = \frac{\pi_A}{\pi_A+\pi_C}E[y(1)|A]+\frac{\pi_C}{\pi_A+\pi_C}E[y(1)|C] \\
E[y|x = 0, z = 0] = \frac{\pi_N}{\pi_N+\pi_C}E[y(0)|N]+\frac{\pi_C}{\pi_N+\pi_C}E[y(0)|C]
$$
From this we can calculate the local average treatment effect: 
$$
E[y(1)-y(0)|C] = \\ \frac{(\pi_A+\pi_C)}{\pi_C}E[y|x =1,z = 1]-\frac{\pi_A }{\pi_C}E[y(1)|A]
- \frac{(\pi_N+\pi_C)}{\pi_C}E[y|x =0,z = 0]+\frac{\pi_N }{\pi_C}E[y(0)|N]
$$
**Note:** We still need $E[y(0)|A]$ and $E[y(1)|N]$ to calculate ATE, which is impossible to get if we don’t make further assumptions.



### Regression Discontinuity

#### Sharp Regression Discontinuity

**Definition: (Running Variable)** Suppose $x$ is a binary treatment and $z$ is a Running Variable if $x = 1$ if $z\geq c$, and $x = 0$ if $z < c$. 

**Definition: (Regression Discontinuity)** Suppose $y_j = \beta_j x_j + e_j$,  we can estimate the average treatment effect at the critical point $E[y(1)-y(0)|z = c)]$ with the following estimator: $lim_{\epsilon\to 0^+} E[y(1)|Z = c+\epsilon] - E[y(0)|Z = c-\epsilon]$, with the assumption that $\beta_j(z)$ is a continuous function of $z$.

#### Fuzzy Regression Discontinuity

**Assumption: (Regression Discontinuity)** $lim_{\epsilon\to 0^+} P(x = 1|z = c+\epsilon) \neq lim_{\epsilon\to 0^+} P(x = 1|z = c-\epsilon)$.

**Definition: (Fuzzy Regression Discontinuity Regressor)** The Fuzzy Regression Discontinuity Regressor is defined as
$$
\frac{\lim_{\epsilon\to 0^+}E[y|z = c+\epsilon] - \lim_{\epsilon\to 0^+}E[y|z = c-\epsilon]}{\lim_{\epsilon\to 0^+}E[x|z = c+\epsilon] - \lim_{\epsilon\to 0^+}E[x|z = c-\epsilon]}
$$
**Assumption: (Monotonicity Property)** Define $x(z)$ to be the treatment with running variable z, then it is non-increasing in $z$, i.e. when the criterion is higher the portion who get treated is lower.

**Definition: (Complier)** In this setup, the complier is defined as $\lim_{\epsilon\to 0^+}x(z+\epsilon) = 0$, and $\lim_{\epsilon\to 0^+}x(z-\epsilon) = 1$.

**Note:** With Sharp Regression Discontinuity, everyone is a complier. With Fuzzy Regression Discontinuity, not everyone is a complier.

**Theorem: (LATE in RD)** The Fuzzy Regression Discontinuity Regressor will give us the LATE of the compliers. That is:
$$
E[y(1)-y(0)|z = c, compliers]
$$
 Proof:

This follows directly from the LATE. $\square$ 

#### Implement RD

**Definition: (McCrary Test)** Given the density of the running variable $z$, we should not see the discontinuity in it. This is called the McCrary Test.

**Definition: (Sharp Local Linear Regression)** Consider the following model:
$$
y_i = \alpha_L +\beta_L (z_i-c) +e_L \space \forall z_i< c\\
y_i = \alpha_H +\beta_H (z_i-c) +e_H \space \forall z_i> c
$$
Hence the Sharp RD estimator is $\hat {RD} = \hat \alpha_H-\hat \alpha_L$.

**Definition: (Fuzzy Local Linear Regression)** Consider the following model:
$$
y_i = \alpha_L +\beta_L (z_i-c) +e_L \space \forall z_i< c\\
y_i = \alpha_H +\beta_H (z_i-c) +e_H \space \forall z_i> c \\
x_i = \gamma_L +\beta_L (z_i-c) +e_L \space \forall z_i< c\\
x_i = \gamma_H +\beta_H (z_i-c) +e_H \space \forall z_i> c \\
$$
Hence the Fuzzy RD estimator is $\hat {RD} = \frac{\hat \alpha_H-\hat \alpha_L}{\hat \gamma_H-\hat \gamma_L}$.



### Exogenously Assigned Treatment

#### Exogenously Assigned Treatment

**Assumption: (Exogenously Assigned Treatment)**

- Conditional Unconfoundedness: $(z\perp y(1), y(0))|x$
- Overlap Assumption: $P(z=1|X = x)\in (0,1)$

**Definition: (Treatment Effect Estimator)** With the above assumption, denote $x$ to be the characteristics, denote $y$ to be the dependent variable, and $z$ to be the treatment. We want to estimate the average treatment effect, i.e. $E[y(1)-y(0)]$. Note that we have, by assumption, that:
$$
E[y(1)-y(0)] = E[E[y(1)-y(0)|X = x]] = \sum_x P(x)(E[y|X=x, z = 1] -E[y|X=x, z = 0] )
$$
So we only need to estimate $E[y|X=x, z = 1]$ and E$[y|X=x, z = 0]$.

#### Kernel Regression

**Definition: (Non-Parametric Regression)** Suppose we want to estimate $E[y|X = x]$ without assuming any parametric model for the function form of this model. This regression is called a Non-Parametric Regression.

**Definition: (Non-Parametric Estimator for categorical Variables)** The Non-Parametric Estimator for $E[y|X = x]$ when $X$ are categorical variables, i.e. the support for the possible $x$ is finite, is defined as
$$
\hat \mu(c) = \frac{\sum_{i=1}^N y_i 1[X_i = c]}{\sum_{i=1}^N 1[X_i = c]}
$$
**Definition: (Kernel Function)** A kernel function would satisfy the following properties:

- $K(0) = 1$
- $K'(t)>0$ for $t<0$ and $K'(t)<0$ for $t>0$
- $lim_{t\to +\infty}K(t) = 0$ and $lim_{t\to -\infty}K(t) = 0$

**Definition: (Non-Parametric Estimator for categorical Variables)** The Non-Parametric Estimator for $E[y|X = x]$ when $X$ are categorical variables, i.e. the support for the possible $x$ is finite, is defined as
$$
\hat \mu(c) = \frac{\sum_{i=1}^N y_i K(X_i - c)}{\sum_{i=1}^N K(X_i - c)}
$$
**Note:** The kernel function that we picked here works as the weight that we give to the different $y_i$. The closer the data i is to $c$, the higher the weight is.

**Definition: (Bandwidth)** We sometimes define the kernel weight as $K(\frac{X_i-c}{h_n})$, where $h_n$ is defined as the Bandwidth.

#### Matching Method

**Definition: (m-th Close Data Point)** Given a data point $i$, the m-th Close Data Point, $l_m(i)$,  is defined as:

- A data point $j$ in the set such that $Z_j\neq Z_i$
- Among such people $l_m(i)$ is the m-th most similar person to $i$, i.e. $\sum_{\{j:Z_j\neq Z_i\}} 1[|X_j-X_i|\leq |X_l-X_i|] = m$

**Definition: (m-th Close Set)** Define the m-th Close Set as $L_m(i) = \{l_1(i),l_2(i),...,l_m(i)\}$. 

**Definition: (Matching Estimator)** The m-close Matching Estimator is defined as $\hat y_i(z) = y_i$ if $Z_i = z$ and $\hat y_i(z) = \frac{1}{m}\sum_{j\in L_m(i)} y_j$ if $Z_j\neq z$.

**Definition: (Matching Method)** Suppose we want to estimate the Treatment Effect $E[y(1)-y(0)]$ under Exogenously Assigned Treatment Assumption. So the estimator is $\frac{1}{N}\sum_{i=1}^N(\hat y_i(1)-\hat y_i(0))$.

#### Propensity Score

**Definition: (Propensity Score)** Propensity Score is defined as $e(x) = P(Z = 1|X = x)$.

**Theorem: (Propensity Score)** Under the assumption of Exogenously Assigned Treatment, we have $E[y(1)] = E[\frac{Zy}{e(x)}]$ and $E[y(0)] = E[\frac{(1-Z)y}{1-e(x)}]$.

Proof:

We have the following equations:
$$
E[\frac{Zy}{e(x)}] = E[\frac{Zy}{e(x)}1(Z = 0)+ \frac{Zy}{e(x)}1(Z = 1)] \\
 = E[\frac{0y(0)}{e(x)}+ E[\frac{y(1)}{e(x)}1(Z = 1)] \\
  = E[E[\frac{y(1)}{e(x)}1(Z = 1)|X = x]] = E[y(1)]
$$
Similarly we can prove the second part. $\square$ 

**Definition: (Propensity Score Estimator)** Under the assumption of Exogenously Assigned Treatment, Propensity Score Estimators are defined as $\hat y(1) = \frac{1}{N}\sum_{i=1}^N\frac{Z_iy_i}{e(x_i)}$ and $\hat y(1) = \frac{1}{N}\sum_{i=1}^N\frac{(1-Z)y}{1-e(x)}$.



## Bayesian Statistics

**Definition: (Bayesian Estimation)** Suppose a parameter $\theta$ is a random variable with a prior belief of $P(\theta)$. $y$ is the dataset that we observe. The Bayesian Estimation gives the likelihood function: $P(\theta| y) = P(y|\theta) P(\theta) / P(y)$.

**Example: (Bernoulli Random Variable Estimation)** Suppose $y_i \sim B(\theta)$. The probability of observing $y$ given $\theta$ is $P(y|\theta) = \theta^M(1-\theta)^{N-M}$. Suppose the prior of $\theta$ is $P(\theta) = \beta ^{-1}(\alpha,\delta)\theta^{\alpha-1}(1-\theta)^{\delta-1}$. By Bayes rule, we have $P(\theta|y)  = \beta ^{-1}(\alpha+M,\delta+N-M)\theta^{M+\alpha-1}(1-\theta)^{N-M+ \delta-1}$. Hence $\theta|y\sim \beta(\alpha+M, \delta+N-M)$.

**Claim: (Bernstein Theorem)** Under certain circumstances, the Bayesian estimation and the classical estimation collapse when the sample size is large enough. 