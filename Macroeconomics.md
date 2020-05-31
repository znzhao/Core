# MACROECONOMICS

## Centralized Growth Model

### Solow Growth Model

#### Setup

**Assumption: (Solow Model)**

- Capital Accumulation: $K_{t+1}  =(1-\delta)K_t + I_t$
- Exogenous investment: $I_t = sY_t$
- Technology: $Y_t = F(K_t,A_tL_t)$, where $A_{t+1} = (1+g)A_t$ 

**Assumption: (Inada Condition)**

- $F(0,0) = 0$
- $F_K>0$, $F_L>0$, $F_{KK}<0 $, $F_{LL}<0$
- $ F(K,L)$ is constant return to scale
- $ F_K(0,L) = F_{L}(K,0) = +\infty $
- $F_K(+\infty,L) = F_{L}(K,+\infty) = 0$

**Definition: (Steady State)** Steady State is when all the endogenous variables are stable, i.e. $x_{t+1} = x_t$.

**Definition: (Golden Rule)** The Golden Rule of saving is the optimal saving rate such that the steady state consumption is maximized.

#### Solution

**Solution: (Solow Growth Model)**

1. Detrend the model by redefine $y_t = Y_t/A_tL_t = F(K_t/A_tL_t,1) = f(k_t)$, hence we can rewrite the law of motion of the capital accumulation as $(1+g) k_{t+1}  = (1-\delta ) k_t+ s f(k_t)$. 
2. Solve for Steady State. Let $ k = k_t = k_{t+1} $, and we have $(g+\delta )k = sf(k)$. The left hand side of the equation is a linear function, the right hand side is a strictly increasing and strictly concave function. Inada condition ensures that there is a unique solution to this equation.
3. Solve for the golden rule of saving. $s^{\star} = argmax_s (1-s)f(k(s)) = f(k(s)) - (g+\delta )k$. Taking the first order conditions, we have $f'(k^{\star}) = g+\delta$, which will determine the optimal capital per capita and hence determine the optimal saving rate.
4. Compare the growth rate of capital with different initial value. Suppose two countries start from different initial capital per capita $k_1<k_2$. the growth rate of capital is defined as $(k_{t+1}-k_t)/k_t = sf(k_t)/k_t -(g+\delta)$, since $f(k)$ is a concave function, we have that $f(k_1)/k_1>f(k_2)/k_2$, i.e. the country that is more poor will grows faster.



### Krueger Growth Model

#### Setup

**Assumption: (Neoclassical Growth Model)**

- Centralized Economy
- Representative Agents
- Utility function $U(C_t)$ is strictly increasing, strictly concave, separable, and satisfies the Inada conditions
- Technology satisfies Inada conditions

**Definition: (Neoclassical Growth Model)** The social planner will choose the optimal $\{C_t, K_t\}$ such that
$$
max \sum_{t = 0}^{+\infty} \beta ^t U(C_t) \\
s.t. \space K_{t+1}+C_t = F(K_t, A_tL_t) + (1-\delta)K_t
$$

#### Solution

**Solution: (Neoclassical Growth Model)**

1. Detrend the model. define variables per capita and rewrite the problem as 
   $$
   max \sum_{t = 0}^{+\infty} \beta ^t U(A_t L_t c_t) \\
   s.t. \space (1+g)(1+n)k_{t+1}+c_t = f(k_t) + (1-\delta)k_t
   $$
   
2. Use the Lagrange method: $\sum_{t = 0}^{+\infty} [\beta ^t U(A_t L_t c_t) - \lambda_t(f(k_t) + (1-\delta)k_t - (1+g)(1+n)k_{t+1}-c_t) ]$ and the first order conditions are: $\beta^tU'(A_tL_tc_t)A_tL_t = \lambda_t$, and $\lambda_t(1+g)(1+n) = \lambda_{t+1}(f'(k_{t+1})+(1-\delta))$. Combine them we get the following first order conditions:
   $$
   U'(A_tL_tc_t) = \beta U'(A_{t+1}L_{t+1}c_{t+1})(f'(k_{t+1})+(1-\delta))\\
   (1+g)(1+n)k_{t+1}+c_t = f(k_t) + (1-\delta)k_t
   $$
   Suppose $U'(A_tL_tc_t)  = h(A_tL_t)U'(c_t)$, and define $\tilde \beta  = \beta  h(A_{t+1}L_{t+1})/ h(A_{t}L_{t})$ we have 
   $$
   (1+g)(1+n)U'(c_t) = \tilde \beta U'(c_{t+1})(f'(k_{t+1})+(1-\delta))\\
   (1+g)(1+n)k_{t+1}+c_t = f(k_t) + (1-\delta)k_t
   $$
   The first equation is called the Euler’s Equation, and the second is the period feasible condition. From these two equations we can solve for the law of motion of the endogenous variables.
   
3. Solve for the Transversality Condition. it is written as $\lim_{t\to +\infty} \lambda_tk_{t+1}  =0$. Plug in $\lambda_t$ and $k_{t+1}$, we have the Transversality condition can be rewrite as: $\lim_{t\to +\infty} \beta^{t+1}h(A_{t+1}L_{t+1})A_{t+1}L_{t+1}U'(c_{t+1})(f'(k_{t+1})+(1-\delta)) k_{t+1}  =0$.

4. Solve for the Steady State. let $c_t = c_{t+1} = \bar c$ and $k_t = k_{t+1} = \bar k$. From the first order conditions we can get the steady state: $f'(\bar k) = (1+g)(1+n)/\tilde \beta- 1+\delta$ and $\bar c = f(\bar k) + (1-\delta)\bar k - (1+g)(1+n)\bar k$.

5. Draw the Phase Diagram. From the Euler’s Equation, we can see that when $k_t<\bar k$, $c_{t+1} >c_t$ because $f’$ is higher, leading to a lower $U'$ in the next period, i.e. $c_t$ is increasing. From the feasible condition, we can see that when $c_t <\bar c$, $k_{t+1}>k_t$, which is easy to show with the second equation. From the Phase Diagram, we can find the stable arm of the system, which is the unique path given the initial point.

   If the path of the system is not the stable arm, either it violates the feasible condition, where the consumption explodes, or it violates the transversality condition, i.e. the economy is saving too much. Neither of the case could be optimal.

**Note:** Generally we should use log-linearization and use Blanchard’s method to give an approximate solution to the system.

#### Log-Linearization

**Definition: (Log-Linearization)** Suppose there is an endogenous variable $x_t$, Log-Linearization of  $x_t$, denoted as $\hat x_t$, is defined as $\hat x_t = ln(x_t/\bar x)\approx (x_t-\bar x)/\bar x$.

**Lemma: (Log-Linearization)** Suppose $y_t = f(x_t)$, then $\hat y_t = (f(x_t) - f(\bar x_t))/f(\bar x) = \frac{f'(\bar x)\bar x}{f(\bar x)} \hat x_t $.

**Solution: (Neoclassical Model)** The first order conditions can be log-linearized as:
$$
\frac{U''(\bar c)\bar c}{U'(\bar c)}\hat c_t = \frac{U''(\bar c)\bar c}{U'(\bar c)}\hat c_{t+1}+\frac{f''(\bar k)\bar k}{f'(\bar k)+(1-\delta)} \hat k_t\\

\bar k(1+g)(1+n)\hat k_{t+1}+\bar c\hat c_t = \frac {\bar kf'(\bar k)}{f(\bar k)}\hat k_t + (1-\delta)\bar k\hat k_t
$$
which is a linear difference equation system.

#### Solution to the Dynamic System

**Definition: (Linear Difference Equation System)** The above equations can be rewrite as
$$
\left[ \begin{array}{ccc}
\hat c_{t+1}\\
\hat k_{t+1} \\
\end{array} 
\right ]  =
M 
\left[ \begin{array}{ccc}
\hat c_{t}\\
\hat k_{t} \\
\end{array} 
\right ]
$$
**Solution: (Linear Difference Equation System)**

1. Find the eigenvalues and the eigenvectors of the matrix $M$ by using the equation $|M-\lambda I| = 0$. Note that this equation will give us that $\lambda_1\lambda_2 = |M|$ and $\lambda_1+\lambda_2 = Trace(M)$. Calculate $(\lambda_1-1)(\lambda_2-1)<0$, which means the system is a saddle point, proving that there is a unique stable arm.

2. Use the singular value decomposition of the matrix, we can write $M = VDV^{-1}$, where $D$ is a diagonal matrix with two eigenvalue on it’s diagonal, and the first one is smaller than 1, and the second one is greater than 1. $V$ is the matrix composed of the eigenvectors.

3. Rewrite the original equation as
   $$
   V^{-1}
   \left[ \begin{array}{ccc}
   \hat c_{t+1}\\
   \hat k_{t+1} \\
   \end{array} 
   \right ]  =
   DV^{-1}
   \left[ \begin{array}{ccc}
   \hat c_{t}\\
   \hat k_{t} \\
   \end{array} 
   \right ] \\
   
   \left[ \begin{array}{ccc}
   V_{11} & V_{12}\\
   V_{21} & V_{22} \\
   \end{array} 
   \right ]
   \left[ \begin{array}{ccc}
   \hat c_{t+1}\\
   \hat k_{t+1} \\
   \end{array} 
   \right ]  =
   \left[ \begin{array}{ccc}
   \lambda_1 & 0\\
   0 & \lambda_2 \\
   \end{array} 
   \right ]
   \left[ \begin{array}{ccc}
   V_{11} & V_{12}\\
   V_{21} & V_{22} \\
   \end{array} 
   \right ]
   \left[ \begin{array}{ccc}
   \hat c_{t}\\
   \hat k_{t} \\
   \end{array} 
   \right ]
   $$
   Now define $z_t = V_{21}\hat c_t + V_{22}\hat k_t $, which corresponds to the eigenvalue that is greater than 1. we have $z_{t+1} = \lambda_2 z_t$, suppose $z_t\neq0$, then either the feasibility or the transversality condition is violated. As a result $z_t$ have to be 0, which will give us the policy function $\hat c_t =- V_{21}^{-1}V_{22}\hat k_t$, and $\hat k_{t+1} = (-M_{21}V_{21}^{-1}V_{22} + M_{22})\hat k_t$.



## Deterministic Dynamic Programming Theory

### Preliminaries

**Definition: (Contraction Mapping)** A function $f:X\to X$ is a contraction mapping if and only if there is a $\beta \in [0,1)$ such that for any $x,y \in X$, $d(f(x),f(y))\leq \beta d(x,y)$.

**Claim: (Blackwell Sufficient Condition)** Let $X\subset \mathbb{R}^l$ and $T:B(X)\to B(X)$ be a functional where $B(X)$ is the set of all bounded real-value functions on $X$. Then $T$ is a contraction mapping if 

1. $\forall f,g \in B(X)$, if $f\leq g$, then $Tf\leq Tg$
2. $\exist \beta <1$ such that $T(f+\alpha ) \leq Tf+\beta \alpha$ for all $f\in B(X)$ and $\forall \alpha \in \mathbb{R}_+$

**Claim: (Contraction Mapping Theorem)** Let $(X,d)$ be a complete metric space, $f:X\to X$ be a  contraction mapping Then f has a fixed point, i.e. there is a $x\in X$ such that $f(x) = x$ and the fixed point is unique.

**Claim: (Useful Corollary)** Suppose $T:S\to S$ and $Tv^{\star} = v^{\star}$ exists. Then:

1. If $S' \subset S$ is a closed subset of $S$, and $T(S')\subset  S'$, then $v^{\star} \in S'$
2. If $T(S') \subset S'' \subset S$, then $v^{\star} \in S''$

**Claim: (Theorem of Maximum)** Let $F:X\times X \to \mathbb{R}$ to be a continuous function, $\Gamma : X\to X$ to be a compact and continuous correspondence. There exists a value function satisfying the Bellman equation $V(x) = sup_{y\in \Gamma(X)} F(x,y)$, which is continuous. Furthermore, the policy correspondence $G:X\to X$ is non-empty and upper hemi-continuous.



### Deterministic Dynamic Programming

#### Bellman Equation

**Definition: (Bellman Equation)** Let $F:X\times X \to \mathbb{R}$ to be a continuous function, $\Gamma : X\to X$ to be a compact and continuous correspondence. The Bellman equation is defined as $V(x)=TV(x) = sup_{y\in \Gamma(X)} F(x,y)+\beta V(y)$.

**Definition: (Graph)** The graph of the correspondence $\Gamma : X\to X$ is $A = graph (\Gamma ) = \{(x,y)\in X\times X|y\in \Gamma(X)\}$.

#### Properties of the Bellman Equation

**Assumption: (Assumption 1)** $X\subset \mathbb{R}^n $ and the correspondence $\Gamma :X\to X$ is non-empty, compact valued and continuous.

**Assumption: (Assumption 2)** $F: A\to \mathbb{R}$ is bounded and continuous.

**Claim: (Continuity and Boundedness)** Under Assumption 1 and 2, use the theorem of maximum, if we start from a continuous function, the fixed point $v^{\star}$ will also be continuous and bounded.

**Assumption: (Assumption 3)** Given $y$, $F(x,.)$ is strictly increasing in $x$.

**Assumption: (Assumption 4)** $\Gamma (x)$ is monotone. i.e. if $x\leq x'$ then $\Gamma(x) \subset \Gamma (x')$

**Claim: (Monotonicity)** Under Assumption 1-4, if we start from a increasing function, the fixed point $v^{\star}$ will also be increasing.

**Assumption: (Assumption 5)** $F(x,y)$ is strictly concave, i.e. $F(\theta (x,y)+(1-\theta)(x',y'))>\theta F(x,y)+(1-\theta )F(x',y')$.

**Assumption: (Assumption 6)** $\Gamma (x)$ is convex. i.e.  $\theta y+(1-\theta ) y'\in \Gamma (\theta x+(1-\theta)x')$ for any $\theta \in (0,1)$ and $y\in \Gamma(x)$ and $y' \in\Gamma(x')$ for any $x$ and $x'$.

**Claim: (Concavity)** Under Assumption 1-2 and 5-6, if we start from a strictly concave function, the fixed point $v^{\star}$ will also be strictly concave, and the policy function exists.

**Assumption: (Assumption 7)** $F(x,y)$ is continuously differentiable on the interior of $A$.

**Claim: (Differentiability)** Under Assumption 1-2 and 5-7, the fixed point $v^{\star}$ will also be strictly concave, and the unique fixed point of $T$ is continuously differentiable at $x_0\in int(A)$ with $\frac{\partial v^{\star}(x_0)}{\partial x^i} = \frac{\partial F(x_0,g(x_0))}{\partial x^i} $.

#### Sequential Problem and Recursive Problem

**Definition: (Sequential Problem)** The sequential problem is defined as:
$$
sup\sum_{t=0}^{+\infty}\beta ^t F(x_t,x_{t+1}) \space s.t.\space x_{t+1} \in \Gamma (x_t), \space x_0\in X 
$$
**Definition: (Recursive Problem)** The recursive problem is defined as
$$
v(x) = sup_{y\in \Gamma(x)} [F(x,y)+\beta v(y)]
$$
**Claim: (Principle of Optimality)** Under Assumption 1 and 2, if $v$ solves the sequential problem it will also solves the recursive problem. Suppose $v^{\star}$ solves the recursive problem and satisfies the boundedness condition, i.e. $lim_{n\to +\infty } \beta ^n v(x_n) = 0$ for all $x\in \pi (x_0)$ and $x_0 \in X$, where $\pi(x_0) = \{\{x_{t+1}\}_{t=0}^\infty| x_{t+1} \in \Gamma (x_t)\}$. Then $v^{\star}$ also solves the sequential problem.

#### Solution to the Bellman Equation

**Solution: (Algorithm to solve for the Euler Equation)**

1. First Order Condition: $F_y(x,y)+\beta V'(y) = 0$
2. Envelope Theorem: $V'(x) = F_x(x,y)$, push into next period, we have $V'(y) = F_x(y,g(y))$
3. Combine them: $F_y(x,y)+\beta F_x(y,g(y)) = 0$, which is the Euler Equation.

**Solution: (Guess and Verify)** 

1. First guess the form of the value function or the form of the policy function.
2. Plug in the Bellman Equation and solve for the parameters with undetermined parameter method.

**Solution: (Value Function Iteration)**

1. Start from any function $v_0 \in B(X)$, define $v_{i+1} = T(v_i)$
2. iterate the algorithm until $d(v_{i+1}, v_i) <\epsilon$



### Examples

####  Tree Cutting Problem

**Assumption: (Tree-cutting Problem)**

- The law of motion of the tree growth: $k_{t+1} = k_t^\alpha$
- Choose between cutting the tree or not

**Definition: (Tree Cutting Problem)** The recursive problem of the tree cutting problem is
$$
V(k_t)  =max_{\{cut,not\}} \{k_t, \beta V(k_t^\alpha)\}
$$

**Solution: (Value Function Iteration)**

1. Start from $V_0 = 0$. we have the policy function: if $k_t>0$, cut the tree, which will always be true.
2. Now $V_1 = k_t$. We have the policy function: if $k_t>\bar k$ where $\bar k = \beta \bar k^\alpha$, cut the tree, otherwise, leave it there.
3. Note that if one wants to cut the tree in the next period he will do it in exactly next period, because if he cut it in next period he will get $ \beta k_t^\alpha$, and if he cut it in next two periods, he will get $ \beta^2 k_t^{\alpha^2} <  \beta k_t^\alpha$, because $\alpha<1$.
4. We then get the value function: $V(k_t) = \bar k$, if $k_t<\bar k$, and $V(k_t) =  k_t $ otherwise.

#### Neoclassical Growth Model

**Definition: (Neoclassical Growth Model)** The recursive problem of the Neoclassical Growth Model is
$$
V(k)  =max\space ln(k^\alpha - k')+\beta V(k'), \space k'\in [\epsilon,K]
$$

**Solution: (Guess and Verify)**

1. First we check that the value function is in fact a contraction mapping. Since $k'\in [\epsilon,K]$, notice that we can define $\bar K = max\{k_0,K\}$, the Bellman function is a mapping $T:B([\epsilon,\bar K])\to B([\epsilon,\bar K])$ where $B([\epsilon,\bar K])$ is the set of all bounded real-value functions on $[\epsilon,\bar K]$. Now check the monotonicity and discounting condition. Suppose $f \in B([\epsilon,\bar K])$ and $h \in B([\epsilon,\bar K])$, and $f\geq h$. Suppose $k' = g(k)$ is the solution to $T(h)$. Then We have:
   $$
   T(h) = max\space ln(k^\alpha - k')+\beta h(k') = ln(k^\alpha - g(k))+\beta h(g(k)) \\
   \leq ln(k^\alpha - g(k))+\beta f(g(k)) \leq max\space ln(k^\alpha - k')+\beta f(k') = T(f)
   $$
   And we also have:
   $$
   T(f+a) = max\space ln(k^\alpha - k')+\beta f(k')+\beta a \leq T(f) +\beta a 
   $$
   By the Blackwell Condition, we conclude that the Bellman function is a contraction mapping.

2. Solve for the Euler Equation, which is $\frac{1}{k^\alpha - k'} = \beta \frac{\alpha {k'}^{\alpha-1}}{{k'}^\alpha - k''}$.

3. Guess and verify. We guess the optimal value function looks like $V(k) = Aln(k)+B$. Using the method of undermined variables, we can plug it back in the Bellman Equation. By first order condition we have the policy function looks like $\frac{1}{k^\alpha - k'} = \beta \frac{A}{k'}$, i.e. $k'=\frac{\beta A }{1+\beta A}k^\alpha$. This will give us 
   $$
   Aln(k)+ (1-\beta)B = -ln(1+\beta A)+\alpha ln(k)+\beta Aln(\frac{\beta A }{1+\beta A})+\beta A\alpha ln(k)
   $$
   Hence$ A = (1+\beta A)\alpha$.

#### Neoclassical Growth Model with Asset

**Assumption: (Setup)**

- Basic neoclassical growth model setup
- There is another asset $a_t$, which can be chosen by the consumer
- The return of the asset is exogenous, given as $r_t$
- Suppose the return is constant

**Definition: (Neoclassical Growth Model with Asset)** The recursive problem of the Neoclassical Growth Model with asset is
$$
V(k,a)  =max\space ln(k^\alpha+ ra - k'-a')+\beta V(k',a'), \space k'\in [\epsilon,K], \space a'\in [0,A]
$$

**Solution: (Check CMT)**

The main aim of this problem is to check the contraction mapping theorem works. Similarly define $\bar K = max\{k_0,K\}$, the Bellman function is a mapping $T:B([\epsilon,\bar K]\times[0,A])\to B([\epsilon,\bar K]\times[0,A])$ where $B([\epsilon,\bar K]\times[0,A])$ is the set of all bounded real-value functions on $[\epsilon,\bar K]\times[0,A]$. 

Now check the monotonicity and discounting condition. Suppose $f \in B([\epsilon,\bar K]\times[-A,A])$ and $h \in B([\epsilon,\bar K]\times[-A,A])$, and $f\geq h$. Suppose $k' = g_1(k,a)$ and $a' = g_2(k,a)$ are the solutions to $T(h)$. Then we have:
$$
T(h) = max\space ln(k^\alpha+ ra - k'-a')+\beta h(k',a') = max\space ln(k^\alpha+ ra - g_1(k,a)-g_2(k,a))+\beta h(g_1(k,a),g_2(k,a)) \\
\leq ln(k^\alpha+ ra - g_1(k,a)-g_2(k,a))+\beta f(g_1(k,a),g_2(k,a)) \leq max\space ln(k^\alpha+ ra - k'-a')+\beta f(k',a') = T(f)
$$
And we also have:
$$
T(f+a) = max\space ln(k^\alpha+ ra - k'-a')+\beta f(k',a')+\beta a \leq T(f) +\beta a
$$
By the Blackwell Condition, we conclude that the Bellman function is a contraction mapping.



## Stochastic Dynamic Programming Theory

### Stochastic Dynamic Programming

#### Markov Process

**Definition: (History)** The History of a process is defined as $S^t = \{S_0,S_1, ...,S_t\}$, where $S_\tau \in S$.

**Definition: (Markov Chain)** $\{S_t\}$ is a Markov Chain if $S_t\in S$ can take only $n$ possible values with $n \in \N$, and $P(S_{t+1}|S^t) = P(S_{t+1}|S_t)$

**Definition: (Markov Process)** A Markov Process is defined as $(S,P,\psi_0)$, where

1. A realization $S_t$ takes one of the $n$ values in $S$
2.  $P_{ij} = P(S_{t+1} = S_j|S_t = S_i)$, $P_{ij} \in [0,1]$, and $\sum_jP_{ij} = 1$
3. $\psi_{0,i}$ is the initial probability of state $i$, $\psi_{0,i} \in [0,1]$, and $\sum_i\psi_{0,i} = 1$

**Definition: (Unconditional Distribution)** The Unconditional Distribution of $S_t$ is $\psi_{t,j} = \sum_iP_{ij}\psi_{t-1,i}$, i.e. $\psi_t = (P')^t\psi_0$.

**Definition: (Unconditional Expectation)** The Unconditional Expectation of $S_t$ is defined as $E[S_t] =  ((P')^t\psi_0)'\tilde S$.

**Definition: (Stationary Distribution)** The Stationary Distribution is defined as $\psi^{\star} = P'\psi^{\star}$, i.e. the stationary distribution solves $(I-P')\psi^{\star} = 0$ and $\sum_i \psi^{\star}_i = 1$.

**Definition: (Conditional Expectation)** The Conditional Expectation of $S_t$ is defined as $E_t[S_{t+1}] = E[S_{t+1}|S_t] = \sum_jP_{ij}S_j$.

####  Stochastic Dynamic Programming

**Definition: (Stochastic Bellman Equation)** Let $F:X\times X \to \mathbb{R}$ to be a continuous function, $\Gamma : X\to X$ to be a compact and continuous correspondence. X can include a random variable. The Bellman equation is defined as $TV(x) = sup_{y\in \Gamma(X)} F(x,y)+\beta E[V(y)|x]$.

**Note:** The properties of the Bellman Equation is not changing when we include random variable in the state variable. Now a policy function $y = g(x)$ is the solution of a stochastic difference equation. There is no steady state in the stochastic model, instead, the endogenous variables goes to a stable distribution. Given the Law of motion of the stochastic process and solve for the policy function, we could calculate the stable distribution.



### Stochastic Growth Model

#### Setup

**Assumption: (Stochastic Growth Model)**

- Social planner’s problem 
- Stochastic TFP shock, following a Markov Process, i.e. $P(z_t = z_j|z_{t-1} = z_i) = \pi_{ij}$
- The history of the process is $z^t = \{z_0,z_1, ... , z_t\}$
- Normal assumptions about the utility function and production function
- For simplicity, suppose there is no growth in the model

#### Sequential Problem

**Definition: (Sequential Problem)** The Sequential Problem of the Stochastic Growth Model is defined as:
$$
max \sum_{t = 0}^{+\infty} \sum_{z^t} \beta ^t U(c_t(z^t))\pi_t(z^t) \\
s.t. \space k_{t+1}(z^t)+c_t(z^t) = z_t(z^t)f(k_t(z^{t-1})) + (1-\delta)k_t(z^{t-1})
$$
**Solution: (Sequential Problem)**

1. Use the Lagrange method. The Lagrange function is:
   $$
   L = \sum_{t = 0}^{+\infty} \sum_{z^t} [ \beta ^t U(c_t(z^t))\pi_t(z^t) \\
   + \lambda_t(z^t) (z_t(z^t)f(k_t(z^{t-1})) + (1-\delta)k_t(z^{t-1}) - k_{t+1}(z^t)-c_t(z^t))]
   $$
   The first order conditions are:
   $$
   \beta ^t U'(c_t(z^t))\pi_t(z^t) = \lambda_t(z^t) \\
   \lambda_t(z^t) = \sum_{z'|z^t}\lambda_{t+1}(z^t,z')[z'f'(k_{t+1}(z^t))+1-\delta]
   $$
   Combine the two first order conditions, we end up with one equation:
   $$
   U'(c_t(z^t)) = \beta \sum_{z'|z^t}U'(c_{t+1}(z^t,z'))[z'f'(k_{t+1}(z^t))+1-\delta]\pi_t(z^t,z')/\pi_t(z^t)
   $$

2. Since $z_t$ is a Markov process, we have $\pi_t(z^t,z')/\pi_t(S^t) = \pi(z'|z_t)$, we can then rewrite the Euler Equation as $U'(c_t) = \beta E_t[U'(c_{t+1})z_{t+1}(f'(k_{t+1})+1-\delta)]$. 

#### Recursive Problem

**Definition: (Recursive Problem)** The Sequential Problem of the Stochastic Growth Model is defined as:
$$
V(k,z) = max \space U(c) + \beta  \sum_{z'}V(k',z')\pi(z',z) \\
s.t. \space k'+c = zf(k) + (1-\delta)k
$$
**Solution: (Recursive Problem)**

1. Take the first order condition, which will give us:
   $$
   U'(zf(k)+(1-\delta)k-k') = \beta \sum_{z'}V_k(k',z')\pi(z',z)
   $$
   Then use the envelope theorem:
   $$
   V_k(k,z) = U'(zf(k)+(1-\delta)k-k')[zf'(k)+1-\delta]
   $$
   Combine These two equations, we can get a system of stochastic differential equations:
   $$
   U'(c) = \beta \sum_{z'} U'(c')[z'f'(k')+1-\delta]\pi(z',z)\\
   k'+c = zf(k) + (1-\delta)k
   $$

2. From this system of stochastic differential equations, solve for $c(k,z)$ and $k’(k,z)$.



## Labor Market Model

### McCall’s Job Searching Model

 #### Setup

**Assumption: (Basic McCall’s Model)**

- Risk-neutral Individual, who only cares about money, receives a job market offer in each period, with wage $w$
- The distribution of wage is $F(w)$ for $w\in[0,B]$
- The worker decides to accept or decline in each period
- After accepting, the worker would work forever
- If she declines the offer, the worker will get some benefit and wait until next period to get another offer

**Definition: (Worker’s Problem)** The Bellman Equation for the worker is:
$$
V(w) = max_{y = \{accept, decline\}}\{w+\beta V(w), b+\beta E[V(w')]\}
$$

#### Solution

**Solution: (Basic McCall’s Model)**

1. Notice that $\bar V = b+\beta E[V(w')]$ is a constant. Hence there is a Reservation Wage $\bar w$, such that $\bar w+\beta V(\bar w) =\bar V $ the optimal policy function of the worker is:
   $$
   y=\begin{equation}
   \left \{
                \begin{array}{lr}
                accept, &  if \space w\geq\bar w \\
                decline, & if  \space w< \bar w
                \end{array}
   \right.
   \end{equation}
   $$
   i.e. the value function of the problem becomes:
   $$
   V(w)=\begin{equation}
   \left \{
                \begin{array}{lr}
                w+\beta V(w) = \frac{1}{1-\beta} w, &  if \space w\geq\bar w \\
                \bar V = \frac{1}{1-\beta}\bar w, & if  \space w< \bar w
                \end{array}
   \right.
   \end{equation}
   $$

2. Next we want to solve for the reservation wage. Note that by the definition of reservation wage, we have:
   $$
   \begin{align}
   \begin{split}
   	\bar V &= b+\beta E[V(w')] \\
   	&= b+\beta \int_0^\bar w V(w')dF(w')+\beta \int_\bar w^B V(w')dF(w') \\
   	&= b+\beta \int_0^B \bar VdF(w')+\beta \int_\bar w^B (V-\bar V)dF(w')\\
   	&= b+\beta \bar V+\beta \int_\bar w^B \frac{w'-\bar w}{1-\beta}dF(w')\\
   \end{split}
   \end{align}
   $$
   Then move $\beta \bar V$ to the other side of the equation, we will get:
   $$
   \begin{align}
   
       (1-\beta) \bar V = b+\beta \int_\bar w^B \frac{w'-\bar w}{1-\beta}dF(w')\\
       (1-\beta) \frac{1}{1-\beta}\bar w = b+\beta \int_\bar w^B \frac{w'-\bar w}{1-\beta}dF(w')\\
   	\bar w = b+ \frac{\beta }{1-\beta} \int_\bar w^B(w'-\bar w)dF(w')\\
   
   \end{align}
   $$
   This will give us a unique reservation wage.

**Lemma: (Newton-Leibniz Formula)** Suppose a function is $g(x) = \int_{a(x)}^{b(x)}f(x,y)dx$, then the first order differentiation of $g(.)$ is:
$$
g'(x) = f(x,b(x))b'(x) - f(x,a(x))a'(x) +\int_{a(x)}^{b(x)}\frac{\partial f(x,y)}{\partial x}dy
$$
**Theorem: (Properties of the Reservation Wage)** Define $R(\bar w) = \frac{\beta }{1-\beta} \int_\bar w^B(w'-\bar w)dF(w')$, this function has the following properties:

1. $R(0) = \frac{\beta}{1-\beta}E[w]$
2. $R(B) = 0$
3. $R'(x) = -\frac{\beta}{1-\beta}(1-F(x))<0$
4. $R''(x) = \frac{\beta}{1-\beta}f(x)>0$

Proof: 

Properties 1 and 2 are trivial. We apply Newton-Leibniz Formula to $R(x)$, and we will get $R'(x) = -\frac{\beta}{1-\beta}(1-F(x))$. And $R''(x) = \frac{\beta}{1-\beta}f(x)$ is trivial to get once we get $R'(x)$. $\square$

**Note:** By the properties of $R(x)$, it is a strictly decreasing and strictly convex function. Since $T(x) = x-b$ is an increasing linear function, We know that there must be a solution to the equation $x-b = R(x)$.

#### Comparative Statics

**Theorem: (Comparative Statics)** The reservation wage have the following properties:

1. When $b$ increases $\bar w$ increases
2. When $\beta$ increases $\bar w$ increases
3. When the distribution moves such that the new distribution $G\leq F$, then $\bar w$ increases
4. When the distribution moves such that the new distribution is risker, then $\bar w$ increases

Proof:

First, when $b$ increases, $T(x) = x-b$ moves downward, and $R(x)$ doesn’t move. Hence $\bar w$ increases.

Second, when $\beta$ increases $R(x)$ moves upward, and $T(x)$ doesn’t move. Hence $\bar w$ increases.

Third, when the new distribution $G\leq F$, $E[w]$ moves upward, and $T(x)$ doesn’t move. Hence $\bar w$ increases. Note that the equation can be rewrite as:
$$
\begin{align}
\begin{split}
	\bar V & = b+\beta \int_0^B V(w')dF(w')\\
	&= b+\beta( V(w')F(w')|_0^B - \int_0^B F(w')dV(w'))\\
	&= b+\beta( \frac{B}{1-\beta} - \int_0^B F(w')dV(w'))\\
	&= b+\beta( \frac{B}{1-\beta} - \int_\bar w^B F(w')\frac{1}{1-\beta}dw')
\end{split}
\end{align}
$$
Hence we can get:
$$
\begin{align}
\begin{split}
	(1-\beta)\bar V & = (1-\beta)b+\beta B- \beta \int_\bar w^B F(w')dw'\\
	\bar w -b & = \beta(B-b) - \beta \int_\bar w^B F(w')dw'
	
\end{split}
\end{align}
$$
Note that the right hand side of the equation is still $R(x)$. Hence when the new distribution has $G\leq F$, we we have $\int_\bar w^B G(w')dw'< \int_\bar w^B F(w')dw'$. Then $R(x)$ moves upward, and $T(x)$ doesn’t move. Hence $\bar w$ increases.

Forth, when the new distribution moves such that $\int_0^x G(w')dw'\geq \int_0^x F(w')dw'$, we have:
$$
\begin{align}
\begin{split}
	\bar w &= b+ \frac{\beta }{1-\beta} \int_\bar w^B(w'-\bar w)dF(w')\\
	&= b+ \frac{\beta }{1-\beta} \int_0^B(w'-\bar w)dF(w') -  \frac{\beta }{1-\beta} \int_0^\bar w(w'-\bar w)dF(w') \\
	&= b+ \frac{\beta }{1-\beta} (E[w']-\bar w) -  \frac{\beta }{1-\beta} \int_0^\bar w(w'-\bar w)dF(w') \\
	&= b+ \frac{\beta }{1-\beta} (E[w']-\bar w) -  \frac{\beta }{1-\beta} ( (w'-\bar w)F(w')|_0^\bar w - \int_0^\bar w F(w')dw' )
\end{split}
\end{align}
$$
Since $(w'-\bar w)F(w')|_0^\bar w   =0$, we have:
$$
\bar w =(1-\beta) b+ \beta E[w']+  \beta \int_0^\bar w F(w')dw' \\
\bar w - b =\beta (E[w']-b)+  \beta \int_0^\bar w F(w')dw'
$$
Note that the right hand side of the equation is still $R(x)$, since the new distribution is risker, $R(x)$ moves upward, and $T(x)$ doesn’t move. Hence $\bar w$ increases. $\square$



### Mutation of McCall’s Model

#### Searching with Probability of Being Fired

**Assumption: (Setup)**

1. Exogenous probability $\delta$ of losing their job every period
2. People who lost their job stay unemployed for a period for the next period and start to search for job in the next period after that

**Definition: (Searching with Probability of Being Fired)** The recursive problem of Searching with Probability of Being Fired is:
$$
V(w) = max_{y = \{accept, decline\}}\{w+\beta(\delta (b + \beta E[V(w')]) + (1-\delta)V(w)), b+\beta E[V(w')]\}
$$
**Solution: (Searching with Probability of Being Fired)**

Define $U = b+\beta E[V(w')]$, we have $V(w) = max\{w+\beta (\delta U+(1-\delta)V(w)), U\}$ we want to solve for the reservation wage $\bar w$ such that $U = \bar w+\beta (\delta U+(1-\delta)V(\bar w))$, which implies that $U = \frac{\bar w}{1-\beta}$.

And we have $V(w) = w+\beta(\delta U+(1-\delta)V(w)) = \beta\delta U+w+\beta (1-\delta)V(w)$, so $V(w) = \frac{\beta\delta U + w}{1-\beta(1-\delta)}$. By definition, we have
$$
\begin{align}
\begin{split}
	U &= b+\beta E[V(w')] \\
	&= b+\beta \int_0^\bar w V(w')dF(w')+\beta \int_\bar w^B V(w')dF(w') \\
	&= b+\beta \int_0^B UdF(w')+\beta \int_\bar w^B (V-U)dF(w')\\
	&= b+\beta U+\beta \int_\bar w^B \frac{\beta\delta U + w}{1-\beta(1-\delta)}-UdF(w')\\
	&= b+\beta U+\beta \int_\bar w^B \frac{(\beta-1) U + w}{1-\beta(1-\delta)}dF(w') \\
	&= b+\beta U+\beta \int_\bar w^B \frac{(w-\bar w)}{1-\beta(1-\delta)}dF(w')
\end{split}
\end{align}
$$
Then move $\beta \bar V$ to the other side of the equation, we will get:
$$
\begin{align}    
(1-\beta) \bar V &= b+\frac{\beta}{1-\beta(1-\delta)} \int_\bar w^B (w-\bar w)dF(w')\\
\bar w &=  b+\frac{\beta}{1-\beta(1-\delta)} \int_\bar w^B (w-\bar w)dF(w')
\end{align}
$$
This will give us a unique reservation wage.

#### Searching with Wage Increase

**Assumption: (Setup)**

1. The wage that that the worker will receive is increasing as time passes
2. The increase rate of the wage is $g$

**Definition: (Searching with Wage Increase)** The recursive problem of Searching with Wage Increase is:
$$
V(w) = max_{y = \{accept, decline\}}\{w+\beta V(w(1+g)), b+\beta E[V(w')]\}
$$
**Solution: (Searching with Wage Increase)**

1. Notice that $\bar V = b+\beta E[V(w')]$ is a constant. Hence there is a Reservation Wage $\bar w$, such that $\bar w+\beta V(\bar w) =\bar V $ the optimal policy function of the worker is:
   $$
   y=\begin{equation}
   \left \{
                \begin{array}{lr}
                accept, &  if \space w\geq\bar w \\
                decline, & if  \space w< \bar w
                \end{array}
   \right.
   \end{equation}
   $$
   i.e. the value function of the problem becomes:
   $$
   V(w)=\begin{equation}
   \left \{
                \begin{array}{lr}
                w+\beta V(w(1+g)) = \frac{1}{1-\beta(1+g)} w, &  if \space w\geq\bar w \\
                \bar V = \frac{1}{1-\beta(1+g)}\bar w, & if  \space w< \bar w
                \end{array}
   \right.
   \end{equation}
   $$

2. Next we want to solve for the reservation wage. Note that by the definition of reservation wage, we have:
   $$
   \begin{align}
   \begin{split}
   	\bar V &= b+\beta E[V(w')] \\
   	&= b+\beta \int_0^\bar w V(w')dF(w')+\beta \int_\bar w^B V(w')dF(w') \\
   	&= b+\beta \int_0^B \bar VdF(w')+\beta \int_\bar w^B (V-\bar V)dF(w')\\
   	&= b+\beta \bar V+\beta \int_\bar w^B \frac{w'-\bar w}{1-\beta(1+g)}dF(w')\\
   \end{split}
   \end{align}
   $$
   Then move $\beta \bar V$ to the other side of the equation, we will get:
   $$
   \begin{align}
   (1-\beta) \bar V &= b+\beta \int_\bar w^B \frac{w'-\bar w}{1-\beta(1+g)}dF(w')\\
   (1-\beta) \frac{1}{1-\beta(1+g)}\bar w &= b+\beta \int_\bar w^B \frac{w'-\bar w}{1-\beta(1+g)}dF(w')\\
    \frac{1-\beta}{1-\beta(1+g)}\bar w &= b+ \frac{\beta }{1-\beta(1+g)} \int_\bar w^B(w'-\bar w)dF(w')\\
   \end{align}
   $$
   This will give us a unique reservation wage.

#### Searching with Changing Environment

**Assumption: (Setup)**

1. The worker can decide whether to keep working or quit the job and be unemployed
2. If the worker quit at time t, he will work at time t and start being unemployed in the next period
3. There are two states in the world: Good and Bad, and the probability of being in good state is $p$
4. If the worker quit in good state, he will draw a new wage from a distribution $F_G(w)$
5. If the worker quit in good state, he will draw a new wage from a distribution $F_B(w)\geq F_G(w)$ for all $w$

**Definition: (Searching with Changing Environment)**  The recursive problem of Searching with Changing Environment is
$$
V(w, S) = max_{y = \{work, unemployed\}}\{w+\beta (pV(w,G)+(1-p)V(w,B)) \\
, b+\beta (p\int_0^MV(w',)dF_S(w') + (1-p)\int_0^MV(w',B)dF_S(w'))\}
$$
where $S\in \{G,B\}$ denotes the state of the economy.

**Note:** Note that now there are two reservation wage $\bar w (G)$ and $\bar w (B)$.



### Diamond-Mortenson-Pissarides Model

#### Setup

**Assumption: (Diamond-Mortenson-Pissarides Model)**

- Unemployed workers find a job with probability $1-F(\bar w)$
- Exogenous probability $\delta$ of losing their job every period
- People who lost their job stay unemployed for a period for the next period and start to search for job in the next period after that
- Each Firm employs one worker
- Firms find new workers by a matching mechanism
- When matched with worker, each firm will produce $z$ amount of output
- Job creates by posting vacancies at cost $kz>0$
- Free Entry
- After a worker and a firm meet, they will decide the wage by bargaining
- Focus on steady state

**Definition: (Matching Function)** A Matching Function matches unemployment number and vacant job number and forms an employment number, i.e. $m_tL_t = M(u_tL_t,v_tL_t)$.

**Assumption: (Matching Function)** Assume that the Matching Function is increasing, concave, and constant return to scale.

**Definition: (Job Finding Rate)** Define the Job Finding Rate as $f_t = m_t/u_t= M(u_t,v_t)/u_t$.

**Definition: (Vacancy Filling Rate)** Define the Vacancy Filling Rate as $q_t = m_t/v_t= M(u_t,v_t)/v_t$.

**Definition: (Labor Market Tightness)** Define the Labor Market Tightness as $\theta_t = v_t/u_t$.

**Lemma: (Properties of the Rates)** We have $f_t = M(1,v_t/u_t) = f(\theta_t)$ and $q_t = M(u_t/v_t,1) = f(\theta_t)/\theta_t$.

**Definition: (Unemployment Rate)** The Unemployment Rate evolves as $u_{t+1} = \delta (1-u_t)+(1-f(\theta_t))u_t$. Furthermore, in steady state, we have $u = \delta / (\delta+f(\theta))$.

**Definition: (Beveridge Curve)** At steady state, define a Beveridge Curve as a function of $v$ and $u$, by the definition of the law of motion of unemployment, i.e. $u = \delta / (\delta+f(v/u))$.

**Definition: (Nash Bargaining)** A Nash Bargaining Function is $max\{(W(w)-U)^\phi(J(w)-V)^{(1-\phi)}\}$. 

#### Bellman Equation

**Definition: (Worker’s Bellman Equations)** At the steady state, the value of working, $W$, and being unemployed, $U$, are:
$$
\begin{align}
W &= w+\beta (\delta U+(1-\delta)W)\\
U &= b+\beta (f(\theta) W+(1-f(\theta))U)
\end{align}
$$
**Definition: (Firm’s Bellman Equations)** At the steady state, the value of producing, $J$, and vacancy, $V$, are:
$$
\begin{align}
J &= z-w+\beta (\delta V+(1-\delta)J)\\
V &= -kz+\beta (q(\theta) J+(1-q(\theta))V)
\end{align}
$$

#### Solution

**Solution: (Steady State Solution)**

1. From the worker’s Bellman Equation, we get $W = \frac{w+\beta \delta U}{1-\beta (1-\delta)}$, and from the firm’s Bellman Equation we get $J = \frac{z-w+\beta \delta V}{1-\beta (1-\delta)}$.

2. Now because of the free entry assumption, the value of posting vacancies should be zero, otherwise the firm will keep posting vacancies. Hence we have at the equilibrium $V = 0$. This leads to $ kz=\beta q(\theta) J$, and:
   $$
   J = z-w+\beta (1-\delta)J \\
   w = z-(1-\beta (1-\delta))J = z-(1-\beta (1-\delta)) \frac{kz}{\beta q(\theta)}
   $$
	The above equation is called the Market Tightness Curve.

3. Now use the Nash Bargaining Function, which is to maximize the following given $U$ and $V$:
   $$
   max\{(W(w)-U)^\phi(J(w)-V)^{(1-\phi)}\}
   $$
   Take the first order conditions we will get $\phi \frac{W'(w)}{W(w)-U} = -(1-\phi) \frac{J'(w)}{J(w)-V}$, where the first order differentiation comes from step 1. We have ${W'(w)} = -J'(w) = 1/(1-\beta(1-\delta))$. Hence we have $\phi (J-V)  =(1-\phi)(W-U)$. Use the fact that $V = 0$, and plug in W and J from step 1, we have:
   $$
   \phi \frac{z-w}{1-\beta (1-\delta)} = (1-\phi)(\frac{w+\beta \delta U}{1-\beta (1-\delta)}-U) \\
      \phi (z-w) = (1-\phi)(w+\beta \delta U-U+U\beta (1-\delta))\\

      w - (1-\beta)U = \phi(w-(1-\beta)U+z-w)\\
      w = \phi z +(1-\phi)(1-\beta)U
   $$
   Observe that now we only need to solve for $U$. Remember that from the Bellman Equation of Unemployment, we have $U(1-\beta) = b+\beta f(\theta)( W-U) =b+\beta f(\theta)(\phi /(1-\phi))(J-V)  = b+\beta f(\theta)(\phi /(1-\phi))\frac{kz}{\beta q(\theta)}$. Now use this to substitute $(1-\beta)U$, and remember $f(\theta)/q(\theta) = \theta$, we have:
   $$
   w = \phi z +(1-\phi)(1-\beta)U = \phi z +(1-\phi)(b+\beta f(\theta) \frac{\phi} {(1-\phi)} \frac{kz}{\beta q(\theta)})\\
      w = \phi z +(1-\phi)(b+\theta \frac{\phi} {(1-\phi)} kz) \\
      w= (1-\phi)b+\phi(1+k\theta)z
   $$
   The above equation is called the Wage Curve.

4. Combine the Market Tightness Curve and the Wage Curve, we can solve for $w$ and $\theta$, and then from the Beveridge Curve we can find the unemployment rate and the vacancy rate.



## Complete Market and Decentralized Economy

### Arrow-Deberu Equilibrium

#### Setup

**Assumption: (Arrow-Deberu)**

- There are $I$ numbers of consumers in total
- The state of the economy is denoted as $S_t$, and the history is denoted as $S^t = \{S_\tau\}_{\tau=0}^t$ 
- Stochastic Endowment Economy, person $i$’s endowment is denoted as $e_t^i(S^t)$
- Identical utility function $U$ among the consumers
- Complete market, meaning there are contingent claims for each state
- The consumers trade with each other at the beginning of the economy, then they will never trade again
- $Prob(S_{t+1}| S_t) = \pi(S_{t+1}|S_t)$ is a Markov process

#### Arrow-Deberu Equilibrium

**Definition: (Arrow-Deberu Equilibrium)** The Arrow-Deberu Equilibrium is defined as a set of price $\{\tilde p^0_t\}$ of consumption, a set of individual decisions $\{C^i_t(S^t)\}$, such that:

1. Given the set of price, the individual decision variables solves the following consumer’s problem:
   $$
   max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^tU(C_t^i(S^t))\pi(S^t) \\
      s.t. \space \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)C_t^i(S^t) \leq \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)e_t^i(S^t)
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
   This is true for any individual. Hence if we take person i’s First Order Conditions and divided with person j’s equation, we will get:
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

**Assumption: (Sequential Market)**

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

**Definition: (Recursive Market Equilibrium)** The Recursive Market Equilibrium is defined as a set of price $\{\tilde q(S'|S)\}$ of consumption, a set of individual decisions $\{C, a\}$, such that:

1. Given the set of price, the individual decision variables solves the following consumer’s problem:
   $$
   v^i(a^i(S),S) = max\{U(C^i)+\beta \sum_{S'}v^i({a^i}'(S'|S),S')\pi(S'|S)\} \\
   s.t. \space C^i +\sum_{S'}\tilde q(S'|S) {a^i}'(S'|S) \leq e^i+a^i(S)\\
   {a^i}'(S'|S) \geq -\bar A
   $$
2. Markets clears, or the feasible condition holds which means:
   $$
   \sum_{i\in I}C^i = \sum_{i\in I}e^i \space for \space each \space t \space and \space S^t
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
   Note that if we divide the first order constraints of two person, we can still have the fact that the consumption of a consumer is a constant rate of the total endowment, i.e. $C_t^i(S^t) = \tilde\mu^i\sum_{i\in I}e_t^i(S^t) = \tilde\mu^iY_t(S^t)$. Hence we can rewrite the price as:
$$
   \tilde q_t(S^t,S') = \beta \frac{U'(Y_{t+1}(S^t,S'))}{U'(Y_t(S^t))}\pi(S'|S^t)
$$
2. Solve for the price:

   Note that from the Euler’s Equation, if the Sequential Market and the Arrow Debreu Market have the same solution then the price of the Arrow securities can be denoted as:
   $$
   \tilde q_t(S^t,S') = p_{t+1}^0(S^t,S')/p_t^0(S^t)
   $$
#### Relationship between Two Economies

 **Theorem: (Duality)** The Solution of the Arrow Debreu Equilibrium and the Sequential Market Equilibrium are the same.

Proof:

The detail of the standard proof is in micro note. Here we provide a different, yet much convenient poof.

First we proof that the solution of the Sequential Market Equilibrium is the solution of the Arrow-Debreu Equilibrium, by adding up all the discounted sequential budget constraints:
$$
lim_{T\to+\infty}\sum_{t=0}^{T} \sum_{S'} (\prod_{j=0}^{t-1}\tilde q_j(S^j,S^{j+1})) C_t^i(S^t) + lim_{T\to+\infty}\sum_{S'}(\prod_{j=0}^{T-1} \tilde q_t(S^j,S^{j+1})) \tilde q_T(S^T,S') a_{T+1}^i(S^T,S')\\
 = lim_{T\to+\infty}\sum_{t=0}^{T-1} \sum_{S'}  (\prod_{j=0}^{t-1}\tilde q_j(S^j,S^{j+1})) e_t^i(S^t)
$$
Since we have the No Ponzi Condition, we have $lim_{T\to+\infty}\sum_{S'}(\prod_{j=0}^{T-1} \tilde q_t(S^j,S^{j+1})) \tilde q_T(S^T,S') a_{T+1}^i(S^T,S') = 0$, and we can define $P^0_t(S^t) = \prod_{j=0}^{t-1}\tilde q_j(S^j,S^{j+1})$, and the lifetime budget constraint becomes:
$$
\sum_{t=0}^{+\infty}\sum_{S^t}P_t^0(S^t)C_t^i(S^t) \leq \sum_{t=0}^{+\infty}\sum_{S^t}P_t^0(S^t)e_t^i(S^t)
$$
Since we have exactly the same budget constraint, and the prices of the contingent claims are also the same, we will get the exact same solution, i.e. the solution to the Sequential Market Equilibrium is the solution to the Arrow Deberu Equilibrium.

However, we have already shown that the Arrow Deberu Equilibrium has an unique solution. Since we know that the Sequential Market Equilibrium has a solution, the solution has to be the same. $\square $



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
max \sum_{t=0}^{+\infty}\sum_{S^t}\sum_{i\in I}\beta^t\lambda^i U(C_t^i(S^t))\pi(S^t)
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
L =\sum_{t=0}^{+\infty}\sum_{S^t}\sum_{i\in I}\{\beta^t \lambda^i U(C_t^i(S^t))\pi(S^t) + \phi_t(S^t)(e_t^i(S^t)-C_t^i(S^t))\}
$$
The first order conditions are:
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

**Theorem: (First Welfare Theorem)** The Arrow-Deberu Equilibrium allocation is Pareto Efficient.

Proof:

Assume an alternative allocation $\{\tilde c_t^i\}$ which pareto dominates the competitive allocation $\{c_t^i\}$, then we have $u(\tilde c_t^i) \geq u(c_t^i) $ for all $i$, and there is a $j$ such that $u(\tilde c_t^j) > u(c_t^j) $. But this new allocation will cost at least the same amount of money as the competitive market solution, otherwise the consumer would get higher utilities. Hence we get $\sum_{t = 0}^\infty\sum_{S^t}p_t^0(S^t)\tilde c_t^i(S^t) \geq \sum_{t = 0}^\infty\sum_{S^t}p_t^0(S^t)c_t^i(S^t)$. similarly, we have $\sum_{t = 0}^\infty\sum_{S^t}p_t^0(S^t)\tilde c_t^j(S^t) > \sum_{t = 0}^\infty\sum_{S^t}p_t^0(S^t) c_t^j(S^t)$. Add them up and use the feasible condition for the whole economy, we end up with $\sum_{t = 0}^\infty\sum_{S^t}p_t^0(S^t)e_t^i(S^t) > \sum_{t = 0}^\infty\sum_{S^t}p_t^0(S^t)e_t^i(S^t)$, which is impossible. $\square$

**Corollary:** The Sequential Market Equilibrium allocation is Pareto Efficient.

#### Duality

**Theorem: (Second Welfare Theorem)** We can solve the Arrow-Debreu Equilibrium by solving the social planer’s problem.

Proof:

Define Total Tax of consumer $i$ as $T_i = \sum_t \sum_{S^t} (e^i_t(S^t)-C^i_t(S^t))\phi_t(S^t)/\lambda_i$. When we set $T_i = 0$, the solution to Social Planner’s problem and the Arrow Debreu Equilibrium is the same. $\square $

**Note:** Although the above theorem is not what Second Welfare Theorem says, it is related to it.



### Asset Pricing

#### Arrow-Debreu Asset Pricing

**Assumption: (Arrow-Deberu)**

- Basic Arrow-Debreu Equilibrium Setup
- Complete market, with one asset to be priced

**Definition: (Arrow-Deberu Equilibrium)** The Arrow-Deberu Equilibrium is defined as a set of price $\{\tilde q_t, P_t\}$ of consumption, a set of individual decisions $\{C^i_t(S^t), b_{t}^i(S^t)\}$, such that:

1. Given the set of price, the individual decision variables solves the following consumer’s problem:
   $$
   max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^tU(C_t^i(S^t))\pi(S^t)
   $$
   subject to the budget constraint:
   $$
   \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)(C_t^i(S^t)+P_t(S^t)b_{t+1}^i(S^t))\leq \sum_{t=0}^{+\infty}\sum_{S^t}\tilde p_t^0(S^t)(e_t^i(S^t)+(P_t(S^t)+d_t(S^t))b_{t}^i(S^{t-1}))
   $$
2. Markets clears, or the feasible condition holds which means:
   $$
   \sum_{i\in I}C_t^i(S^t) = \sum_{i\in I}e_t^i(S^t) +Bd_t(S^t) = Y_{t}(S^{t})\space for \space each \space t \space and \space S^t
   $$
   And asset market clears, i.e.
   $$
   \sum_{i\in I}b_{t+1}^i(S^t) = B
   $$

**Solution: (Asset Pricing)**

Solving this problem will give us the same First Order Conditions for the contingent claims. However, it will also give us the following Asset Pricing Equation:
$$
P_t(S^t) = \sum_{S'}\beta \frac{U'(Y_{t+1}(S^t,S'))}{U'(Y_{t}(S^t))}\pi(S'|S^t)(P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1})) \\ 
P_t(S^t) = \sum_{S'} \frac {\tilde p_{t+1}^0(S^{t+1})}{\tilde p_t^0(S^t)}(P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1})
$$
which can also be rewrite as:
$$
P_t(S^t) = \sum_{\tau =t+1}^{+\infty} E_t[ \beta^{\tau-t}\frac{U'(Y_{\tau}(S^\tau))}{U'(Y_{t}(S^t))}d_\tau(S^\tau)]+lim_{T\to+\infty}E_t[\beta^T\frac{U'(Y_{T+1}(S^T,S'))}{U'(Y_{t}(S^t))}P_{T+1}(S^{T+1})]
$$
Because of no arbitrage condition, we have $lim_{T\to+\infty}E_t[\beta^T\frac{U'(Y_{T+1}(S^T,S'))}{U'(Y_{t}(S^t))}P_{T+1}(S^{T+1})] = 0$.

#### Sequential Asset Pricing

**Assumption: (Sequential Market)**

- Basic Sequential Market
- Complete market, with one asset to be priced, which is also called the Lucas Tree

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
   \sum_{i\in I}C_t^i(S^t) = \sum_{i\in I}e_t^i(S^t) +Bd_t(S^t) = Y_{t}(S^{t})\space for \space each \space t \space and \space S^t
   $$
   And asset market clears, i.e.
   $$
   \sum_{i\in I}b_{t+1}^i(S^t) = B
   $$

**Solution: (Asset Pricing)**

Solving this problem will give us the same Asset Pricing Equation, which can be rewrite as:
$$
P_t(S^t) = \sum_{S'} \tilde q_t(S^t,S')(P_{t+1}(S^{t+1})+d_{t+1}(S^{t+1})\\
P_t(S^t) = \sum_{\tau =t+1}^{+\infty}E_t[\beta^{\tau-t}\frac{U'(Y_{\tau}(S^\tau))}{U'(Y_{t}(S^t))}d_\tau(S^\tau)] + lim_{T\to+\infty}E_t[\beta^T\frac{U'(Y_{T+1}(S^T,S'))}{U'(Y_{t}(S^t))}P_{T+1}(S^{T+1})]
$$
Because of no arbitrage condition, we have $lim_{T\to+\infty}E_t[\beta^T\frac{U'(Y_{T+1}(S^T,S'))}{U'(Y_{t}(S^t))}P_{T+1}(S^{T+1})] = 0$.



### Neoclassical Growth Model and Rational Expectation

**Assumption: (Setup)**

- Representative agent for the household
- Representative firm, aggregate shock in technology
- Competitive market, free entry leading to zero profit at equilibrium

**Definition: (Household’s Sequential Problem)** A Neoclassical Growth Model Household’s problem is:
$$
max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^tU(c_t(S^t))\pi(S^t) \\
s.t. \space c_t(S^t) +k_{t+1}(S^{t}) \leq w_t(z_t, \tilde K_t) n_t+r_t(z_t, \tilde K_t)k_t(S^{t-1}) +(1-\delta)k_t(S^{t-1}) + D_t \\
\tilde K_{t+1} = H(\tilde K_{t}, z_t ,z_{t+1})\\
k_t(S^t) \geq 0 , \space k_{t+1}(S^{t+1}) \geq0,\space n_t = 1,\space D_t = 0
$$
where $\tilde K_{t+1} = H(\tilde K_{t}, z_t ,z_{t+1})$ is the perceived law of motion of aggregate capital.

**Definition: (Household’s Recursive Problem)** A Neoclassical Growth Model Household’s problem can also be written as:
$$
V(k,z,\tilde K) = max \{U(c)+\beta \sum_{z'}V(k',z',\tilde K')\pi(z'|z) \\s.t. \space c +k' \leq w(z,\tilde K) +(r(z,\tilde K) +1-\delta)k \\\tilde K' = H(\tilde K, z ,z')\\c \geq 0 , \space k' \geq0
$$
where $\tilde K' = H(\tilde K, z ,z')$ is the perceived law of motion of aggregate capital.

**Note:** The recursive form of the problem is equivalent to the sequential form of the problem.

**Definition: (Firm’s Problem)** A Neoclassical Growth Model Firm’s problem is:
$$
D_t = max_{K_t,N_t} \{z_tF(K_t,N_t) - w_t N_t - r_t K_t\}
$$
**Definition: (Neoclassical Growth Model)** The Neoclassical Growth Model in this problem is defined as a set of price $\{r_t, w_t\}$, a set of individual decisions $\{c_t^i, k_t^i\}$ for each individual consumer $i \in I$, and a set of aggregate variables $\{C_t, K_t\}$ such that:

1. Given the set of price and the set of aggregate variables, the individual decision variables solves the consumer’s problem.

2. Given the price, the aggregate variables solve the firm’s problem.

3. Markets clears, which means:
   $$
   C_t+K_{t+1}  =z_tF(K_t,1)+(1-\delta)K_t\\C_t = c_t,\space K_t = k_t,\space and\space N_t = n_t
   $$
4. The true law of motion of the distribution is consistent with the solution to the consumer’s problem, i.e. $K_{t+1} = H(K_{t}, z_t ,z_{t+1})$.

**Solution: (Solve the Model by Solving the Social Planner’s Problem)**

Under Rational Expectation Condition, we have $K_{t} = \tilde K_{t}$. Since at the equilibrium we have the profit is zero, plug in the market clearing conditions we will have $z_tF(K_t,N_t) = w_tN_t + r_tK_t =  w_tn_t + r_tk_t $. So we have:
$$
max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^tU(C_t(S^t))\pi(S^t) \\
s.t. \space C_t(S^t) + K_{t+1}(S^{t}) \leq z_t F(K_t(S^{t-1}),N_t) +(1-\delta)K_t(S^{t-1})\\K_t(S^{t-1}) \geq 0 , \space K_{t+1}(S^{t}) \geq 0,\space N_t = 1
$$
Or to write in the recursive way:
$$
V(K,z) = max \{U(C)+\beta \sum_{z'}V(K',z')\pi(z'|z) \\s.t. \space C +K' \leq  zF(K,1) +(1-\delta)K \\C \geq 0 , \space K' \geq0
$$
which is just the Social Planner’s problem. Hence we can just solve it by solving the social planner’s problem.



### Complete Market with Endogenous Growth

**Assumption: (Setup)**

- Heterogeneity agents for the household, but aggregate endowment shock is zero.
- Complete market, with Arrow securities available
- Representative firm, aggregate shock in technology
- Competitive market, free entry leading to zero profit at equilibrium

**Definition: (Household’s Sequential Problem)** A Neoclassical Growth Model Household’s problem is:
$$
max \sum_{t=0}^{+\infty}\sum_{S^t}\beta^t U(c^i_t(S^t))\pi(S^t) \\
s.t. \space c^i_t(S^t) +\sum_{S'}\tilde q_t(S^t,S') a_{t+1}^i(S^t,S')+k^i_{t+1}(S^{t}) \\
\leq e_t^i(S^t)+ a_{t}^i(S^{t-1},S_t)+ w_t(z_t, \tilde K_t) n^i_t+r_t(z_t, \tilde K_t)k^i_t(S^{t-1}) +(1-\delta)k^i_t(S^{t-1}) + D_t k^i_t(S^{t-1}) / K_t^i(S^{t-1})\\
\tilde K_{t+1} = H(\tilde K_{t}, z_t ,z_{t+1})\\
k^i_t(S^{t-1}) \geq 0 , \space k^i_{t+1}(S^{t}) \geq0, \space a' \geq -\bar A, \space n^i_t = 1,\space D_t = 0
$$
where $\tilde K_{t+1} = H(\tilde K_{t}, z_t ,z_{t+1})$ is the perceived law of motion of aggregate capital.

**Definition: (Household’s Recursive Problem)** A Neoclassical Growth Model Household’s problem can also be written as:
$$
V(a,k,e,z,\tilde K) = max \{U(c)+\beta \sum_{e',z'}V(a',k',e',z',\tilde K')\pi(e',z'|e,z) \\
s.t. \space c +\sum_{e',z'}\tilde q(e',z'|e,z) a'(e',z'|e,z)+k' \leq e +a(e,z)+ w(z,\tilde K) +(r(z,\tilde K) +1-\delta)k \\
\tilde K' = H(\tilde K, z ,z')\\
c \geq 0 , \space k' \geq 0, \space a' \geq -\bar A
$$
where $\tilde K' = H(\tilde K, z ,z')$ is the perceived law of motion of aggregate capital.

**Note:** The recursive form of the problem is equivalent to the sequential form of the problem.

**Definition: (Firm’s Problem)** A Neoclassical Growth Model Firm’s problem is:
$$
D_t = max_{K_t,N_t} \{z_tF(K_t,N_t) - w_t N_t - r_t K_t\}
$$
**Definition: (Neoclassical Growth Model)** The Neoclassical Growth Model in this problem is defined as a set of price $\{r_t, w_t\}$, a set of individual decisions $\{c_t^i, a_t^i, k_t^i\}$ for each individual consumer $i \in I$, and a set of aggregate variables $\{C_t, K_t\}$ such that:

1. Given the set of price and the set of aggregate variables, the individual decision variables solves the consumer’s problem.

2. Given the price, the aggregate variables solve the firm’s problem.

3. Markets clears, which means:
   $$
   C_t+K_{t+1}  =z_tF(K_t,1)+(1-\delta)K_t\\C_t = \int_0^1c_t^i di,\space K_t = \int_0^1 k_t^i di,\space A_t = \int_0^1 a_t^i di = 0,\space and\space N_t = \int_0^1 n_t^i di
   $$
4. The true law of motion of the distribution is consistent with the solution to the consumer’s problem, i.e. $K_{t+1} = H(K_{t}, z_t ,z_{t+1})$.

**Solution: (Aggregate Solution)**

Under Rational Expectation Condition, we have $K_{t} = \tilde K_{t}$. Then the recursive problem of the consumer can be rewrite as:
$$
V(a,k,e,z,K) = max \{U(c)+\beta \sum_{e',z'}V(a',k',e',z',K')\pi(e',z'|e,z) \\
s.t. \space c +\sum_{e',z'}\tilde q(e',z'|e,z) a'(e',z'|e,z)+k' \leq e +a(e,z)+ w(z,K) +(r(z,K) +1-\delta)k \\
c \geq 0 , \space k' \geq 0, \space a' \geq -\bar A
$$
Solving the Euler Equation of the individual consumer’s problem, we will get:
$$
U'(c_t^i(S^t)) = E_t[\beta U'(c_{t+1}^i(S^{t+1}))(r_{t+1}(z_{t+1},K_{t+1}))+1-\delta)]
$$
Now Take the first order condition of $a$, we will get $\tilde q_t(S^t,S'){U'(C_t^i(S^t))} = \beta {U'(C_{t+1}^i(S^t,S'))}\pi(S'|S^t)$, Since different agents are facing the same Arrow securities, we have $\frac{U'(C_t^i(S^t))}{U'(C_t^j(S^t))} = \frac{U'(C_{t+1}^i(S^t,S'))}{U'(C_{t+1}^j(S^t,S'))}$, which means each person is consuming a constant amount of total consumption. Assume that the utility is homogenous, we can rewrite the above equation as:
$$
U'(C_t(z_{t},K_{t}))) = E_t[\beta U'(C_{t+1}(z_{t+1},K_{t+1}))(r_{t+1}(z_{t+1},K_{t+1}))+1-\delta)]
$$
and we can get $r_{t+1}(z_{t+1},K_{t+1})$ from the first order conditions of the firm: 
$$
r_t(z_t, K_t) = z_tF_K(K_t,1)
$$
Combine these two equations with the market clearing condition:
$$
C_t+K_{t+1}  =z_tF(K_t,1)+(1-\delta)K_t
$$
 From the above three equations we can get a system of law of motion of $\{C_t, K_t, r_t\}$,  which are all aggregate variables. In this model, since we have complete market, the distribution of people’s wealth doesn’t matter. The individual’s behavior is nondetermined.



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
- Focus on steady state
- $Prob(n_{t+1}| n_t) = \pi(n_{t+1}|n_t)$

#### Competitive Equilibrium

**Definition: (Recursive Competitive Equilibrium)** The Recursive Competitive Equilibrium at the steady state in this problem is defined as a set of price of the bond $\{q\}$, a set of individual decisions $\{c^i, a^i\}$ and a set of aggregate variables $\{C, \mu\}$, where $\mu(a, y)$ is the joint distribution of $a$ and $y$, such that:

1. Given the set of price and the set of aggregate variables, the individual decision variables solve the following consumer’s problem:
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
   Since we are solving the steady state equilibrium, the bond price does not change, the consumer in the model would just use $q' = q$ to forecast the bond price in next period. 
2. Markets clear, which means:
   $$
   C = \sum_a\sum_yy\mu(a,y),\space A = \sum_a\sum_ya\mu(a,y)=0
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
2. For value $q^j$, and solve for the consumer’s recursive problem, and it will give back policy functions $a' = g(a, y, q^j)$ and $c = g_c(a, y, q^j)$.
   Note the consumer has a borrowing constraint, which means the solution goes in the following way:
   $$
   L = U(a+y-q^ja')+\beta\sum_{y'}V(a',y',q^j)\pi(y'|y)+\lambda(a'+\bar  A)
   $$
   Derive the Euler Equation:
   $$
   (ENV)\space V'(a,y,q^0) = U'(c) \\
   (FOC)\space -q^jU'(c)+\beta \sum_{y'}V'(a',y',q)\pi(y'|y)+\lambda=0
   $$

   and it will give the solution as:
   $$
   a' = -\bar A, \space and \space if \space a’>-\bar A, \space q^0 U'(c) = \beta\sum_{y'}U'(c')\pi(y'|y)
   $$

3. Use the true law of motion $\mu(a',y') = \sum_a\sum_y 1_{a'=g(a,y,q^j)}\pi(y'|y)\mu(a,y)$  and try to calculate a steady distribution $\mu(a,y|r^j)$
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
- Focus on steady state
- $Prob(n_{t+1}| n_t) = \pi(n_{t+1}|n_t)$

#### Competitive Equilibrium

**Definition: (Recursive Competitive Equilibrium)** The Recursive Competitive Equilibrium at the steady state in this problem is defined as a set of price $\{r, w\}$, a set of individual decisions $\{c^i, k^i\}$ and a set of aggregate variables $\{C, K, \mu\}$, where $\mu(k, n)$ is the joint distribution of $k$ and $n$, such that:

1. Given the set of price and the set of aggregate variables, the individual decision variables solve the following consumer’s problem:
   $$
   V(k^i, n^i, r ) = max\{U(c^i)+\beta\sum_{{n^{i}}'} V({k^i}', {n^{i}}', r' ) \pi({n^{i}}'|{n^{i}})\}
   $$
   subject to the budget constraint:
   $$
   c^i + {k^i}' \leq (r+1-\delta)k^i+wn^i
   $$
   and the perceived law of motion of the interest rate in next period:
   $$
   r' = H(r) = r
   $$
Since we are solving the steady state equilibrium, the interest rate of capital does not change, the consumer in the model would just use $r' = r$ to forecast the interest rate in next period. 

2. Given the price, the aggregate variables solve the firm’s problem:
   $$
   D = max\{K^\alpha N^{1-\alpha} - rK - wN\}
   $$
3. Markets clears, which means:
   $$
   C = K^\alpha N^{1-\alpha} -\delta K
   \\
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
2. For value  $r^j$, and solve for the consumer’s recursive problem, and combine the solution to the firm’s First Order Conditions $w(r)$. This will give back policy functions $k' = g(k, n, r^j)$ and  $c = g_c(k, n, r^j)$
3. Use the true law of motion $\mu(k',n') = \sum_k\sum_n 1_{k'=g(k,n,r^j)}\pi(n'|n)\mu(k,n)$  and try to calculate a steady distribution $\mu(k,n|r^j)$
4. Get the aggregate capital by $K(r^j) = \sum_k\sum_ng(k,n,r^j)\mu(k,n|r^j)$ , calculate all the other aggregate variables similarly
5. Calculate the excess supply, $z(r^j) = K(r^j)^\alpha N^{1-\alpha} -\sum_k\sum_ng_c(k, n, r^j)\mu(k,n) - \delta K(r^j)$
6. If $z(r^j)>0$, it means the excess aggregate supply is too high, which means the firm will produce less in the next period, so the demand of capital will decrease, which means we should set $r^{j+1} <r^j$, and vice versa
7. Iterate from step 2, until $|z(r^j)-z(r^{j+1})| < \epsilon$



### Krusell-Smith Model

#### Setup

**Assumption: (The Household)**

- A continuum of households
- Heterogenetic household  with no aggregate endowment risk
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

1. Given the set of price and the set of aggregate variables, the individual decision variables solve the following consumer’s problem:
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

**Note:** The consumers need to forecast the distribution of the the capital in the next period only because they need to predict the aggregate capital in the next period.

**Note:** One way to solve this problem is instead of forecasting the full distribution, forecasting the moments of the distribution. One simple approximation of the forecasting model is to use only the first order of moments to approximate, i.e. $ln K_{t+1} = a_z+b_zlogK_t$.

#### Solution

**Solution: (Quantitative Method)**

1. Pick the initial value of $\{a_z^0, b_z^0\}$

2. For value  $\{a_z^j, b_z^j\}$, plug into the perceived law of motion $ln \tilde K_{t+1} = a_z^j+b_z^jlog\tilde K_t$, and solve for the following problem:
   $$
   V(k_t^i, n_t^i, z_t, \tilde K_t ) = max\{U(c_t^i)+\beta\sum_{n_{t+1}^i}\sum_{z_{t+1}} V(k_{t+1}^i, n_{t+1}^i, z_{t+1}, \tilde K_{t+1} ) \pi(n_{t+1}^i,z_{t+1}|n_t^i, z_t)\}
   $$
   subject to
   $$
   c_t^i + k_{t+1}^i \leq (r_t+1-\delta)k_t^i+w_tn_t^i
   $$

   $$
   ln \tilde K_{t+1} = a_z^j+b_z^jln\tilde K_t
   $$
   This is equivalent to solve the consumer’s problem. Solving this recursive problem, and combining the solution to the firm’s First Order Condition, $w(r)$, will give back the policy functions $k_{t+1}^i = g(k_t^i, n_t^i, z_t, \tilde K_t )$

3. Starting from a set of initial points $\{ k_0^i, n_0^i, z_0, \tilde K_0 \}$, use the individual decision rules, simulate a panel of technology shock and labor endowment, and use that to generate a panel of individual capital stocks $\{k_{t+1}^i\}_{t=0}^T$, and use the panel to generate $K_t = \frac{1}{I}\sum_i k_t^i$

4. Run a regression of $lnK_{t+1} = a_z'+b_z'lnK_t+e_t$, and get $\{a_z^j, b_z^j\}$

5. Set $a_z^{j+1} = a_z' $, and $b_z^{j+1} = b_z' $, and iterate from step 2, until $||(a_z^j,b_z^j) - (a_z^{j+1},b_z^{j+1})|| < \epsilon$



## Overlapping Generation

### Diamond’s Model

#### Setup

**Assumption: (Setup)**

- Different generations of agents alive
- Agents live for 2 periods, young and old
- Agents work and save in the first period, and retire in the second period
- Each individual provide one unit of labor
- Population growth rate is $n$

**Definition: (Consumer’s problem)** The consumer solves the following problem:
$$
   max \{U(C_{1,t})+\beta U(C_{2,t+1})\} \\
   s.t. \space C_{1,t}+S_t = W_t\\
   C_{2,t+1} = (1+r_{t+1})S_t
$$
where $C_{1,t}$ denotes the consumption of the young generation in period $t$, and  $C_{1,t+1}$ denotes the consumption of the old generation in period $t+1$.

**Definition: (Firm’s problem)** The firm solves the following problem:
$$
   max \{F(K_t,N_t) - r_tK_t-W_tN_t\} = N_t(f(k_t)-r_tk_t-W_t)
$$
**Definition: (OLG Equilibrium)** An OLG Equilibrium is defined as a set of price $\{r_t, W_t\}$ and endogenous variables $\{C_t, K_t, S_t\}$ such that:

1. Given the price, the endogenous variables solve the consumer’s problem.

2. Given the price, the endogenous variables solve the firm’s problem.

3. Market clears, i.e.
   $$
   C_{1,t}N_t+C_{2,t}N_{t-1} +S_tN_t = F(K_t,N_t)+K_t, \space S_tN_t = K_{t+1}, \space N_{t+1} = (1+n)N_t
   $$
#### Solution

**Solution: (OLG)**

1. First we solve the first order condition of the firm. We will get: $F_K(K_t,N_t) = r_t$ and $F_N(K_t,N_t) = W_t$. Note that $F$ is a homogenous of degree 1 function, hence we have $f'(k_t) = r_t$ and since we are in a competitive market at the equilibrium the profit is zero, we have $f(k_t)-f'(k_t)k_t=W_t$

2. Now solve the consumer’s problem, we have first order conditions:
   $$
   U'(C_{1,t}) = \beta(1+r_{t+1})U'(C_{2,t+1})\\
   U'(W_t-S_t) = \beta(1+r_{t+1})U'((1+r_{t+1})S_t)
   $$
   Plug in the wage and interest rate from step 1, we have:
   $$
   U'(f(k_t)-f'(k_t)k_t-S_t) = \beta(1+f'(k_{t+1}))U'((1+f'(k_{t+1}))S_t)
   $$

3. Now combine with the capital aggregation equation $N_tS_t = K_{t+1}$, hence $S_t = (1+n)k_{t+1}$, we can derive the law of motion of capital per capita:
   $$
   U'(f(k_t)-f'(k_t)k_t-(1+n)k_{t+1}) = \beta(1+f'(k_{t+1}))U'((1+f'(k_{t+1}))(1+n)k_{t+1})
   $$
   This implies that we have different possibilities of converging equilibria.



### Pareto Efficiency

**Definition: (Social Planner’s Problem)** A social Planner’s Problem solves the following:
$$
max \{\beta U(C_{2,0})+\sum_{t=0}^{+\infty} \tilde \beta ^{t-1} [U(C_{1,t})+\beta U(C_{2,t+1})]\} \\
s.t. \space C_{1,t}N_t+C_{2,t}N_{t-1} + K_{t+1} = F(K_t,N_t) +K_t
$$
**Solution: (Social Planner’s Problem)**

First we detrend the problem to $C_{1,t}+C_{2,t}/(1+n) + (1+n)k_{t+1} = f(k_t)+k_t$. Then take the Lagrange function of the problem: $\sum_{t=0}^{+\infty} \tilde \beta ^{t-1} [U(C_{1,t})+\beta U(C_{2,t+1}) +\lambda_t(f(k_t)+k_t-C_{1,t}-C_{2,t}/(1+n) - (1+n)k_{t+1}]$.

We have the first order condition: $U'(C_{1,t}) = \lambda_t, \beta U'(C_{2,t+1}) = 1/(1+n)\lambda_{t+1}\tilde \beta$ and $(1+n)\lambda_t = \tilde \beta \lambda_{t+1}(f'(k_t)+1)$. which will give us the law of motion of $k_t$.

**Note:** The market equilibrium does not necessarily deliver the pareto optimal solution.