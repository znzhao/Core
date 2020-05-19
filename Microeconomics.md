# MICROECONOMICS

## Preference Theory

### Preference

#### Order Theory

**Definition: (Binary Relation)** A Binary Relation on $X$ is a subset $R$ on $X\times X$, if $(x,y) \in R$, we write $xRy$ and $xRyRz$. 

**Definition: (Reflexivity)** A relationship is reflexive if $xRx\in R$.

**Definition: (Transitivity)** A relationship is transitive if $xRyRz \in R$ implies $xRz\in R$.

**Definition: (Completeness)** A relationship is complete if either $xRy\in R$ or $yRx\in R$.

**Definition: (Symmetry)** A relationship is symmetric if $xRy\in R$ implies $yRx\in R$.

**Definition: (Anti-Symmetry)** A relationship is anti-symmetric if $xRyRx\in R$ and implies $y=x$.

**Definition: (Preorder)** $R$ is a Preorder if $R$ is reflexive and transitive.

**Definition: (Partial Order)** R is a Partial Order if $R$ is transitive and antisymmetric.

**Definition: (Linear Order)** R is a Linear Order if $R$ is a complete partial order.

#### Preference

**Assumption: (Consumption)** The consumer has preferences over consumption bundle $X$, which is a nonempty, convex, compact subset of $\mathbb{R}^n$. $0$ is always in $X$.

**Definition: (Preference)** A Preference relation is a binary relation on the set of alternatives $X$, denoted as $"\succsim"$.

**Definition: (Strict Preference)** A Strict Preference relation is a binary relation on the set of alternatives $X$, denoted as $"\succ"$, if $x\succsim y$ but $y\nsucceq x$.

**Definition: (Indifferent Preference)** An Indifferent Preference relation is a binary relation on the set of alternatives $X$, denoted as $"\sim"$, if $x\succsim y$ and $y\succeq x$.

**Definition: (At Least As Good Set)** At Least As Good Set is defined as $\succsim(x^0) = \{x\in X, x\succsim x^0\}$.

**Definition: (No Better Than Set)** No Better Than Set is defined as $\precsim(x^0) = \{x\in X, x\precsim x^0\}$.

**Definition: (Strictly Preferred To Set)** Strictly Preferred To Set is defined as $\succ(x^0) = \{x\in X, x\succ x^0\}$.

**Definition: (Strictly Worse Set)** Strictly Worse Set is defined as $\prec(x^0) = \{x\in X, x\prec x^0\}$.

**Definition: (Indifferent Curve)** Indifferent Curve is defined as $\sim(x^0) = \{x\in X, x\sim x^0\}$.



### Axiom

**Axiom: (A1 - Completeness)** For any distinct bundles $x$ and $y$, either $x\succsim y$ or $y\succsim x$.

**Axiom: (A2 - Transitivity)** For any distinct bundles $x,y$ and $z$, $x\succsim y\succsim z$ implies $x\succsim z$.

**Lemma: (Completeness and Transitivity)** if $\succsim$ is complete and transitive, then $\succ$ and $\sim$ are also complete and transitive.

**Definition: (Rationality)** A preference is called rational if it satisfies completeness and transitivity.

**Theorem: (Ranking)** Given a finite set of bundles $A\subset \mathbb{R}^n_+$, if the preference relation satisfies A1 and A2, then bundles in A can be ranked in a list consistent with the preference.

Proof:

It suffices to show that there is a maximum of $A$. Define an algorithm to find this item. Start with the first item in the set. Suppose next item is preferred to the item in hand, switch the items, i.e. if $x^m\succsim x^\star$ but  $x^m\nsucceq x^\star$ do the switching. Keep doing this until we compare every item in the set.

The only potential trouble happens when we switch the items. We want to show that $x^\star$ is preferred to any other item before the switching. Suppose there is no switching before. This implies that $x^1\succsim x^i$ for $i = 2,3,..., m-1$. From the switching we know that $x^m \succsim x^1$, by Transitivity, we have $x^\star = x^m \succsim x^i$ for $i<m$. Now suppose there are $k$ numbers of switching happened before. We have $x^{m_k} \succsim x^i $ for $i$ between $m_{k-1}$ and $m_k$, plus we have $x^{m_k} \succsim x^{m_{k-1}} $. This implies that $x^\star = x^m \succsim x^i$ for any $i<m$.  If we repeat this algorithm, we will have $x^\star\succsim x^i$ for any $i \in X$, i.e. $x^\star$ is the maximum. $\square$

**Axiom: (A3 - Continuity)** For any bundle $x$, the set $\succsim(x)$ and $\precsim(x)$ are closed, or the set $\succ(x)$ and $\prec(x)$ are open.

**Theorem: (Continuity)** Suppose a preference is complete, transitive and continuous. Then for any $x\in X$, $y\in \succ(x)$ and $z\in \prec(x)$, there is a number $t\in (0,1)$ such that $ty+(1-t)z \in \sim(x)$.

Proof:

Define a subset of real number: $T = \{t\in (0,1)|ty+(1-t)z \in \succsim(x)\}$. Defined $t_0 = inf(T)$. Claim that $t_0 \in \sim(x)$. Suppose $t_0\nsim x$, then either $t_0\prec x$ or $ t_0\succ x$. Suppose $t_0\prec x$, then since $\prec(x)$ is open, there is a $t>t_0$ such that $ty+(1-t)z \in \prec(x)$, contradicting to the fact that $t_0$ is the infimum. Suppose $t_0\succ x$, then since $\succ(x)$ is open, there is a $t<t_0$ such that $ty+(1-t)z \in \succ(x)$, again contradicting to the fact that $t_0$ is the infimum. $\square$

**Axiom: (A4’ - Local Non-Satiation)** For any $x$, for any $\epsilon>0$, there is another bundle $y\in B_\epsilon(x)$ such that $y\succ x$.

**Axiom: (A4 - Strict Monotonicity)** For any $x$ and $y$, if $y\geq x$ then  $y\succsim x$, and if if $y\gg x$ then  $y\succ x$.

**Claim: (Local Non-Satiation and Strictly Monotonicity)** If a preference is strictly monotonic then it is locally non-satiated.

**Axiom: (A5’ - Convexity)** If $y\succsim x$, then $ty+(1-t)x\succsim x$ for any $t\in [0,1]$. 

**Axiom: (A5 - Strict Convexity)** If $y\succsim x$, and $y\neq x$, then $ty+(1-t)x\succ x$ for any $t\in (0,1)$.

 **Axiom: (A6 - Homothetic)** If $y\sim x$, then $ty\sim tx$ for any $t>0$.



### Utility Function

#### Existence of Utility Functions

**Definition: (Utility Function)** A function $U:\mathbb{R}^n_+\to \mathbb{R}$ is called a utility function representing the preference if for any $x,y\in X$, $U(x)\geq U(y)$ if and only if $x\succsim y$.

**Theorem: (Existence of Utility Function)** If the preference is complete, transitive, continuous, and strictly monatomic, then there is a real-valued and continuous function representing the preference.

Proof:

Let $e = [1,1,...,1]$ be a vector in $\mathbb{R}^n$. For any $x\in X$, define $U(x)$ so that $x\sim U(x)e$. We claim that such a number is well defined.

1. First we show that this number exists. Consider the following two sets: $A = \{t\geq 0|te\succsim x\}$ and $B = \{t\leq 0|te\precsim x\}$. Want to show that $A\cap B \neq \phi$. By continuity, both sets are closed. By strict monotonicity and transitivity, if $t_0\in A$, then $\forall t>t_0$ we have $t\in A$. Similarly, if $t_0\in B$, then $\forall t<t_0$ we have $t\in B$. So $A = [t_1,+\infty]$, and $B = [0,t_2]$. Suppose $t_1>t_2$, this would violate the completeness of the preference. Hence $t_1\leq t_2$, this number always exists.
2. Second we show that such a number is unique. Suppose $t_0<t_1$ and $x\sim t_0e\sim t_1 e$, by strict monatomicity, we have $t_0e\prec t_1 e$, which is a contradiction.

Now we will show that $U(x)$ represents the preference, i.e. $x\succsim y$ if and only if $U(x)\geq U(y)$. We have $U(x)e\sim x\succsim y\sim U(y)e$, and the statement is true as a result of strictly monotonicity.

The last step is to show $U(x)$ is continuous. It suffices to show that $U^{-1}(a,b)$ is an open set. $U^{-1}(a,b) = \{x\in X|a<U(x)<b\} = \{x\in X|ae \prec U(x)e \prec be\}  =  \{x\in X|ae \prec x \prec be\} = \succ(ae) \cap \prec(be)$. By continuity, we have both sets are opens, then the intersection of them is also open. $\square$

**Definition: (Marginal Utility)** The marginal utility is defined as $MU_i = \partial U/\partial x_i$.

**Definition: (Marginal Rate of Substitution)** The Marginal Rate of Substitution is defined as $MRS_{ij} = MU_i/MU_j$.

**Definition: (Elasticity of Substitution)** The Elasticity of Substitution is defined as $\sigma_{ij} =\frac{dln(x_i/x_j)}{dln(U_j/U_i)}$.

#### Properties

**Lemma: (Utility and Preference)** $U(x)> U(y)$ if and only if $x\succ y$ and $U(x) =  U(y)$ if and only if $x\sim y$.

**Theorem: (Monotonic Transformation)** If $U$ is a function that represents the preference, and $V$ is another function representing the same preference, then $V = g(U)$ for some strictly increasing function $g:\mathbb{R}\to \mathbb{R}$. Inversely, if  $V = g(U)$ for some strictly increasing function $g:\mathbb{R}\to \mathbb{R}$, then $V$ is another function representing the same preference.

Proof:

$U(x) \geq U(y)$ is equivalent to $g(U(x)) \geq g(U(y))$. Hence the statement is true. $\square$

**Theorem: (Properties of Utility Function)** The following statements are true:

1. $U$ is strictly increasing if and only if the preference is strictly monotonic
2. $U$ is quasi-concave if and only if the preference is convex
3. U is strictly quasi-concave if and only if the preference is strictly convex.

Proof:

These statements are true by definitions. Proof is omitted. $\square$

**Definition: (Homogeneity)** A utility function is called to be homogenous of degree $k$ if $U(tx) = t^kU(x) \forall t>0$.

**Theorem: (Homogeneity and Homothetic Preference)** A utility function is homogenous if and only if the preference is homothetic.

Proof: 

Suppose a utility function is homogenous, then $U(tx) = t^kU(x)$. We have $x\sim y$ if and only if $U(x) = U(y)$. Then $U(tx) = t^kU(x) = t^kU(y) = U(ty)$, i.e. $tx\sim ty$, the preference is homothetic.

Suppose the preference is homothetic, then $x\sim y$ implies $tx\sim ty$. Define a utility function as $x\sim U(x)e$, where $e = (1,1,...,1)$. Then we have $tx \sim U(tx)e$. But homothetic preference implies that $tx \sim tU(x)e$. By transitivity we have $tU(x) = U(tx)$, i.e. $U$ is homogenous of degree 1. $\square$



## Consumer Theory

### Utility Maximization

#### Utility Maximization Problem

**Assumption: (Consumer)** The utility function is continuous, strictly increasing, strictly quasi-concave.

**Definition: (Budget Set)** Denote $B$ as the set of feasible choices for the consumer, it is a budget set when $B = \{x\geq0|px\leq I\}$. Note that there can be $k$ goods.

**Definition: (Consumer’s Problem)** The consumer is solving the Utility Maximizing Problem:
$$
max\space U(x)\\
s.t. \space px\leq I, \space x\in \R^n_+
$$
**Theorem: (Existence and Uniqueness of the Solution)** The solution to the consumer’s problem exists and is unique.

Proof:

The utility function is continuous, the budget set is compact, hence there is a maximum on the constraint.

Now we prove the uniqueness. Suppose there are two solutions to the problem, $x^1$ and $x^2$. Then $px^1\leq I$ and $px^2\leq I$, which implies that $px^t = p(tx^1+(1-t)x^2)\leq I$. Since both are solutions, we have $U(x^1) = U(x^2) = U$. Then $U(x^t)\leq U$, contradicting to the fact that $U$ is strictly quasi-concave. $\square$

**Theorem: (Exhausting the Budget)** With out the loss of generality, we could impose the budget constraint with equality.

Proof:

Suppose not, then the solution to the problem satisfies $px<I$, which cannot be true when $U$ is strictly increasing. $\square$

#### Solution

**Solution: (Kuhn-Tucker Method)**

Define the Lagrange Function as $L = U(x)+\lambda (I-px)+\mu x$. The Kuhn-Tucker condition to solve the problem is the first order conditions, i.e.
$$
\frac{\partial L}{\partial x_i} = U_i(x_i)+\lambda p_i+\mu_i =0\\
\lambda (I-px) = 0\\
\mu_i x_i = 0
$$
**Theorem: (Kuhn-Tucker Theorem)** Suppose $U$ is strictly quasi-concave and differentiable, $(p,I)\gg 0$, then if $(x^\star,\lambda^\star)\gg 0 $ solve the first order conditions, then $(x^\star,\lambda^\star)$ solve the consumer’s problem.

Proof:

First notice one fact: when $x^1 \neq x$, $\nabla U(x)\neq 0$, and $U(x^1)>U(x)$, then $\nabla U(x)(x^1-x)>0$.

Now prove the statement. Suppose not, the there is another solution $(x^1,\lambda^1)$ such that $U(x^1)>U(x^\star)$. By the fact above, we have $\nabla U(x^\star)(x^1-x^\star)>0$, and $px^1\leq I$. Notice that since $(x^\star,\lambda^\star)$ solve the Kuhn-Tucker conditions, we have $\nabla U(x^\star) = \lambda^\star p$. By assumption, $\lambda^\star p\gg 0$, so $\nabla U(x^\star)\gg 0$. So $\nabla U(x^\star)(x^1-x^\star) =\lambda^\star p(x^1-x^\star) >0$ implies that $px^1>px^\star = I$, which is a contradiction to the fact that $x^1$ is feasible. $\square$

**Definition: (Marshallian Demand)** The solution the the utility maximizing problem is called the Marshallian Demand, denoted by $x^\star(p,I)$.

**Definition: (Elasticity)** The Price Elasticity of the demand is defined as $\epsilon_i = \partial lnx^\star(p,I)/\partial lnp_i$.



#### Indirect Utility Function

**Definition: (Indirect Utility Function)** The Indirect Utility Function, also known as the Value Function, is defined as $V(p,I) = U(x^\star(p,I))$.

**Theorem: (Properties of the Indirect Utility Function)** If $U(.)$ is continuous and strictly increasing on $\mathbb{R}^n_+$, then $V(p,I)$ is:

1. Continuous on its domain
2. Homogenous of degree 0 in $(p,I)$
3. Strictly increasing in $I$
4. Decreasing in $p$
5. Quasi-convex in $(p,I)$
6. If $V(p,I)$ is differentiable and $\partial V/\partial I \neq 0 $, then it satisfies Roy’s Identity: $-\frac{\partial V / \partial p_i}{\partial V/\partial I} = x_i(p,I)\geq 0$.

Proof:

1. The continuity of the value function follows from the theorem of maximum.

2. The value function is homogenous of degree 0 since $tpx\leq tI$ is identical to $px\leq I$.

3. consider $I'>I$, suppose $x(p,I)$ and $x'(p,I')$ are the solutions to the maximizing problem separately, then $px\leq I < I' = px'$. So consider $\epsilon \gg 0$ and $p(x+\epsilon)<I'$, but since the utility function is strictly increasing, $U(x+\epsilon)>U(x)$, hence $V(p,I')\geq U(x+\epsilon)>V(p,I)$.

4. consider $p'\leq p$, suppose $x(p,I)$ and $x'(p',I)$ are the solutions to the maximizing problem separately, then $p'x\leq px\leq I$ and $p'x'\leq I $. Then we have $V(p',I)\geq U(x) = V(p,I)$.

5. Now we want to show that $V$ is quasi-convex in $(p,I)$. It suffices to show that $B(p^1,I^1) \cup B(p^2,I^2) \supset B(\bar p,\bar I)$, where $B(\bar p,\bar I) = B(tp^1+(1-t)p^2,tI^1+(1-t)I^2)$. We will argue by contradiction. This means that there exists $\bar x \in B(\bar p, \bar I)$, such that $\bar x\notin B(p^1,I^1)$, and $\bar x\notin B(p^2,I^2)$. This implies that $p^1\bar x >I^1$ and $p^2\bar x >I^2$, then $tp^1\bar x >tI^1$ and $(1-t)p^2\bar x >(1-t)I^2$. Now if we combine them we would get $\bar p\bar x >\bar I$, contradicting to the fact that $\bar p\bar x \leq \bar I$.

6. The first proof follows from the Envelope Theorem. We have $\partial V / \partial p_i = \partial L/\partial p_i = -\lambda x_i$ and $\partial V / \partial I = \partial L/\partial I = \lambda $, which will give us the Roy’s Identity.

   Another proof defines $x^0 = x(p^0,I^0)$. Consider $V(p,px^0)-U(x^0)$ as a function of prices. Note that $V(p,px^0)-U(x^0)\geq 0$ for any $p\in \mathbb{R}^n_+$ because $x^0$ is always affordable. This function is minimized at the price $p^0$. Since the function is differentiable, we have the first order condition: $\partial V(p^0,p^0x^0)/\partial p_i+(\partial V(p^0,p^0x^0)/\partial I) x^0 = 0$, which will give us the Roy’s Identity. $\square$



### Expenditure Minimization

#### Expenditure Minimizing Problem

**Definition: (Expenditure Minimizing Problem)** The expenditure minimizing problem is defined as
$$
min_{x\in \R^m_+} \space px \\
s.t. \space U(x)\geq U_0
$$
**Theorem: (Existence of the solution)** Let $U = \{u\in \mathbb{R}| \exist x \space s.t. \space U(x) = u\}$. If $U_0\in U$, and $U(.)$ is continuous, then there is a solution to the minimization problem. Furthermore, if $U(.)$ is strictly increasing and continuous and strictly quasi-concave, and $p\gg 0 $, then the solution is unique.

Proof:

First, if $U_0\in U$, by definition there is a $x_0$ such that $U(x_0) = U_0$. So $px_0$ is enough to achieve the utility level. So the problem is equivalent to
$$
min_{x\in \R^m_+} \space px \\
s.t. \space U(x)\geq U_0 \\
px\leq px_0
$$
Now we are minimizing a continuous function over a compact set, hence the solution exists.

Next we prove the uniqueness. Suppose there are two solutions to the problem, we have $p_x^1 = px^2 = I$ and $x^1\neq x^2$. Since $U(x^1)\geq U_0$ and $U(x^2)\geq U_0$, we have $U(x^t) = U(tx^1+(1-t)x^2)>min\{U(x^1),U(x^2)\} = U_0$ due to the strict quasi-concavity of the utility function. Note that $px^1 = px^2 = px^t$. Then there exists $x'\ll x^t$ such that $U(x')=U_0$ and $px'<I$, contradicting to the fact that $x_1$ and $x_2$ are both solutions. $\square$

#### Solution

**Solution: (Lagrange Method)**

Define the Lagrange function as $L = px+\lambda(U_0-U(x))$. Take the first order conditions we will get $p_i = \lambda\partial U/\partial x_i$ and $U(x) = U_0$.

**Definition: (Hicks Demand)** The solution to the expenditure minimizing problem is called the Hicks Demand, denoted by $x^H(p,U)$.

####  Expenditure Function

**Definition: (Expenditure Function)** The Expenditure Function is defined as $e(p,U) = px^H(p,U)$.

**Theorem: (Properties of the Expenditure Function)** If $U(.)$ is continuous, strictly increasing and strictly quasi-concave, then the expenditure function is:

1. Zero when $U$ takes the lowest utility level in available $U$
2.  Continuous on $\mathbb{R}^N_+\times U$
3. For $p\gg 0$, the expenditure function is strictly increasing and unbounded in $U$
4. Increasing in $p$
5. Homogenous of degree 1 in $p$
6. concave in $p$
7. If $U(.)$ is differentiable, then the Shephard’s lemma is true, i.e. $\partial e(p^0,U^0)/\partial p_i = x_i^H(p^0,U^0)$.

Proof:

1. The bundle giving the lowest utility level is $(0,0,...,0)$. the expenditure to achieve this bundle is trivially zero.

2. Given the objective function is continuous and the feasible set is compact, by the Theorem of Maximum the expenditure function is continuous.

3. First prove the monotonicity. Suppose $U'>U$, let $px' = e(p,U')$, $U(x')\geq U'\geq U$, since $U(.)$ is strictly increasing and $px = e(p,U)$, we have $px = e(p,U)\leq e(p,U') = px'$, since $x$ is minimizing the objective function. Now we only need to show that $px'\neq px$. Suppose $px' = px$, since $U(x')\geq U'> U\geq U(0)$, we have $x'\neq 0$. There exists some $x_i'>0$ such that $U(\tilde x) = U(x_1',x_2',...,x_i'-\epsilon, ..., x_n')>U$ because $U'> U$ and $U$ is continuous. So $\tilde x$ is feasible for the minimization problem, and $px\leq p\tilde x<px'$, i.e. the expenditure function is strictly increasing in $U$.

   Now we prove the unboundedness. Since $U(.)$ is increasing and continuous, the attainable utility level is an interval: $U = [U(0),\bar U)$, where $\bar U$ is a finite number or infinity. Pick an increasing sequence of utility level $U_n\to \bar U$, we want to show that $e(p,U_n)$ is unbounded above. Suppose this is not true. Since $U(.)$ is strictly increasing, let $px^n  = e(p,U_n)$, if $e(p,U_n)$ is bounded, then $x^n$ is also bounded. Then there is a subsequence of $x^n$,denoted as $x^{n_k}$ which goes to some $\bar x \in \mathbb{R}^n_+$. Then since $U(.)$ is continuous, we have $U(x^{n_k})\to U(\bar x)$. Since there is only one limit of the sequence $U_n$, which is $\bar U$, we have $ U(\bar x) = \bar U$. But then $\bar U $ would be attainable, which is impossible.

4. Suppose $p^1<p^2$, and $x^1$ and $x^2$ are the solutions to the minimizing problem, separately. Since $U_0$ is always attainable, we have $p^1x^1\leq p^1x^2 < p^2x^2$.

5. At price $tp$, the problem can be rewrite as $t[min_{x\in \mathbb{R}^m_+} \space px] \space s.t. \space U(x)\geq U_0$, which is identical to the original problem. So the solution is the same, i.e. $e(tp,U_0) = tpx  =t(px) = te(p,U_0)$.

6. Consider $p^1$ and $p^2$, define $\bar p = tp^1+(1-t)p^2$. Let $\bar x = x^H(\bar p, U_0)$, $x^1 = x^H(p^1, U_0)$, and $x^2 = x^H(p^2, U_0)$.  Then we have $p^1x^1 \leq p^1 \bar x$ and $p^2x^2 \leq p^2 \bar x$. Combine them we have $\bar p (tx^1+(1-t)x^2)\leq \bar p\bar x$, i.e. the expenditure function is concave.

7. The first proof follows from the Envelope Theorem. We have $\partial e / \partial p_i = \partial L/\partial p_i =  x_i^H$.

   An alternative proof is to consider the function $F(p) = e(p,U_0)-px^0$, where $x^0 = x^H(p,u^0)$. This function is maximized at $p$. So the first order condition is $\partial e(p^0,U^0)/\partial p_i - x_i^H(p^0,U^0)  =0$. $\square$



### Duality

**Lemma: (Duality)** Generally, we have $e(p,V(p,I))\leq I$, and $V(p,e(p,U))\geq U$.

**Theorem: (Duality Theorem)** If $U(.)$ is continuous and strictly increasing, then $e(p,V(p,I)) = I$ and $V(p,e(p,U))= U$.

Proof:

1. Prove by contradiction. Suppose $e(p,V(p,I_0)) < I_0$, let $U_0  =V(p,I_0)$ so then $e(p,U_0)<I_0$. Since $e(p,U)$ is continuous in $(p,U)$, there is a $\epsilon >0$ such that $e(p,U_0+\epsilon)<I_0$, denote $I_\epsilon = e(p,U_0+\epsilon)$, then $I_\epsilon<I_0$. But then we have $U_0+\epsilon \leq V(p,I_\epsilon)<V(p,I_0) = U_0$, which is impossible.
2. Prove by contradiction. Suppose $V(p,e(p,U_0)) > U_0$, let $I_0  = e(p,U_0)$ so then $V(p,I_0)>U_0$. Since $V(p,I)$ is continuous in $(p,I)$, there is a $\epsilon >0$ such that $V(p,I_0-\epsilon)>U_0$, denote $U_\epsilon = V(p,I_0-\epsilon)$, then $U_\epsilon>U_0$. But then we have $I_0-\epsilon \geq e(p,U_\epsilon)>e(p,U_0) = I_0$, which is impossible. $\square$

**Theorem: (Duality of the Solutions)** Suppose $U$ is continuous, strictly increasing and strictly quasi-concave. Then we have $x^\star  =x^H(p,V(p,I))$ and $x^H = x^\star(p,e(p,U))$ for all $p\gg 0$ and U attainable.

Proof:

1. By continuity and strictly quasi-concavity, both solutions are unique. By definition we have $e(p,V(p,I)) = px^H(p,V(p,I))$. By the duality theorem $e(p,V(p,I)) =I = px^H(p,V(p,I))$. Then by definition of the utility maximizing problem, $x^H(p,V(p,I))$ is affordable under income level $I$ and gives a utility level of $V(p,I)$. So $x^H(p,V(p,I))$ is a solution to the utility maximizing problem. However, since the solution is unique, we have $x^\star  =x^H(p,V(p,I))$.
2. Similarly, by definition we have $V(p,e(p,U)) = U(x^\star(p,e(p,U)))$. By the duality theorem $V(p,e(p,U)) = U = U(x^\star(p,e(p,U)))$. Then by definition of the expenditure minimizing problem, $x^\star(p,e(p,U))$ is attainable at utility level $U$ and gives an expenditure level of $e(p,U)$. So $x^\star(p,e(p,U))$ is a solution to the expenditure minimizing problem. However, since the solution is unique, we have $x^H = x^\star(p,e(p,U))$. $\square$



###  Slutsky Equation

**Theorem: (Slutsky Equation)** We have $\frac{\partial x_i(p,I)}{\partial p_j} = \frac{\partial x_i^H(p,U)}{\partial p_j}-x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}$ for any $i,j$.

Proof:

From the duality theorem, we have $x^H = x^\star(p,e(p,U))$. Take total differentiation with respect to $p_j$, we have $\frac{\partial x_i(p,I)}{\partial p_j} = \frac{\partial x_i^H(p,U)}{\partial p_j}-x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}$. $\square$

**Definition: (Substitution Effect)** $\frac{\partial x_i^H(p,U)}{\partial p_j}$ is defined as the Substitution Effect.

**Definition: (Income Effect)** $-x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}$ is defined as Income Effect.

**Definition: (Normal Good)** A good is Normal at a point if $\frac{\partial x_i(p,I)}{\partial I}>0$.

**Definition: (Inferior Good)** A good is Inferior at a point if $\frac{\partial x_i(p,I)}{\partial I}<0$.

**Definition: (Giffen Good)** A good is Giffen at a point if $\frac{\partial x_i(p,I)}{\partial p_j}<0$.



### Properties of Demand

**Theorem: (Properties of Marshallian Demand)** Under all assumptions of the utility function, the Marshallian demand is homogenous of degree 0, and it satisfies the budget balance.

Proof:

We have $V(p,I) = V(tp,tI)$, which is equivalent to $U(x^\star(p,I)) = U(x^\star(tp,tI))$. Since $U(.)$ is continuous and strictly increasing, $x^\star(p,I) = x^\star(tp,tI)$. The budget balance follows from the strictly increasing property of the utility. Suppose $px^\star(p,I) <I$, then we can find another bundle such that $U(x’)>U(x^\star)$ and $px'<I$, contradicting to the fact that $x^\star$ is the solution. $\square$

**Theorem: (Properties of Hicks Demand)** Under all assumptions of the utility function, and suppose $(p,I)\gg 0$, the Hicks demand is homogenous of degree 0 with respect to $p$, and exhausts the utility constraint.

Proof:

At price $tp$, the problem can be rewrite as $t[min_{x\in \mathbb{R}^m_+} \space px] \space s.t. \space U(x)\geq U_0$, which is identical to the original problem. So the solution is the same.

Exhausting the utility constraint follows from the strictly increasing property of the utility. Suppose $U(x^\star(p,I)) >U$, then we can find another bundle such that $U(x’)<U(x^\star)$ and $px'<I$, when $p\gg 0$. This is contradicting to the fact that $x^\star$ is the solution. $\square$

**Definition: (Slutsky Matrix)** Define the Slutsky Matrix as $S(p,I) = [\frac{\partial x_i(p,I)}{\partial p_j} +x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}]$.

**Theorem: (Properties of Slutsky Matrix)** The Slutsky matrix is symmetric and negative semi-definite. 

Proof: 

Note that by Slutsky Equation, $S(p,I) = [\frac{\partial x_i(p,I)}{\partial p_j} +x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}] = [\frac{\partial x_i^H(p,V(p,I))}{\partial p_j}]$. By Shephard’s lemma, we have $\partial e(p,U)/\partial p_i = x_i^H(p,U)$, hence $\frac{\partial x_i^H(p,V(p,I))}{\partial p_j} = \frac{\partial^2 e(p,U)}{\partial p_i\partial p_j}$, by Young’s theorem this is symmetric. Since $e(p,U)$ is concave, $[\frac{\partial x_i^H(p,V(p,I))}{\partial p_j}]$ is negative semi-definite. $\square$

**Theorem: (Slutsky Property)** Suppose that $x(p, I)\in \mathbb{R}^n_+$ satisfies budget balance and homogeneity. Then for all $(p, y)$, $S(p, y)p= 0$.

Proof:

Note that $S(p, y)p= \sum_{j=1}^n(\frac{\partial x_i}{\partial p_j}+x_j\frac{\partial x_i}{\partial I})p_j = \sum_{j=1}^n(p_j\frac{\partial x_i}{\partial p_j}+p_jx_j\frac{\partial x_i}{\partial I}) = \sum_{j=1}^n(p_j\frac{\partial x_i}{\partial p_j})+I\frac{\partial x_i}{\partial I} = 0$. $\square$



### Integrability

#### Recover Utility from the Expenditure Function

**Theorem: (Recovering Expenditure Function)** Suppose $e: \mathbb{R}^n\times \mathbb{R}$ satisfies the seven properties of the expenditure function, then define $u(x) = max\{u\geq U(0)|px\geq e(p,u) \space \forall p\gg 0\}$. $u(x)$ is well defined, unbounded, increasing and quasi-concave.

Proof:

1. First we prove the function is well defined. Define $\bar U = \{u\geq U(0)|px\geq e(p,u) \space \forall p\gg 0\}$. We want to show that $\bar U$ is a non-empty, closed, bounded set. The set is non-empty because $U(0)$ is always in the set. it is bounded below by $U(0)$ and bounded above since $e$ is increasing in $u$ and unbounded above in $u$ by assumption. We only need to show that $\bar U$ is closed. Let $u_n$ be a sequence such that $u_n\to u$, suppose $u_n \in \bar U$, which implies $px\geq e(p,u_n)$. Since $e$ is continuous, $e(p,u_n)\to e(p,u)$. Then $px\geq e(p,u)$, i.e. $u\in \bar U$, $\bar U$ is closed. Since t $\bar U$ is non-empty, closed, and bounded, the maximum exists. Hence $u(x)$ is well-defined. The function is unbounded above by construction. 
2. Second we prove the function is increasing. Suppose we have $x^1\geq x^2$, we have $px^1\geq px^2\geq e(p,u(x^2))$ by the definition of $u(x^2)$. This implies $u(x^2)\in \bar U(x^1)$. Since $u(x^1)$ is the maximum, we have $u(x^1)\geq u(x^2)$.
3. Third we prove the function is quasi-concave. Take any $x^1$ and $x^2$ and $t\in [0,1]$. By definition we have $px^1\geq e(p,u(x^1))$ and $px^2\geq e(p,u(x^2))$. So $p(tx^1+(1-t)x^2)\geq te(p,u(x^1))+(1-t)e(p,u(x^2))\geq min\{e(p,u(x^1)),e(p,u(x^2))\}$. Hence we have $min\{e(p,u(x^1)),e(p,u(x^2))\} \in \bar U(tx^1+(1-t)x^2)$. since $u(tx^1+(1-t)x^2)$ is the maximum, we have $u(tx^1+(1-t)x^2)\geq min\{e(p,u(x^1)),e(p,u(x^2))\}$, i.e. u(x) is quasi-concave. $\square$

**Theorem: (Verification)** Suppose $e: \mathbb{R}^n\times \mathbb{R}\to \mathbb{R}$ is any function that satisfies the seven properties of the expenditure function, then define $u(x) = max\{u\geq0|px\geq e(p,u) \space \forall p\gg 0\}$. Then $e(p^0,U_0) = min_{x\in \mathbb{R}^m_+} \space p^0x \space s.t. \space u(x)\geq U_0$.

Proof:

1. First we prove that $[min_{x\in \mathbb{R}^m_+} \space p^0 x \space s.t. \space u(x)\geq U_0]\geq e(p^0,U_0)$.

   Fix $p^0\gg0$ and $U_0\geq 0$, for any $x$ such that $u(x)\geq U_0$, by the definition of $u(x)$, we have $px^0\geq e(p,u(x))$ for all $p$. This implies $p^0 x^0\geq e(p^0,u(x))$. Furthermore, since $e(p,u)$ is increasing in $u$, and $u(x)\geq U_0$, we have $p^0 x\geq e(p^0,u(x)) \geq e(p^0,U_0)$. Recall this inequality holds for all $x$ such that $u(x)\geq U_0$. Suppose the solution to minimization problem is $x^0$, we have $p^0 x^0 \geq e(p^0,U_0)$, i.e. $[min_{x\in \mathbb{R}^m_+} \space p^0 x \space s.t. \space u(x)\geq U_0]\geq e(p^0,U_0)$.

2. Now we prove that $[min_{x\in \mathbb{R}^m_+} \space px \space s.t. \space u(x)\geq U_0]\leq e(p^0,U_0)$.

   It suffices to find $x'$ such that $u(x')\ge U_0$ and $p^0x'\leq e(p^0, U_0)$. Let $\frac{\partial e(p^0,U_0)}{\partial p} = x'$. We first prove that $ u(x')\ge U_0$. By assumption we have that $e(p,U)$ is homogenous of degree 1 in prices. So by Euler’s theorem, $\frac{\partial e(p^0,U_0)}{\partial p}p = e(p^0,U_0)$. Also, we know that $e(p,U)$ is concave in $p$, so $e(p,U_0) \leq e(p^0, U_0)+(p-p^0)\frac{\partial e(p^0,U_0)}{\partial p}$. Plug in the Euler’s theorem, we have $e(p,U_0) \leq p \frac{\partial e(p^0,U_0)}{\partial p} =  px'$ for any $p$.  By definition, $u(x')\geq U_0$.

   Now we prove that $p^0x'\leq e(p^0, U_0)$. This is true because $e(.)$ also satisfies the Shepherd’s lemma, which gives us $p^0x' =p^0\frac{\partial e(p^0,U_0)}{\partial p}= e(p^0, U_0)$. Combine 1 and 2, we prove the theorem. $\square$

**Solution: (Algorithm of Recovering Expenditure Function)**

Solve for the recovered expenditure function with the following algorithm:
$$
u(x) = max\{u\geq U(0)|px\geq e(p,u) \space \forall p\gg 0\} = max_{u} min _ppx-e(p,u)
$$


#### Recover Expenditure Function from the Demand

**Theorem: (Homogeneity)** If $x(p,I)$ satisfies budget balance and symmetry of associated Slutsky matrix $S(p,I)$, then it is homogenous of degree 0 in $p$.

Proof:

By budget balance, . $px(p,I) = I = \sum_{i = 1}^n p_ix_i(p,I)$. Differentiate with respect to $p_i$, we will get $\sum_{i = j}^n p_j \frac{\partial x_j}{\partial p_i}+x_i(p,I) = 0$, or $\sum_{i = j}^n p_j \frac{\partial x_j}{\partial p_i} = -x_i(p,I)$. Now differentiate with respect to $I$, we will get $\sum_{i=1}^n p_j \frac{\partial x_j}{\partial I} = 1$. Now define $f_i(t) = x_i(tp,tI)$. We want to show that $f_i(t) = f(1)$, i.e. $\frac{\partial f_i}{\partial t}  =0$. We have:


$$
f_i'(t) = [\sum_{j = 1}^n \frac{\partial x_i}{ \partial p_j}p_j +\frac{\partial x_i}{\partial I}I] |_{(tp,tI)} \\
= \sum_{j = 1}^n (\frac{\partial x_i(tp,tI)}{ \partial p_j}tp_j )+\frac{\partial x_i(tp,tI)}{\partial I}tI \\
= \sum_{j = 1}^n (\frac{\partial x_i(tp,tI)}{ \partial p_j}tp_j +\frac{\partial x_i(tp,tI)}{\partial I}tx_jp_j)
$$
Using symmetry, we have
$$
f_i'(t)= \sum_{j = 1}^n \frac{\partial x_j(tp,tI)}{ \partial p_i}tp_j + \sum_{j = 1}^n \frac{\partial x_j(tp,tI)}{\partial I}tp_jx_i(t)\\
 =   -x_i(t) + x_i(t) = 0
$$
This finishes the proof. $\square$ 

**Theorem: (Integrability Theorem)** If a differentiable function $x:\mathbb{R}^n_+ \times \mathbb{R}_+\to \mathbb{R}^n_+$ satisfies budget balance, symmetry and negative semi-definite of Slutsky matrix, then it is the demand function generated by some increasing, quasi-concave function.

Proof:

1. First we want to show that suppose $e(p,U)$ is an expenditure function that is generated by some utility function, i.e. that is not related to the given function $x(.)$, the solutions would coincide. However, when we have $\frac{\partial e(p,U)}{\partial p_i} = x_i(p,e(p,U))$ for all $i$, the Marshallian demand generated by the same utility function satisfies $x^\star(p,I) = x(p,I)$. This follows from duality and Shepherd’s lemma. We have $x^\star(p,e(p,U)) = x^H(p,U) = x(p,e(p,U))$. For each fixed $p$, as $U$ varies $e(p,U)$ assumes all numbers on $[0,+\infty)$, so we could change $e(p,U)$ to $I$ and have the aimed equation.

2. Second we want to show that the solution to $\frac{\partial e(p,U)}{\partial p_i} = x_i(p,e(p,U))$ for all $i$ always exists. By Fubini theorem, if $[\frac{\partial^2 e(p,U)}{\partial p_i\partial p_j}]$ is symmetric, the solution exists, which is guaranteed by the assumption of $x(p,I)$.

3. Now we want to show that the solution $e(p,U)$ satisfies the 7 properties of expenditure functions.

   It is obviously zero when $U$ take the lowest utility level. Since we generated the function from a differential equation it is also continuous. By construction the function is strictly increasing and unbounded in $U$ since we can always choose the function to be that way. It is increasing in $p$ because $\frac{\partial e(p,U)}{\partial p_i} = x_i(p,e(p,U)) \geq 0$. It is concave in $p$ since $S(p,I)$ is negative semi-definite. Shepherd’s lemma is automatically true. We only need to show that $e(p,U)$ is homogenous of degree 1 in $p$. Since we have $e(p,U) = \sum_{i=1}^np_ix(p_i,e(p,U)) = \sum_{i=1}^np_i\frac{\partial e(p,U)}{\partial p_i}$, by Euler’s theorem, $e(p,U)$ is homogenous of degree 1. $\square$



### Revealed Preference

**Definition: (Weak Axiom of Revealed Preference)** Consumer choice satisfies the Weak Axiom of Revealed Preference (WARP) if for any pair of $x^1\neq x^2$, $x^1$ is chosen at price $p^1$ and $x^2$ is chosen at $p^2$, then $p^1x^1\geq p^1x^2$ implies $p^2x^1 <p^2x^2$.

**Definition: (Strong Axiom of Revealed Preference)** Consumer choice satisfies the Strong Axiom of Revealed Preference (SARP) if for any $x^1\neq x^2 \neq ...\neq x^k$, $x^1$ is chosen at price $p^1$ and $x^2$ is chosen at $p^2$, then $p^1x^1\geq p^1x^2$, $p^2x^2\geq p^2x^3$ and so on implies $p^kx^1 <p^kx^k$.

**Theorem: (Homogeneity)** Suppose the choice function satisfies the budget balance and WARP, then it is homogenous of degree 0.

Proof:

Let $x = x(p,I)$ and $x' = x(tp,tI)$. Suppose $x\neq x'$. Assuming budget balance and WARP, we have $px = I$ and $tpx' = tI$. since $t\neq 0$ is a number, we have $tpx = tI$, i.e. $x$ is affordable under $(tp,tI)$, by WARP, we have $px'>px$. Similarly since $x'$ is affordable under $(p,I)$, by WARP we have $tpx>tpx'$, which is a contradiction. $\square$

**Theorem: (Slutsky Property)** Suppose the choice function satisfies the budget balance and WARP, then its Slutsky matrix is negative semi-definite.

Proof:

Let $x^0 = x(p^0,I^0)$ and consider $x(p,px^0)$. for an arbitrary price level $p^1$, let $x^1 = x(p^1,p^1x^0)$. Budget balance implies hat $p^1x^1 = p^1x^0$. $x^0$ is affordable under $p^1$, if $x^1\neq x^0$, by WARP, $p^0x^1>p^0x^0$, and when $x^1 = x^0$, we have $p^0x^1\geq p^0x^0$. Now combine the conditions we have
$$
(p^0-p^1)x^1\geq (p^0-p^1)x^0 \\
(p^0-p^1)(x^1-x^0) \geq 0
$$
Let $p^1 = p^0+tz$, where $t>0$ and $z$ is a vector in $\mathbb{R}^n$. so this becomes $tz(x^1-x^0)\leq 0$. Choose $t$ close to zero, we have $tzx(p^1,p^1x^0)\leq tzx^0$, i.e. $zx(p^0+tz , (p^0+tz)x^0)\leq zx^0$. If we define a function $f(t) = zx(p^0+tz , (p^0+tz)x^0)$, this implies that the function attains its maximum when $t = 0$. Note that $t\in [0,\bar t)$, so the equivalent condition is $f'(0)\leq 0$. So we have
$$
f'(t)|_{t= 0} = \sum _{i=1}^n z_i(\sum_{j=1}^n\frac{\partial x_i(p^0+tz,(p^0+tz)x^0)}{\partial p_j}|_{t= 0}z_j+\frac{\partial x_i(p^0+tz,(p^0+tz)x^0)}{\partial I}|_{t= 0}(\sum_{j=1}^nz_jx^0_j)) \\
= \sum _{i=1}^n \sum_{j=1}^n z_i z_j(\frac{\partial x_i(p^0,p^0x^0)}{\partial p_j}+\frac{\partial x_i(p^0,p^0x^0)}{\partial I}x^0_j) \\
=z^TS(p^0,I^0)z\leq 0
$$
So the Slutsky matrix is negative semi-definite. $\square$

**Theorem: (Recover WARP)** Suppose that a choice function $x(p,y)$ satisfies homogeneity and budget balance. Suppose further that whenever $p^1$ is not proportional to $p^0$, we have $(p^1)^TS(p^0,I)p^1<0$. Then $x(p,I)$ satisfies WARP.

Proof:

1. Suppose $p^1 = tp^0$. If $p^0x^0\geq p^0x^1$, if $x^1\neq x^0$, we want to show that $p^1 x^0 > p^1 x^1$. This is trivial when $p^0 x^0 > p^0 x^1$. However, when $p^0 x^0 = p^0 x^1$, we must have $x^1 = x^0$, contradiction.
2. Suppose $p^1 = p^0+z \neq kp^0$. Define $f(t) = zx(p^0+tz , (p^0+tz)x^0)$. Since $(p^1)^TS(p^0,I)p^1<0$, we have $f'(0)<0$ for $t\in [0,\bar t)$. Hence $f(0)>f(1)$, and $(p^0-p^1)x(p^1,p^1x^0) > (p^0-p^1)x^0$, i.e. $p^0x(p^1,p^1x^0) > p^0x^0$, which means for any other price $p^1$ if $x^0$ is affordable, then at price level $p^0$, the new bundle is not affordable, i.e. WARP is satisfied. $\square$

**Theorem: (Slutsky Property with Two Goods)** Suppose there are only two goods and that a consumer’s choice function $x(p,I)$ satisfies budget balance. If $x(p,I)$ is homogeneous of degree zero in $(p,I)$, then the Slutsky matrix associated with $x(p,I)$ is symmetric.

Proof:

We want to show that $\frac{\partial x_1}{\partial p_2}+\frac{\partial x_1}{\partial I} x_2  =\frac{\partial x_2}{\partial p_1}+\frac{\partial x_2}{\partial I} x_1$. From budget balance we have $p_1x_1(p_1,p_2,I)+p_2x_2(p_1,p_2,I) = I$.  Take total differentiation with respect to $p_1$, we have $x_1+\frac{\partial x_1}{\partial p_1}p_1+p_2\frac{\partial x_2}{\partial p_1} = 0$. Take total differentiation with respect to $p_2$, we have $x_2+\frac{\partial x_1}{\partial p_2}p_1+p_2\frac{\partial x_2}{\partial p_2} = 0$. Take total differentiation with respect to $I$, we have $\frac{\partial x_1}{\partial I}p_1+p_2\frac{\partial x_2}{\partial I} = 1$. Combine them we have
$$
\frac{\partial x_1}{\partial p_2}+\frac{\partial x_1}{\partial I} x_2 = -\frac{x_2}{p_1}-\frac{p_2}{p_1}\frac{\partial x_2}{\partial p_2} + \frac{\partial x_1}{\partial I} x_2 \\
=-\frac{x_2}{p_1}-\frac{p_2}{p_1}\frac{\partial x_2}{\partial p_2} + [\frac{1}{p_1}-\frac{p_2}{p_1}\frac{\partial x_2}{\partial I}] x_2\\
=-\frac{p_2}{p_1}\frac{\partial x_2}{\partial p_2} - \frac{p_2x_2}{p_1}\frac{\partial x_2}{\partial I} \\
$$
 Now since $x(p,I)$ is homogeneous of degree zero in $(p,I)$, Euler’s theorem gives us $p_1\frac{\partial x_2}{\partial p_1}+p_2\frac{\partial x_2}{\partial p_2}+I\frac{\partial x_2}{\partial I} = 0$. Plug this into the equation, we have
$$
-\frac{p_2}{p_1}\frac{\partial x_2}{\partial p_2} - \frac{p_2x_2}{p_1}\frac{\partial x_2}{\partial I} = \frac{\partial x_2}{\partial p_1}+\frac{I}{p_1}\frac{\partial x_2}{\partial I} - \frac{p_2x_2}{p_1}\frac{\partial x_2}{\partial I}\\
= \frac{\partial x_2}{\partial p_1}+\frac{\partial x_2}{\partial I} x_1
$$
And this finishes the proof. $\square$

**Theorem: (Equivalent Definition of WARP)** Suppose that the choice function $x(p,I)$ is homogeneous of degree zero in $(p,I)$.Show that WARP is satisfied for all $(p,I)$ if and only if it is satisfied on $\{(p,1)|p\in R^n_+\}$.

Proof:

1. If WARP is satisfied for all $(p,I)$, then of course it will be true on $\{(p,1)|p\in R^n_+\}$.
2. Suppose $p^0x(p^0,1)\geq p^0x(p^1,1)$ implies $p^1x(p^0,1)>p^1x(p^1,1)$. The choice function is homogenous of degree 0. Now suppose $p^0x(p^0,I)≥p^0x(p^1,I)$, we have $p^0/Ix(p^0/I,1)\geq p^0/Ix(p^1/I,1)$, which implies that $p^1/Ix(p^0/I,1)> p^1/Ix(p^1/I,1)$, i.e. $p^1x(p^0,I)≥p^1x(p^1,I)$. So WARP is generally true. $\square$



## Uncertainty

### Axiom

**Definition: (Simple Lottery)** A simple lottery is a lottery all of whose outcomes are members of finite outcome set $A$. A simple lottery is denoted as $g\in G_s\{p_1\circ a_1, ..., p_n\circ a_n| p_i\geq 0, \sum_{i=1}^np_i = 1\}$.

**Axiom: (G1 - Completeness)** For any distinct bundles $g$ and $g’$, either $g\succsim g'$ or $g\precsim g'$.

**Axiom: (G2 - Reflexivity)** $g\succsim g$.

**Axiom: (G3 - Transitivity)** For any distinct bundles $g$ , $g'$ and $g''$, if $g\succsim g'\succsim g''$ then $g\succsim g''$.

**Lemma: (Ranking)** By G1-G3 we can rank any finite elements in $A$.

**Axiom: (G4’ - Archimedean)** For any $\pi,\rho,\sigma \in G$, if $\pi\succ\rho\succ \sigma$, then there exist  $\alpha, \beta\in (0,1)$ such that $(\alpha\circ\pi,(1-\alpha)\circ\sigma) \succ \rho$, and $(\beta\circ\pi,(1-\beta)\circ\sigma) \prec \rho$.

**Axiom: (G4 - Continuity)** For any bundles $g$, there exists a probability $\alpha \in [0,1]$ such that $g\sim (\alpha\circ a_1, (1-\alpha)\circ a_n)$.

**Claim: (Archimedean and Continuity)** If a preference is continuous, then it is Archimedean.

**Axiom: (G5 - Monotonicity)** For any $\alpha \in [0,1]$ and $\beta \in [0,1]$,  $(\alpha\circ a_1, (1-\alpha)\circ a_n)\succsim (\beta\circ a_1, (1-\beta)\circ a_n)$ if and only if $\alpha \geq \beta$.

**Axiom: (G6 - Substitution)** If $g = (p_1\circ g_1,..., p_k\circ g_k)$ and $h = (p_1\circ h_1,..., p_k\circ h_k)$, and $g_i\sim h_i$ for all $i = 1,2, ...,k$, then $g\sim h$.

**Axiom: (G7 - Reduced to simple gamble)** If $g = (p_1\circ g_1,..., p_kg_k) \in G$ is a compound lottery and $g_s = (\alpha_1\circ a_1,..., \alpha_n\circ a_n)$ is the simple lottery induced by $g$, then $g\sim g_s$.

**Axiom: (G8 - Independence)** For any $\pi,\rho,\sigma \in G$ and $\alpha\in (0,1)$, we have $(\alpha\circ\pi+(1-\alpha)\circ\sigma) \sim (\alpha\circ\rho+(1-\alpha)\circ\sigma)$ is equivalent to $\pi\sim \rho$.

**Theorem: (Independence Property)** If a preference is substitutable and able to reduce to simple gamble, then it is independent.

Proof: 

By substitution axiom we have $(\alpha\circ\pi+(1-\alpha)\circ\sigma) \sim (\alpha\circ\rho+(1-\alpha)\circ\sigma)$ if $\pi\sim\rho$. Now if we have $(\alpha\circ\pi+(1-\alpha)\circ\sigma) \sim (\alpha\circ\rho+(1-\alpha)\circ\sigma)$ let $\alpha =1$ we have $\pi\sim\rho$. $\square$ 



### Expected Utility Property

**Definition: (Expected Utility Property)** The utility function satisfies the Expected Utility Property if for all $g\in G$, $U(g) = U(g_s) = \sum_{i=1}^n p_iU(a_i)$, where $g_s$ is the simple lottery induced by $g$. This is also called a Von-Neumann-Morgenstern Utility Function.

**Theorem: (Von-Neumann-Morgenstern Utility Function)** If a preference satisfies the axiom G1-G7, then there is a Von-Neumann-Morgenstern utility function representing the preference.

Proof:

By construction, for each gamble $g\in G$, let $U(g)$ defined as $g\sim(U(g)\circ a_1, (1-U(g))\circ a_n)$. Since the preference is continuous, $U(g)$ always exists. Since the preference is monotonic, $U(g)$ is unique. Suppose $g\succsim g'$, by transitivity we have $(U(g)\circ a_1, (1-U(g))\circ a_n) \succsim (U(g')\circ a_1, (1-U(g'))\circ a_n)$. By monotonicity we have $U(g)\geq U(g')$. The inverse is also true, so $U(g)$ represents the preference.

Now we want to show that $U(g)$ has the Von-Neumann-Morgenstern property. Let $g\in G$ be arbitrary, denote $g_s = (p_1\circ a_1, ..., p_n\circ a_n)$ as the simple gamble induced by $g$. By the ability to reduce to simple gamble, we have $g\sim g_s$, or $U(g) = U(g_s)$. Notice that $a_i \sim (U(a_i)\circ a_1,(1-U(a_i))\circ a_n)$ for all $i$, so by substitution, we have $ g_s = (p_1\circ a_1, ..., p_n\circ a_n)\sim (p_1\circ (U(a_1)\circ a_1,(1-U(a_1))\circ a_n), ..., p_n\circ (U(a_n)\circ a_1,(1-U(a_n))\circ a_n))$. Now reduce that to simple gamble, we have $g_s\sim (\sum_{i=1}^np_iU(a_i) \circ a_1, (1- \sum_{i=1}^np_iU(a_i) )\circ a_1)$, by definition and transitivity, we have $U(g) = U(g_s) = \sum_{i=1}^n p_iU(a_i)$. $\square$

**Theorem: (Unique up to Linear Transformation)** Suppose $U(.) $ is a Von-Neumann-Morgenstern utility function representing a preference. Then $V(.)$ is another Von-Neumann-Morgenstern utility function representing the same preference if and only if $V(g) = \alpha+\beta U(g)$.

Proof:

1. If $V(g) = \alpha+\beta U(g)$, then the rest is trivial to prove.
2. If $V(.)$ is another Von-Neumann-Morgenstern utility function representing the same preference, we have $U(g)= \sum_{i=1}^n p_iU(a_i) = \sum_{i=1}^n p_i[\alpha_iU(a_1)+(1-\alpha_i)U(a_n)]$ and $V(g)= \sum_{i=1}^n p_iV(a_i) = \sum_{i=1}^n p_i[\alpha_iV(a_1)+(1-\alpha_i)U(a_n)]$, by continuity. Then as we can see, both $U(.)$ and $V(.)$ are linear functions of $\{p_i\}$, which means there exists $\alpha$ and $\beta$ such that $V(g) = \alpha+\beta U(g)$. $\square$



### Risk Aversion

**Definition: (Risk Averse)** Given a gamble distribution $F$, $\delta_\mu$ is the distribution that will yield the expected value of $F$ for sure. Then the preference relation is Risk Averse if for all $F$, $\delta_\mu \succsim F$. It is called Risk Loving if for all $F$, $\delta_\mu \precsim F$. It is Risk Neutral if for all $F$, $\delta_\mu \sim F$.

**Note:** A preference can be neither risk averse, risk loving nor risk neutral.

**Definition: (Certainty Equivalent)** Given a strictly increasing and continuous VNM utility function $U(w)$ over wealth, the Certainty Equivalent $CE(F,U)$ is defined as $U(CE(F,U)) = \int U(x)dF(x)$. Or, $CE(F,U)$ is the amount of wealth such that $\delta_{CE} \sim F$.

**Definition: (Risk Premium)** Define Risk Premium as $r(F,U) = \mu_F-CE(F,U)$.

**Definition: (Probability Premium)** The Probability Premium $p$ is defined as the probability higher than 0.5 such that $U(x) = (\frac{1}{2} +p)U(x+\epsilon)+(\frac{1}{2} - p)U(x-\epsilon)$.

**Theorem: (Risk Aversion)** Suppose a preference has the expected utility property, the following are equivalent:

1. the preference is risk averse
2. $U(.)$ is concave
3. $CE(F,U)\leq \delta_F$
4. $r(F,U)$ is positive

Proof:

1. From 1 to 2. If the preference is risk averse, we have $\delta_\mu \succsim F$, for any $x,y\in R$, and $\forall \alpha \in [0,1]$, define a discrete random variable $X$, such that $P(X = x) = \alpha$, and $P(X=y) = 1-\alpha$. Let $F_X$ be the cumulative distribution, and by risk aversion, we have $\delta_\mu \succsim F_X$. Then $U(\delta_mu) \geq U(F_X)$, i.e. $U(\alpha x+(1-\alpha)y) \geq \alpha U(x)+(1-\alpha)U(y)$, i.e. $U(.)$ is concave.
2. From 2 to 3. If $U(.)$ is concave, by Jensen’s inequality, we have $U(E[X])\geq E[U(X)] = U(CE(F,U))$, since $U(.)$ is strictly increasing, we have $E[X]\geq CE(F,U)$.
3. By definition $CE(F,U)\leq \delta_F$ is equivalent to $r(F,U)\geq 0$
4. From 4 to 1. If $r(F,U)$ is positive, we have $CE(F,U)\leq \delta_F$, i.e. $U(E[x])\geq U(CE(F,U)) = E[U(X)]$. So the preference is risk averse.

**Definition: (Comparing Risk Aversion)** Given 2 preferences, preference 1 is more risk averse than preference 2 if and only if $F\succsim_1 \delta_x$ implies $F\succsim_2 \delta_x$.

**Definition: (Arrow-Pratt Measure of Absolute Risk Aversion)** The Absolute Risk Aversion is defined as $\lambda(x) = -\frac{U''(x)}{U'(x)}$ for all $X\in \mathbb{R}$.

**Definition: (Arrow-Pratt Measure of Relative Risk Aversion)** The Relative Risk Aversion is defined as $R(x) = -\frac{xU''(x)}{U'(x)}$ for all $X\in \mathbb{R}$.

**Theorem: (Relative Risk Aversion)** Suppose 2 preferences have the expected utility property, the following are equivalent:

1. Preference 1 is more risk averse than preference 2
2. $U_1(.) = \phi(U_2(.))$ for some concave and strictly increasing function $\phi:\mathbb{R}\to\mathbb{R}$
3. $CE(F,U_1)\leq CE(F,U_2)$ for all $F$
4. $r(F,U_1) \geq r(F,U_2)$ for all $F$
5. $\lambda_1(x) \geq \lambda_2(x)$ for all $x$

Proof:

1. From 1 to 3. If preference 1 is more risk averse than preference 2, for a given $F$, we have  $F\succsim_1 \delta_x$ implies $F\succsim_2 \delta_x$ for all $x$. This means for any given $x$, if $x\leq CE(F,U_1)$ then we have $x\leq CE(F,U_2)$, i.e. $CE(F,U_1)\leq CE(F,U_2)$.
2. From 3 to 1. If $CE(F,U_1)\leq CE(F,U_2)$ for all $F$, This means for any given $x$, if $x\leq CE(F,U_1)$ then we have $x\leq CE(F,U_2)$, i.e. we have  $F\succsim_1 \delta_x$ implies $F\succsim_2 \delta_x$, preference 1 is more risk averse than preference 2.
3. From 2 to 3. If $U_1(x) = \phi(U_2(x))$, we have for a given $F$, the definition of certainty equivalence and Jensen’s inequality suggests $U(CE(F,U_1)) = \int U_1(x)dF(x) = \int \phi(U_2(x))dF(x) \leq \phi(\int U_2(x)dF(x)) =\int U_1(x)dF(x)= U(CE(F,U_2))$, since $U(.)$ is strictly increasing, we have $CE(F,U_1)\leq CE(F,U_2)$.
4. From 3 to 2. Since $U(.)$ is strictly increasing, define $\phi(.) = U_1(U_2^{-1}(.))$. $\phi(.)$ is obviously strictly increasing. Now we have $\int \phi(U_2(x))dF(x)= \int U_1(x)dF(x) = U(CE(F,U_1))  \leq U(CE(F,U_2)) =\int U_1(x)dF(x) = \phi(\int U_2(x)dF(x))$, i.e. Jensen’s inequality holds. $\phi(.)$ is concave.
5. Proof between 3 and 4 is trivial.
6. Between 5 and 2. If $U_1(.) = \phi(U_2(.))$, we have $\phi'>0$ and $\phi''<0$. By definition $\lambda_1(x) = -\frac{U_1''}{U_1'} = \lambda_2-\frac{\phi''}{\phi'}U_2'>\lambda_2$. Notice this process can be inversed, so the opposite is also true. $\square$



### Comparing Gambles

**Definition: (First Order Stochastically Domination)** $F$ First Order Stochastically Dominate $G$, denoted by $F\succsim _{FOSD} G$, if $\int UdF\geq \int UdG$ for all non-decreasing function $U:\mathbb{R}\to \mathbb{R}$.

**Theorem: (FOSD Property)** $F\succsim _{FOSD} G$ if and only if $F(x)\leq G(x)$ for all $x$.

Proof:

If $F\succsim _{FOSD} G$, then $\int UdF\geq \int UdG$  for all non-decreasing function $U:\mathbb{R}\to \mathbb{R}$. Now by integration by parts, we have $\int_a^b U(x)dF(x) = U(x)F(x)|_a^b-\int_a^bU'(x)F(x)dx = U(b)-\int_a^bU'(x)F(x)dx$. So $\int_a^b U(x)(dF(x)-dG(x)) = \int_a^bU'(x)(G(x)-F(x))dx$. Since $U'(x)\geq 0$, we have $F(x)\leq G(x)$. Suppose for some $x'$ we have $F(x')> G(x')$,  since all the probability distributions are right continuous, we can define $U(x) = 1$ for $x\geq x'$ and 0 for $x< x'$. This will lead to a contradiction that  $\int UdF< \int UdG$. It is trivial to show the inverse of this is also true. $\square$ 

**Definition: (Second Order Stochastically Domination)** $F$ Second Order Stochastically Dominate $G$, denoted by $F\succsim _{SOSD} G$, if $\int UdF\geq \int UdG$ for all non-decreasing and concave function $U:\mathbb{R}\to \mathbb{R}$.

**Claim: (SOSD Property)** $F\succsim _{SOSD} G$ if and only if $\int_{-\infty}^xF(t)dt\leq \int_{-\infty}^xG(t)dt$ for all $x$.



### Anscombe-Aumann Structure

#### Definition

**Definition: (State)** $s\in \Omega$ is the State of a finite possible state world.

**Definition: (Outcomes)** $X = \{x_1,...,x_n\}$ is the set of Outcomes.

**Definition: (Anscombe-Aumann Act)** An Anscombe-Aumann Act is a function $h:\Omega\to \Delta X$, or we can denote it as $h_s\in H = (\Delta X)^\Omega$. We denote the probability of outcome $x$ at state $s$ as $h_s(x)$.

**Definition: (Constant Act)** A Constant Act is defined as an Anscombe-Aumann Act which satisfies $h_s= h_{s'}$ for any $s,s'\in \Omega$.

**Definition: (Affine)** Function $f:\Pi\to\mathbb{R}$ is an Affine if for any $\pi, \rho \in\Pi$, and $\alpha\in [0,1]$, we have $ f(\alpha\pi+(1-\alpha)\rho) = \alpha f(\pi)+(1-\alpha)f(\rho) $.

**Definition: (Linear)** Function $f:\Pi\to\mathbb{R}$ is an Affine if for any $\pi, \rho \in\Pi$, and $\alpha, \beta\in \mathbb{R}$, we have  $f(\alpha\pi+\beta\rho) = \alpha f(\pi)+\beta f(\rho) $.

#### Mixture Space Theorem

**Claim: (Mixture Space Theorem)** A preference on a convex subset of $\mathbb{R}^n$ is complete, transitive, independent and Archimedean if and only if there exists an affine function $U:\Pi\to \mathbb{R}$ representing the preference. Moreover, if $U(.)$ is an affine representation then $V(.)$ is an affine representation of the same preference if and only if there exist $a>0$ and $b\in \mathbb{R}$ such that $V(\pi) = \alpha U(\pi)+b$.

**Claim: (State Dependent Expected Utility)** A preference on a convex subset of $\mathbb{R}^n$ is complete, transitive, independent and Archimedean if and only if there exists a set of Von-Neumann-Morgenstern utility functions $U_1,..,U_m:X\to\mathbb{R}$, such that $U(h) = \sum_s\sum_x h_s(x)U_s(x)$.

#### Subject Probability

**Definition: (Changing Act)** Given an act $h\in \Delta X^\Omega $, $s\in \Omega$, and a lottery $\pi\in \Omega$, define a new act $(h-s,\pi) =(h_1,h_2,...,h_{s-1},\pi,h_{s+1}, ..., h_n)$.

**Definition: (Null State)** A state is Null if for any $h\in \Delta X^\Omega$, any $\pi,\rho \in \Delta X$ we have $(h-s,\pi)\sim (h-s,\rho)$.

**Definition: (State Independence)** a preference is state independent if for all non-null states $s,t\in \Omega$, for all acts $h,g\in \Delta X^\Omega$, any lottery $\pi,\rho \in \Delta X$, $(h-s,\pi)\succsim (h-s,\rho)$ implies $(g-t,\pi)\succsim (g-t,\rho)$.

**Definition: (Monotonicity)** a preference is monotonic if for all acts $h,g\in \Delta X^\Omega$, the constant act $h_s\succ g_s \forall s\in \Omega$ implies $h\succ g$.

**Theorem: (State Independence and Monotonicity)** if a preference is state independent, then it is monotonic.

Proof:

1. Suppose we have $S$ states in total. We know $h_s = (\pi_s,\pi_s,...,\pi_s)\succ g_s = (\rho_s,\rho_s,...,\rho_s)$. By state independence, we have $(h-t,\pi_s)\succ (h-t,\rho_s)$ for any $h$ and any $t$. Suppose it’s not true, i.e. $(h-t,\pi_s)\precsim (h-t,\rho_s)$, by state independence we can write $h_s\sim(h_s-t,\pi_s)\precsim (h_s-t,\rho_s)\precsim...\precsim(g_s-t,\pi_s)\precsim (g_s-t,\rho_s)\sim g_s$, since it works for all state $t$. Contradiction. Hence we have $\pi_s\succ \rho_s$ at each state. 
2. Now want to show that suppose $h\succ g$ and $\pi\succ \rho$ at each state, then $(h-s,\pi)\succ (g-s,\rho)$. By state independence,  $(h-s,\pi)\succ (h-s,\rho)$ implies $(g-s,\pi)\succ (g-s,\rho)$. We only need to show $(h-s,\pi)\succ (g-s,\rho)$, but this is because of the fact that $\pi\succ \rho$ at each state.
3. Now start with $(\pi_1,\pi_1,...,\pi_1)\succ(\rho_1,\rho_1,...,\rho_1)$. By step 2 we have $(\pi_1,\pi_2,...,\pi_1)\succ(\rho_1,\rho_2,...,\rho_1)$. Then repeat using step 2 we will have $(\pi_1,\pi_2,...,\pi_S)\succ(\rho_1,\rho_2,...,\rho_S)$, which is what we want to show. $\square$ 

**Claim: (Expected Utility Theorem)** A preference relation on $H$ is independent , Archimedean, state independent if and only if there exists a Von-Neumann-Morgenstern utility function $U:X\to\mathbb{R}$, such that $U(h) = \sum_s\mu(s)\sum_x h_s(x)U(x)$, where $\mu(s)$ denote the subjective probability of state $s$.



## Production Theory

### Production

#### Production Possibility Set

**Definition: (Production Possibility Set)** The set $Y\subset \mathbb{R}^n$, where $y = (y_1,y_2,...,y_n) \in Y$, and if $y_k>0$ it is the output, if $y_k<0$ it is the input.

**Axiom: (Properties of Production Possibility Set)** The production possibility set satisfies: 

1. (No Free Lunch) $Y\cap \mathbb{R}^n_+ \subset {0}$
2. (Possibility of Inaction) $0\in Y$
3. (Free Disposal) If $y\in Y$, then $y'\in Y$ for all $y'<y$
4. (Irreversibility) If $y\in Y$ and $y\neq 0$, then $-y\notin Y$
5. (Non Increasing Return to Scale) If $y\in Y$ then $\alpha y\in Y$ for all $\alpha \in [0,1]$
6. (Non Decreasing Return to Scale) If $y\in Y$ then $\alpha y\in Y$ for all $\alpha \in [1, +\infty)$
7. (Constant Return to Scale)  If $y\in Y$ then $\alpha y\in Y$ for all $\alpha \in [0, +\infty)$
8. (Increasing Return to Scale) If $y\in Y$ then $\alpha y\in Y$ for all $\alpha \in (1, +\infty)$ and If $y\in Y$ then $\alpha y\notin Y$ for all $\alpha \in (0, 1)$
9. (Decreasing Return to Scale)  If $y\in Y$ then $\alpha y\in Y$ for all $\alpha \in (0,1)$ and If $y\in Y$ then $\alpha y\notin Y$ for all $\alpha \in (1,+\infty)$
10. (Additivity) If $y,y'\in Y$, then $y+y'\in Y$
11. (Convexity) $Y$ is convex
12. (Convex Cone) For any $y,y' \in Y$ and $\alpha,\beta \geq 0$, we have $\alpha y+ \beta y' \in Y$

**Note:** Increasing return to scale and additivity don’t imply each other, especially when the other properties do not hold. Consider a production function where irreversibility doesn’t hold.

**Theorem: (Properties of Production Possibility Set)** the following are true:

1. $Y$ is additive and non-increasing return to scale if and only if it is a convex cone.
2. For any convex  $Y\subset \mathbb{R}^n$ with $0\in Y$, there is a convex $Y'\subset \mathbb{R}^{n+1}$ such that $Y'$ is constant return to scale and $Y' = \{(y,-1)|y\in Y\}$.

Proof:

1. If $Y$ is a convex cone, then by definition it is additive and non-increasing return to scale. If $Y$ is additive and non-increasing return to scale, for any $y,y' \in Y$ and $\alpha,\beta \geq 0$, by additivity $ky\in Y$. Then by non-increasing return to scale $\alpha ky\in Y\space \forall \alpha\in (0,1)$. Then by additivity $\alpha y+ \beta y' \in Y$.
2. Let $Y' = \{\alpha(y,-1)|y\in Y, \forall \alpha>0\}$. By definition $Y'$ is constant return to scale. $\square$

#### Production Function

**Definition: (Production Function)** Let $y\in \mathbb{R}^m_+$ denotes the outputs and $x\in \mathbb{R}^k_+$ denotes the inputs. Suppose $m=1$, then define the production function as $y=f(x)$. The corresponding production possibility set is $Y = \{(-x,y)\in \mathbb{R}^k_-\times\mathbb{R}^m_+|y\leq f(x)\}$.

**Assumption: (Production Function)** The production function $f$ is continuous, strictly increasing and strictly quasi-concave on $\mathbb{R}^n_+$, and $f(0) = 0$.

**Definition: (Isoquant)** Isoquant is a collection of input combinations which keep output fixed, $Q(y) = \{x\in \mathbb{R}^k_+|f(x)=y\}$.

**Theorem: (Properties of Production Function)** The following are true:

1. $Y$ is constant return to scale if and only if $f(t x) = t f(x)$ for all $t>0$
2. $Y$ is increasing return to scale if and only if $f(t x) > t f(x)$ for all $t>1$
3. $Y$ is decreasing return to scale if and only if $f(t x) < t f(x)$ for all $t>1$
4. $Y$ is convex if and only if $f(x)$ is concave

Proof:

1. If $f(t x) = t f(x)$ for all $t>0$, then it is trivial to show that $Y$ is constant return to scale. Now suppose the reverse is true. By definition we have if $y = f(x)$ then $tf(x)\leq f(tx)$ for all $t\geq 0$ and if $y = f(z)$, then $sf(z)\leq f(sz)$ for all $s>0$. Now set $s = 1/t$ and set $z = tx$ we have $tf(x)\geq f(tx)$, hence $tf(x)= f(tx)$.
2. If $f(t x) > t f(x)$ for all $t>1$, then it is trivial to show that $Y$ is increasing return to scale. Now suppose increasing return to scale is true. By definition we have if $y = f(x)$ then $ty < f(tx)$ for all $t>1$ and $(x,y)$. So $f(tx) > tf(x)$.
3. If $f(t x) < t f(x)$ for all $t>1$, then it is trivial to show that $Y$ is decreasing return to scale. Now suppose decreasing return to scale is true. By definition we have if $y = f(x)$ then $ty > f(tx)$ for all $t>1$ and $(x,y)$. So $f(tx) < tf(x)$.
4. This is automatically true by definition. $\square$ 

**Definition: (Separable Production Function)** Let $K$ be the number of inputs. Suppose we can take partition of $K$, i.e. $K_1,...,K_s$, $s\in S$ then the production function is weakly separable if:
$$
\frac{\partial (f_i(x)/f_j(x)) }{\partial x_k} = 0 \space \forall i,j \in K_s,\space  k\notin K_s
$$
where $f_i = \partial f(x)/\partial x_i$. Furthermore, if $S>2$, the production function is strongly separable if:
$$
\frac{\partial (f_i(x)/f_j(x)) }{\partial x_k} = 0 \space \forall i\in K_s,\space \forall j \in K_t,\space  k\notin K_s \cup K_t
$$


### Cost Minimization

**Definition: (Cost Minimization Problem)** The Cost Minimization Problem of the firm is defined as:
$$
C(w,y) = min_{x\in \R^n_k} wx \space s.t.\space f(x)\geq y
$$
**Solution: (Cost Minimization Problem)**

The solution to this problem is the same as the expenditure minimization problem. The existence of the solution comes from the same theorem. The first order condition are $w_i = f_i(x)$. Combine them with the production constraint $f(x) = y$ we can get the solution.

**Claim: (Properties of Cost Function)** If $f$ satisfies our assumptions, the the cost function $C(w,y)$ has the following properties:

1. $C(w,0) = 0$
2. $C(w,y)$ is continuous
3. For $w\gg 0$ $C(w,y)$ is strictly increasing and unbounded above in $y$
4. $C(w,y)$ is increasing in $w$
5. $C(w,y)$ is homogenous of degree 1 in $w$
6. $C(w,y)$ is concave in $w$
7. Shepard’s Lemma is true, i.e. $\partial C(w^0,y^0)/\partial w_i = x_i(w^0,y^0)$

**Definition: (Conditional Input Demand)** The solution to the cost minimization problem is the conditional input demand function, denoted as $x(w,y)$.

**Claim: (Properties of Conditional Input Demand)** Under the assumption of production function, suppose the cost function is twice differentiable, we have

1. $x(w,y)$ is homogeneous of degree 0 in $w$
2. The substitution matrix $\sigma(w,y) = [\partial x_i/\partial w_j]$ is symmetric and negative semi-definite. In particular, this implies that $\partial x_i/\partial w_j\leq 0$ for all $i$. 

**Claim: (Recovering Production Function from Cost Function)** For a given function $C:\mathbb{R}^n_+\times \mathbb{R}_+ \to \mathbb{R}_+$, satisfying properties 1-7 for a cost function, the function $f(x) = max\{y\geq 0|wx\geq c(w,y) \forall w\gg0\}$ is an increasing, unbounded above, quasi-concave function. Moreover, the cost function generated by $f(x)$ is $C(.)$.

**Claim: (Integrability)** If a differentiable function $x:\mathbb{R}^k_+ \times \mathbb{R}_+\to \mathbb{R}^k_+$ is homogenous of degree 0, and $wx(w,y)$ is strictly increasing in $y$, and satisfies symmetry and negative semi-definite of Slutsky matrix, if and only if it is the conditional input demand function generated by some strictly increasing, quasi-concave production function.



### Profit Maximization

**Definition: (Profit Maximization Problem)** The Profit Maximization Problem of the firm is defined as:
$$
\pi(p, w) = max_{y,x\in \R^{k+1}_+} py-wx \space s.t.\space f(x)\geq y
$$
**Note:** When the production function is constant or increasing return to scale, the solution to the profit maximization problem doesn’t exist.

**Solution: (Profit Maximization Problem)** The first order conditions are $pf_i(x)  =w_i$.

**Claim: (Properties of Profit Function)** If $f$ satisfies the assumption, and suppose the profit function exists, then for $(p,w)\gg 0$, we have

1. $\pi(p,w)$ is continuous
2. $\pi(p,w)$ is increasing in $p$
3. $\pi(p,w)$ is decreasing in $w$
4. $\pi(p,w)$ is homogenous of degree 1 in $(p,w)$
5. $\pi(p,w)$ is convex in $(p,w)$
6. $\pi(p,w)$ is differentiable in $(p,w)\gg 0$, and Hoteling's Lemma is true, i.e. $\partial \pi(p^0,w^0)/\partial p = y(p^0,w^0)$ and  $-\partial \pi(p^0,w^0)/\partial w_i = x_i(p^0,w^0)$.

**Definition: (Input Demand and Output Supply)** The solution to the profit maximization problem are the Input Demand and Output Supply functions, i.e. $x(p,w)$ and $y(p,w)$.

**Claim: (Properties of Input and Output)** Under the assumption of production function, suppose the cost function is twice differentiable, we have

1. $x(p,w)$ and $y(p,w)$ are homogeneous of degree 0 in $(p,w)$
2. No inferior goods and no inferior inputs, i.e. $\partial y /\partial p \geq 0 $ and $\partial x_i/\partial w_i \leq 0$
3. The substitution matrix $\sigma(p,w)$ is symmetric and positive semi-definite.

**Claim: (Recovering Production Function from Profit Function)** For a given function $\pi:\mathbb{R}^{n+1}_+\times \mathbb{R}_+ \to \mathbb{R}_+$, satisfying properties 1-7 for a profit function, the function $f(x) = max\{y\geq 0|py-wx\leq \pi(w,y)\space  \forall (p,w)\gg0\}$ is an increasing, unbounded above, quasi-concave function. Moreover, the profit function generated by $f(x)$ is $\pi(.)$.

**Claim: (Integrability)** If a differentiable function $x:\mathbb{R}^k_+ \times \mathbb{R}_+\to \mathbb{R}^k_+$ is homogenous of degree 0, and satisfies symmetry and positive semi-definite of Slutsky matrix, if and only if it is the conditional input demand function generated by some strictly increasing, quasi-concave production function.



### Short Run Problem and Long Run Problem

#### Short Run Cost Minimization

**Definition: (Short Run Cost Minimization Problem)** Let the production function be $f(x,\bar x)$, where $x$ is a vector of variable inputs and $\bar x$ is a vector of fixed inputs. Then the Short Run Cost Minimization Problem is:
$$
SC(w,\bar w, y; \bar x) = min_x wx+\bar w \bar x \space s.t. \space f(x,\bar x)\geq y
$$
And $wx(w,\bar w, y; \bar x)$ is called total variable cost, and $wx(w,\bar w, y; \bar x)+\bar w\bar x$ is called total cost.

**Theorem: (MC and AVC)** When marginal cost is greater than the average variable cost, i.e. $MC>AVC$, $AVC$ is increasing, and vice versa.

Proof:

By definition $AVC = VC(y)/y$, take differentiation we have $\frac{d}{dy}AVC = \frac{y\frac{d}{dy}VC-VC}{y} = MC-AVC$. Hence it has the same sign as $MC-AVC$. $\square$ 

**Corollary: (MC and AVC)** The MC curve will pass through the minimization point of AVC. 

**Theorem: (Relationship between Short Run and Long Run)** By definition we have $C(w,\bar w,y)\leq SC(w,\bar w, y;\bar x)$. Furthermore, let $\bar x(w,\bar w, y) $ denote the optimal choice of input at $(w,\bar w, y)$, then we have $C(w,\bar w, y) = SC(w,\bar w, y; \bar x(w,\bar w, y)  )$. This implies that $\frac{dc(w,\bar w, y)}{dy} = \frac{\partial SC(w,\bar w,y ;\bar x(w,\bar w, y) )}{\partial y}$.

Proof:

$C(w,\bar w,y)\leq SC(w,\bar w, y;\bar x)$ is true because $C(w,\bar w,y)$ is the minimization. We have $C(w,\bar w, y) = SC(w,\bar w, y; \bar x(w,\bar w, y))$. This implies that $\bar x(w,\bar w, y)$ minimizes $SC(w,\bar w, y;\bar x)$, i.e.$\frac{\partial SC(w,\bar w,y ;\bar x(w,\bar w, y) )}{\partial \bar x}=0$. Now take differentiation of the equation $C(w,\bar w, y) = SC(w,\bar w, y; \bar x(w,\bar w, y)  )$, we have $\frac{dc(w,\bar w, y)}{dy} = \frac{\partial SC(w,\bar w,y ;\bar x(w,\bar w, y) )}{\partial y}+\frac{\partial SC(w,\bar w,y ;\bar x(w,\bar w, y) )}{\partial \bar x}\frac{\partial \bar x(w,\bar w, y)}{\partial y} = \frac{\partial SC(w,\bar w,y ;\bar x(w,\bar w, y) )}{\partial y}$. $\square$ 

#### Short Run Profit Maximization

**Definition: (Short Run Profit Maximization Problem)** Let the production function be $f(x,\bar x)$, where $x$ is a vector of variable inputs and $\bar x$ is a vector of fixed inputs. Then the Short Run Profit Maximization Problem is:
$$
\pi(p,w, \bar w; \bar x) = max_{y,x\in \R^{k+1}_+} py-wx-\bar w\bar x \space s.t.\space f(x,\bar x)\geq y
$$
**Claim: (Break Even Point)** The firm will stop producing when $p\leq min(AVC)$ in the short run and it will stop producing when $p\leq min(ATC)$ in the long run.

**Theorem: (Relationship between Short Run and Long Run)** By definition we have $\pi(p,w, \bar w; \bar x) \leq \pi(p,w)$. Furthermore, let $\bar x(p,w,\bar w) $ denote the optimal choice of input at $(p,w,\bar w)$, then we have $\pi(p,w, \bar w; \bar x(p,w,\bar w)) = \pi(p,w)$.

Proof:

$\pi(p,w, \bar w; \bar x) \leq \pi(p,w)$ is true because $\pi(p,w)$ is the maximization. We have $\pi(p,w, \bar w; \bar x(p,w,\bar w)) = \pi(p,w)$. This implies that $\bar x(w,\bar w, y)$ maximize $\pi(p,w, \bar w; \bar x)$, i.e.$\frac{\partial \pi(p,w, \bar w; \bar x(p,w,\bar w) )}{\partial \bar x}=0$. $\square$ 

### Multi Product Firms

**Definition: (Transformation Function)** Given a production set $Y\subset \mathbb{R}^n$ the Transformation Function is $F:Y\to \mathbb{R}$, such that $Y = \{y\in Y|F(y)\leq 0\}$.

**Definition: (Transformation Frontier)** Given a production set $Y\subset \mathbb{R}^n$ the Transformation Frontier is $F:Y\to \mathbb{R}$, such that $Y = \{y\in Y|F(y)= 0\}$.

**Definition: (Marginal Rate of Transformation)** Given a differentiable transformation function $F$ and a point $y$ on the frontier, the Marginal Rate of Transformation for good i and j is defined as $MRT_{i,j} = \frac{\partial F/\partial y_i}{\partial F/ \partial y_j} = -\frac{dy_j}{dy_i}$.

**Definition: (Multi Product Firm Profit Maximization)** Multi Product Firm Profit Maximization Problem is defined as:
$$
\pi(p) = max_{y\in Y} \{py\} = max \{py\} \space s.t. \space F(y) \leq 0
$$
**Theorem: (Existence of Profit)** If $Y$ satisfies non-decreasing return to scale, then either $\pi(p)\leq 0$ or $\pi(p) = +\infty$.

Proof:

Suppose at some $y\in Y$ we have $py>0$, Since $Y$ satisfies non-decreasing return to scale, we have $ty\in Y$ for $t>1$.  So $tpy>py$ is always feasible. As $t\to+\infty$, $\pi\to+\infty$. $\square$ 



## General Equilibrium

### Barter Exchange Economy

#### Setup

**Assumption: (Setup)**

- No production, an endowment economy
- Society admits to the institution of private ownership
- Principle of voluntary and non-coercive trade is respected

**Assumption: (Consumers’ Behavior)** Agents have complete, transitive, continuous, and strictly convex preference over bundles in $\mathbb{R}^n_+$.

**Definition: (Barter Exchange Economy)** An Exchange Economy is defined as:

1. Agents $I  = \{1,2,...,I\}$
2. $\Epsilon = (\succsim_i, e^i)_{i\in I}$ defines an exchange economy
3. Allocation defined as $x = (x^1,...x^I)$

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

**Assumption: (Excess Demand)** The utility functions are continuous, strongly increasing and strictly quasi-concave on $\mathbb{R}^n_+$.

**Theorem: (Properties of Excess Demand)** Under the above assumption about consumer behavior, we have:

1. $z(p)$ is continuous on $\mathbb{R}^n_+$
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

**Assumption: (Consumer’s Behavior)** The utility functions are continuous, strongly increasing and strictly quasi-concave on $\mathbb{R}^n_+$.

**Theorem: (Utility and Aggregate Demand)** If each consumer’s utility satisfies the assumption above, and if the aggregate endowment of each good is positive, then the aggregate excess demand satisfies the following properties:

1. $z(p)$ is continuous on $\mathbb{R}^n_+$
2. $pz(p) = 0\space \forall p\gg 0$
3. If $\{p^m\}$ is a sequence of price vectors in $\mathbb{R}^n_+$ converging to $\bar p \ne 0$, and $\bar p_k = 0$ for some $k$, then for some good $k’$ with $\bar p_k' = 0$ the associated sequence of excess demands for good $k'$ at any price in that sequence, $\{z_{k’}(p^m)\}$, is unbounded above. 

Proof:

Continuity follows from the continuity of individual demands. Walras Law follows from the individual budget constraint. We only need to show the third property.

Suppose $\bar p$ is a price vector such that $p_k = 0$, we need to find a $k'$ such that property 3 is true. We are going to argue with contradiction. Take a sequence of price vectors $p^m \to \bar p$, suppose that the aggregate excess demand $\{z_{k’}(p^m)\}$ is bounded,  then demand $x^{i,m} (p^m, e^i p^m)$ for individual $i$ is bounded. Then there is a converging subsequence $x^{i,m_j} \to x^{i\star}$.

Now construct another allocation $\hat x^i$ such that $\hat x^i_r = x^{i\star}_r$ for $r \neq k$ and  $\hat x^i_k = x^{i\star}_k+1$. Then $\bar p \hat x^{i} =\bar p x^{i\star} = \bar p e^{i}>0$. But since the utility is strongly increasing, we have $u^i(\hat x^i)>u^i(x^{i\star})$.

Now because $u^i$ is continuous, there exist a $t \in(0,1)$, such that $u^i(t\hat x^i)>u^i(x^{i\star})$ and $\bar p t\hat x^{i} <\bar p x^{i\star} = \bar p e^{i}$. Then because as $p^m \to \bar p$, $x^{i,m_j} \to x^{i\star}$, there exist a $m$ such that $u^i(t\hat x^i)>u^i(x^{i,m} (p^m, e^i p^m))$ and $p^m t\hat x^{i} <p^m e^{i}$, which is a contradiction to the fact that $x^{i,m} (p^m, e^i p^m)$ is the solution to the maximizing problem of the consumer. $\square$



### Existence of Equilibrium

**Definition: (Walrasian Equilibrium)** a vector $p^\star \in \mathbb{R}^n_+$ is called a Walrasian Equilibrium if $z(p^\star) = 0$.

**Lemma: (Brower’s Fixed Point Theorem)** If $f:S \to S$ is a continuous function mapping from a non-empty, compact and convex subset of $\mathbb{R}^n_+$ to itself, then there is a fixed point $x^\star\in S$ such that $f(x^\star) = x^\star$.

**Theorem: (Aggregate Excess and Walrasian Equilibrium)** Suppose $z(p)$ has the following properties:

1. $z(p)$ is continuous on $\mathbb{R}^n_+$
2. $pz(p) = 0\space \forall p\gg 0$
3. If $\{p^m\}$ is a sequence of price vectors in $\mathbb{R}^n_+$ converging to $\bar p \ne 0$, and $\bar p_k = 0$ for some $k$, then for some good $k’$ with $\bar p_k' = 0$ the associated sequence of excess demands for good $k'$ , $\{z_{k’}(p^m)\}$, is unbounded above as $p^m\to \bar p$

Then there is a price vector $p^\star \gg 0$ such that $z(p^\star) = 0$, i.e. the Walrasian Equilibrium exists.

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

2. Now take a sequence of price vectors $\{p^\epsilon\}$ that satisfies the above equation, as $\epsilon $ goes to zero. Since $p^\epsilon \in S_\epsilon \space \forall \epsilon>0$, we have $p^\epsilon \in [0,1]$, which is bounded, there exists a subsequence of $\{p^\epsilon\}$ that converges to a price vector, denoted as $p^\star\geq 0$.

   Note that $p^\star\neq 0$ because its components add up to 1. We claim that $p^\star \gg 0$. We argue with contradiction. Suppose there is a $\bar k$ such that $p_\bar k^\star = 0$, by property 3 that is given to us in the first place, there is a $k'$ such that $p_{k'}^\star = 0$ and when $\epsilon$ goes to zero, $z_{k’}(p^\epsilon)$ is unbounded above.

   Then $p_{k'}^\epsilon [n\epsilon +\sum_{m =1}^n max\{0,\bar z_m(p^\epsilon)\}] \leq p_{k'}^\epsilon [n\epsilon +n\}] \to 0$, but $\epsilon +max\{0,\bar z_k(p^\epsilon)\} \to 1$, which means the above equation cannot hold, which is a contradiction.

3. Now we find a price vector $p^\star \gg 0$. Want to show that $z(p^\star) = 0$.

   Note that as $\epsilon\to 0$, the above equation becomes:
   $$
   p_k^\star \sum_{m =1}^nmax\{0,\bar z_m(p^\star)\} = max\{0,\bar z_k(p^\star)\}
   $$
   Multiply both sides by $z_k(p^\star)$ and sum over $k$, we get:
   $$
   0 = p^\star z(p^\star)\sum_{m =1}^nmax\{0,\bar z_m(p^\star)\} = \sum_{k =1}^nz_k(p^\star) max\{0,\bar z_k(p^\star)\}
   $$
   by Walras Law (property 2), we have $p^\star z(p^\star) = 0$. To summary we have:
   $$
   \sum_{k =1}^nz_k(p^\star) max\{0,\bar z_k(p^\star)\}=\sum_{k =1}^nz_k(p^\star) max\{0,min\{1,  z_k(p^\star)\}\} = 0
   $$
   Suppose for some $k$, we have $z_k(p^\star) > 0$, then $\bar z_k(p^\star) > 0$ and hence $z_k(p^\star)\bar z_k(p^\star) > 0$, which means the above equation cannot hold. Hence $z_k(p^\star) \leq 0$ for all $k$.

   Now remember the Walras Law, $\sum_{k=1}^n p^\star_kz_k(p^\star) = 0$ we conclude that $z_k(p^\star) = 0$ for all $k$, i.e. $z(p^\star) = 0$. $\square$

**Corollary: (Existence of Equilibrium)** The Walrasian Equilibrium exists.



### Production Equilibrium

#### Setup

**Assumption: (Setup)**

- There are firms in the economy
- Profit must be distributed
- $\sum_i\theta_{ij} =1$ denote the private ownership of the firm 



#### Aggregate Supply

**Assumption: (Firm)** The firms in the model satisfy the following assumptions:

1. (Nonnegative Profits) $0\in Y^j \subset\mathbb{R}^n$
2. (Inputs are required, imposing continuity) $Y^j$ is closed and bounded
3. (Convexity) $Y^j$ is strictly convex, ruling out constant or increasing return to scale technology, and guarantees the existence of profit maximizing solutions.

 **Definition: (Firm’s Problem)** Firm $j$ solves the following problem:
$$
\pi^j(p) = max_{y^j\in Y^j}p y^j
$$
**Note:** Under the assumption above, for any given price vector $p\gg0$ the solution of the problem is unique, denoted by $y^j(p)$, which is continuous on $\mathbb{R}^n_+$ and the profit function $\pi^j(p) = py^j(p)$ is well defined.

**Definition: (Aggregate Production Possibility)** Define the Aggregate Production Possibility Set as $Y = \{y|y = \sum_{j\in J}y^j\}$.

**Note:** if $\forall j$, $y^j$ satisfies the assumption above, then so will $Y$. Condition 1 and 3 follow directly from the corresponding properties of $y^j$. The closeness follows too only when boundedness is true.

**Theorem: (Aggregate Profit Maximization)** For any price $p\gg 0$, we have $p\bar y \geq py \space \forall y$ if and only if for some $\bar y^j \in Y^j$, we may write $\bar y = \sum_{j\in J}\bar y^j$.

Proof:

1. Take $\bar y \in Y$ that will maximize the aggregate profits, suppose $\bar y = \sum_{j\in J}\bar y^j$ and for some firm $k$, $\bar y^j$ does not maximize firm $k$’s profit. Then there is another $\tilde y^k \in Y^k$ such that  $p\tilde y^k \geq p\bar y^k$, but then the summation of the profit will be $p(\sum_{j\neq k }\bar y^j+\tilde y^j) \geq  p\sum_{j\in J}\bar y^j$, which is a contradiction.
2. Suppose $\{\bar y^j\}$ maximize each firm’s profit, then take the summation we have $p\bar y \geq py \space \forall y$. $\square$

#### Aggregate Demand

**Assumption: (Consumers’ Behavior)** Agents have complete, transitive, continuous, strongly increasing and strictly convex preference over bundles in $\mathbb{R}^n_+$.

**Definition: (Consumer’s Problem)** Consumer $i$ choose $x^i$ to solve:
$$
max_{x\in \R^n_+}U^i(x) \space s.t.px = pe^i + \sum_{j =1}^J \theta_{ij}\pi_j(p)
$$
**Note:** If $y^j$ and $u^i$ satisfies the assumptions above, then the solution of the consumer exists and is unique for $p\gg 0$. Plus, $x^i(p,m^i(p))$ is continuous in $p$ and $m^i(p)$ is also continuous.

#### Existence of the Equilibrium

**Definition: (Walrasian Equilibrium)** a vector $p^\star \in \mathbb{R}^n_+$ is called a Walrasian Equilibrium if 
$$
z(p^\star) = \sum_{i\in I}(x^i(p^\star)-e^i) - \sum_{j\in J} y^j(p^\star)= 0
$$
**Theorem: (Existence of The Equilibrium)** Consider the economy $(u^i,e^i,\theta^{ij},y^j)$ with $i\in I$ and $j\in J$. If All the assumptions are satisfied, and $y+\sum_{i\in I }e_i \gg 0$ for some production vector $y \in \sum_{j\in J}y^j$, then there exists at least one price vector $p^\star\gg 0$ such that $z(p^\star) =0$.

Proof:

We will verify that $z(p)$ satisfies the three properties of the Equilibrium Existence Theorem.

1. $z(p)$ is continuous because of the continuity of the individual demand function and supply function.

2. Walras Law is still true because of budget balance.

3. We want to show that if $p^m \to \bar p $,  and $\exist k$, such that $\bar p_k = 0$, then  $\exist k'$ with  $\bar p_{k'} = 0$, such that the excess demand of $k'$, $z_{k'}(p^m)$  is unbounded as $p^m \to p^\star$.

   If there is some consumers with strictly positive income at the limit price $\bar p$, then this person’s income will remain to be positive at $p^m$ as $p^m \to p^\star$ due to the fact that $m^i(p)$ is continuous. This person’s demand for good $k$ will be unbounded above as  $p_k^m \to 0 $.

   Hence it suffices to show that there is some consumers with strictly positive income at the limit price $\bar p$. 
   
   Because $y+\sum_{i\in I }e_i \gg 0$, for some $y$ we have $\bar p(y+\sum_{i\in I }e_i) > 0$. Consider the sum of consumer’s budget constraint:
   $$
   \sum_{i\in I }m^i(\bar p) =\bar p \sum_{i\in I } e^i +\sum_{i\in I } \sum_{j =1}^J \theta_{ij}\pi_j(p) = \bar p \sum_{i\in I } e^i + \sum_{j =1}^J (\sum_{i\in I }\theta_{ij})\pi_j(p)\\
   = \bar p \sum_{i\in I } e^i + \sum_{j =1}^J \pi_j(p) = \bar p (\sum_{i\in I } e^i +y) >0
   $$
   So there is some person that has strictly positive income, otherwise the above equation would not hold. $\square$



## Welfare Theorem

### Pareto Optimality

#### Pareto Optimality In Barter Economy

**Definition: (Feasible Allocation)** The Feasible Set is defined as $F(e) = \{\sum_{i\in I} x^i= \sum_{i\in I} e^i \}$.

**Definition: (Pareto Optimality)** A feasible allocation $x^\star\in F(e)$ is Pareto Efficient if there is no other feasible allocation such that $x^i \succsim_i x^{*i}$ for all $i$, and there exists a $j$ such that $x^j \succ_j x^{*j}$.

**Definition: (Blocking Coalition)** Let $S\subset I$ be a coalition of consumers, We say $S$ blocks allocation $x$ if there is another allocation $x'$ such that

1. $\sum_{i\in S}x'^i=\sum_{i\in S} e^i$
2. $x'^i \succsim_i x^i\space \forall i\in S$ and $\exist j\in S$ such that $x'^j \succ_j x^j$

**Theorem: (Efficiency of Unblocked Allocation)** Any unblocked allocation is Pareto Optimal.

Proof:

Suppose not. Then the allocation is not Pareto Optimal, so there is is another feasible allocation $y$ such that $x'^i \succsim_i x^i\space \forall i\in I$ and $\exist j\in I$ such that $x'^j \succ_j x^j$, which means $I$ is blocked by itself. $\square $

**Note:** Not all Pareto Optimal allocations are unblocked.

**Definition: (Core)** The Core of an exchange economy, denoted as $ \mathcal{C}(e)$, is the set of all unblocked feasible allocations.

#### Pareto Optimality In Production Economy

**Definition: (Feasible Allocation in Production Economy)** An allocation $(x,y)$ is feasible if $\sum_{i\in I} x^i \leq \sum_{i\in I} e^i + \sum_{j\in J} y^j$.

**Definition: (Pareto Optimality in Production Economy)** A feasible allocation $(x^\star,y^\star)$ is Pareto Efficient if there is no other feasible allocation $(x,y)$ such that $x^i \succsim_i x^{*i}$ for all $i$, and there exists a $j$ such that $x^j \succ_j x^{*j}$.

**Definition: (Blocking Coalition in Production Economy)** Let $S\subset I$ be a coalition of consumers, We say $S$ blocks allocation $(x,y)$ if there is another allocation $(x',y')$ such that

1. $y'\in Y$
2. $\sum_{i\in S}x'^i=\sum_{i\in S} e^i+\sum_{j\in J}y'^j$
3. $x'^i \succsim_i x^i\space \forall i\in S$ and $\exist j\in S$ such that $x'^j \succ_j x^j$

**Definition: (Utility Possibility Set)** The Utility Possibility Set is defined as $U = \{u_i\}_{i\in I }$ such that
$$
U = \{(\bar u_1,..., \bar u_I)\in \R^I|u_i(x^i)\geq \bar u_i \space \forall i\in I \space \& \space x \space feasible \}
$$
**Definition: (Pareto Optimality Alternative Definition)** A feasible allocation $x^\star$ is Pareto Efficient if $\{\bar u\in U|\bar u \geq u^\star\} = \{u^\star\}$ where $u^\star = (u_1(x_1^\star), ..., u_I(x_I^\star))$.

**Definition: (Boundary)** Let $\partial U$ denote the Boundary of the Utility Possibility Set, also known as the utility frontier: $\{u\in U|\nexists u'\in U, u'>u\}$.

**Theorem: (Pareto Optimality Alternative Definition)** A feasible allocation $x^\star$ is Pareto Optimal if and only if $u^\star = (u_1^\star(x_1^\star),..., u_I^\star (x_I^\star)) \in \partial U$.

Proof:

1. Let $x^\star$ be a Pareto Optimal solution, suppose $u(x^\star) \notin \partial U$, then there exists $\bar u \in U$ such that $\bar u > u^\star$, which implies that $x^\star$ is not Pareto Optimal.
2. Let $u(x^\star) \in \partial U$,  suppose  $x^\star$ is not Pareto Optimal, then there exists $\bar u \in U$ such that $\bar u > u^\star$, then $u(x^\star) \notin \partial U$, contradiction. $\square$

#### Solve for Pareto Optimality

**Theorem: (Solution of Pareto Optimality)** let the utility functions $u_i$, for $i\in I $, be continuous. Suppose $u_1$ is strongly increasing, then $x^\star$ is Pareto Optimal if and only if it’s a solution to the following problem:
$$
max\{u_1(x^1)\} \space s.t.\space u_i(x^i)\geq\bar u_i \space \& \space \sum_{i\in I} x^i \leq \sum_{i\in I} e^i + \sum_{j\in J} y^j
$$
for some $(\bar u_2, ..., \bar u_i) \in U_{-1}$.

Proof:

1. Want to show that the Pareto Optimal allocation solves the problem. By definition, if we set $u_i =  u_i^\star$ for $i = 2,...,I$, then $u_1^\star$ is the maximum utility we could get to give to person 1, hence it’s a solution.

2. Want to show the solution to the problem is Pareto Optimal. Let $x^\star$ be the solution, suppose that is not Pareto Optimal, then there is another allocation, $\tilde x$, which is feasible and satisfying $u_i(\tilde x^i) \geq u_i(x^{i\star})$ for all $i$ and there is one $j$ such that $u_j(\tilde x^j) > u_j(x^{j\star})$.

   Case 1: when  $u_1(\tilde x^1) > u_1(x^{1\star})$, then automatically $x^\star $ is not the solution, contradiction.

   Case 2: when $u_k(\tilde x^k) > u_1(x^{k\star})$, for some $k\neq1$, and suppose $\tilde x^k>0$. Without loss of generosity, we could assume that the consumption of the first good of consumer $k$ is greater than zero, i.e. $\tilde x_1^k >0$. Now let $w\in \mathbb{R}^n$ be a vector with $w_1 = 1$ and $w_m = 0$ for $m = 2,...,n$, i.e. $w = (1,0,0,...0)$. by continuity of $u_k$, there is a $\epsilon >0$ such that $u_k(\tilde x^k -\epsilon w) > u_k(x^{k\star})$. 

   Now consider another bundle $\hat x$, where $\hat x^1 = \tilde x^1 +\epsilon w$, $\hat x^i = \tilde x^i$ for $i\neq {1,k}$ and $\hat x^k = \tilde x^k -\epsilon w$. By strongly monotonicity, $u_1(\hat x_1) >u_1(x^\star)$ and $\hat x$ is still feasible and everyone else is getting at least as good as $x^\star$. So $x^\star$ is not the solution, contradiction.

   Case 3: when $u_k(\tilde x^k) > u_k(x^{k\star})$ for some $k\neq1$, and suppose  $\tilde x^k=0$. If $x^{k\star} = 0$, then the equation before would become $u_k(0) > u_k(0)$, which is not possible. Since we know $x^{k\star} \geq0$, this means the only possible case is $x^{k\star} > 0$. Now we can define a new allocation $\hat x$, where $\hat x^1 = x^{1\star} +x^{k\star}$, $\hat x^i = x^{i\star}$ for $i\neq {1,k}$ and $\hat x^k = 0$. Then by strongly monotonicity, $u_1(\hat x_1) >u_1(x^\star)$ and $\hat x$ is still feasible and everyone else is getting at least as good as $x^\star$. So $x^\star$ is not the solution, contradiction. $\square$

#### Social Planner

**Definition: (Social Planner’s Problem)** Let $\lambda \gg 0$, consider the following social planner’s problem:
$$
max \space \{U(x) = \sum_{i\in I } \lambda_i U_i(x^i)\} \space s.t.\space \sum_{i\in I }x^i \leq \sum_{i\in I }e^i +\sum_{j\in J }y^i, \space x^i \gg 0
$$

**Theorem: (Sufficient Condition for Pareto Optimality)** If $x^\star$ is a solution to the social planner’s problem, then $x^\star$ is Pareto Optimal.

Proof:

Let $x^\star$ to be a solution to the social planner’s problem, and suppose $x^\star$ is not Pareto Optimal. Then there exists another allocation $\tilde x$ such that  $u_i(\tilde x^i) \geq u_i(x^{i\star})$ for all $i$, and there exists a $j$ such that $u_j(\tilde x^j) > u_j(x^{j\star})$. Then multiply each side by $\lambda_i$ and add up all the equations, we will get $\sum_{i\in I } \lambda_i u_i(\tilde x^i > \sum_{i\in I } \lambda_i u_i(x^{i\star})$, hence $x^\star$ is not the solution to the above problem, Contradiction. $\square$

**Lemma: (Convexity)** Let $u_i$ be concave, then the utility possibility set is convex.

**Lemma: (Supporting Hyperplane Theorem)** Let $Z \subset \mathbb{R}^n$ be convex, $a\in R^n$ be a point that is not in the interior of $Z$, then there exists a vector $p\in \mathbb{R}^n\backslash\{0\}$ such that $pa\geq pz \space \forall z\in Z$.

**Theorem: (Necessary Condition for Social Planner’s Problem)** Let $u_i$ be concave, $x^\star$ be Pareto Optimal. There exists a vector $\lambda \in \mathbb{R}^I_+\backslash\{0\}$, such that $x^\star$ is a solution to the social planner’s problem.

Proof:

Suppose $x^\star$ is Pareto Optimal. Then $u^\star = (u_1(x^{1\star}),...,u_1(x^{1\star}))$ is on the boundary of the utility possibility set. By Convexity Lemma, $U$ is a convex set. By Supporting Hyperplane Theorem, there exists $\lambda \in \mathbb{R}^I\backslash\{0\}$, such that $\lambda u^\star \geq \lambda u \space \forall u\in U$, hence $\sum_{i\in I }\lambda_i u^{i\star} \geq \sum_{i\in I }\lambda_i u^{i}$. 

It remains to show that $\lambda \geq 0$. Suppose not, then there is a $k$ such that $\lambda_k <0$. Then
$$
\lambda u^\star = \sum_{i\in I }\lambda_i u^{i\star} \geq \sum_{i\neq k }\lambda_i u^{i} +\lambda_k u^{k}
$$
But this is impossible to hold since $u^{k}$ can goes to negative infinity. When it does so, and $\lambda_k <0$, the right hand side of the equation will goes to positive infinity, but the left hand side stays finite, so we get a contradiction. $\square $

**Note:** The social planner problem coincide the competitive equilibrium in the following sense:
$$
\frac{u_1^A}{u_2^A} =\frac{u_1^B}{u_2^B} = \frac{p_1}{p_2} = \frac{\theta_1}{\theta_2}
$$

Notice that the Lagrange multiplier for the market clearing condition coincide with the price of that good.

**Note:** An algorithm to solve for a competitive equilibrium with a given set of $\lambda$ is to set tax $T = \theta(x-e) = \lambda U'(x)(x-e)=0$ and solve for the $\lambda$.



### First Welfare Theorem

**Theorem: (Local Non-satiation)** Suppose the preference is locally non-satiated, $p\gg0$, and $x^{i\star}$ is defined as the solution to the maximizing problem of the consumer given a budget constraint $px^i \leq m_i(p)$. Then we have:
$$
(x^i \succsim_i x^{i\star})\Rightarrow (px^i \geq m_i(p)) \\
(x^i \succ_i x^{i\star})\Rightarrow (px^i > m_i(p))
$$
Proof:

If $x^i \succsim_i x^{i\star}$ and suppose $px^i < m_i(p)$, then by local non-satiation there exists another bundle $\tilde x^i \in B_\epsilon(x^i)$ such that $u_i(\tilde x^i) >u_i(x^{i\star})$ and  $p\tilde x^i < m_i(p)$. Hence $x^{i\star}$ is not the solution to the maximizing problem, contradiction.

If $x^i \succ_i x^{i\star}$ and suppose $px^i \leq m_i(p)$, then  $x^{i\star}$ is not the solution to the maximizing problem, contradiction. $\square$

**Theorem: (First Welfare Theorem)** Suppose that each consumer’s preference are locally non-satiated, then for any allocation $(x^\star,y^\star)$ that forms a Walrasian Equilibrium with some price vector $p^\star$ is Pareto Optimal.

Proof:

Suppose an allocation $(x^\star,y^\star)$ that forms a Walrasian Equilibrium with some price vector $p^\star$ is not Pareto Optimal. Then there is another feasible allocation $(x,y)$ such that $x^i \succsim_i x^{i\star}\space \forall i\in I $, and $\exist i' \space x^{i'} \succ_{i'} x^{i'*}$. by local non-satiation, we have $px^i \geq m_i(p) \space \forall i\in I$ and $px^{i'} > m_{i'}(p)$. If we combine them, we can get:
$$
\sum_{i\in I} p^\star x^i > \sum_{i\in I} p^\star e^i +\sum_{i\in I} \sum_{j\in J} \theta^{ij} p^\star y^{j\star} = \sum_{i\in I} p^\star e^i + \sum_{j\in J} (\sum_{i\in I}\theta^{ij}) p^\star  y^{j\star} \\
=\sum_{i\in I} p^\star e^i + \sum_{j\in J} p^\star y^{j\star}
$$
Since $y^{j\star}$ is the solution to the profit maximization problem of the firm, we have $\sum_{j\in J} p^\star y^{j\star} \geq \sum_{j\in J} p^\star y^{j}$ for any $j$. Combine this with the above equation, we have:
$$
\sum_{i\in I} p^\star x^i >\sum_{i\in I} p^\star e^i + \sum_{j\in J} p^\star y^{j\star} >\sum_{i\in I} p^\star e^i +\sum_{j\in J} p^\star y^{j}
$$
which is impossible if the feasible condition holds. Hence we get a contradiction. $\square$



### Core and Equilibria

#### Core and Equilibria

**Theorem: (Core and Equilibria)** Suppose the preference is locally non-satiated, then the Walrasian Equilibrium Allocation is in the core.

Proof:

Suppose not, and let $(x^\star, y^\star)$ and $p^\star$ be a Walrasian Equilibrium Allocation, which is blocked by a subset $S\subset I$, then we have $x^i \succsim_i x^{i\star}$ for all $i\in S$ and there exists $i'$ such that $x^{i'} \succ_{i'} x^{{i'}*}$, and $\sum_{i\in S} x^i \leq \sum_{i \in S} e^i + \sum_{i \in S} \sum_{j \in J} \theta^{ij} y^j$. Since we have local non-satiation, by the Local Non-satiation Theorem, $p^\star x^i \geq p^\star x^{i\star} = p^\star e^i +\sum_j \theta^{ij} p^\star y^{*j} \space \forall i \in S$ and $p^\star x^{i'} > p^\star e^{i'} +\sum_{j\in J} \theta^{{i'}j} p^\star y^{*j}$. Now since $y^\star$ is the solution to the profit maximization problem, at price $p^\star$ we have $p^\star y^{*j}\geq p^\star y^{j}$. Combine them we can get:
$$
\sum_{i\in S}p^\star x^{i} > \sum_{i\in S}p^\star e^{i} +p^\star\sum_{j\in J} \sum_{i\in S}\theta^{{i}j} y^j
$$
But this cannot hold when feasibility is satisfied. Contradiction. $\square$

#### Replica Economy

**Definition: (r-Ford Replica Economy)** Suppose there are $I$ types of consumers in the basic exchange economy. The r-Ford Replica Economy, denoted as $E_r$, is defined as an economy with $r$ consumers of each type for a total of $rI$ consumers. For any type $i$, all $r$ consumers of that type share the common preference $\succsim_i$ on $\R^n_+$ and have identical endowments $e^i\gg 0$. Assume each preference can be represented by a utility function.

**Definition: (Compare Replica Economy)** If we have two economy and suppose $r>r'$, we say the first replica economy is larger.

**Theorem: (Equal Treatment in the Core)**  If $x$ is an allocation in the core of a r-Ford Replica Economy, then every consumer of type $i$ must have the same bundle according to $x$, i.e. $x^{iq} = x^{iq'}$ for all $i = 1,2,...,I$ and for all $q,q' = 1,2,..., r$.

Proof:

1. We will prove this theorem with contradiction. Suppose an allocation $x$ does not have the equal treatment property, i.e. for all $i$, there are $q,q'= 1,2,...,r$ such that $x^{iq} \neq x^{iq'}$. We want to show this allocation is not in the core of the economy. Since there are only finitely many type of consumers and finitely many replication of each type, there would be a person for each type such that he is worst among his type. Without loss of generality, we assume the first person of each type is the worst one, i.e. $x^{i1}\precsim_i x^{iq}$ for all $q$. 

2. Now define the bundle $\bar x$ as $\bar x^i = \sum_{q=1}^r x^{iq}/r$, the average consumption of each type. We want to show that the consumptions of  first consumer of each type are blocked by $\bar x$. Note that $x^{i1}\precsim_i x^{iq}$ and $x^{iq} \neq x^{iq'}$ implies that $x^{iq} \neq \bar x^{i}$ Because for each type $i$, the preferences are all strictly quasi-convex, we have $x^{i1}\prec_i \bar x^{i}$, i e. the original bundle is blocked by $\bar x$.

3. Now we only need to show that $\bar x$ is attainable by the coalition of the first consumer for each type. Note that we have:
   $$
   \sum_{i=1}^I\bar x^i = \sum_{i=1}^I \sum_{q=1}^r x^{iq}/r =  \sum_{i=1}^I \sum_{q=1}^r e^{iq}/r  = \sum_{i=1}^I e^{iq}
   $$
   Hence bundle $x$ is not in the core. $\square$ 

**Theorem: (Shirking Core Lemma)** Define $C_r = \{x = (x^1,...,X^I)\in F(e)|(X^{11},X^{12},...,X^{1r},...,X^{Ir}) \in Core(E_r) \}$. Then we have $C_r\subset C_{r'}$ if $r>r'$.

Proof:

It suffices to show that for $r>1$, $C_{r+1}\subset C_{r}$, i.e. suppose $x\in C_{r+1}$ we can derive $x\in C_{r}$. Suppose not, then there is another bundle $x'$ such that $x'$ blocks $x$ in r-fold, which means  $x'$ blocks $x$ in 1-fold. If we replicate that to (r+1)-fold, we will have $x'$ blocks $x$ in (r+1)-fold.  Contradiction to the fact that $x$ is in the core. $\square$ 

**Theorem: (WEA Lemma)** An allocation $x$ is an equilibrium allocation for $E_r$ if and only if $x = (x^1,...,x^1,x^2,...,x^2,...,x^I,...,x^I)$, where $(x^1,x^2,...x^I)$ is an equilibrium allocation for $E_1$.

Proof:

1. Suppose $x$ is an equilibrium allocation for $E_r$. So there is a price $p$ to support this equilibrium. Then by previous theorem it is in the core of $E_r$. By previous lemma  $(x^1,x^2,...x^I)$ is in the core of $E_1$. We only need to show that under the same price $p$ it is an equilibrium for $E_1$. Just pick one of each type and combine them as a new set of consumers we will get this statement because $x$ is an equilibrium allocation for $E_r$.
2. Now suppose $x$ is an equilibrium allocation for $E_1$. So there is a price $p$ to support this equilibrium. Then by previous theorem it is in the core of $E_1$. We only need to show that under the same price $p$ it is an equilibrium for $E_r$. Replicate this bundle for r times  we will get this statement because $x$ is an equilibrium allocation for $E_1$. $\square$

**Note:** This lemma implies that the point in the core of $E_1$ which is not the equilibrium cannot be in the core of $E_r$ when $r>1$. 

**Assumption: (Edgeworth Debreu Scarf Theorem)**

- If $x\in C_1$ then $x\gg 0$
- For each $i$, the utility function is differentiable on $R^n_+$ and $\nabla U^i(x)>0$

**Theorem: (Edgeworth Debreu Scarf Theorem)** If $x\in C_r$ for all $r$, then $x$ is a Walrasian equilibrium allocation for $E_1$.

Proof:

Suppose $\tilde x \in C_r$ for every r. We want to show that $\tilde x$ is a Walrasian equilibrium allocation.

1. First we want to show $U^i((1-t)\tilde x ^i + te^i)\leq U^i(\tilde x^i)$ for every $t\in [0,1]$ and every $i$. Suppose this inequality does not hold. Then there is a $\bar t\in [0,1]$ and an $i$, such that $U^i((1-\bar t)\tilde x ^i + \bar te^i) > U^i(\tilde x^i)$. By strictly quasi-concavity, this implies $U^i(\bar x^i) = U^i((1-t)\tilde x ^i + te^i) > U^i(\tilde x^i)$ for all $t\in [0,\bar t]$. By the continuity of the utility function, there is a positive integer $r$ such that $t = \frac{1}{r}$. 

   Now consider a coalition that consists of $r$ type 1 consumers and $r-1$ number of other type consumers. Assign $\bar x^1$ to all of the type 1 consumers and assign $\tilde x^i$ to all the other type consumers. We can conclude that this new bundle is at least as good as the bundle $\tilde x$. We only need to show that this bundle is feasible to make sure it will block the bundle $\tilde x$. Note that we have:
   $$
   r\bar x^1 + (r-1) \sum_{i\neq 1} \tilde x^i  =r[\frac{1}{r}e^1+\frac{r-1}{r}e^1]+(r-1)\sum_{i\neq 1} \tilde x^i \\
   =e^1+(r-1) \sum_{i=1}^I \tilde x^i = e^1+(r-1) \sum_{i=1}^I \tilde e^i = r\bar e^1 + (r-1) \sum_{i\neq 1} \tilde e^i
   $$
   
   which means bundle $\tilde x$ is blocked in $E_r$, contradicting to the fact that $\tilde x \in C_r$. So $U^i((1-t)\tilde x ^i + te^i)\leq U^i(\tilde x^i)$ for every $t\in [0,1]$ and every $i$ is true.
   
2. Now define $F(t) = U^i((1-t)\tilde x ^i + te^i)$. The above statement implies that $F(t)$ attains its maximum at $t = 0$. By Kuhn Tucker Theorem we have $\nabla U^i(\tilde x)(e^i - \tilde x^i)\leq 0$ for all $i$. Now since $\tilde x\in E_1$, it is Pareto efficient. Moreover, by assumption we have $\nabla U^i(\tilde x)\gg 0$. We want to show that $\nabla U^i(\tilde x) = \alpha_{ij} \nabla U^j(\tilde x)$. Suppose not, then at $\tilde x$, $ U^i_n(\tilde x)/U^i_m(\tilde x) > U^j_n(\tilde x)/U^j_m(\tilde x)$, which implies that this bundle $\tilde x$ is not pareto efficient, Contradiction. Note that this is in fact a simple version of second welfare theorem.

   Hence, there is a $p\gg 0$ such $\lambda^i p = \nabla U^i(\tilde x)$ for all $i$. Combine this with the fact that $\nabla U^i(\tilde x)(e^i - \tilde x^i)\leq 0$, we have $p\tilde x^i \geq p e^i$ for all $i$. 

3. We now show that $p\tilde x^i = p e^i$ for all $i$. Suppose not, then there exists $i$ such that $p\tilde x^i > p e^i$. if we sum over $i$, we will get $\sum_{i=1}^I p\tilde x^i > \sum_{i=1}^I p e^i$ Since $\tilde x \in C_r$, it must be feasible in $E_1$, which implies that $\sum_{i=1}^I \tilde x^i \leq \sum_{i=1}^I e^i$. If we product it with $p\gg 0$, we have $\sum_{i=1}^I p\tilde x^i \leq \sum_{i=1}^I pe^i$, which is a contradiction. $\square$




###  Second Welfare Theorem

**Definition: (Equilibrium with Transfers)** Given an economy $\{x^i,\succsim_i, e^i\},\{y^j\}$, an allocation $(x^\star, y^\star)$ and a price vector $p^\star$ constitute an equilibrium with transfers if there are some wealth levels $w = (w_1,...w_I)$ with $\sum_{i\in I }w_i = p^\star e+\sum_{j\in J} p^\star y^j$ where $y^{j\star}$ solves the profit maximization problem, and for each $i$, $x^\star$ solves the utility maximizing problem with the wealth level assigned to them, and the feasible condition holds, i.e. we have $\sum_{i\in I} x^{i\star} \leq \sum_{i \in I} e^{i\star} + \sum_{j \in J} y^{j\star}$.

**Definition: (Income Transfer)** Define the Income Transfer of individual $i$ as $T_i = w_i - [p^\star e_i+p^\star\sum_{j \in J} \theta^{ij}y^{j\star}]$.

**Definition: (Quasi-Equilibrium)** Given an economy $\{x^i,\succsim_i, e^i\},\{y^j\}$, an allocation $(x^\star, y^\star)$ and a price vector $p^\star$ constitute a Quasi-Equilibrium with transfers if there are some wealth levels $w = (w_1,...w_I)$ with $\sum_{i\in I }w_i = p^\star e+\sum_{j\in J} p^\star y^j$ such that:

1. $\forall j \in J, \space p^\star y^j \leq p^\star y^{j\star} $ for all $y^j\in Y^j$
2. $\forall i \in I, \space x^i \succ_i x^{i\star} $ implies that $p^\star x^i \geq w_i $
3. Feasibility is still true, i.e. $\sum_{i\in I} x^{i\star} \leq \sum_{i \in I} e^{i\star} + \sum_{j \in J} y^{j\star}$

**Note:** The Definition of Quasi-Equilibrium will eliminate the problem of boundary solutions. Convexity ensures the existence of a hyperplane that support the better-than set.

**Lemma: (Separating Hyperplane Theorem)** If $A$ and $B$ are two disjoint convex subset of $\mathbb{R}^n$, then there exist a vector $p$, such that $pz\geq r$ for all $z \in A$, and $pz\leq r$ for all $z \in B$.

**Theorem: (Second Welfare Theorem)** Consider an economy $\{x^i,\succsim_i, e^i\},\{y^j\}$, we assume that $Y^j$ are convex for all $j\in J $, the preferences are convex and locally non-satiated. for all $i \in I$, then for each Pareto Optimal allocation $(x^\star, y^\star)$, there exists a price vector $p^\star \neq 0$, such that $(x^\star, y^\star)$ forms a Quasi-Equilibrium with transfers.

Proof:

1. Aggregation

   Start with a Pareto Optimal allocation $(x^\star, y^\star)$, define the strictly-better-than sets as $V_i = \{x^i \in \mathbb{R}^n| x^i \succ_i x^{i\star}\}$, and define $V = \sum_{i\in I} V_i$. Since we have that preferences are convex, which means for any two bundles $x'$ and $x''$, suppose $x' \succsim_ix''$, then for any $\theta \in [0,1]$, we have $\theta x'+(1-\theta) x''\succsim_ix''$,  i.e. $V_i$ are convex. Take the sum of finitely many convex set and we will still get a convex set, so $V$ is also convex.

   Now we aggregate all the firms and define the aggregate production set as $Y = \sum_{j\in J}Y^j = \{\sum_{j\in J}y^j\in \mathbb{R}^n|y^j\in Y^j \space \forall j\in J\}$, and the set of attainable consumption bundles as $Y+\{e\}$. Since  $Y^j$ are convex, we can conclude that $Y$ is also convex, and so is $Y+\{e\}$.

2. Separation

   Now want to show that $(Y+{e}) \cap V = \varnothing $. Because $(x^\star, y^\star)$ is Pareto Optimal, this must be true, otherwise there will exist a $x^{\star\star}$ in the intersection area such that $x^{i\star\star} \succ_i x^{i\star}$, which is still feasible, contradicting to the fact that $(x^\star, y^\star)$ is Pareto Optimal.

   Now $Y+{e}$ and $V$ are two convex and disjoint set, by the Separating Hyperplane Theorem, there exists a vector $p\neq 0$, such that $pz\geq r$ for all $z\in V$ and $pz\leq r$ for all $z\in Y+\{e\}$.

   We claim that if $x_i \succsim_i x_i^\star$ for all $i$, then $p x \geq r$. Take any  $x_i \succsim_i x_i^\star$, by local non-satiation, there exists $\hat x_i \in B_\epsilon(x_i)$ such that $\hat x_i \succ_i x_i^\star$, hence $\hat x_i \in V_i$ and $\sum_{i\in I}\hat x_i \in V$. So $p \sum_{i\in I}\hat x_i \geq r$ by the separation. Now take a sequence of $\hat x_i \to x_i$, then we have $p \sum_{i\in I} x_i \geq r$, which is what we claimed to be true. Now apply the result to $x_i = x_i^\star$, we have $x_i^\star \succsim_i x_i^\star$, so by the claim we have $p x^\star \geq r$. 

   Similarly, the separation gives us $pz\leq r$ for all $z = (\sum_{j\in J}y^{j}+e)\in Y+\{e\}$, which can be rewrite as $p(\sum_{j\in J}y^{j}+e)\leq r$. Remember $(x^\star, y^\star)$ is Pareto Optimal in the first place, and all Pareto Optimal allocations are feasible, i.e. $\sum_{i\in I} x_i^\star  \leq \sum_{j\in J}y^{j\star}+e$. Multiply by the price, we get $r \leq p\sum_{i\in I} x_i^\star  \leq p(\sum_{j\in J}y^{j\star}+e) \leq r$. 

   In a word, we conclude that $r = p\sum_{i\in I} x_i^\star  = p(\sum_{j\in J}y^{j\star}+e) $.

3. Decentralization

   Last we want to show that $x^\star$ satisfies the consumer’s conditions of being a part of the Quasi-Equilibrium at price $p = p^\star$, i.e. we want to show that $\forall i \in I, \space x^i \succ_i x^{i\star} $ implies that $p^\star x^i \geq w_i $ for some $w_i$.

   Suppose for person $k$ we have $x^k \succ_k x^{k\star} $, define $\hat x^i = x^{i\star}$ for $i\neq k$ and $\hat x^k = x^{k}$ then use the claim from step 2, we get that  $\hat x_i \succsim_i x_i^\star$ for all $i$, then $p \hat x \geq r$. Since from step 2 we have $r = p\sum_{i\in I} x_i $, we have the following equation:
   $$
   p(x_k+\sum_{i\neq k} x_k^\star) = p \hat x \geq r = p\sum_{i\in I} x_i^\star
   $$
   Hence $px_k \geq px_k^\star$.

   Similarly, we want to show that $\forall j \in J, \space p^\star y^j \leq p^\star y^{j\star} $ for all $y^j\in Y^j$. Note that following similar steps, we have:
   $$
   p(e+y_k+\sum_{j\neq k} y_k^\star) = p (e+\hat y) \leq r = p(e+\sum_{j\in J} x_j^\star)
   $$
   Hence $py^j \leq py^{j\star} $.

   In conclusion, $(x^\star, y^\star), p^\star$ forms a Quasi-Equilibrium with transfers. $\square$

**Theorem: (Quasi-Equilibrium and Competitive Equilibrium)** Suppose $X^i$ is convex and the preference is continuous, and  $(x^\star, y^\star)$  along with the price $p^*$ forms a Quasi-Equilibrium with transfers. If there is a consumption vector $x^i$ such that $p^\star x^i<w^i$, then it forms a competitive equilibrium.

Proof:

By the definition of a competitive equilibrium, it equivalent to show that if $x^i\succ x^{i\star}$ implies $p^\star x^i \geq w^i$, then $x^i\succ x^{i\star}$ implies $p^\star x^i > w^i$. Suppose this is not true, i.e. there is an allocation such that $\bar x^i\succ x^{i\star}$ with $p^\star \bar x^i = w^i$. By the cheaper consumption assumption, there is a consumption vector $\tilde x^i$ such that $p^\star \tilde x^i<w^i$. Since the preference is continuous, there is a $\alpha\in (0,1)$, such that $\alpha \bar x^i+(1-\alpha)\tilde x^i \succ x^{i\star}$ and $p^\star (\alpha\bar x^i+(1-\alpha)\tilde x^i)< w^i$, which is impossible since we found a bundle that is preferred to $x^{i\star}$ and cost less than $w^i$, contradicting to the fact that $x^{i\star}$ is the maximized solution. $\square$ 

**Corollary: (Quasi-Equilibrium and Competitive Equilibrium)** Suppose $X^i$ is convex and the preference is continuous, and  $(x^\star, y^\star)$  along with the price $p^*$ forms a Quasi-Equilibrium with transfers. If $w^i>0$ for all $i$, then it forms a competitive equilibrium.




### Application

#### Labor

**Definition: (Labor Market Equilibrium)** An allocation $(x^1,...,x^I, n^1, ...,n^I)$, where $x^i$ denotes the consumption of individual $i$ and $n^i$ denotes the labor input of individual $i$, and a price vector $(p,w)$, where $p$ is the price vector of the goods and $w$ is wage, constitute a Labor Market Equilibrium such that:

1. The firm is maximizing it’s profit $\pi = py-\sum_i wn$ subject to $l^i\geq 0$ and $y\leq f(n)$
2. For every $i$, $(x^i, n^i)$ maximizes the individual’s utility subject to the budget constraint $px^i \leq pe^i+ wn^i$
3. Markets clear, i.e. $\sum_i x^i = e^i$ and $\sum_i n^i = $n for all $i$

#### Public Goods

**Definition: (Lindahl Equilibrium)** A Lindahl Equilibrium for the public goods economy is a price equilibrium with transfers for the artificial economy with personalized commodities. That is, an allocation $(x^1,...,x^I, q,z)$, where $x^i$ denotes the private good of individual $i$, $q$ denotes the amount of public good, and $z$ denotes the input vector of the private goods, and a price vector $(p,r)$, where $p$ is the price vector of the private goods and $r$ is the price vector of the public goods for the agents, constitute a Lindahl Equilibrium if there is a set of wealth levels $(w_1,...,w_I)$ satisfying $\sum_iw_i = \sum_ipx^i+ (\sum_i r_i)q-pz$, note that all the terms on the right hand side is the product of vectors, such that:

1. $q\leq f(z)$ and the firm is maximizing it’s profit $\pi = (\sum_ir_i)q-pz$ subject to $z\geq 0$ and $q \leq f(z)$.
2. For every $i$, $(x^i, q^d_i)$ maximizes the individual’s utility subject to the budget constraint $px^i+r_iq^d_i \leq w_i$
3. Markets clear, i.e. $\sum_i x^i+z = e^i$ and $q^d_i = q$ for all $i$

#### Non-convex Production Technology

**Note:** When the production technology is not convex, the second welfare theorem might be violated.

**Claim: (Marginal Cost Price Equilibrium)** Consider an economy $\{x^i,\succsim_i, e^i\},\{y^j\}$, we assume that $Y^j$ are non-convex, the preferences are convex and locally non-satiated. If $(x^\star, y^\star)$ is Pareto optimal, then there exists a price vector $p$ and wealth levels $w$ with $\sum_iw_i = \sum_ipe^i + \sum_j py^{\star j}$, such that:

1. For any firm $j$ we have $p = \gamma_j \nabla F_j(y^{\star j})$ for some $\gamma_j>0$
2. For any $i$, $x^{\star i}$ maximizes the utility function subject to the budget constraint $px^i\leq w_i$
3. Market clears, i.e. $\sum_ix^{\star i} = \sum_ie ^i + \sum_j y^{\star j}$



###  Time and Uncertainty

#### Arrow Deberu Equilibrium

**Assumption: (Setup)** 

- There are $L$ commodities and $S$ states in the world
- $x^i\in \R^{LS}$ denotes the consumption bundle of individual $i$, $y^j\in Y^j\subset \R^{LS}$ denotes the production plan of firm $j$
- For each preference there exists an utility function satisfying the expected utility property and has a state independent representation, i.e. $U_i(x^i) = \sum_{s\in S} \pi_{si}U_i(x^i_s)$, where $\{\pi_{si}\}$ is the subjective probability of person $i$

**Definition: (State Contingent Commodity)** A State Contingent Commodity is a title to deliver or receive some amount of the good if a particular state occurs.

**Definition: (Budget Set)** The Budget Set is defined as $B_i(p,e_i) = \{ x_i|\sum_{s\in S} p_sx^i_s \leq  \sum_{s\in S} p_se^i_s + \sum_{j\in J} \theta^{ij}\sum_{s\in S} p_s y^j_s  \}$.

**Definition: (Arrow Deberu Equilibrium)** An Arrow Deberu Equilibrium is defined as an allocation $(x^\star, y^\star)\in \R^{ILS} \times \R^{JLS}$ and a price vector $p^\star\in \R^{LS}_+$ which satisfies the following:

1. For each $i\in I$, $x^\star$ maximizes utility, i.e. $U_i(x^{\star i}) \geq U_i(x^{i})$ for all $x^i\in B_i(p^\star,e^i)$
2. For each $j\in J$, $y^\star$ maximizes profit, i.e. $p^\star y^{\star j} \geq p^\star y^j$ for all $y^j\in Y^j$ 
3. All markets clear, i.e. $\sum_{i=1}^I x^{\star i}_s = \sum_{i=1}^I e^i_s + \sum_{j=1}^Jy^{\star j}_s$ for all $s\in S$ 

**Theorem: (Pareto Allocations in ADE)** Suppose $\pi_{si}/\pi_{s'i} = \pi_{si'}/\pi_{s'i'}$ for all $s,s'\in S$ and for al $i,i'\in I$. then the Pareto optimal allocation satisfies $\frac{\partial U_i(x^i)/ \partial x^i_{sn}}{ \partial U_i(x^i)/ \partial x^i_{s'm}}= \frac{ \partial U_{i'}(x^{i'})/ \partial x^{i'}_{sn}}{\partial U_{i'}(x^{i'})/ \partial x^{i'}_{s'm}}$.

Proof:

The Pareto optimal allocations requires that $MRS^i_{nm} = MRS^{i'}_{nm}$. Since $U_i(x^i) = \sum_{s\in S} \pi_{si}U_i(x^i_s)$, we can plug it in and get $\frac{\pi_{si} \partial U_i(x^i)/ \partial x^i_{sn}}{\pi_{s'i} \partial U_i(x^i)/ \partial x^i_{s'm}}= \frac{\pi_{si'} \partial U_{i'}(x^{i'})/ \partial x^{i'}_{sn}}{\pi_{s'i'}\partial U_{i'}(x^{i'})/ \partial x^{i'}_{s'm}}$. However, since $\pi_{si}/\pi_{s'i} = \pi_{si'}/\pi_{s'i'}$, we have $\frac{\partial U_i(x^i)/ \partial x^i_{sn}}{ \partial U_i(x^i)/ \partial x^i_{s'm}}= \frac{ \partial U_{i'}(x^{i'})/ \partial x^{i'}_{sn}}{\partial U_{i'}(x^{i'})/ \partial x^{i'}_{s'm}}$. $\square$

**Theorem: (Price Relationship in ADE)** Suppose $\pi_{si}/\pi_{s'i} = \pi_{si'}/\pi_{s'i'}$ for all $s,s'\in S$ and for all $i,i'\in I$. Suppose given $s,s'\in S$, we have  $\sum_{i=1}^I e^i_s + \sum_{j=1}^Jy^{\star j}_s > \sum_{i=1}^I e^i_{s'} + \sum_{j=1}^Jy^{\star j}_{s'}$, then the ADE price satisfies $p_{sn}/p_{s'n} < \pi_{s}/  \pi_{s'}$.

Proof:

At ADE we have $p_{sn}/p_{s'n} = \frac{\pi_{si} \partial U_i(x^i)/ \partial x^i_{sn}}{\pi_{s'i} \partial U_i(x^i)/ \partial x^i_{s'n}}$. It suffices to show that $\phi = \frac{\partial U_i(x^i)/ \partial x^i_{sn}}{\partial U_i(x^i)/ \partial x^i_{s'n}}< 1$. Suppose $\phi \geq 1$, we have  $\partial U_i(x^i)/ \partial x^i_{sn}\geq \partial U_i(x^i)/ \partial x^i_{s'n}$. By assumption we have $U_i(.)$ is an increasing and strictly concave function. This implies $x^i_{sn}\leq x^i_{s'n}$, for all $n$, and for all $i,i'\in I$.

Now sum over $i,i'\in I$, we have $\sum_{i\in I} x^i_{sn}\leq \sum_{i'\in I} x^i_{s'n}$. By market clearing this implies $\sum_{i=1}^I e^i_s + \sum_{j=1}^Jy^{\star j}_s \leq \sum_{i=1}^I e^i_{s'} + \sum_{j=1}^Jy^{\star j}_{s'}$, contradicting to the condition we have. $\square$ 

#### Radner Sequential Equilibrium

**Theorem: (No Spot Market)** Given an ADE, there is no incentive to trade in spot markets.

Proof:

Suppose there are trades in the spot market. Then after the trading in the spot markets, there is a state $t$ and a feasible bundle $(x_{t1},..., x_{tL})$ where $x_{tl}\in \R^I$ that consumers prefer weakly to $x_{tl}^\star$ with one consumer’s preference being strict, i.e. for all $i$, we have $(x_{11}^\star,..., x_{1L}^\star, ..., x_{t1},..., x_{tL}, ..., x_{S1}^\star,..., x_{SL}^\star)\succsim (x_{11}^\star,...x_{SL}^\star)$, with strictly preference for at least one $i$.

However, this is impossible because of the first welfare theorem. So that means given an ADE solution, there is no incentive to trade in spot markets. $\square$

**Definition: (Arrow Securities)** Suppose there is only one good that is traded at both date 0 and date 1, and the rest of the goods are traded at only date 1. Then the good that is traded in both periods is called the Arrow Securities.

**Definition: (Radner Sequential Equilibrium)** A collection formed by a price vector $q = (q_1,...,q_S)\in \R^S$ for contingent first good commodities at $t = 0$, a spot price vector $p_s = (p_1,...,p_L)_s \in \R^L$ for each state $s$ and for every consumer $i$, consumption plans $z_i^\star = (z_{1i}^\star，..., z_{Si}^\star)\in \R^S$ at $t = 0$, and $x_i^\star = (x_{1i}^\star，..., x_{Si}^\star)\in \R^L\times \R^S$ at $t = 1$ constitutes a Radner Equilibrium if:

1. for every individual, the consumption plans $(z_i^\star, z_i^\star)$ solve the following problem:
   $$
   max\space U_i(x_{1i},...,x_{Si}) \\
   s.t. \space \sum_s q_sz_{si}\leq 0 \\
   p_sx_{si}\leq p_s e^i_s+p_{1s}z_{si} \space \forall s
   $$

2. Markets clear, i.e. $\sum_iz_{si}^\star \leq 0$ and $\sum_i x_{si}^\star \leq \sum_i e_{s}^i$ for all $s$.

**Theorem: (Duality)** An Arrow Deberu Equilibrium is equivalent to a Radner Sequential Equilibrium.

Proof:

1. Suppose an ADE allocation is given, then $p_s$ is known. Let $q_s = p_{1s}$ for all $s$. With this we claim that for every consumer $i$, the budget set of the Arrow-Debreu problem is identical to the budget set of the Radner problem, i.e.
   $$
   B^{AD}_i = \{x\in \R^{LS}_+| \sum_s p_s(x_{si}-e_s^i)\leq 0  \} \\
   = B^{RS}_i = \{x\in \R^{LS}_+| \sum_s q_sz_{si}\leq 0, \space p_sx_{si}\leq p_s e^i_s+p_{1s}z_{si} \space \forall s\}
   $$
   For any point $x\in B_i^{AD}$, denote $z = (1/p_{1s})p_s(x_{si}-e^i_s)$. Then obviously we have $\sum_s q_sz_{si}\leq 0$ and $p_sx_{si}= p_s e^i_s+p_{1s}z_{si}$. So $x\in B_i^{RS}$. Hence $B_i^{AD}\subset B_i^{RS}$. Conversely, for any point $x\in B_i^{RS}$, we have $\sum_s p_s(x_{si}-e_s^i) \leq \sum_s q_sz_{si}\leq 0$. So $x\in B_i^{AD}$. Hence $B_i^{RS}\subset B_i^{AD}$. Hence we conclude that $B^{AD}_i = B^{RS}_i$. Then if an allocation is an ADE it is also a RSE. Note that the market clearing condition holds automatically.

2. Suppose an RSE allocation is given, then $(p_s, q_s)$ is known. We can choose $\mu_s$ so that $\mu_sp_{1s} = q_s$. So we can rewrite the budget set of the Radner problem as:
   $$
   B^{RS}_i = \{x\in \R^{LS}_+| \sum_s q_sz_{si}\leq 0, \space \mu_sp_s(x_{si}-e^i_s)\leq q_sz_{si} \space \forall s\}
   $$
   By similar arguments we have $B^{AD}_i = B^{RS}_i$, again. Then if an allocation is an RSE it is also a ADE. Note that the market clearing condition holds automatically, again. $\square$ 

   