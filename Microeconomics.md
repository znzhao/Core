# MICRO ECONOMICS

## Content

[TOC]

## Preference Theory

### Preference

### Axiom

### Utility Function

## Consumer Theory

### Utility Maximization

### Indirect Utility Function

### Expenditure Minimization

### Expenditure Function

### Duality

### Demand Function

### Comparative Statics and Slutsky Equation

### Integrability

### Revealed Preference

## Uncertainty

### Axiom

### Expected Utility Property

### Risk Aversion

### Comparing Gamble

### Anscombe-Aumann Structure

### Mixture Space Theorem

### State Dependence and Expected Utility

## Production Theory

### Production Set

### Production Function

### Transformation Function

### Cost Minimization

### Profit Maximization

### Short Run and Long Run Problem

### Multi Product Firms

## Walrasian Equilibrium

### Barter Exchange Economy

#### Setup

**Assumption: (Setup)**

- No production, an endowment economy
- Society admits to the institution of private ownership
- Principle of voluntary and non-coercive trade is respected

**Assumption: (Consumers’ Behavior)** Agents have complete, transitive, continuous, and strictly convex preference over bundles in $\R^n_+$.

**Definition: (Barter Exchange Economy)** An Exchange Economy is defined as:

1. Agents $I  = \{1,2,...,I\}$
2. $\Epsilon = (\succsim_i, e^i)_{i\in I}$ defines an exchange economy
3. Allocation defined as $x = (x^1,...x^I)$
4. Feasible Set defined as $F(e) = \{\sum_{i\in I} x^i= \sum_{i\in I} e^i \}$

**Definition: (Edgeworth Box)** With 2 consumers and 2 goods in the economy, the Edgeworth box is a rectangular diagram with one consumer's origin on one corner, the other's origin on the opposite corner. The width of the box is the total amount of one good, and the height is the total amount of the other good.

**Definition: (Contract Curve)** With 2 consumers and 2 goods in the economy, the Contract Curve is the subset of allocations where the consumers’ indifference curves through the point are tangent to each other.

**Note:** Anything on the contract curve and inside the lens is a Barter Exchange Equilibrium.

**Definition: (Individual Rationality)** A feasible allocation is Individually Rational if $x^i \succsim e^i$ for any $i$.

#### Excess Demand

**Definition: (Consumer’s Problem)** Consumer $i$ choose $x^i$ to solve:
$$
max_{x\in \R^n_+}U^i(x) \space s.t.px = pe^i
$$
**Note:** Under the normal assumption, this problem has a unique solution given price vector.

**Definition: (Excess Demand)** Define the excess demand for good k as $z_k(p) = \sum_{i\in I} x_k^i(p,pe^i) - \sum_{i\in I}e_k^i$ at price $p \gg 0$.

**Definition: (Aggregate Excess Demand)** Define the aggregate excess demand as $z(p) = (z_1(p),...,z_n(p))$ at price $p \gg 0$.

#### Properties of Excess Demand

**Assumption: (Excess Demand)** The utility functions are continuous, strictly increasing and strictly quasi-concave on $\R^n_+$.

**Theorem: (Properties of Excess Demand)** Under the above assumption about consumer behavior, we have:

1. $z(p)$ is continuous on $\R^n_+$
2. $z(p)$ is homogenous of degree zero at $p$
3. (Walras Law) $pz(p) = 0\space \forall p\gg 0$, i.e. the value of excess demand is always zero.

Proof:

Continuity follows from continuity of individual demand functions. Homogeneity follows from the individual budget constraint. Now try to prove Walras Law. The budget constraint of each individual can be rewrite as:
$$
\sum_{k = 1}^n p_k[x_k^i(p,pe^i) - e_k^i] = 0
$$
Summing over $i$, we get:
$$
\sum_{i =1}^n \sum_{k = 1}^n p_k[x_k^i(p,pe^i) - e_k^i] = 0
$$
If we change the order of summation, we get:
$$
\sum_{k = 1}^np_k[\sum_{i =1}^n x_k^i(p,pe^i) -\sum_{i =1}^n  e_k^i] =  \sum_{k = 1}^np_kz_k(p) = pz(p) = 0
$$
which is what we want to show. $\square$

**Corollary: (Walras Law)** If there are $n$ markets in total and $n-1$ markets clear, then the last market clears, too.

**Assumption: (Consumer’s Behavior)** The utility functions are continuous, strongly increasing and strictly quasi-concave on $\R^n_+$.

**Theorem: (Utility and Aggregate Demand)** If each consumer’s utility satisfies the assumption above, and if the aggregate endowment of each good is positive, then the aggregate excess demand satisfies the following properties:

1. $z(p)$ is continuous on $\R^n_+$
2. $pz(p) = 0\space \forall p\gg 0$
3. If $\{p^m\}$ is a sequence of price vectors in $\R^n_+$ converging to $\bar p \ne 0$, and $\bar p_k = 0$ for some $k$, then for some good $k’$ with $\bar p_k' = 0$ the associated sequence of excess demands for good $k'$ at any price in that sequence, $\{z_{k’}(p^m)\}$, is unbounded above. 

Proof:

Continuity follows from the continuity of individual demands. Walras Law follows from the individual budget constraint. We only need to show the third property.

Suppose $\bar p$ is a price vector such that $p_k = 0$, we need to find a $k'$ such that property 3 is true. We are going to argue with contradiction. Take a sequence of price vectors $p^m \to \bar p$, suppose that the aggregate excess demand $\{z_{k’}(p^m)\}$ is bounded, then demand $x^{i,m} (p^m, e^i p^m)$ for individual $i$ is bounded. Then there is a converging subsequence $x^{i,m_j} \to x^{i*}$.

Now construct another allocation $\hat x^i$ such that $\hat x^i_r = x^{i*}_r$ for $r \neq k$ and  $\hat x^i_k = x^{i*}_k+1$. Then $\bar p \hat x^{i} =\bar p x^{i*} = \bar p e^{i}>0$. But since the utility is strongly increasing, we have $u^i(\hat x^i)>u^i(x^{i*})$.

Now because $u^i$ is continuous, there exist a $t \in(0,1)$, such that $u^i(t\hat x^i)>u^i(x^{i*})$ and $\bar p t\hat x^{i} <\bar p x^{i*} = \bar p e^{i}$. Then because as $p^m \to \bar p$, $x^{i,m_j} \to x^{i*}$, there exist a $m$ such that $u^i(t\hat x^i)>u^i(x^{i,m} (p^m, e^i p^m))$ and $p^m t\hat x^{i} <p^m e^{i}$, which is a contradiction to the fact that $x^{i,m} (p^m, e^i p^m)$ is the solution to the maximizing problem of the consumer. $\square$



### Existence of Equilibrium

**Definition: (Walrasian Equilibrium)** a vector $p^* \in \R^n_+$ is called a Walrasian Equilibrium if $z(p^*) = 0$.

**Lemma: (Brower’s Fixed Point Theorem)** If $f:S \to S$ is a continuous function mapping from a non-empty, compact and convex subset of $\R^n_+$ to itself, then there is a fixed point $x^*\in S$ such that $f(x^*) = x^*$.

**Theorem: (Aggregate Excess and Walrasian Equilibrium)** Suppose $z(p)$ has the following properties:

1. $z(p)$ is continuous on $\R^n_+$
2. $pz(p) = 0\space \forall p\gg 0$
3. If $\{p^m\}$ is a sequence of price vectors in $\R^n_+$ converging to $\bar p \ne 0$, and $\bar p_k = 0$ for some $k$, then for some good $k’$ with $\bar p_k' = 0$ the associated sequence of excess demands for good $k'$ , $\{z_{k’}(p^m)\}$, is unbounded above as $p^m\to \bar p$

Then there is a price vector $p^* \gg 0$ such that $z(p^*) = 0$, i.e. the Walrasian Equilibrium exists.

Proof:

1. For every $k$, let $\bar z_k(p) = min(z_k(p),1) \space \forall p\gg 0$, and let $\bar z(p) = (\bar z_1(p), ..., \bar z_n(p) )$. By definition, $\bar z(p) $ is bounded above by 1. Now define:
   $$
   S_\epsilon = \{p|\sum_{k = 1}^n p_k =1 \space and \space p_k \geq \frac {\epsilon}{1+2n} \space \forall k \}
   $$
   It’s easy to show that $S_\epsilon$ is closed and bounded (hence compact), convex, and non-empty. Now for every good $k$ and every $p\in S_\epsilon$, define $f_k(p)$ as follows:
   $$
   f_k(p) = \frac{\epsilon +p_k+max\{0,\bar z_k(p)\}}{n\epsilon +1 +\sum_{m =1}^nmax\{0,\bar z_m(p)\}}
   $$
   And similarly define  $f(p) = (f_1(p), ..., f_n(p) )$. Note that $f(p) $ satisfies the following properties:

   - $\sum_{k=1}^n f_k(p) = 1$ (since $\sum_{k = 1}^np_k = 1$)
   - $f_k(p) \geq \frac {\epsilon}{n\epsilon +1+ n} = \frac {\epsilon}{1+2n}$ (since $max\{0,\bar z_m(p)\} \leq 1$ and $p_k+max\{0,\bar z_k(p)\}\geq 0$)
   - $f:S_\epsilon \to S_\epsilon $ is a continuous function mapping from a non-empty, compact and convex set to itself

   By Brower’s Fixed Point Theorem, there exists a fixed point $f(p^\epsilon)  =p^\epsilon$. Hence from the definition of $f_k(p)$, we have:
   $$
   p_k^\epsilon = f_k(p^\epsilon) = \frac{\epsilon +p_k^\epsilon+max\{0,\bar z_k(p^\epsilon)\}}{n\epsilon +1 +\sum_{m =1}^nmax\{0,\bar z_m(p^\epsilon)\}}
   $$
   Hence we can rewrite it as:
   $$
   p_k^\epsilon [n\epsilon +\sum_{m =1}^nmax\{0,\bar z_m(p^\epsilon)\}] =\epsilon +max\{0,\bar z_k(p^\epsilon)\}
   $$
   which means for every $\epsilon \in (0,1)$ there is a price vector in $S_\epsilon$ satisfying the above equation. 

2. Now take a sequence of price vectors $\{p^\epsilon\}$ that satisfies the above equation, as $\epsilon $ goes to zero. Since $p^\epsilon \in S_\epsilon \space \forall \epsilon>0$, we have $p^\epsilon \in [0,1]$, which is bounded, there exists a subsequence of $\{p^\epsilon\}$ that converges to a price vector, denoted as $p^*\geq 0$.

   Note that $p^*\neq 0$ because its components add up to 1. We claim that $p^* \gg 0$. We argue with contradiction. Suppose there is a $\bar k$ such that $p_\bar k^* = 0$, by property 3 that is given to us in the first place, there is a $k'$ such that $p_{k'}^* = 0$ and when $\epsilon$ goes to zero, $z_{k’}(p^\epsilon)$ is unbounded above.

   Then $p_{k'}^\epsilon [n\epsilon +\sum_{m =1}^n max\{0,\bar z_m(p^\epsilon)\}] \leq p_{k'}^\epsilon [n\epsilon +n\}] \to 0$, but $\epsilon +max\{0,\bar z_k(p^\epsilon)\} \to 1$, which means the above equation cannot hold, which is a contradiction.

3. Now we find a price vector $p^* \gg 0$. Want to show that $z(p^*) = 0$.

   Note that as $\epsilon\to 0$, the above equation becomes:
   $$
   p_k^* \sum_{m =1}^nmax\{0,\bar z_m(p^*)\} = max\{0,\bar z_k(p^*)\}
   $$
   Multiply both sides by $z_k(p^*)$ and sum over $k$, we get:
   $$
   0 = p^* z(p^*)\sum_{m =1}^nmax\{0,\bar z_m(p^*)\} = \sum_{k =1}^nz_k(p^*) max\{0,\bar z_k(p^*)\}
   $$
   by Walras Law (property 2), we have $p^* z(p^*) = 0$. To summary we have:
   $$
   \sum_{k =1}^nz_k(p^*) max\{0,\bar z_k(p^*)\}=\sum_{k =1}^nz_k(p^*) max\{0,min\{1,  z_k(p^*)\}\} = 0
   $$
   Suppose for some $k$, we have $z_k(p^*) > 0$, then $\bar z_k(p^*) > 0$ and hence $z_k(p^*)\bar z_k(p^*) > 0$, which means the above equation cannot hold. Hence $z_k(p^*) \leq 0$ for all $k$.

   Now remember the Walras Law, $\sum_{k=1}^n p^*_kz_k(p^*) = 0$ we conclude that $z_k(p^*) = 0$ for all $k$, i.e. $z(p^*) = 0$. $\square$

Corollary: (Existence of Equilibrium) The Walrasian Equilibrium exists.



### Production Equilibrium (Read the book)

#### Setup

**Assumption: (Setup)**

- There are firms in the economy
- Profit must be distributed
- $\sum_i\theta_{ij} =1$ denote the private ownership of the firm 

**Assumption: (Firm)** The firms in the model satisfy the following assumptions:

1. (Nonnegative Profits) $0\in Y^j \subset\R^n$
2. (Inputs are required, imposing continuity) $Y^j$ is closed and bounded
3. (Convexity) $Y^j$ is strictly convex, ruling out constant or increasing return to scale technology, and guarantees the existence of profit maximizing solutions.

 **Definition: (Firm’s Problem)** Firm $j$ solves the following problem:
$$
\pi^j(p) = max_{y^j\in Y^j}p y^j
$$
**Note:** Under the assumption above, for any given price vector $p\gg0$ the solution of the problem is unique, denoted by $y^j(p)$, which is continuous on $\R^n_+$ and the profit function $\pi^j(p) = py^j(p)$ is well defined.

#### Aggregate Supply

**Definition: (Aggregate Production Possibility)** Define the Aggregate Production Possibility Set as $Y = {y|y = \sum_{j\in J}y^j}$.

**Note:** if $\forall j$, $y^j$ satisfies the assumption above, then so will $Y$. Condition 1 and 3 follow directly from the corresponding properties of $y^j$. The closeness follows too only when boundedness is true.

**Theorem: (Aggregate Profit Maximization)** For any price $p\gg 0$, we have $p\bar y \geq py \space \forall y$ if and only if for some $\bar y^j \in Y^j$, we may write $\bar y = \sum_{j\in J}\bar y^j$.

Proof:

1. Take $\bar y \in Y$ that will maximize the aggregate profits, suppose $\bar y = \sum_{j\in J}\bar y^j$ and for some firm $k$, $\bar y^j$ does not maximize firm $k$’s profit. Then there is another $\tilde y^k \in Y^k$ such that  $p\tilde y^k \geq p\bar y^k$, but then the summation of the profit will be $p(\sum_{j\neq k }\bar y^j+\tilde y^j) \geq  p\sum_{j\in J}\bar y^j$, which is a contradiction.
2. Suppose $\{\bar y^j\}$ maximize each firm’s profit, then take the summation we have $p\bar y \geq py \space \forall y$. $\square$

#### Aggregate Demand

**Assumption: (Consumers’ Behavior)** Agents have complete, transitive, continuous, and strictly convex preference over bundles in $\R^n_+$.

**Definition: (Consumer’s Problem)** Consumer $i$ choose $x^i$ to solve:
$$
max_{x\in \R^n_+}U^i(x) \space s.t.px = pe^i + \sum_{j =1}^J \theta_{ij}\pi_j(p)
$$
Note: If $y^j$ and $u^i$ satisfies the assumptions above, then the solution of the consumer exists and is unique for $p\gg 0$. Plus, $x^i(p,m^i(p))$ is contimuous in $p$ and $m^i(p)$ is also contimuous.

#### Existence of the Equilibrium

**Definition: (Walrasian Equilibrium)** a vector $p^* \in \R^n_+$ is called a Walrasian Equilibrium if 
$$
z(p^*) = \sum_{i\in I}(x^i(p^*)-e^i) - \sum_{j\in J} y^j(p^*)= 0
$$
**Theorem: (Existance of The Equilbrium)** Consider the economy $(u^i,e^i,\theta^{ij},y^j)$ with $i\in I$ and $j\in J$. If All the assuptions are satisfied, and $y+\sum_{i\in I }ei \gg 0$ for some production vector $y \in \sum_{j\in J}y^j$, then there exists at least one price vector $p^*\gg 0$ such that $z(p^*) =0$.

Proof:

We will verify that $z(p)$ satisfies the three properties of the Equilibrium Existance Theorem.

1. $z(p)$ is continuous because of the continuity of the individual demand function and supply fuction.

2. Walras Law is still true because of budget balanceness.

3. We want to show that if $p^m \to \bar p $,  and $\exist k$, such that $\bar p_k = 0$, then  $\exist k'$ with  $\bar p_{k'} = 0$, such that the excess demand of $k'$, $z_{k'}(p^m)$  is unbounded as $p^m \to p^*$.

   If there is some consumers with strictly positive income at the limit price $\bar p$, then this person’s income will remain to be positive at $p^m$ as $p^m \to p^*$ due to the fact that $m^i(p)$ is contimuous. This person’s demand for good $k$ will be unbounded above as  $p_k^m \to 0 $.

   Hence it suffices to show that there is some consumers with strictly positive price at the limit price $\bar p$. 
   
   Because $y+\sum_{i\in I }ei \gg 0$, for some $y$ we have $\bar p(y+\sum_{i\in I }ei) > 0$. Consider the sum of consumer’s budget constraint:
   $$
   \sum_{i\in I }m^i(\bar p) =\bar p \sum_{i\in I } e^i +\sum_{i\in I } \sum_{j =1}^J \theta_{ij}\pi_j(p) = \bar p \sum_{i\in I } e^i + \sum_{j =1}^J (\sum_{i\in I }\theta_{ij})\pi_j(p)\\
   = \bar p \sum_{i\in I } e^i + \sum_{j =1}^J \pi_j(p) = \bar p (\sum_{i\in I } e^i +y) >0
   $$
   So there is some person that has strictly positive income, otherwise the above equation would not hold. $\square$



## Welfare Theorem

### Pareto Optimality

#### Pareto Optimality In Barter Economy

**Definition: (Pareto Optimality)** A feasible allocation $x\in F(e)$ is Pareto Efficient if there is no other feasible allocation  such that $y^i \succsim_i x^i$ for all $i$, and there exists a $j$ such that $y^j \succ_j x^j$.

**Definition: (Blocking Coalition)** Let $S\subset I$ be a coalition of consumers, We say $S$ blocks allocation $x$ if there is another allocation $y$ such that

1. $\sum_{i\in S}y^i=\sum_{i\in S} e^i$
2. $y^i \succsim_i x^i\space \forall i\in S$ and $\exist j\in S$ such that $y^j \succ_j x^j$

**Theorem: (Efficiency of Unblocked Allocation)** Any unblocked allocation is Pareto Optimal.

Proof:

Suppose not. Then the allocation is not Pareto Optimal, so there is is another feasible allocation $y$ such that $y^i \succsim_i x^i\space \forall i\in I$ and $\exist j\in I$ such that $y^j \succ_j x^j$, which means $I$ is blocked by itself. $\square $

**Note:** Not all Pareto Optimal allocations are unblocked.

**Definition: (Core)** The Core of an exchange economy, denoted as $ \mathcal{C}(e)$, is the set of all unblocked feasible allocations.

#### Pareto Optimality In Production Economy

**Definition: (Feasible Allocation)** An allocation $(x,y)$ is feasible if $\sum_{i\in I} x^i \leq \sum_{i\in I} e^i + \sum_{j\in J} y^j$.

**Definition: (Pareto Optimality)** A feasible allocation $x\in F(e)$ is Pareto Efficient if there is no other feasible allocation  such that $y^i \succsim_i x^i$ for all $i$, and there exists a $j$ such that $y^j \succ_j x^j$.

**Definition: (Utility Possibility Set)** The Utility Possibility Set is defined as $U(x) = \{u_i\}_{i\in I }$ and $x$ is feasible, i.e.
$$
U = \{(\bar u_1,..., \bar u_I)\in \R^I|u_i(x^i)\geq \bar u_i \space \forall i\in I \space \& \space x \space feasible \}
$$
**Definition: (Pareto Optimality Alternative Definition)** A feasible allocation $x^*$ is Pareto Efficient if $\{\bar u\in U|\bar u \geq u^*\}$ where $u^* = (u_1(x_1^*), ..., u_I(x_I^*))$.

**Definition: (Boundary)** Let $\partial U$ denote the Boundary of the Utility Possibility Set, i.e.
$$
\partial U = \{(\bar u_1,..., \bar u_I)\in \R^I|u_i(x^i) = \bar u_i \space \forall i\in I \space \& \space x \space feasible \}
$$
**Theorem: (Pareto Optimality Alternative Definition)** A feasible allocation $x^*$ is Pareto Optimal if and only if $u^* = (u_1^*(x_1^*),..., u_I^*x(_I^*)) \in \partial U$.

Proof:

1. Let $x^*$ be a Pareto Optimal solution, suppose $u(x^*) \notin \partial U$, then there exists $\bar u \in U$ such that $\bar u > u^*$, which implies that $x^*$ is not Pareto Optimal.
2. Let $u(x^*) \in \partial U$,  suppose  $x^*$ is not Pareto Optimal, then there exists $\bar u \in U$ such that $\bar u > u^*$, then $u(x^*) \notin \partial U$, contradiction. $\square$

**Note:** $\partial U$ is a synonym of the utility frontier: $\{u\in U|\nexists u'\in U, u'>u\}$.

#### Solve for Pareto Optimality

Theorem: (Solution of Pareto Optimality) let the utility functions $u_i$, for $i\in I $, be continuous. Suppose $u_1$ is strongly increasing, then $x^*$ is Pareto Optimal if and only if it’s a solution to the following problem:
$$
max_xu_1(x^1) \space s.t.\space u_i(x^i)\geq\bar u_i \space \& \space \sum_{i\in I} x^i \leq \sum_{i\in I} e^i + \sum_{j\in J} y^j
$$
for some $(\bar u_2, ..., \bar u_i) \in U_{-1}$.

Proof:

1. Want to show that the Pareto Optimal allocation solves the problem. By definiton, if we set $u_i =  u_i^*$ for $i = 2,...,I$, then $u_1^*$ is the maximum utility we could get to give to person 1, hence it’s a solution.

2. Want to show the solution to the problem is Pareto Optimal. Let $x^*$ be the solution, suppose that is not Pareto Optimal, then there is another allocation, $\tilde x$, which is feasible and satisfiying $u_i(\tilde x^i) \geq u_i(x^{i*})$ for all $i$ and there is one $j$ such that $u_j(\tilde x^j) > u_j(x^{j*})$.

   Case 1: when  $u_1(\tilde x^1) > u_1(x^{1*})$, then automatically $x^* $ is not the solution, contradiction.

   Case 2: when $u_k(\tilde x^k) > u_1(x^{k*})$ for some $k\neq1$, and suppose  $\tilde x^k>0$. Without loss of generosity, we could assume the consumption of the first good of consumer $k$ is greater than zero, i.e. $\tilde x_1^k >0$. Now let $w\in \R^n$ be a vector with $w_1 = 1$ and $w_m = 0$ for $m = 2,...,n$, i.e. $w = (1,0,0,...0)$. by continuity of $u_k$, there is a $\epsilon >0$ such that $u_k(\tilde x^k -\epsilon w) > u_k(x^{k*})$. 

   Now consider another bundle $\hat x$, where $\hat x^1 = \tilde x^1 +\epsilon w$, $\hat x^i = \tilde x^i$ for $i\neq {1,k}$ and $\hat x^k = \tilde x^k -\epsilon w$. By strictly monotonicity, $u_1(\hat x_1) >u_1(x^*)$ and $\hat x$ is still feasible and everyone else is getting at least as good as $x^*$. So $x^*$ is not the solution, contradiction.

   Case 3: when $u_k(\tilde x^k) > u_1(x^{k*})$ for some $k\neq1$, and suppose  $\tilde x^k=0$. If $x^{k*} = 0$, then the equation before would become $u_k(0) > u_1(0)$, which is not possible. Since we know $x^{k*} \geq0$, this means the only possible case is $x^{k*} > 0$. Now we can define a new allocation $\hat x$, where $\hat x^1 = x^{1*} +x^{k*}$, $\hat x^i = x^{i*}$ for $i\neq {1,k}$ and $\hat x^k = 0$. Then by strictly monotonicity, $u_1(\hat x_1) >u_1(x^*)$ and $\hat x$ is still feasible and everyone else is getting at least as good as $x^*$. So $x^*$ is not the solution, contradiction. $\square$

### Social Planner



### First Welfare Theorem



### Second Welfare Theorem