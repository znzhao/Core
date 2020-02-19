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

1. For any $\epsilon >0$, Since $\hat\theta_N = argmax \space Q_N(\theta)$, we have $Q_N(\hat\theta_N)\geq Q_N(\theta_0)>Q_N(\theta_0)-\epsilon/3$. Since we have $Q_N(\theta)\to^p Q(\theta)$ uniformly over $\Theta$, when $N\to 0$, we have $P(Q(\hat\theta_N)\geq Q_N(\hat\theta_N)-\epsilon/3)\to 0$ and $P(Q_N(\theta_0)\geq Q(\theta_0)-\epsilon/3)\to 0$. Now combine these three inequalities we have $P(Q(\hat\theta_N)>Q(\theta_0)-\epsilon/3-\epsilon/3-\epsilon/3)\to 0$, i.e. $P(Q(\hat\theta_N)>Q(\theta_0)-\epsilon)\to 0$.
2. Now, denote $N(\theta_0)$ as a neighborhood of $\theta_0$. Define $\theta^\star = argmax_{\theta\in\Theta\cap N^c} \space Q(\theta)$. By assumption $Q(.)$ is continuous, $\Theta\cap N^c$ is compact, so $\theta^\star$ always exists. Now since $Q(\theta)$ is uniquely maximized at $\theta_0$ over $\Theta$, we have $Q(\theta^\star)< Q(\theta_0)$.
3. Since $Q(\theta_0)-Q(\theta^\star)>0$, we can define $Q(\theta_0)-Q(\theta^\star)= \epsilon$, plug it back to step 1 we have $P(Q(\hat\theta_N)>Q(\theta_0)-Q(\theta_0)+Q(\theta^\star))\to 0$, i.e. $P(Q(\hat\theta_N)>Q(\theta^\star))\to 0$. However, by definition $\theta^\star = argmax_{\theta\in\Theta\cap N^c} \space Q(\theta)$, so it implies that $P(\hat\theta_N\in N(\theta_0))\to 0$, which is exactly what I want to show. $\square$

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

**Definition: (Marginal Effect)** The Marginal Effect of the independent variable is $\frac{P(y=1|X)}{x} = \beta g(X\beta)$.

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
For the linear index model, $Q_N(\theta) = \frac{1}{N} \sum_{i=1}^N (y_ilnG(X_i\beta)+(1-y_i)ln(1-G(X_i\beta)))$.

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
- $G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}$ is continuous and twice differentiable, and $G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}>0$ in the neighborhood of $\theta_0$ 
- $\int sup_{\beta}||\nabla_{\beta}G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}||dz< +\infty$ and $\int sup_{\beta}||\nabla_{\beta\beta}G(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}||dz< +\infty$
- $E[sup_{\beta}||\nabla_{\beta}lnG(X_i\beta)^{y_i}(1-G(X_i\beta))^{1-y_i}||]<+\infty$
- $J = \frac{g(x_i\beta)^2x_i'x_i}{G(x_i\beta)[1-G(x_i\beta)]}$ is the Jacobian matrix of the regression, which is symmetric and positive semidefinite

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


## Panel Data

### Cross Sectional Data

**Definition: (Pooled OLS)** For a given data set $(y_{it}, x_{it})$, $i= 1,2,...,N$ and $t = 1,2,..., T$, we assume $y_{it} = x_{it}\beta+ u_{it}$, with $N\to +\infty$ and $T<+\infty$. This model is called the Pooled OLS.



**Assumption: (Pooled OLS)**

- $$

### Panel Data Model

### Fixed Effect Estimator

#### Fixed Effect

#### Dummy Variable Regression

### First Difference Estimator

