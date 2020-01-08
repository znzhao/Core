# MICRO ECONOMICS

## Preference Theory

### Preference

#### Order Theory

**Definition: (Binary Relation)** A Binary Relation on $X$ is a subset $R$ on $X\times X$, if $(x,y) \in R$, we write $xRy$ and $xRyRz$. 

**Definition: (Reflexivity)** A relationship is reflexive if $xRx\in R$.

**Definition: (Transitivity)** A relationship is transitive if $xRyRz in R$ implies $xRz\in R$.

**Definition: (Completeness)** A relationship is complete if either $xRy\in R$ or $yRx\in R$.

**Definition: (Symmetry)** A relationship is symmetric if $xRy\in R$ implies $yRx\in R$.

**Definition: (Anti-Symmetry)** A relationship is anti-symmetric if $xRyRx\in R$ and implies $y=x$.

**Definition: (Preorder)** $R$ is a Preorder if $R$ is reflexive and transitive.

**Definition: (Partial Order)** R is a Partial Order if $R$ is transitive and antisymmetric.

**Definition: (Linear Order)** R is a Linear Order if $R$ is a complete partial order.

#### Preference

**Assumption: (Consumption)** The consumer has preferences over consumption bundle $X$, which is a nonempty, convex, compact subset of $\R^n$. $0$ is always in $X$.

**Definition: (Preference)** A Preference relation is a binary relation on the set of alternatives $X$, denoted as $"\succsim"$.

**Definition: (Strict Preference)** A Strict Preference relation is a binary relation on the set of alternatives $X$, denoted as $"\succ"$, if $x\succsim y$ but $y\nsucceq x$.

**Definition: (Indifferent Preference)** An Indifferent Preference relation is a binary relation on the set of alternatives $X$, denoted as $"\succ"$, if $x\succsim y$ but $y\nsucceq x$.

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

**Theorem: (Ranking)** Given a finite set of bundles $A\subset \R^n_+$, if the preference relation satisfies A1 and A2, then bundles in A can be ranked in a list consistent with the preference.

Proof:

It suffices to show that there is a maximum of $A$. Define an algorithm to find this item. Start with the first item in the set. Suppose next item is preferred to the item in hand, switch the items, i.e. if $x^m\succsim x^*$ but  $x^m\nsucceq x^*$ do the switching. Keep doing this until we compare every item in the set.

The only potential trouble happens when we switch the items. We want to show that $x^*$ is preferred to any other item before the switching. Suppose there is no switching before. This implies that $x^1\succsim x^i$ for $i = 2,3,..., m-1$. From the switching we know that $x^m \succsim x^1$, by Transitivity, we have $x^* = x^m \succsim x^i$ for $i<m$. Now suppose there are $k$ numbers of switching happened before. We have $x^{m_k} \succsim x^i $ for $i$ between $m_{k-1}$ and $m_k$, plus we have $x^{m_k} \succsim x^{m_{k-1}} $. This implies that $x^* = x^m \succsim x^i$ for any $i<m$.  If we repeat this algorithm, we will have $x^*\succsim x^i$ for any $i \in X$, i.e. $x^*$ is the maximum. $\square$

**Axiom: (A3 - Continuity)** For any bundle $x$, the set $\succsim(x)$ and $\precsim(x)$ are closed, or the set $\succ(x)$ and $\prec(x)$ are open.

**Theorem: (Continuity)** Suppose a preference is complete, transitive and continuous. Then for any $x\in X$, $y\in \succ(x)$ and $z\in \prec(x)$, there is a number $t\in (0,1)$ such that $ty+(1-t)z \in \sim(x)$.

Proof:

Define a subset of real number: $T = \{t\in (0,1)|ty+(1-t)z \in \succsim(x)\}$. Defined $t_0 = inf(T)$. Claim that $t_0 \in \sim(x)$. Suppose $t_0\nsim x$, then either $t_0\prec x$ or $ t_0\succ x$. Suppose $t_0\prec x$, then since $\prec(x)$ is open, there is a $t>t_0$ such that $ty+(1-t)z \in \prec(x)$, contradicting to the fact that $t_0$ is the infimum. Suppose $t_0\succ x$, then since $\succ(x)$ is open, there is a $t<t_0$ such that $ty+(1-t)z \in \succ(x)$, again contradicting to the fact that $t_0$ is the infimum. $\square$

**Axiom: (A4’ - Local Non-Satiation)** For any $x$, for any $\epsilon>0$, there is another bundle $y\in B_\epsilon(x)$ such that $y\succ x$.

**Axiom: (A4 - Strict Monotonicity)** For any $x$ and $y$, if $y\geq x$ then  $y\succsim x$, and if if $y\gg x$ then  $y\succ x$.

**Lemma: (Local Non-Satiation and Strictly Monotonicity)** If a preference is strictly monotonic then it is locally non-satiated.

**Axiom: (A5’ - Convexity)** If $y\succsim x$, then $ty+(1-t)x\succsim x$ for any $t\in [0,1]$. 

**Axiom: (A5 - Strict Convexity)** If $y\succsim x$, and $y\neq x$, then $ty+(1-t)x\succ x$ for any $t\in (0,1)$.

 **Axiom: (A6 - Homothetic)** If $y\sim x$, then $ty\sim tx$ for any $t>0$.



### Utility Function

#### Existence of Utility Functions

**Definition: (Utility Function)** A function $U:\R^n_+\to \R$ is called a utility function representing the preference if for any $x,y\in X$, $U(x)\geq U(y)$ if and only if $x\succsim y$.

**Theorem: (Existence of Utility Function)** If the preference is complete, transitive, continuous, and strictly monatomic, then there is a real-valued and continuous function representing the preference.

Proof:

Let $e = [1,1,...,1]$ be a vector in $\R^n$. For any $x\in X$, define $U(x)$ so that $x\sim U(x)e$. We claim that such a number is well defined.

1. First we show that this number exists. Consider the following two sets: $A = \{t\geq 0|te\succsim x\}$ and $B = \{t\leq 0|te\precsim x\}$. Want to show that $A\cap B \neq \phi$. By continuity, both sets are closed. By strict monotonicity and transitivity, if $t_0\in A$, then $\forall t>t_0$ we have $t\in A$. Similarly, if $t_0\in B$, then $\forall t<t_0$ we have $t\in B$. So $A = [t_1,+\infty]$, and $B = [0,t_2]$. Suppose $t_1>t_2$, this would violate the completeness of the preference. Hence $t_1\leq t_2$, this number always exists.
2. Second we show that such a number is unique. Suppose $t_0<t_1$ and $x\sim t_0e\sim t_1 e$, by strict monatomicity, we have $t_0e\prec t_1 e$, which is a contradiction.

Now we will show that $U(x)$ represents the preference, i.e. $x\succsim y$ if and only if $U(x)\geq U(y)$. We have $U(x)e\sim x\succsim y\sim U(y)e$, and the statement is true as a result of strictly monotonicity.

The last step is to show $U(x)$ is continuous. It suffices to show that $U^{-1}(a,b)$ is an open set. $U^{-1}(a,b) = \{x\in X|a<U(x)<b\} = \{x\in X|ae \prec U(x)e \prec be\}  =  \{x\in X|ae \prec x \prec be\} = \succ(ae) \cap \prec(be)$. By continuity, we have both sets are opens, then the intersection of them is also open. $\square$

#### Properties

**Lemma: (Utility and Preference)** $U(x)> U(y)$ if and only if $x\succ y$ and $U(x) =  U(y)$ if and only if $x\sim y$.

**Theorem: (Monotonic Transformation)** If $U$ is a function that represents the preference, and $V$ is another function representing the same preference, then $V = g(U)$ for some strictly increasing function $g:\R\to \R$. Inversely, if  $V = g(U)$ for some strictly increasing function $g:\R\to \R$, then $V$ is another function representing the same preference.

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
\frac{\partial L}{\partial x_i} = \lambda p_i+\mu_i \\
\lambda (I-px) = 0\\
\mu_i x_i = 0
$$
**Definition: (Marginal Utility)** The marginal utility is defined as $MU_i = \partial U/\partial x_i$.

**Definition: (Marginal Rate of Substitution)** The Marginal Rate of Substitution is defined as $MRS_{ij} = MU_i/MU_j$.

**Theorem: (Kuhn-Tucker Theorem)** Suppose $U$ is strictly quasi-concave and differentiable, $(p,I)\gg 0$, then if $(x^*,\lambda^*)\gg 0 $ solve the first order conditions, then $(x^*,\lambda^*)$ solve the consumer’s problem.

Proof:

First notice one fact: when $x^1 \neq x$, $\nabla U(x)\neq 0$, and $U(x^1)>U(x)$, then $\nabla U(x)(x^1-x)>0$.

Now prove the statement. Suppose not, the there is another solution $(x^1,\lambda^1)$ such that $U(x^1)>U(x^*)$. By the fact above, we have $\nabla U(x^*)(x^1-x^*)>0$, and $px^1\leq I$. Notice that since $(x^*,\lambda^*)$ solve the Kuhn-Tucker conditions, we have $\nabla U(x^*) = \lambda^*p$. By assumption, $\lambda^*p\gg 0$, so $\nabla U(x^*)\gg 0$. So $\nabla U(x^*)(x^1-x^*) =\lambda^*p(x^1-x^*) >0$ implies that $px^1>px^* = I$, which is a contradiction to the fact that $x^1$ is feasible. $\square$

**Definition: (Marshallian Demand)** The solution the the utility maximizing problem is called the Marshallian Demand, denoted by $x^*(p,I)$.

#### Indirect Utility Function

**Definition: (Indirect Utility Function)** The Indirect Utility Function, also known as the Value Function, is defined as $V(p,I) = U(x^*(p,I))$.

**Theorem: (Properties of the Indirect Utility Function)** If $U(.)$ is strictly increasing on $\R^n_+$, then $V(p,I)$ is:

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

   Another proof defines $x^0 = x(p^0,I^0)$. Consider $V(p,px^0)-U(x^0)$ as a function of prices. Note that $V(p,px^0)-U(x^0)\geq 0$ for any $p\in \R^n_+$ because $x^0$ is always affordable. This function is minimized at the price $p^0$. Since the function is differentiable, we have the first order condition: $\partial V(p^0,p^0x^0)/\partial p_i+(\partial V(p^0,p^0x^0)/\partial I) x^0 = 0$, which will give us the Roy’s Identity. $\square$



### Expenditure Minimization

#### Expenditure Minimizing Problem

**Definition: (Expenditure Minimizing Problem)** The expenditure minimizing problem is defined as
$$
min_{x\in \R^m_+} \space px \\
s.t. \space U(x)\geq U_0
$$
**Theorem: (Existence of the solution)** Let $U = \{u\in \R| \exist x \space s.t. \space U(x) = u\}$. If $U_0\in U$, and $U(.)$ is continuous, then there is a solution to the minimization problem. Furthermore, if $U(.)$ is strictly increasing and continuous and strictly quasi-concave, and $p\gg 0 $, then the solution is unique.

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

**Definition: (Hicks Demand)** The solution the the expenditure minimizing problem is called the Hicks Demand, denoted by $x^H(p,U)$.

####  Expenditure Function

**Definition: (Expenditure Function)** The Expenditure Function is defined as $e(p,U) = px^H(p,U)$.

**Theorem: (Properties of the Expenditure Function)** If $U(.)$ is continuous, strictly increasing and strictly quasi-concave, then the expenditure function is:

1. Zero when $U$ takes the lowest utility level in available $U$
2.  Continuous on $\R^N_+\times U$
3. For $p\gg 0$, the expenditure function is strictly increasing and unbounded in $U$
4. Increasing in $p$
5. Homogenous of degree 1 in $p$
6. concave in $p$
7. If $U(.)$ is differentiable, then the Shephard’s lemma is true, i.e. $\partial e(p^0,U^0)/\partial p_i = x_i^H(p^0,U^0)$.

Proof:

1. The bundle giving the lowest utility level is $(0,0,...,0)$. the expenditure to achieve this bundle is trivially zero.

2. Given the objective function is continuous and the feasible set is compact, by the Theorem of Maximum the expenditure function is continuous.

3. First prove the monotonicity. Suppose $U'>U$, let $px' = e(p,U')$, $U(x')\geq U'\geq U$, since $U(.)$ is strictly increasing and $px = e(p,U)$, we have $px = e(p,U)\leq e(p,U') = px'$, since $x$ is minimizing the objective function. Now we only need to show that $px'\neq px$. Suppose $px' = px$, since $U(x')\geq U'> U\geq U(0)$, we have $x'\neq 0$. There exists some $x_i'>0$ such that $U(\tilde x) = U(x_1',x_2',...,x_i'-\epsilon, ..., x_n')>U$ because $U'> U$ and $U$ is continuous. So $\tilde x$ is feasible for the minimization problem, and $px\leq p\tilde x<px'$, i.e. the expenditure function is strictly increasing in $U$.

   Now we prove the unboundedness. Since $U(.)$ is increasing and continuous, the attainable utility level is an interval: $U = [U(0),\bar U)$, where $\bar U$ is a finite number or infinity. Pick an increasing sequence of utility level $U_n\to \bar U$, we want to show that $e(p,U_n)$ is unbounded above. Suppose this is not true. Since $U(.)$ is strictly increasing, let $px^n  = e(p,U_n)$, if $e(p,U_n)$ is bounded, then $x^n$ is also bounded. Then there is a subsequence of $x^n$,denoted as $x^{n_k}$ which goes to some $\bar x \in \R^n_+$. Then since $U(.)$ is continuous, we have $U(x^{n_k})\to U(\bar x)$. Since there is only one limit of the sequence $U_n$, which is $\bar U$, we have $ U(\bar x) = \bar U$. But then $\bar U $ would be attainable, which is impossible.

4. Suppose $p^1<p^2$, and $x^1$ and $x^2$ are the solutions to the minimizing problem, separately. Since $U_0$ is always attainable, we have $p^1x^1\leq p^1x^2 < p^2x^2$.

5. At price $tp$, the problem can be rewrite as $t[min_{x\in \R^m_+} \space px] \space s.t. \space U(x)\geq U_0$, which is identical to the original problem. So the solution is the same, i.e. $e(tp,U_0) = tpx  =t(px) = te(p,U_0)$.

6. Consider $p^1$ and $p^2$, define $\bar p = tp^1+(1-t)p^2$. Let $\bar x = x^H(\bar p, U_0)$, $x^1 = x^H(p^1, U_0)$, and $x^2 = x^H(p^2, U_0)$.  Then we have $p^1x^1 \leq p^1 \bar x$ and $p^2x^2 \leq p^2 \bar x$. Combine them we have $\bar p (tx^1+(1-t)x^2)\leq \bar p\bar x$, i.e. the expenditure function is concave.

7. The first proof follows from the Envelope Theorem. We have $\partial e / \partial p_i = \partial L/\partial p_i =  x_i^H$.

   An alternative proof is to consider the function $F(p) = e(p,U_0)-px^0$, where $x^0 = x^H(p,u^0)$. This function is maximized at $p$. So the first order condition is $\partial e(p^0,U^0)/\partial p_i - x_i^H(p^0,U^0)  =0$. $\square$



### Duality

**Lemma: (Duality)** Generally, we have $e(p,V(p,I))\leq I$, and $V(p,e(p,U))\geq U$.

**Theorem: (Duality Theorem)** If $U(.)$ is continuous and strictly increasing, then $e(p,V(p,I)) = I$ and $V(p,e(p,U))= U$.

Proof:

1. Prove by contradiction. Suppose $e(p,V(p,I_0)) < I_0$, let $U_0  =V(p,I_0)$ so then $e(p,U_0)<I_0$. Since $e(p,U)$ is continuous in $(p,U)$, there is a $\epsilon >0$ such that $e(p,U_0+\epsilon)<I_0$, denote $I_\epsilon = e(p,U_0+\epsilon)$, then $I_\epsilon<I_0$. But then we have $U_0+\epsilon \leq V(p,I_\epsilon)<V(p,I_0) = U_0$, which is impossible.
2. Prove by contradiction. Suppose $V(p,e(p,U_0)) > U_0$, let $I_0  = e(p,U_0)$ so then $V(p,I_0)>U_0$. Since $V(p,I)$ is continuous in $(p,I)$, there is a $\epsilon >0$ such that $V(p,I_0-\epsilon)>U_0$, denote $U_\epsilon = V(p,I_0-\epsilon)$, then $U_\epsilon>U_0$. But then we have $I_0-\epsilon \geq e(p,U_\epsilon)>e(p,U_0) = I_0$, which is impossible. $\square$

**Theorem: (Duality of the Solutions)** Suppose $U$ is continuous, strictly increasing and strictly quasi-concave. Then we have $x^*  =x^H(p,V(p,I))$ and $x^H = x^*(p,e(p,U))$ for all $p\gg 0$ and U attainable.

Proof:

1. By continuity and strictly quasi-concavity, both solutions are unique. By definition we have $e(p,V(p,I)) = px^H(p,V(p,I))$. By the duality theorem $e(p,V(p,I)) =I = px^H(p,V(p,I))$. Then by definition of the utility maximizing problem, $x^H(p,V(p,I))$ is affordable under income level $I$ and gives a utility level of $V(p,I)$. So $x^H(p,V(p,I))$ is a solution to the utility maximizing problem. However, since the solution is unique, we have $x^*  =x^H(p,V(p,I))$.
2. Similarly, by definition we have $V(p,e(p,U)) = U(x^*(p,e(p,U)))$. By the duality theorem $V(p,e(p,U)) = U = U(x^*(p,e(p,U)))$. Then by definition of the expenditure minimizing problem, $x^*(p,e(p,U))$ is attainable at utility level $U$ and gives an expenditure level of $e(p,U)$. So $x^*(p,e(p,U))$ is a solution to the expenditure minimizing problem. However, since the solution is unique, we have $x^H = x^*(p,e(p,U))$. $\square$



###  Slutsky Equation

**Theorem: (Slutsky Equation)** We have $\frac{\partial x_i(p,I)}{\partial p_j} = \frac{\partial x_i^H(p,U)}{\partial p_j}-x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}$ for any $i,j$.

Proof:

From the duality theorem, we have $x^H = x^*(p,e(p,U))$. Take total differentiation with respect to $p_j$, we have $\frac{\partial x_i(p,I)}{\partial p_j} = \frac{\partial x_i^H(p,U)}{\partial p_j}-x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}$. $\square$

**Definition: (Substitution Effect)** $\frac{\partial x_i^H(p,U)}{\partial p_j}$ is defined as the Substitution Effect.

**Definition: (Income Effect)** $-x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}$ is defined as Income Effect.

**Definition: (Normal Good)** A good is Normal at a point if $\frac{\partial x_i(p,I)}{\partial I}>0$.

**Definition: (Inferior Good)** A good is Inferior at a point if $\frac{\partial x_i(p,I)}{\partial I}<0$.

**Definition: (Giffen Good)** A good is Giffen at a point if $\frac{\partial x_i(p,I)}{\partial p_j}<0$.



### Properties of Demand

**Theorem: (Properties of Marshallian Demand)** Under all assumptions of the utility function, the Marshallian demand is homogenous of degree 0, and it satisfies the budget balance.

Proof:

We have $V(p,I) = V(tp,tI)$, which is equivalent to $U(x^*(p,I)) = U(x^*(tp,tI))$. Since $U(.)$ is continuous and strictly increasing, $x^*(p,I) = x^*(tp,tI)$. The budget balance follows from the strictly increasing property of the utility. Suppose $px^*(p,I) <I$, then we can find another bundle such that $U(x’)>U(x^*)$ and $px'<I$, contradicting to the fact that $x^*$ is the solution. $\square$

**Theorem: (Properties of Hicks Demand)** Under all assumptions of the utility function, and suppose $(p,I)\gg 0$, the Hicks demand is homogenous of degree 0 with respect to $p$, and exhausts the utility constraint.

Proof:

At price $tp$, the problem can be rewrite as $t[min_{x\in \R^m_+} \space px] \space s.t. \space U(x)\geq U_0$, which is identical to the original problem. So the solution is the same.

Exhausting the utility constraint follows from the strictly increasing property of the utility. Suppose $U(x^*(p,I)) >U$, then we can find another bundle such that $U(x’)<U(x^*)$ and $px'<I$, when $p\gg 0$. This is contradicting to the fact that $x^*$ is the solution. $\square$

**Definition: (Slutsky Matrix)** Define the Slutsky Matrix as $S(p,I) = [\frac{\partial x_i(p,I)}{\partial p_j} +x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}]$.

**Theorem: (Properties of Slutsky Matrix)** The Slutsky matrix is symmetric and negative semi-definite. 

Proof: 

Note that by Slutsky Equation, $S(p,I) = [\frac{\partial x_i(p,I)}{\partial p_j} +x_j(p,I)\frac{\partial x_i(p,I)}{\partial I}] = [\frac{\partial x_i^H(p,V(p,I))}{\partial p_j}]$. By Shephard’s lemma, we have $\partial e(p,U)/\partial p_i = x_i^H(p,U)$, hence $\frac{\partial x_i^H(p,V(p,I))}{\partial p_j} = \frac{\partial^2 e(p,U)}{\partial p_i\partial p_j}$, by Young’s theorem this is symmetric. Since $e(p,U)$ is concave, $[\frac{\partial x_i^H(p,V(p,I))}{\partial p_j}]$ is negative semi-definite. $\square$



### Integrability

#### Recover Utility from the Expenditure Function

**Theorem: (Recovering Expenditure Function)** Suppose $e: \R^n\times \R$ satisfies the seven properties of the expenditure function, then define $u(x) = max\{u\geq U(0)|px\geq e(p,u) \space \forall p\gg 0\}$. $u(x)$ is well defined, unbounded, increasing and quasi-concave.

Proof:

1. First we prove the function is well defined. Define $\bar U = \{u\geq U(0)|px\geq e(p,u) \space \forall p\gg 0\}$. We want to show that $\bar U$ is a non-empty, closed, bounded set. The set is non-empty because $U(0)$ is always in the set. it is bounded below by $U(0)$ and bounded above since $e$ is increasing in $u$ and unbounded above in $u$ by assumption. We only need to show that $\bar U$ is closed. Let $u_n$ be a sequence such that $u_n\to u$, suppose $u_n \in \bar U$, which implies $px\geq e(p,u_n)$. Since $e$ is continuous, $e(p,u_n)\to e(p,u)$. Then $px\geq e(p,u)$, i.e. $u\in \bar U$, $\bar U$ is closed. Since t $\bar U$ is non-empty, closed, and bounded, the maximum exists. Hence $u(x)$ is well-defined. The function is unbounded above by construction. 
2. Second we prove the function is increasing. Suppose we have $x^1\geq x^2$, we have $px^1\geq px^2\geq e(p,u(x^2))$ by the definition of $u(x^2)$. This implies $u(x^2)\in \bar U(x^1)$. Since $u(x^1)$ is the maximum, we have $u(x^1)\geq u(x^2)$.
3. Third we prove the function is quasi-concave. Take any $x^1$ and $x^2$ and $t\in [0,1]$. By definition we have $px^1\geq e(p,u(x^1))$ and $px^2\geq e(p,u(x^2))$. So $p(tx^1+(1-t)x^2)\geq te(p,u(x^1))+(1-t)e(p,u(x^2))\geq min\{e(p,u(x^1)),e(p,u(x^2))\}$. Hence we have $min\{e(p,u(x^1)),e(p,u(x^2))\} \in \bar U(tx^1+(1-t)x^2)$. since $u(tx^1+(1-t)x^2)$ is the maximum, we have $u(tx^1+(1-t)x^2)\geq min\{e(p,u(x^1)),e(p,u(x^2))\}$, i.e. u(x) is quasi-concave. $\square$

 **Theorem: (Verification)** Suppose $e: \R^n\times \R\to \R$ is any function that satisfies the seven properties of the expenditure function, then define $u(x) = max\{u\geq0|px\geq e(p,u) \space \forall p\gg 0\}$. Then $e(p^0,U_0) = min_{x\in \R^m_+} \space p^0x \space s.t. \space u(x)\geq U_0$.

Proof:

1. First we prove that $[min_{x\in \R^m_+} \space p^0 x \space s.t. \space u(x)\geq U_0]\geq e(p^0,U_0)$.

   Fix $p^0\gg0$ and $U_0\geq 0$, for any $x$ such that $u(x)\geq U_0$, by the definition of $u(x)$, we have $px^0\geq e(p,u(x))$ for all $p$. This implies $p^0 x^0\geq e(p^0,u(x))$. Furthermore, since $e(p,u)$ is increasing in $u$, and $u(x)\geq U_0$, we have $p^0 x\geq e(p^0,u(x)) \geq e(p^0,U_0)$. Recall this inequality holds for all $x$ such that $u(x)\geq U_0$. Suppose the solution to minimization problem is $x^0$, we have $p^0 x^0 \geq e(p^0,U_0)$, i.e. $[min_{x\in \R^m_+} \space p^0 x \space s.t. \space u(x)\geq U_0]\geq e(p^0,U_0)$.

2. Now we prove that $[min_{x\in \R^m_+} \space px \space s.t. \space u(x)\geq U_0]\leq e(p^0,U_0)$.

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

By budget balance, . $px(p,I) = I = \sum_{i = 1}^n p_ix_i(p,I)$. Differentiate with respect to $p_i$, we will get $\sum_{i = j}^n p_j \frac{\partial x_j}{\partial p_i}+x_i(p,I) = 0$, or $\sum_{i = j}^n p_j \frac{\partial x_j}{\partial p_i} = -x_i(p,I)$. Now differentiate with respect to $I$, we will get $\sum_{i=1}^n p_j \frac{\partial x_j}{\partial I} = 1$. Now define $f_i(t) = x_i(tp,tI)$. We want to show that $f_i(t) = f_(1)$, i.e. $\frac{\partial f_i}{\partial t}  =0$. We have:


$$
f_i'(t) = [\sum_{j = 1}^n \frac{\partial x_i}{ \partial p_j}p_j +\frac{\partial x_i}{\partial I}I] |_{(tp,tI)} \\
= \sum_{j = 1}^n \frac{\partial x_i(tp,tI)}{ \partial p_j}tp_j +\frac{\partial x_i(tp,tI)}{\partial I}tI 
$$
Using symmetry, we have
$$
f_i'(t)= \sum_{j = 1}^n \frac{\partial x_j(tp,tI)}{ \partial p_i}tp_j + \sum_{j = 1}^n \frac{\partial x_j(tp,tI)}{\partial I}tp_jx_i(t)\\
 =  \sum_{j = 1}^n( -x_i(t)p_j + p_jx_i(t)) = 0
$$
This finishes the proof. $\square$ 

**Theorem: (Slutsky Property)** Suppose that $x(p, I)\in \R^n_+$ satisfies budget balance and homogeneity. Then for all $(p, y)$, $S(p, y)p= 0$.

Proof:

Note that $S(p, y)p= \sum_{j=1}^n(\frac{\partial x_i}{\partial p_j}+x_j\frac{\partial x_i}{\partial I})p_j = \sum_{j=1}^n(p_j\frac{\partial x_i}{\partial p_j}+p_jx_j\frac{\partial x_i}{\partial I}) = \sum_{j=1}^n(p_j\frac{\partial x_i}{\partial p_j}+I\frac{\partial x_i}{\partial I}) = 0$. $\square$

**Theorem: (Integrability Theorem)** If a differentiable function $x:\R^n_+ \times \R_+\to \R^n_+$ satisfies budget balance, symmetry and negative semi-definite of Slutsky matrix, then it is the demand function generated by some increasing, quasi-concave function.

Proof:

1. First we want to show that suppose $e(p,U)$ is an expenditure function that is generated by some utility function, that is not related to the given function $x(.)$. However, when we have $\frac{\partial e(p,U)}{\partial p_i} = x_i(p,e(p,U))$ for all $i$, the Marshallian demand generated by the same utility function satisfies $x^*(p,I) = x(p,I)$. This follows from duality and Shepherd’s lemma. We have $x^*(p,e(p,U)) = x^H(p,U) = x(p,e(p,U))$. For each fixed $p$, as $U$ varies $e(p,U)$ assumes all numbers on $[0,+\infty)$, so we could change $e(p,U)$ to $I$ and have the aimed equation.

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
Let $p^1 = p^0+tz$, where $t>0$ and $z$ is a vector in $\R^n$. so this becomes $tz(x^1-x^0)\leq 0$. Choose $t$ close to zero, we have $tzx(p^1,p^1x^0)\leq tzx^0$, i.e. $zx(p^0+tz , (p^0+tz)x^0)\leq zx^0$. If we define a function $f(t) = zx(p^0+tz , (p^0+tz)x^0)$, this implies that the function attains its maximum when $t = 0$. Note that $t\in [0,\bar t)$, so the equivalent condition is $f'(0)\leq 0$. So we have
$$
f'(t)|_{t= 0} = \sum _{i=1}^n z_i(\sum_{j=1}^n\frac{\partial x_i(p^0+tz,(p^0+tz)x^0)}{\partial p_j}|_{t= 0}z_j+\frac{\partial x_i(p^0+tz,(p^0+tz)x^0)}{\partial I}|_{t= 0}(\sum_{j=1}^nz_jx^0_j)) \\
= \sum _{i=1}^n \sum_{j=1}^n z_i z_j(\frac{\partial x_i(p^0,p^0x^0)}{\partial p_j}+\frac{\partial x_i(p^0,p^0x^0)}{\partial I}x^0_j) \\
=z^TS(p^0,I^0)z\leq 0
$$
So the Slutsky matrix is negative semi-definite. $\square$

**Theorem: (Recover WARP)** Suppose that a choice function x(p,y) satisfies homogeneity and budget balance. Suppose  further that whenever $p^1$ is not proportional to $p^0$, we have $(p^1)^TS(p^0,I)p^1<0$. Then $x(p,I)$ satisfies WARP.

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

By substitution axiom we have $(\alpha\circ\pi+(1-\alpha)\circ\sigma) \sim (\alpha\circ(p_1\circ a_1,...,p_n \circ a_n),(1-\alpha)\circ(r_1\circ a_1,...,r_n \circ a_n))$ and $(\alpha\circ\rho+(1-\alpha)\circ\sigma) \sim (\alpha\circ(q_1\circ a_1,...,q_n \circ a_n),(1-\alpha)\circ(r_1\circ a_1,...,r_n \circ a_n))$. By the ability to reduce to simple gamble , we have $(\alpha\circ(q_1\circ a_1,...,q_n \circ a_n),(1-\alpha)\circ(r_1\circ a_1,...,r_n \circ a_n))\sim (\alpha\circ(p_1\circ a_1,...,p_n \circ a_n),(1-\alpha)\circ(r_1\circ a_1,...,r_n \circ a_n))$. Hence by transitivity and $\pi\sim \rho$, we have $(\alpha\circ\pi+(1-\alpha)\circ\sigma) \sim (\alpha\circ\rho+(1-\alpha)\circ\sigma)$. $\square$



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

**Definition: (Probability Premium)** 







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

**Definition: (Arrow-Pratt Measure of Absolute Risk Aversion)** The Absolute Risk Aversion is defined as $\lambda(x) = -\frac{U''(x)}{U'(x)}$ for all $X\in \R$.

**Definition: (Arrow-Pratt Measure of Relative Risk Aversion)** The Relative Risk Aversion is defined as $R(x) = -\frac{xU''(x)}{U'(x)}$ for all $X\in \R$.

**Theorem: (Relative Risk Aversion)** Suppose 2 preferences have the expected utility property, the following are equivalent:

1. Preference 1 is more risk averse than preference 2
2. $U_1(.) = \phi(U_2(.))$ for some concave and strictly increasing function $\phi:\R\to\R$
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

**Definition: (First Order Stochastically Domination)** $F$ First Order Stochastically Dominate $G$, denoted by $F\succsim _{FOSD} G$, if $\int UdF\geq \int UdG$ for all non-decreasing function $U:\R\to \R$.

**Theorem: (FOSD Property)** $F\succsim _{FOSD} G$ if and only if $F(x)\leq G(x)$ for all $x$.

Proof:

If $F\succsim _{FOSD} G$, then $\int UdF\geq \int UdG$  for all non-decreasing function $U:\R\to \R$. Now by integration by parts, we have $\int_a^b U(x)dF(x) = U(x)F(x)|_a^b-\int_a^bU'(x)F(x)dx = U(b)-\int_a^bU'(x)F(x)dx$. So $\int_a^b U(x)(dF(x)-dG(x)) = \int_a^bU'(x)(G(x)-F(x))dx$. Since $U'(x)\geq 0$, we have $F(x)\leq G(x)$. Suppose for some $x'$ we have $F(x')> G(x')$,  since all the probability distributions are right continuous, we can define $U(x) = 1$ for $x\geq x'$ and for $x< x'$. This will lead to a contradiction that  $\int UdF< \int UdG$. It is trivial to show the inverse of this is also true. $\square$ 

**Definition: (Second Order Stochastically Domination)** $F$ Second Order Stochastically Dominate $G$, denoted by $F\succsim _{SOSD} G$, if $\int UdF\geq \int UdG$ for all non-decreasing and concave function $U:\R\to \R$.

**Claim: (SOSD Property)** $F\succsim _{SOSD} G$ if and only if $\int_{-\infty}^xF(t)dt\leq \int_{-\infty}^xG(t)dt$ for all $x$.



### Anscombe-Aumann Structure

#### Definition

**Definition: (State)** $s\in \Omega$ is the State of a finite possible state world.

**Definition: (Outcomes)** $X = \{x_1,...,x_n\}$ is the set of Outcomes.

**Definition: (Anscombe-Aumann Act)** An Anscombe-Aumann Act is a function $h:\Omega\to \Delta X$, or we can denote it as $h_s\in H = (\Delta X)^\Omega$. We denote the probability of outcome $x$ at state $s$ as $h_s(x)$.

**Definition: (Constant Act)** A Constant Act is defined as an Anscombe-Aumann Act which satisfies $h_s= h_{s'}$ for any $s,s'\in \Omega$.

**Definition: (Affine)** Function $f:\Pi\to\R$ is an Affine if for any $\pi, \rho \in\Pi$, and $\alpha\in [0,1]$, we have $ f(\alpha\pi+(1-\alpha)\rho) = \alpha f(\pi)+(1-\alpha)f(\rho) $.

**Definition: (Linear)** Function $f:\Pi\to\R$ is an Affine if for any $\pi, \rho \in\Pi$, and $\alpha, \beta\in \R$, we have  $f(\alpha\pi+\beta\rho) = \alpha f(\pi)+\beta f(\rho) $.

#### Mixture Space Theorem

**Claim: (Mixture Space Theorem)** A preference on a convex subset of $\R^n$ is complete, transitive, independent and Archimedean if and only if there exists an affine function $U:\Pi\to \R$ representing the preference. Moreover, if $U(.)$ is an affine representation then $V(.)$ is an affine representation of the same preference if and only if there exist $a>0$ and $b\in \R$ such that $V(\pi) = \alpha U(\pi)+b$.

**Claim: (State Dependent Expected Utility)** A preference on a convex subset of $\R^n$ is complete, transitive, independent and Archimedean if and only if there exists a set of Von-Neumann-Morgenstern utility functions $U_1,..,U_m:X\to\R$, such that $U(h) = \sum_s\sum_x h_s(x)U_s(x)$.

#### Subject Probability

**Definition: (Changing Act)** Given an act $h\in \Delta X^\Omega $, $s\in \Omega$, and a lottery $\pi\in \Omega$, define a new act $(h-s,\pi) =(h_1,h_2,...,h_{s-1},\pi,h_{s+1}, ..., h_n)$.

**Definition: (Null State)** A state is Null if for any $h\in \Delta X^\Omega$, any $\pi,\rho \in \Delta X$ we have $(h-s,\pi)\sim (h-s,\rho)$.

**Definition: (State Independence)** a preference is state independent if for all non-null states $s,t\in \Omega$, for all acts $h,g\in \Delta X^\Omega$, any lottery $\pi,\rho \in \Delta X$, $(h-s,\pi)\succsim (h-s,\rho)$ implies $(g-t,\pi)\succsim (g-t,\rho)$.

**Definition: (Monotonicity)** a preference is state independent if for all acts $h,g\in \Delta X^\Omega$, the constant act $h_s\succ g_s \forall s\in \Omega$ implies $h\succ g$.

**Theorem: (State Independence and Monotonicity)** if a preference is state independent, then it is monotonic.

Proof:



**Claim: (Expected Utility Theorem)** A preference relation on $H$ is independent , Archimedean, state independent if and only if there exists a Von-Neumann-Morgenstern utility function $U:X\to\R$, such that $U(h) = \sum_s\mu(s)\sum_x h_s(x)U(x)$, where $\mu(s)$ denote the subjective probability of state $s$.



## Production Theory

### Production Set



### Production Function



### Transformation Function



### Cost Minimization



### Profit Maximization



### Short Run and Long Run Problem



### Multi Product Firms



## General Equilibrium

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

**Corollary: (Existence of Equilibrium)** The Walrasian Equilibrium exists.



### Production Equilibrium

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

**Definition: (Aggregate Production Possibility)** Define the Aggregate Production Possibility Set as $Y = \{y|y = \sum_{j\in J}y^j\}$.

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
Note: If $y^j$ and $u^i$ satisfies the assumptions above, then the solution of the consumer exists and is unique for $p\gg 0$. Plus, $x^i(p,m^i(p))$ is continuous in $p$ and $m^i(p)$ is also continuous.

#### Existence of the Equilibrium

**Definition: (Walrasian Equilibrium)** a vector $p^* \in \R^n_+$ is called a Walrasian Equilibrium if 
$$
z(p^*) = \sum_{i\in I}(x^i(p^*)-e^i) - \sum_{j\in J} y^j(p^*)= 0
$$
**Theorem: (Existence of The Equilibrium)** Consider the economy $(u^i,e^i,\theta^{ij},y^j)$ with $i\in I$ and $j\in J$. If All the assumptions are satisfied, and $y+\sum_{i\in I }ei \gg 0$ for some production vector $y \in \sum_{j\in J}y^j$, then there exists at least one price vector $p^*\gg 0$ such that $z(p^*) =0$.

Proof:

We will verify that $z(p)$ satisfies the three properties of the Equilibrium Existence Theorem.

1. $z(p)$ is continuous because of the continuity of the individual demand function and supply function.

2. Walras Law is still true because of budget balance.

3. We want to show that if $p^m \to \bar p $,  and $\exist k$, such that $\bar p_k = 0$, then  $\exist k'$ with  $\bar p_{k'} = 0$, such that the excess demand of $k'$, $z_{k'}(p^m)$  is unbounded as $p^m \to p^*$.

   If there is some consumers with strictly positive income at the limit price $\bar p$, then this person’s income will remain to be positive at $p^m$ as $p^m \to p^*$ due to the fact that $m^i(p)$ is continuous. This person’s demand for good $k$ will be unbounded above as  $p_k^m \to 0 $.

   Hence it suffices to show that there is some consumers with strictly positive income at the limit price $\bar p$. 
   
   Because $y+\sum_{i\in I }ei \gg 0$, for some $y$ we have $\bar p(y+\sum_{i\in I }ei) > 0$. Consider the sum of consumer’s budget constraint:
   $$
   \sum_{i\in I }m^i(\bar p) =\bar p \sum_{i\in I } e^i +\sum_{i\in I } \sum_{j =1}^J \theta_{ij}\pi_j(p) = \bar p \sum_{i\in I } e^i + \sum_{j =1}^J (\sum_{i\in I }\theta_{ij})\pi_j(p)\\
   = \bar p \sum_{i\in I } e^i + \sum_{j =1}^J \pi_j(p) = \bar p (\sum_{i\in I } e^i +y) >0
   $$
   So there is some person that has strictly positive income, otherwise the above equation would not hold. $\square$



## Welfare Theorem

### Pareto Optimality

#### Pareto Optimality In Barter Economy

**Definition: (Feasible Allocation)** The Feasible Set is defined as $F(e) = \{\sum_{i\in I} x^i= \sum_{i\in I} e^i \}$.

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

**Definition: (Pareto Optimality)**

**Definition: (Utility Possibility Set)** The Utility Possibility Set is defined as $U(x) = \{u_i\}_{i\in I }$ and $x$ is feasible, i.e.
$$
U = \{(\bar u_1,..., \bar u_I)\in \R^I|u_i(x^i)\geq \bar u_i \space \forall i\in I \space \& \space x \space feasible \}
$$
**Definition: (Pareto Optimality Alternative Definition)** A feasible allocation $x^*$ is Pareto Efficient if $\{\bar u\in U|\bar u \geq u^*\} = \{u^*\}$ where $u^* = (u_1(x_1^*), ..., u_I(x_I^*))$.

**Definition: (Boundary)** Let $\partial U$ denote the Boundary of the Utility Possibility Set, also known as the utility frontier: $\{u\in U|\nexists u'\in U, u'>u\}$.

**Theorem: (Pareto Optimality Alternative Definition)** A feasible allocation $x^*$ is Pareto Optimal if and only if $u^* = (u_1^*(x_1^*),..., u_I^*x(_I^*)) \in \partial U$.

Proof:

1. Let $x^*$ be a Pareto Optimal solution, suppose $u(x^*) \notin \partial U$, then there exists $\bar u \in U$ such that $\bar u > u^*$, which implies that $x^*$ is not Pareto Optimal.
2. Let $u(x^*) \in \partial U$,  suppose  $x^*$ is not Pareto Optimal, then there exists $\bar u \in U$ such that $\bar u > u^*$, then $u(x^*) \notin \partial U$, contradiction. $\square$

#### Solve for Pareto Optimality

**Theorem: (Solution of Pareto Optimality)** let the utility functions $u_i$, for $i\in I $, be continuous. Suppose $u_1$ is strongly increasing, then $x^*$ is Pareto Optimal if and only if it’s a solution to the following problem:
$$
max\{u_1(x^1)\} \space s.t.\space u_i(x^i)\geq\bar u_i \space \& \space \sum_{i\in I} x^i \leq \sum_{i\in I} e^i + \sum_{j\in J} y^j
$$
for some $(\bar u_2, ..., \bar u_i) \in U_{-1}$.

Proof:

1. Want to show that the Pareto Optimal allocation solves the problem. By definition, if we set $u_i =  u_i^*$ for $i = 2,...,I$, then $u_1^*$ is the maximum utility we could get to give to person 1, hence it’s a solution.

2. Want to show the solution to the problem is Pareto Optimal. Let $x^*$ be the solution, suppose that is not Pareto Optimal, then there is another allocation, $\tilde x$, which is feasible and satisfying $u_i(\tilde x^i) \geq u_i(x^{i*})$ for all $i$ and there is one $j$ such that $u_j(\tilde x^j) > u_j(x^{j*})$.

   Case 1: when  $u_1(\tilde x^1) > u_1(x^{1*})$, then automatically $x^* $ is not the solution, contradiction.

   Case 2: when $u_k(\tilde x^k) > u_1(x^{k*})$ for some $k\neq1$, and suppose  $\tilde x^k>0$. Without loss of generosity, we could assume the consumption of the first good of consumer $k$ is greater than zero, i.e. $\tilde x_1^k >0$. Now let $w\in \R^n$ be a vector with $w_1 = 1$ and $w_m = 0$ for $m = 2,...,n$, i.e. $w = (1,0,0,...0)$. by continuity of $u_k$, there is a $\epsilon >0$ such that $u_k(\tilde x^k -\epsilon w) > u_k(x^{k*})$. 

   Now consider another bundle $\hat x$, where $\hat x^1 = \tilde x^1 +\epsilon w$, $\hat x^i = \tilde x^i$ for $i\neq {1,k}$ and $\hat x^k = \tilde x^k -\epsilon w$. By strongly monotonicity, $u_1(\hat x_1) >u_1(x^*)$ and $\hat x$ is still feasible and everyone else is getting at least as good as $x^*$. So $x^*$ is not the solution, contradiction.

   Case 3: when $u_k(\tilde x^k) > u_k(x^{k*})$ for some $k\neq1$, and suppose  $\tilde x^k=0$. If $x^{k*} = 0$, then the equation before would become $u_k(0) > u_k(0)$, which is not possible. Since we know $x^{k*} \geq0$, this means the only possible case is $x^{k*} > 0$. Now we can define a new allocation $\hat x$, where $\hat x^1 = x^{1*} +x^{k*}$, $\hat x^i = x^{i*}$ for $i\neq {1,k}$ and $\hat x^k = 0$. Then by strongly monotonicity, $u_1(\hat x_1) >u_1(x^*)$ and $\hat x$ is still feasible and everyone else is getting at least as good as $x^*$. So $x^*$ is not the solution, contradiction. $\square$

#### Social Planner

**Definition: (Social Planner’s Problem)** Let $\lambda \gg 0$, consider the following social planner’s problem:
$$
max \space \{U(x) = \sum_{i\in I } \lambda_i U_i(x^i)\} \space s.t.\space \sum_{i\in I }x^i \leq \sum_{i\in I }e^i +\sum_{j\in J }y^i \space x^i \gg 0
$$

**Theorem: (Sufficient Condition for Pareto Optimality)** If $x^*$ is a solution to the social planner’s problem, then $x^*$ is Pareto Optimal.

Proof:

Let $x^*$ to be a solution to the social planner’s problem, and suppose $x^*$ is not Pareto Optimal. Then there exists another allocation $\tilde x$ such that  $u_i(\tilde x^i) \geq u_i(x^{i*})$ for all $i$, and there exists a $j$ such that $u_j(\tilde x^j) > u_j(x^{j*})$. Then multiply each side by $\lambda_i$ and add up all the equations, we will get $\sum_{i\in I } \lambda_i u_i(\tilde x^i > \sum_{i\in I } \lambda_i u_i(x^{i*})$, hence $x^*$ is not the solution to the above problem, Contradiction. $\square$

**Lemma: (Convexity)** Let $u_i$ be concave, then the utility possibility set is convex.

**Lemma: (Supporting Hyperplane Theorem)** Let $Z \subset \R^n$ be convex, $a\in R^n$ be a point that is not in the interior of $Z$, then there exists a vector $p\in \R^n\backslash\{0\}$ such that $pa\geq pz \space \forall z\in Z$.

**Theorem: (Necessary Condition for Social Planner’s Problem)** Let $u_i$ be concave, $x^*$ be Pareto Optimal. There exists a vector $\lambda \in \R^I_+\backslash\{0\}$, such that $x^*$ is a solution to the social planner’s problem.

Proof:

Suppose $x^*$ is Pareto Optimal. Then $u^* = (u_1(x^{1*}),...,u_1(x^{1*}))$ is on the boundary of the utility possibility set. By Convexity Lemma, $U$ is a convex set. By Supporting Hyperplane Theorem, there exists $\lambda \in \R^I\backslash\{0\}$, such that $\lambda u^* \geq \lambda u \space \forall u\in U$, hence $\sum_{i\in I }\lambda_i u^{i*} \geq \sum_{i\in I }\lambda_i u^{i}$. 

It remains to show that $\lambda \geq 0$. Suppose not, then there is a $k$ such that $\lambda_k <0$. Then
$$
\lambda u^* = \sum_{i\in I }\lambda_i u^{i*} \geq \sum_{i\neq k }\lambda_i u^{i} +\lambda_k u^{k}
$$
But this is impossible to hold since $u^{k}$ can goes to negative infinity. When it does so, and $\lambda_k <0$, the right hand side of the equation will goes to positive infinity, but the left hand side stays finite, so we get a contradiction. $\square $



### First Welfare Theorem

**Theorem: (Local Non-satiation)** Suppose the preference is locally non-satiated, $x^{i*}$ is defined as the solution to the maximizing problem of the consumer given a budget constraint $px^i \leq m_i(p)$. Then we have:
$$
(x^i \succsim_i x^{i*})\Rightarrow (px^i \geq m_i(p)) \\
(x^i \succ_i x^{i*})\Rightarrow (px^i > m_i(p))
$$
Proof:

If $x^i \succsim_i x^{i*}$ and suppose $px^i < m_i(p)$, then by local non-satiation there exists another bundle $\tilde x^i \in B_\epsilon(x^i)$ such that $u_i(\tilde x^i) >u_i(x^{i*})$ and  $p\tilde x^i < m_i(p)$. Hence $x^{i*}$ is not the solution to the maximizing problem, contradiction.

If $x^i \succ_i x^{i*}$ and suppose $px^i \leq m_i(p)$, then  $x^{i*}$ is not the solution to the maximizing problem, contradiction. $\square$

**Theorem: (First Welfare Theorem)** Suppose that each consumer’s preference are locally non-satiated, then for any allocation $(x^*,y^*)$ that forms a Walrasian Equilibrium with some price vector $p^*$ is Pareto Optimal.

Proof:

Suppose an allocation $(x^*,y^*)$ that forms a Walrasian Equilibrium with some price vector $p^*$ is not Pareto Optimal. Then there is another feasible allocation $(x,y)$ such that $x^i \succsim_i x^{i*}\space \forall i\in I $, and $\exist i' \space x^{i'} \succ_{i'} x^{i'*}$. by local non-satiation, we have $px^i \geq m_i(p) \space \forall i\in I$ and $px^{i'} > m_{i'}(p)$. If we combine them, we can get:
$$
\sum_{i\in I} p^*x^i > \sum_{i\in I} p^*e^i +\sum_{i\in I} \sum_{j\in J} \theta^{ij} p^*y^{j*} = \sum_{i\in I} p^*e^i + \sum_{j\in J} (\sum_{i\in I}\theta^{ij}) p^*y^{j*} \\
=\sum_{i\in I} p^*e^i + \sum_{j\in J} p^*y^{j*}
$$
Since $y^{j*}$ is the solution to the profit maximization problem of the firm, we have $\sum_{j\in J} p^*y^{j*} \geq \sum_{j\in J} p^*y^{j}$ for any $j$. Combine this with the above equation, we have:
$$
\sum_{i\in I} p^*x^i >\sum_{i\in I} p^*e^i + \sum_{j\in J} p^*y^{j*} >\sum_{i\in I} p^*e^i +\sum_{j\in J} p^*y^{j}
$$
which is impossible if the feasible condition holds. Hence we get a contradiction. $\square$



### Core and Equilibria (P239 Jehle and Reny)

**Theorem: (Core and Equilibria)** Suppose the preference is locally non-satiated, then the Walrasian Equilibrium Allocation is in the core.

Proof:

Suppose not, and let $(x^*, y^*)$ and $p^*$ be a Walrasian Equilibrium Allocation, which is blocked by a subset $S\subset I$, then we have $x^i \succsim_i x^{i*}$ for all $i\in S$ and there exists $i'$ such that $x^{i'} \succ_{i'} x^{{i'}*}$, and $\sum_{i\in S} x^i \leq \sum_{i \in S} e^i + \sum_{i \in S} \sum_{j \in J} \theta^{ij} y^j$. Since we have local non-satiation, by the Local Non-satiation Theorem, $p^*x^i \geq p^*x^{i*} = p^*e^i +\sum_j \theta^{ij} p^*y^j \space \forall i \in S$ and $p^*x^{i'} > p^*e^{i'} +\sum_{j\in J} \theta^{{i'}j} p^*y^j$. Combine them we can get:
$$
\sum_{i\in S}p^*x^{i} > \sum_{i\in S}p^*e^{i} +p^*\sum_{j\in J} \sum_{i\in S}\theta^{{i}j} y^j
$$
But this cannot hold when feasibility is satisfied. Contradiction. $\square$



### Second Welfare Theorem

**Definition: (Equilibrium with Transfers)** Given an economy $\{x^i,\succsim_i, e^i\},\{y^j\}$, an allocation $(x^*, y^*)$ and a price vector $p^*$ constitute an equilibrium with transfers if there are some wealth levels $w = (w_1,...w_I)$ with $\sum_{i\in I }w_i = p^* e+\sum_{j\in J} p^* y^j$ where $y^{j*}$ solves the profit maximization problem, and for each $i$, $x^*$ solves the utility maximizing problem with the wealth level assigned to them, and the feasible condition holds, i.e. we have $\sum_{i\in I} x^{i*} \leq \sum_{i \in I} e^{i*} + \sum_{j \in J} y^{j*}$.

**Definition: (Income Transfer)** Define the Income Transfer of individual $i$ as $T_i = w_i - [p^*e_i+p^*\sum_{j \in J} \theta^{ij}y^{j*}]$.

**Definition: (Quasi-Equilibrium)** Given an economy $\{x^i,\succsim_i, e^i\},\{y^j\}$, an allocation $(x^*, y^*)$ and a price vector $p^*$ constitute a Quasi-Equilibrium with transfers if there are some wealth levels $w = (w_1,...w_I)$ with $\sum_{i\in I }w_i = p^* e+\sum_{j\in J} p^* y^j$ such that:

1. $\forall j \in J, \space p^*y^j \leq p^*y^{j*} $ for all $y^j\in Y^j$
2. $\forall i \in I, \space x^i \succ_i x^{i*} $ implies that $p^*x^i \geq w_i $
3. Feasibility is still true, i.e. $\sum_{i\in I} x^{i*} \leq \sum_{i \in I} e^{i*} + \sum_{j \in J} y^{j*}$

**Note:** The Definition of Quasi-Equilibrium will eliminate the problem of boundary solutions. Convexity ensures the existence of a hyperplane that support the better-than set.

**Lemma: (Separating Hyperplane Theorem)** If $A$ and $B$ are two disjoint convex subset of $\R^n$, then there exist a vector $p$, such that $pz\geq r$ for all $z \in A$, and $pz\leq r$ for all $z \in B$.

**Theorem: (Second Welfare Theorem)** Consider an economy $\{x^i,\succsim_i, e^i\},\{y^j\}$, we assume that $Y^j$ are convex for all $j\in J $, the preferences are convex and locally non-satiated. for all $i \in I$, then for each Pareto Optimal allocation $(x^*, y^*)$, there exists a price vector $p^* \neq 0$, such that $(x^*, y^*)$ forms a Quasi-Equilibrium with transfers.

Proof:

1. Aggregation

   Start with a Pareto Optimal allocation $(x^*, y^*)$, define the strictly-better-than sets as $V_i = \{x^i \in \R^n| x^i \succ_i x^{i*}\}$, and define $V = \sum_{i\in I} V_i$. Since we have that preferences are convex, which means for any two bundles $x'$ and $x''$, suppose $x' \succsim_ix''$, then for any $\theta \in [0,1]$, we have $\theta x'+(1-\theta) x''\succsim_ix''$,  i.e. $V_i$ are convex. Take the sum of finitely many convex set and we will still get a convex set, so $V$ is also convex.

   Now we aggregate all the firms and define the aggregate production set as $Y = \sum_{j\in J}Y^j = \{\sum_{j\in J}y^j\in \R^n|y^j\in Y^j \space \forall j\in J\}$, and the set of attainable consumption bundles as $Y+\{e\}$. Since  $Y^j$ are convex, we can conclude that $Y$ is also convex, and so is $Y+\{e\}$.

2. Separation

   Now want to show that $(Y+{e}) \cap V = \varnothing $. Because $(x^*, y^*)$ is Pareto Optimal, this must be true, otherwise there will exist a $x^{**}$ in the intersection area such that $x^{i**} \succ_i x^{i*}$, which is still feasible, contradicting to the fact that $(x^*, y^*)$ is Pareto Optimal.

   Now $Y+{e}$ and $V$ are two convex and disjoint set, by the Separating Hyperplane Theorem, there exists a vector $p\neq 0$, such that $pz\geq r$ for all $z\in V$ and $pz\leq r$ for all $z\in Y+\{e\}$.

   We claim that if $x_i \succsim_i x_i^*$ for all $i$, then $p x \geq r$. Take any  $x_i \succsim_i x_i^*$, by local non-satiation, there exists $\hat x_i \in B_\epsilon(x_i)$ such that $\hat x_i \succ_i x_i^*$, hence $\hat x_i \in V_i$ and $\sum_{i\in I}\hat x_i \in V$. So $p \sum_{i\in I}\hat x_i \geq r$ by the separation. Now take a sequence of $\hat x_i \to x_i$, then we have $p \sum_{i\in I} x_i \geq r$, which is what we claimed to be true. Now apply the result to $x_i = x_i^*$, we have $x_i^* \succsim_i x_i^*$, so by the claim we have $p x^* \geq r$. 

   Similarly, the separation gives us $pz\leq r$ for all $z = (\sum_{j\in J}y^{j}+e)\in Y+\{e\}$, which can be rewrite as $p(\sum_{j\in J}y^{j}+e)\leq r$. Remember $(x^*, y^*)$ is Pareto Optimal in the first place, and all Pareto Optimal allocations are feasible, i.e. $\sum_{i\in I} x_i^*  \leq \sum_{j\in J}y^{j*}+e$. Multiply by the price, we get $r \leq p\sum_{i\in I} x_i^*  \leq p(\sum_{j\in J}y^{j*}+e) \leq r$. 

   In a word, we conclude that $r = p\sum_{i\in I} x_i^*  = p(\sum_{j\in J}y^{j*}+e) $.

3. Decentralization

   Last we want to show that $x^*$ satisfies the consumer’s conditions of being a part of the Quasi-Equilibrium at price $p = p^*$, i.e. we want to show that $\forall i \in I, \space x^i \succ_i x^{i*} $ implies that $p^*x^i \geq w_i $ for some $w_i$.

   Suppose for person $k$ we have $x^k \succ_k x^{k*} $, define $\hat x^i = x^{i*}$ for $i\neq k$ and $\hat x^k = x^{k}$ then use the claim from step 2, we get that  $\hat x_i \succsim_i x_i^*$ for all $i$, then $p \hat x \geq r$. Since from step 2 we have $r = p\sum_{i\in I} x_i $, we have the following equation:
   $$
   p(x_k+\sum_{i\neq k} x_k^*) = p \hat x \geq r = p\sum_{i\in I} x_i^*
   $$
   Hence $px_k \geq px_k^*$.

   Similarly, we want to show that $\forall j \in J, \space p^*y^j \leq p^*y^{j*} $ for all $y^j\in Y^j$. Note that following similar steps, we have:
   $$
   p(e+y_k+\sum_{j\neq k} y_k^*) = p (e+\hat y) \leq r = p(e+\sum_{j\in J} x_j^*)
   $$
   Hence $py^j \leq py^{j*} $.

   In conclusion, $(x^*, y^*), p^*$ forms a Quasi-Equilibrium with transfers. $\square$

   

### Some Applications (P567 MWG)

