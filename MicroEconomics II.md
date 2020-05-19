# Microeconomics II

## Static Games of Complete Information

### Normal Form Games

**Definition: (Strategic Form Game)** A Strategic Form Game, G, is defined as a triplet: $G = \{N,S,u\}$. It is consisted of the following:

- A finite set of players: $N = \{1,2,...,n\}$
- A finite set of actions: For each $i\in N$, let $S_i$ denote the set of players $i$'s pure strategies, and call $s_i$ a typical element of $S_i$
- A pure strategy profile $s = (s_1, s_2,..., s_n)$ lists one pure strategy for each player, and the set of pure strategy profiles is $S = (\times_{i\in N}S_i)$
- Payoffs: Let $u = (u_1,u_2,..., u_n)$ denote a list of payoff functions $u_i : S \to R$ for each $ i \in N$. These payoffs essentially reflect the rules of the game

**Definition: (Zero-Sum Game)** The game above is a Zero-Sum Game if $\forall s\in S \sum_{i=1}^nu_i(s)=0$.

**Definition: (Mixed Extension)** $\Gamma = \{N,\Sigma,U\}$ is the Mixed Extension of $G = \{N,S,u\}$, which is consisted of the following:

- Let $\Sigma_i$ denote the set of mixed strategies of player $i \in N$. A typical element, $\sigma_i$, is a probability distribution over the set $S_i$ of player i's pure strategies: $\sigma_i =(\sigma_i(s_1); \sigma_i(s_2),..., \sigma_i(s_k))$, where $k = |S_i|$. Thus, $\Sigma_i$ is the set of all possible probability distributions over players $i$'s pure strategies:
  $$
  \Sigma_i = \{\sigma_i:S_i\to[0,1]^{|S_i|}|\sum_{s_i\in S_i}\sigma_i(s_i) = 1\} = \Delta (S_i) = \Delta^{|S_i|-1}
  $$
  This set is a simplex in $\R^{|S_i|}$. Observe that the dimension of this simplex is $|S_i|-1$, because of the constraint that probabilities must sum up to one. The n-dimensional simplex is often denoted $\Delta^{n-1}$.

- A mixed strategy prole $\sigma = (\sigma_1; \sigma_2,...,\sigma_n)$ lists one mixed strategy for each player. The set of mixed strategy profiles is $\Sigma = \times_{i\in N}\Sigma_i$

- Player i's payoff, $U_i(\sigma)$, from a mixed strategy profile $\sigma$, is a Von Neumann-Morgenstern expected utility:
  $$
  U_i(\sigma) = \sum_{s\in S} (\prod_{i\in N} \sigma_i(s_i))u_i(s) = E_\sigma[u_i(s)]
  $$

**Note:** We could use the notation $s = (s_i, s_{-i}) $, where $s_{-i} = (s_1,s_2,...,s_{i-1},s_{i+1},..., s_n)$.



### Dominance

#### Strict Dominance and Weakly Dominance

**Definition: (Strict Dominance)** $\sigma_i\in \Sigma_i$ is Strictly Dominated if there exists another $\sigma_i'\in \Sigma_i$ such that for all $s_{-i}\in S_{-i}$, we have $U_i(\sigma_i',s_{-i})>U_i(\sigma_i,s_{-i})$.

**Note:** When considering 2 by 2 games, we can only consider strict dominance with pure strategy. 

**Theorem: (Equivalent Strict Dominance)** $\sigma_i\in \Sigma_i$ is strictly dominated if and only if there exists another $\sigma_i'\in \Sigma_i$ such that for all $\sigma_{-i}\in \Delta S_{-i}$, we have $U_i(\sigma_i',\sigma_{-i})>U_i(\sigma_i,\sigma_{-i})$.

Proof:

By definition, $\sigma_i\in \Sigma_i$ is strictly dominated if there exists another $\sigma_i'\in \Sigma_i$ such that for all $s_{-i}\in S_{-i}$, we have $U_i(\sigma_i',s_{-i})>U_i(\sigma_i,s_{-i})$. By expected utility, we have $U_i(\sigma_i',\sigma_{-i})=\sum_{s_{-i}\in S_{-i}} \sigma _{-i}(s_{-i})u_i(\sigma_i',s_{-i})>\sum_{s_{-i}\in S_{-i}} \sigma _{-i}(s_{-i}) u_i(\sigma_i,s_{-i}) = U_i(\sigma_i,\sigma_{-i})$. $\square$

**Definition: (Weakly Dominance)** $\sigma_i\in \Sigma_i$ is Weakly Dominated if there exists another $\sigma_i'\in \Sigma_i$ such that for all $s_{-i}\in S_{-i}$, we have $U_i(\sigma_i',s_{-i})\geq U_i(\sigma_i,s_{-i})$ and there exists $s_{-i}\in S_{-i}$, we have $U_i(\sigma_i',s_{-i})> U_i(\sigma_i,s_{-i})$.

**Theorem: (Equivalent Dominance)** If the pure strategy $s_i$ is strictly (weakly) dominated then any mixed strategy that plays $ s_i$ with positive probability is also strictly (weakly) dominated.

Proof:

If the pure strategy $s_i$ is strictly dominated, then there is a $\sigma_i'\in \Sigma_i$ such that for all $s_{-i}\in S_{-i}$, we have $U_i(\sigma_i',s_{-i})>U_i(s_i,s_{-i})$. Then suppose $\sigma_i\in \Sigma_i$ is a mixed strategy that plays $ s_i$ with positive probability, and we have 
$$
U_i(\sigma_i,s_{-i})=\sum_{s\neq s_i} \sigma_{i}(s)u_i(s,s_{-i})+\sigma_{i}(s_i)u_i(s_i,s_{-i})\\
<\sum_{s\neq s_i} \sigma_{i}(s)u_i(s,s_{-i})+\sigma_{i}(s_i)U_i(\sigma_i',s_{-i})\\
=\sum_{s\neq s_i} \sigma_{i}(s)u_i(s,s_{-i})+\sigma_{i}(s_i)(\sum_{s\neq s_i} \sigma'_{i}(s)u_i(s,s_{-i})+\sigma'_{i}(s_i)u_i(s_i,s_{-i}))\\
=\sum_{s\neq s_i} (\sigma_{i}(s)+\sigma_{i}(s_i) \sigma'_{i}(s))u_i(s,s_{-i})+\sigma_{i}(s_i)\sigma'_{i}(s_i)u_i(s_i,s_{-i})=U_i(\hat \sigma_i,s_{-i})
$$
Hence $\sigma_i$ is strictly dominated by $\hat \sigma_i$, where $\hat \sigma_i(s) = \sigma_{i}(s)+\sigma_{i}(s_i) \sigma'_{i}(s)$ for $s \neq s_i$, and $\hat \sigma_i(s) = \sigma_{i}(s_i)\sigma'_{i}(s_i)$ for $s= s_i$. $\square$

#### IDSDS and IDWDS

**Definition: (Iterated Deletion of Strictly Dominated Strategies)** For a given mixed extension game $\Gamma = \{N,\Sigma,U\}$, Let $\Sigma^0 = \Sigma$. For every $i\in N$, and for every $k\geq 1$, let $\Sigma^k_i = \{\sigma_i | not \space strictly \space dominated|\Sigma^{k-1}_i\}$. So the Solution in Iterated Strict Dominance is defined as:
$$
\Sigma^\infty =\times_{i\in N} \cap_{k=0}^{\infty}\Sigma^k_i
$$



**Definition: (Iterated Deletion of Weakly Dominated Strategies)** For a given mixed extension game $\Gamma = \{N,\Sigma,U\}$, Let $\Sigma^0 = \Sigma$. For every $i\in N$, and for every $k\geq 1$, let $\Sigma^k_i = \{\sigma_i | not \space weakly \space dominated|\Sigma^{k-1}_i\}$. So the Solution in Iterated Weakly Dominance is defined as:
$$
\Sigma^\infty =\times_{i\in N} \cap_{k=0}^{\infty}\Sigma^k_i
$$

**Note:** Iterated Deletion of Weakly Dominated Strategies is not a good definition. We should never use this algorithm to solve for a solution of a game.

**Note:** A Nash equilibrium may be a profile of weakly dominated strategies.

**Theorem: (Order of Deletion)** In the iterated deletion of dominated strategies, the order of deletion:

1.  does not matter for strictly dominated strategies
2.  does matter for weakly dominated strategies. Different orders can lead to different results, and different number of strategy profiles surviving the iterated deletion of weakly dominated strategies.

Proof:

1. Consider the k-th round, given $ \Sigma_i^{k-1}$. Suppose $\sigma_i\in \Sigma_i^{k-1}$ is strictly dominated. Then there exists a $\hat \sigma_i \in \Sigma_i^{k-1}$ such that for all $s_{-i} \in S_i^{k-1}$, we have $U_i(\hat \sigma_i,s_{-i})>U_i(\sigma_i,s_{-i})$. Without loss of generality, suppose that $\hat \sigma_i$ is not strictly dominated. Then $\hat \sigma_i \in \Sigma_i^{k}$. Suppose we do not delete $\sigma_i$ in the k-th round, i.e. $\hat \sigma_i \in \Sigma_i^{k}$. By definition,  $\sigma_i$ is still strictly dominated by $\hat \sigma_i $, since $S^{k}_i\subset S^{k-1}_i$, so it will be deleted in the (k+1)-th round.
2. However, with IDWDS, $S^k_{-i}$ may no longer include the strategies $s_{-i}$ against which $\hat \sigma_i$ did strictly better than $\sigma_i$ under $S^{k-1}_{-i}$. $\square$ 



### Nash Equilibrium

#### Nash Equilibrium

**Definition: (Best Response)** $\sigma_i\in \Sigma_i$ is a Best Response to $\sigma_{-i}\in \Sigma_{-i}$ if for all $s'_i\in S_i$, $U_i(\sigma_i,\sigma_{-i})\geq U_i(s'_i,\sigma_{-i})$. 

**Definition: (Profitable Deviation)** For a given strategy profile $\sigma \in \Sigma$, if there is a strategy $\hat \sigma_i\in \Sigma_i$ such that $U_i(\hat\sigma_i, \sigma_{-i}) > U_i(\sigma_i, \sigma_{-i})$, then we say $\sigma_i$ has a Profitable Deviation.

**Definition: (Nash Equilibrium)** The strategy profile $\sigma^\star \in \Sigma^\star$ is a Nash Equilibrium if for all $i\in N$, we have for all $s'_i\in S_i$, $U_i(\sigma_i^\star, \sigma_{-i}^\star)\geq U_i(s'_i, \sigma_{-i}^\star)$.

**Theorem: (Equivalent Definition of Nash Equilibrium)** A Nash Equilibrium is a strategy profile where no body has a profitable deviation in pure strategies given the other players’ strategies. 

Proof:

It suffices to show that for a non Nash equilibrium strategy profile $\sigma\in \Sigma$, there is a profitable deviation in pure strategies. Since $\sigma$ is not a Nash equilibrium, let $\hat \sigma_i$ to be a profitable deviation from $\sigma_i$, i.e. $U_i(\hat \sigma_i,\sigma_{-i})>U_i( \sigma_i,\sigma_{-i})$ Suppose not, then for any $\hat s_i$ in the support of $\hat \sigma_i$, we have $u_i(\hat s_i,\sigma_{-i})\leq u_i( \sigma_i,\sigma_{-i})$. But then by expected utility property, we have $U_i(\hat \sigma_i,\sigma_{-i}) = \sum_{\hat s_i\in S_i}\hat \sigma_i(\hat s_i)U_i(\hat s_i,\sigma_{-i}) \leq \sum_{\hat s_i\in S_i}\hat \sigma_i(\hat s_i)U_i( \sigma_i,\sigma_{-i}) = U_i( \sigma_i,\sigma_{-i})$, which is a contradiction. $\square$

**Theorem: (Mixed Strategy Nash Equilibrium)** If $\sigma^\star$ is a Nash equilibrium in non-degenerate mixed strategies, i.e. there exist $s_i, s'_i \in S_i$ such that $\sigma^\star _{i}(s_i)>0$ and $\sigma^\star _{i}(s_i)>0$, it must be that $U_i(s_i,\sigma_{-i}^\star) = U_i(s'_i,\sigma_{-i}^\star)$. In general, if $\sigma^\star _{i}(s_i)>0$, then $U_i(s_i,\sigma_{-i}^\star) \geq U_i(s'_i,\sigma_{-i}^\star)$ for all $s_i' \in S_i$.

Proof:

Suppose the claim is incorrect. With out loss of generality, suppose $U_i(s_i,\sigma_{-i}^\star) > U_i(s'_i,\sigma_{-i}^\star)$, we have
$$
U_i(\sigma_i^\star,\sigma_{-i}^\star) = \sum_{s\neq  s'_i} \sigma_i^\star (s)u_i(s,\sigma_{-i}^\star)+ \sigma_i^\star(s'_i)U_i(s'_i,\sigma_{-i}^\star)< \sum_{s\neq  s'_i} \sigma_i^\star (s)u_i(s,\sigma_{-i}^\star)+ \sigma_i^\star(s'_i)U_i(s_i,\sigma_{-i}^\star) = U_i(\hat \sigma_i,\sigma_{-i}^\star)
$$
where $\hat \sigma_i$ is a profitable deviation of $\sigma_i^\star$, with probability $\hat \sigma_i(s) = \sigma_i^\star(s)$ if $s\neq s_i$ and $s\neq s'_i$, $\hat \sigma_i(s) = \sigma_i^\star(s_i)+\sigma_i^\star(s'_i)$ if $s= s_i$, and  $\hat \sigma_i(s) = 0$ if $s = s'_i$, which is impossible, because  $\sigma^\star$ is a Nash equilibrium and there is no profitable deviation. Contradiction. $\square$ 

#### Existence of the Nash Equilibrium

**Definition: (Finite Game)** A game $\Gamma = \{N,\Sigma,U\}$ is a finite game if $N$ and each $S_i$ are finite.

**Definition: (Best Response Correspondence)** For any $\sigma\in \Sigma$, define $r(\sigma) = \{(r_{-1}(\sigma_{-1}),...,r_{-N}(\sigma_{-N}))\}\subset \Sigma$ as the Best Response Correspondence.

**Definition: (Fixed Point)** A Fixed Point of $r$ is a strategy profile $\sigma^\star \in \Sigma$ such that $\sigma^\star \in r(\sigma^\star)$. It is a Nash Equilibrium.

**Lemma: (Kakutani Fixed Point Theorem)** Let $X\in \R^k$ be a compact convex set, suppose for each $x\in X$, the set $j(x)$ is a non-empty convex subset of $X$, and the graph of $j(x)$, denoted as $G = \{(x,y)|y\in j(x)\}$ is a closed subset of $X\times X$, then $j(x)$ admits a fixed points in $X$.

**Definition: (Upper Hemi-Continuous)** The correspondence $f$ is Upper Hemi-Continuous if for every $(x,y)\in X\times Y$, if $x^n\to x$ for $x^n\in X$, and $y^n\to y$ such that $y^n \in f(x^n)$, then $y\in f(x)$.

**Lemma: (Upper Hemi-Continuity and Closed Graph)** If the image of a compact sets are bounded, that $f$ is upper hemi-continuous is equivalent to that it has a closed graph.

**Theorem: (Existence of the Nash Equilibrium )** Every finite strategic-form game has a mixed strategy Nash Equilibrium.

Proof:

Let us show that we can apply Kakutani's fixed point theorem to $r$.

1. $\Sigma$ is a compact and convex set. Note that $N$ and $S_i$ are finite, Remember $\Sigma_i = \Delta(S_i)$ is the $|S_i|-1$ dimensional simplex, which is compact and convex. Hence $\Sigma = \times_{i\in N}\Sigma_i$ is also compact and convex.
2. $r$ is not empty-valued. If $S_i$ is finite, then at least one of its elements does better than the others against $\sigma_{-i}$.
3. $r$ is convex-valued. Suppose $\sigma_i\in r_i(\sigma_{-i})$ and $\hat \sigma_i\in r_i(\sigma_{-i})$. By definition of $r$ we have $u(\sigma_i,\sigma_{-i})\geq u_i(\sigma_i',\sigma_{-i})$ and $u(\hat \sigma_i,\sigma_{-i})\geq u_i(\sigma_i',\sigma_{-i})$ for all $\sigma_{-i}\in \Sigma_{-i}$. Take the linear combination of them, we get $\lambda u(\sigma_i,\sigma_{-i})+(1-\lambda)u(\hat \sigma_i,\sigma_{-i})\geq u_i(\sigma_i',\sigma_{-i})$. Then by expected utility property, we have $\lambda u(\sigma_i,\sigma_{-i})+(1-\lambda)u(\hat \sigma_i,\sigma_{-i}) = u( \lambda \sigma_i+(1-\lambda)\hat \sigma_i,\sigma_{-i})$. So $\lambda \sigma_i+(1-\lambda)\hat \sigma_i\in r_i(\sigma_{-i})$.
4. $r$ has a closed graph. By the lemma it is equivalent to prove that $r$ is upper hemi-continuous , i.e. we want to show that if $(\sigma^n, \tilde \sigma^n) \to (\sigma, \tilde \sigma)$ such that $\tilde \sigma^n\in r(\sigma^n)$ we have $\tilde \sigma\in r(\sigma)$. Suppose $\tilde \sigma\notin r(\sigma)$. In this case there exists a player $i$ such that there exists a $\sigma^+_i \neq \tilde \sigma_i$ and $\epsilon>0$ such that $u_i(\sigma_i^+,\sigma_{-i})>u_i(\tilde \sigma_i,\sigma_{-i})+\epsilon$. Now since $\tilde \sigma^n\in r(\sigma^n)$ we have $u_i(\tilde \sigma_i^n,\sigma_{-i}^n) \geq u_i(\sigma_i^+,\sigma_{-i}^n)$ for all $n$. Taking the limit we have $u_i(\tilde \sigma_i,\sigma_{-i}) \geq u_i(\sigma_i^+,\sigma_{-i})$, which is a contradiction.
5. Then by Kakutani’s fixed point theorem, the fixed point exists. $\square$ 

#### Rationalizability

**Definition: (Never a Best Response)** $ \sigma_i \in \Sigma_i$ is never a best response if there exists no $ \sigma_{-i} \in \Sigma_{-i}$ for which $ \sigma_i$ is a best response. 

**Theorem: (Never a Best Response and Strictly Dominated Strategies)** if a strategy is strictly dominated then it is never a best response.

Proof:

If $\sigma_i$ is strictly dominated by $\hat\sigma_i$, then the best response of any given $\sigma_{-i}$ would be $\hat\sigma_i$ or some other strategies. So it can never be a best response. $\square$ 

**Note:** The inverse of this statement is not true.

**Theorem: (Never a Best Response and Strictly Dominated Strategies II)** If there are only 2 players in the game, then if a strategy is never a best response then it is strictly dominated.

Proof:

Suppose $s_1\in S_1$ is never a best response for player 1. Suppose $s_1$ is not strictly dominated. Construct the following correspondence: $H(\sigma_1,\sigma_2) = \{\hat \sigma_1|r(\sigma_2) = \hat \sigma_1\}\times \{\hat \sigma_2|U_1(s_1,\hat \sigma_2)\geq U_1(\sigma_1,\hat \sigma_2)\}$ for $\sigma_i\in \Sigma_i$. Note that the first part of the correspondence follows from the existence of the Nash equilibrium, so it satisfies all the conditions of Kakutani’s theorem. The second part of the correspondence is the set of mixed strategies for player 2 for which $s_1$ is not strictly dominated. 

1. By assumptions $s_1$ is not strictly dominated, so this set is not empty. 

2. Note that this set is convex valued. Suppose $U_1(s_1,\hat \sigma_2)\geq U_1(\sigma_1,\hat \sigma_2)$ and $U_1(s_1,\hat \sigma_2')\geq U_1(\sigma_1,\hat \sigma_2')$ are satisfied, then the linear combination of these two also satisfies $U_1(s_1,\lambda\hat \sigma_2+(1-\lambda)\hat \sigma_2')\geq U_1(\sigma_1,\lambda\hat \sigma_2+(1-\lambda)\hat \sigma_2')$ by the expected utility property.
3. It is also upper hemi-continuous. Suppose $\sigma_1^n\to \sigma_1$, and $\hat\sigma_2^n\in \{\hat \sigma_2|U_1(s_1,\hat \sigma_2)\geq U_1(\sigma_1^n,\hat \sigma_2)\}$, and $\hat\sigma_2^n\to \hat\sigma_2$, we want to show that $\hat\sigma_2\in \{\hat \sigma_2|U_1(s_1,\hat \sigma_2)\geq U_1(\sigma_1,\hat \sigma_2)\}$. By condition we have $U_1(s_1,\hat \sigma_2^n)\geq U_1(\sigma_1^n,\hat \sigma_2^n)$ for all n. When $n\to +\infty$, we have $U_1(s_1,\hat \sigma_2)\geq U_1(\sigma_1,\hat \sigma_2)$.

Hence $H(\sigma_1,\sigma_2)$ satisfies the conditions for Kakutani’s theorem. Therefore we have a fixed point $(\sigma_1^\star, \sigma_2^\star)$ such that $U_1(s_1,\sigma_2^\star)\geq U_1(\sigma_1^\star,\sigma_2^\star)$ and $U_1(\sigma_1^\star , \sigma_2^\star) \geq U_1 (\sigma_1 , \sigma_2^\star)$ for all $\sigma_1\in \Sigma_1$. Then combine these two equation, we have $U_1(s_1,\sigma_2^\star)\geq U_1(\sigma_1^\star,\sigma_2^\star)\geq U_1 (\sigma_1 , \sigma_2^\star)$, i.e. $s_1$ can be a best response sometimes, contradicting to the fact that $s_1$ is never a best response. $\square$ 

**Definition: (Rationalizability)** Rationalizability is the iterated deletion of strategies that are never a best response.



### Correlated Strategy

#### Public randomization

**Definition: (Sunspot)** A Sunspot is a random variable $z\in \Omega$, whose realization can be perfectly observed by all the players in the game. It stands for the public states in the game.

**Definition: (State Dependent Strategy)** A State Dependent Strategy is a function $s_i: \Omega\to \Delta S_i$.

**Claim: (Joint Randomization Nash Equilibrium)** If players can jointly observe a sun spot before play, they can achieve any linear combinations of the payoffs of the Nash Equilibria by joint randomization between the two pure strategy Nash Equilibria.

#### Correlated private signals

**Definition: (Correlation Device)** A correlation device is a triple: $\{\Omega, \pi, \{P_i\}_{i\in N}\}$, where $\Omega$ is a finite state space corresponding to the outcomes of the device, and $\pi$ is a probability measure on the state space $\Omega$. For each $ i \in N$, $P_i$ is a partition of $\Omega$ representing player i’s information.

**Definition: (Correlated Game)** A Correlated Game is defined as $\Gamma = \{N,\Sigma,U\}\times \{\Omega, \pi, \{P_i\}_{i\in N}\}$.

**Definition: (Correlated Strategy)** A Correlated Strategy is defined as a probability distribution over all of the strategy profiles $p\in \Delta (\times_{i=1}^n S_i)$.

**Definition: (Marginal Probability of a Strategy)** the Marginal Probability of playing a strategy is $p(s_i) = \sum_{s_{-i}\in S_{-i}}p(s_{i},s_{-i})$.

**Definition: (Conditional Probability of a Strategy)** the Conditional Probability of other playing a strategy is $p(s_{-i}|s_i) = p(s_i,s_{-i})/p(s_{i})$.

**Definition: (Correlated Strategy Equilibrium)** A Correlated Strategy Equilibrium is a correlated strategy profile where for all $s'_i\in S_i$, we have
$$
\sum_{s_{-i}\in S_{-i}} p(s_{-i}|s_i)u_i(s_i,s_{-i}) \geq \sum_{s_{-i}\in S_{-i}} p(s_{-i}|s_i)u_i(s_i',s_{-i})
$$
**Note:** Correlated strategy equilibrium can include the mixed strategy equilibrium, but they are not the same. The mixed strategy equilibrium is when the player’s strategies are independent to each other’s strategy.

**Theorem: (Linear Combination)** The linear combination of two correlated equilibria is a correlated equilibrium.

Proof:

Suppose two correlated equilibria are $p^1$ and $p^2$, we have $\sum_{s_{-i}\in S_{-i}} p^1(s_i,s_{-i}) u_i(s_i,s_{-i}) \geq \sum_{s_{-i}\in S_{-i}} p^1(s_i,s_{-i}) u_i(s_i',s_{-i})$ and $\sum_{s_{-i}\in S_{-i}} p^2(s_i,s_{-i}) u_i(s_i,s_{-i}) \geq \sum_{s_{-i}\in S_{-i}} p^2(s_i,s_{-i}) u_i(s_i',s_{-i})$. Suppose one linear combination of them is $\gamma p^1+(1-\gamma)p^2$. From the assumption, we can easily conclude that:
$$
\sum_{s_{-i}\in S_{-i}} (\gamma p^1(s_i,s_{-i})+(1-\gamma)p^2(s_i,s_{-i})) u_i(s_i,s_{-i}) \geq \sum_{s_{-i}\in S_{-i}} (\gamma p^1(s_i,s_{-i})+(1-\gamma)p^2(s_i,s_{-i})) u_i(s_i',s_{-i})
$$
which is what we want to show. $\square$

**Theorem: (Linear Combination)** Every mixed strategy Nash equilibrium can be denoted as a correlated equilibrium.

Proof:

For a mixed strategy Nash equilibrium $\sigma$, we can define $p(s_i,s_{-i})  =\sigma_i(s_i)\sigma_{-i}(s_{-i})$. Now by definition, we have $\sum_{s_{i}\in S_{i}} \sum_{s_{-i}\in S_{-i}} \sigma(s_i)\sigma_{-i}(s_{-i}) u_i(s_i,s_{-i}) \geq \sum_{s_{i}\in S_{i}}\sum_{s_{-i}\in S_{-i}} \sigma(s_i)\sigma_{-i} u_i(s_i',s_{-i})$. We want to show that $ \sum_{s_{-i}\in S_{-i}} \sigma(s_i)\sigma_{-i}(s_{-i}) u_i(s_i,s_{-i}) \geq \sum_{s_{-i}\in S_{-i}} \sigma(s_i)\sigma_{-i} u_i(s_i',s_{-i})$ for all $s_i$. Remember from the mixed strategy Nash equilibrium theorem we have $U_i(s_i,\sigma_{-i}^\star) \geq U_i(s'_i,\sigma_{-i}^\star)$, which is exactly what we want to show. $\square$

**Solution: (Social Optimal)**

The social optimal correlated equilibrium is a correlated equilibrium such that the aggregated social welfare is maximized.



## Dynamic Games of Complete Information

### Extensive Form Game

#### Extensive Form Game

**Definition: (Extensive Form Game)** An Extensive Form Game is defined as $(N,A,X,Z,\iota, u)$ , where we have:

- A finite collection of decision nodes $x\in X$, each corresponding to a history
- A finite collection of terminal nodes $z\in Z$
- A finite set of players $N$
- A function attributing a player to each decision node $\iota: X\to N$
- For each $x \in X$, the set of feasible actions $A(x)$
- A payoff function attributing a payoff profile to each terminal $u:z\to \R^N$

**Definition: (Pure Strategy Profile)** A Pure Strategy for player i is a mapping $s_i:X\to A_i$ with the constraint that $s_i(x)\in A(x)$ for all $x \in X_i$. The set of player i’s pure strategies is $S_i=\times_{x\in X_i} A(x)$ and the set of pure strategy profiles is $S = \times_{i\in N} S_i$.

**Claim: (Associated Normal Form)** For any extensive form game, we can always write down the associated normal form game, which is also known as the associated strategic form game. Reduce the equivalent to one single representative, and we will get a reduced normal form game.

#### Imperfect information

**Definition: (Information Set)** Consider a partition $H$ of $X$ such that if $x$ and $x'$ are in the same element $h\in H$, we have

- $\iota (x) = \iota (x')$
- $A (x) = A (x') = A(h)$

Then $H$ partitions $X$ into Information Sets.

**Note:** In a game of perfect information, all the information sets are singletons.

**Definition: (Nature)** The Nature is the player 0 whose actions are the possible outcomes of a lottery.

**Definition: (Extensive Form Game)** An Extensive Form Game is defined as $\{N,A,X,Z,\iota, H,\pi ,u\}$.

**Definition: (Pure Strategy Profile)** A Pure Strategy for player i is a mapping $s_i:H_i\to A_i$ with the constraint that $s_i(h)\in A(h)$ for all $h \in H_i$. The set of player i’s pure strategies is $S_i=\times_{h\in H_i} A(h)$ and the set of pure strategy profiles is $S = \times_{i\in N} S_i$.



### Subgame Perfection 

#### Backwards Induction

**Definition: (Backwards Induction)** Consider an extensive form game of perfect information, Let $Y_0 = Z$. For every $j\geq 1$, let
$$
Y_j = \{x\in X \setminus \cup_{k=0}^{j-1} Y_k| \nexists x'\in X\setminus \cup_{k=0}^{j-1} Y_k, x\prec x' \}
$$
The backward induction solution $a^\star$ is defined as follows: let $u^\star(z) = u(z)$ for every $z\in Z$ \. For every $j\geq 1$ and every $x\in Y_j$ let $a^\star = argmax_{a\in A(x)} u^\star _{\iota(x)}(x,a)$ and $u^\star (x) = u^\star(x, a^\star)$.

**Note:** Backwards induction is equivalent to iterated weak dominance in a certain order.

#### Proper Subgame

**Definition: (Proper Subgame)** A decision node $x\in X$ defines a Proper Subgame of an extensive form game if $h(x) = \{x\}$ and for every node $y\in X$ following $x$, if $y'\in h(y)$ then $y'$ also follows $x$.

**Definition: (Pure Strategy Subgame Perfect Equilibrium)** A pure strategy profile $s\in S$ constitutes a Pure Strategy Subgame Perfect Equilibrium if $s$ induces a Nash equilibrium in every proper subgame of the extensive form game.

**Note:** $BI\subset SPE\subset NE$.

#### Mixed Strategy and Behavioral Strategy

**Definition: (Mixed Strategy)** For player $i\in N$ a Mixed Strategy is defined as $\sigma_i\in \Sigma_i$, where $\Sigma_i = \Delta(\times_{h\in H_i}A(h))$.

**Definition: (Behavioral Strategy)** For player $i\in N$, a Behavioral Strategy is defined as $b_i\in B_i$, where $B_i = \times_{h\in H_i}\Delta(A(h))$.

**Definition: (Equivalent Strategies)** Two strategies are Equivalent if they lead to the same distribution over outcomes for all strategies of the opponents.

**Definition: (Perfect Recall)** No player may “forget” information she previously knew.

**Claim: (Kuhn’s Theorem)** Under perfect recall, mixed and behavioral strategies are equivalent.

**Definition: (Behavioral Strategy SPE)** A behavioral strategy profile $b$ is a SPE of the finite extensive-form game $\Gamma$ if it induces a Nash equilibrium in every proper subgame of $\Gamma$.

**Claim: (Selten’s Theorem)** Every finite extensive-form game with perfect recall has a SPE.



### One Shot Deviation

**Definition: (Continuation Game)** An information set $h\in H$ defines a Continuation Game of an extensive form game if for every node $y\in X$ following $h$, if $y'\in h(y)$ then $y'$ also follows $h$.

**Definition: (Continuation Strategy)** Consider $s_i\in S_i$ and $h\in H$. Let $s_i|h$ be strategy that $s_i$ induces over the continuation game $\Gamma(h)$, i.e. $s_i|_h(h') = s_i(h,h')$ for all $h' \in H_i|h$, where $H_i|h$ is the set of all continuation histories $h'$ following $h$ such that $(h,h')\in H_i$.

**Definition: (Outcome Function)** For  every $s\in S$ define $O(s)$ to  be  the  terminal  node that is reached when $s$ is played.  Let $O_h$ denote the outcome function in $\Gamma(h)$.

**Theorem: (One Shot Deviation Principle)** Suppose $s^\star$ is a SPE of a finite horizon game of perfect information if and only if there exists no profitable one shot deviation, that is for every $h \in H_i$, we have $u_i(O_h(s_i^\star|_h,s_{-i}^\star|_h)) \geq u_i(O_h(s_i|_h,s_{-i}^\star|_h))$ for every strategy $s_i\in S_i$ restricted to the continuation game $\Gamma(h)$ that differs from $s_i^\star|_h$ only in the action it prescribes at the initial information set of $\Gamma(h)$, i.e. $s_i^\star(h)\neq s_i(h)$ and $s_i^\star(h,h')\neq s_i(h,h')$ for every $h' \in H_i|_h$.

Proof:

It is trivial to show if $s^\star$ is a SPE then there is no profitable one shot deviation. So it suffices to show that it a strategy profile has no profitable OSD then it is a SPE.

It is equivalent to show that if $s^\star$ is not a SPE, then there is a profitable OSD. Suppose there is no profitable OSD. However, by the fact $s^\star$ is not a SPE, we know for sure there is a profitable deviation. Since we are arguing with a finite game, we can find the shortest profitable deviation by choosing $s_i$ that does better for player $i$ than $s_i^\star$ but differs from it as seldom as possible in $\Gamma(h')$.

Let $h^\star \in H$ be the longest history at which $s_i$ and $s_i^\star$ differ. In the continuation game $\Gamma(h^\star)$, $s_i^\star$ and $s_i$ only differs at the first information set, and $s_i|_{h^\star}$ does strictly better than $s_i^\star|_{h^\star}$, otherwise we could find a shorter profitable deviation $s_i'\in \Gamma (h')$, contradicting to the fact that $s_i$ is the shortest profitable deviation.

But then we found a profitable OSD, hence establishing a contradiction. $\square$ 

**Definition: (Continuity at Infinity)**  Let $ h, h' \in H$ be two infinite-horizon histories. A game is Continuous at Infinity if for every $i\in N$, if
$$
lim_{t\to \infty} sup_{(h,h')|h_t=h_t'}|u_i(h)-u_i(h')|=0
$$
**Note:** If continuity at infinity is satisfied then OSD can still work.

**Note:** The one shot deviation principle should be checked at every history, on path or off path, i.e. no matter whether the history happened or not, we should always check that there is no profitable OSD.



### Rubinstein Bargaining Model

#### Setup

**Assumption: (Setup)**

- Two parties alternate in making offers. Given a party’s offer, the other party may either accept (and the game ends) or reject, in which case the game proceeds to the next round. 
- There is no bound on the number of possible rounds: $T = \{0, 1, 2, . . . \}$. The fact that one offer is rejected places no restrictions on subsequent offers. (For instance, a player who has just rejected an offer, x, may make a counteroffer that is worse for her than x was.)
- Let X denote the set of possible offers at every stage: $X = \{x = (x_1,x_2)|x_1\geq 0, x_2\geq 0, x_1+x_2=1\}$
- Payoffs: perpetual disagreement: payoff of 0 to both.
- Agreement on $x \in X$ at date t is denoted as the outcome $(x, t) \in X \times T$ and is assessed by both parties as follows: $u_i(x, t) = \delta_i ^ t x_i$ , $\forall i \in \{1, 2\}$, where $\delta _i \in (0, 1)$ is player i’s discount factor.

#### Nash Equilibrium

**Theorem: (Nash Equilibrium)**  For all $\bar x \in X$, there exists a Nash Equilibrium of the following form: for each $i \in \{1, 2\}$: at each history in $B_i$ , Player i offers $\bar x$; at each history in $B_j$ , Player i accepts x if and only if $ x_i ≥ \bar x_i$.

Proof:

Given j’s strategy, there is no profitable deviation for player i. If i offers $x< \bar x$, then he will obviously get less, which is not profitable. If he offers $x>\bar x$, then the other player will reject. and he will get $\delta_i\bar x_i<\bar x_i$, so it’s not profitable.

Now suppose the player j reject, then he well propose $\bar x$ again in the next turn. so he will get $\delta_j\bar x_j<\bar x_j$, which is not profitable. $\square$ 

**Note:** There is an one shot deviation for this game: at the history that player 1 proposes $x_2\in (\delta_2 \bar x_2,\bar x_2)$, player 2 has an OSD, which is to deviate to accept. Because playing reject is a non credible threat. Notice that we are checking an OSD that is not on the path of the game. remember in a SPE we need to check every subgame of the game, no matter if it is on path or not. 

**Theorem: (Nash Equilibrium)**  For all $\bar x,\bar y \in X$, suppose $\bar y_1/ \delta_1 \geq\bar x_1\geq \delta _1 \bar y_1$ and $\bar x_2/ \delta_2 \geq\bar y_2\geq \delta_2 \bar x_2$. There exists a Nash Equilibrium of the following form: at each history in $B_1$ , Player 1 offers $\bar x$, and Player 2 accepts x if and only if $ x_2 ≥ \bar x_2$; at each history in $B _2$, Player 2 offers $\bar y$, and Player 1 accepts y if and only if $ y_1 ≥ \bar y_1$.

Proof:

Consider $x_1>\bar x_1$, then player 2 will reject and offer $\bar y$, it can only be a Nash equilibrium if $x_1>\delta_1 \bar y_1$, which is implied by $\bar x_1\geq \delta_1\bar y_1$, and similarly $\bar y_2\geq \delta_2\bar x_2$.

Now suppose the player 2 deviates to reject, then he well propose $\bar y$ in the next turn. so he will get $\delta_2\bar y_2<\bar x_2$, which is implied by $\bar x_2\geq \delta_2\bar y_2$, and similarly $\bar y_1\geq \delta_1\bar x_1$ . $\square$ 

#### Candidate SPE

**Theorem: (SPE)** We claim that the following strategy profile is a SPE of the game:

- At each history in $B_1$, player 1 offers $x^\star = (x^\star_1,x^\star_2)$, and player 2 accepts if $x\geq x_2^\star$
- At each history in $B_2 $, player 2 offers $y^\star = (y^\star_1,y^\star_2)$, and player 1 accepts if $y\geq y_1^\star$

Proof:

1. To ensure hat our candidate equilibrium strategy prole does not contain incredible threats, we require that accepting your opponent's offer today is no better than (rejecting her offer today and) having your own offer accepted tomorrow:
   $$
   u_1(y^\star,t)\leq u_1(x^\star,t+1)\\
   u_2(x^\star,t)\leq u_2(y^\star,t+1)
   $$
   Since both players are trying to make a offer that will give themselves more, we can change the inequality signs to equality signs. So we have:
   $$
   y_1^\star = \delta_1x_1^\star\\
   x_2^\star = \delta_2y_2^\star
   $$
   which will give us $x^\star = (\frac{1-\delta_2}{1-\delta_1\delta_2},\frac{\delta_2(1-\delta_1)}{1-\delta_1\delta_2})$, and $y^\star = (\frac{\delta_1(1-\delta_2)}{1-\delta_1\delta_2},\frac{1-\delta_1}{1-\delta_1\delta_2})$.

2. Now check the one shot deviation:

   Consider each history in subgame $B_1$: first consider the deviation for player 1. Suppose he make an offer such that $x_1>x_1^\star$, then player 2 will reject. Then player 1’s payoff is $u_1(y^\star, 1) = \delta_1 y^\star_1 = \delta_1^2x_1^\star<x_1^\star$, which is not profitable. So there is no profitable deviation for player 1.

   Now consider deviation for player 2. First, check the on-path deviation: if player 1 offers $x_1^\star$, then player 2 deviate to reject, he will get $u_2(y^\star,1) = \delta_2y_2^\star = x_2^\star$, which is not profitable. Second check the off-path history: if player 1 offers $x_2>x_2^\star$, and he reject, he will get $u_2(y^\star,1) = \delta_2 y_2^\star = x_2^\star<x_2$, which is not profitable;  if player 1 offers $x_2<x_2^\star$, and he accept, he will get $u_2(x,0) = x_2< \delta_2 y_2^\star = x_2^\star$, which is also not profitable.

   In a word, it is a SPE. $\square$

#### Uniqueness of SPE

**Theorem: (Uniqueness of SPE)** The SPE of Rubinstein Bargaining Model is Unique.

Proof:

1. Consider for each $i\in \{1,2\}$ the set of SPE strategies is defined as $\Sigma_i^\star = \{\sigma =SPE(B_i)\}$. Define $m_i$ and $M_i$ as
   $$
   m_i= inf_{\sigma\in \Sigma_i^\star}\{u_i(x,t)|\sigma\in B_i\} \\
   M_i= sup_{\sigma\in \Sigma_i^\star}\{u_i(x,t)|\sigma\in B_i\}
   $$
   
2. In any SPE, Player j is guaranteed the payoff $m_j$ in a subgame $B_j$. Thus, in a subgame $B_i$, she rejects all offers that give her less than $\delta_jm_j $. Therefore, in a subgame $B_i$, player i cannot get more than $1 - \delta_jm_j$, so $M_i\leq  1 - \delta_jm_j$.

3. In any SPE, Player j’s best payoff is  $M_j$ in a subgame $B_j$. Thus, in a subgame $B_i$, she accepts all offers that give her more than $\delta_jM_j $. Therefore, in a subgame $B_i$, player i cannot get less than $1 - \delta_jM_j$, so $m_i\geq  1 - \delta_jM_j$.

4. Combine these two inequalities and use the fact that $M_i\geq m_i$, we have $m_j=M_j$. Thus in every subgame where player i makes the offer, the SPE payoff is unique. Hence the SPE is unique. $\square$



### Repeated Games

#### Basic Structure

**Definition: (Repeated Game)** Consider the mixed extension of the stage game $G = (N,A,u)$. The players play G at each date. Let $G(\infty)$ denote the infinitely Repeated Game.

**Definition: (Perfect Monitoring)** At the end of each period $t \geq 0$ (after each stage game is played) all players observe the realized action profile, then the players have Perfect Monitoring.

**Definition: (History)** A History up to time t is the outcomes up to time t, denoted as $h^t = (a^0,a^1, ...,a^{t-1}) \in H^t$. So the Set of Possible Histories is defined as $H = \cup_{t=0}^\infty H^t$

**Definition: (Strategies)** In $G(\infty)$, a Pure Strategy is defined as $s_i\in S_i:H\to A_i$, and a behavioral strategy is defined as $\sigma_i\in \Sigma_i:H\to \Delta(A_i)$. Each Pure Strategy Profile $s = (s_1,...,s_n)$ induces a unique Outcome Path $a(s) = (a^0(s),a^1(s) ...)$.

**Definition: (Continuation Strategy)** A Continuation Strategy is defined as $s_i|_{h^t}(h^\tau) = s_i(h^t,h^\tau)$ induced by a history $h^t\in  H^t$.

**Definition: (Average Discounted Payoff)** The average discounted payoff is defined as $U_i(s) = (1-\delta)\sum_{t=0}^\infty \delta^tu_i(a^t(s))$.

**Definition: (Nash Equilibrium)** The strategy profile $\sigma^\star\in \Sigma$ is a Nash Equilibrium of $G(\infty )$ if for every $i \in N$, and for all $\sigma_i\in \Sigma_i$ we have $U_i(\sigma^\star_i,\sigma^\star_{-i})\geq U_i(\sigma_i,\sigma^\star_{-i})$.

**Corollary: (Existence of Nash Equilibrium)** By the existence of Nash Equilibrium for the stage game, we have that the Nash Equilibrium of a repeated game always exists.

**Definition: (Subgame Perfect Equilibrium)** The strategy profile $\sigma^\star\in \Sigma$ is a Subgame Perfect Equilibrium of $G(\infty )$ if for every $t\geq 0$, and for all every history $h^t\in H^t$, $\sigma^\star |_{h^t}$ is a Nash Equilibrium of $G(\infty)$.

**Corollary: (Existence of Nash Equilibrium)** By the existence of Nash Equilibrium for the stage game, we have that the Subgame Perfect Equilibrium) of a repeated game always exists.

#### Automaton

**Definition: (Automaton)** An Automaton of player i is defined with following components:

- A set of states $W_i$
- An initial state $w_0\in W_i$
- An output function $f:W_i\to \Delta A_i$
- A Transition function $T: W_i\times A_i \to W_i$

**Note:** The total number of possible transitions is the number of types of histories for the player.

#### Folk Theorem

**Definition: (Feasible Payoff)** Let $F$ denotes the Feasible Payoff $F = conv\{v\in \R^n|\exist a\in A, v = u(a)\}$.

**Definition: (Mixed Strategy Minmax)** Player i’s mixed strategy minmax is defined as $\underline v_i  = min_{\sigma_{-i}}max_{\sigma_i} U_i(\sigma_i,\sigma_{-i})$.

**Corollary: (Nash Equilibrium Lower Bound)** Suppose $\sigma^\star$ is a (possibly mixed) Nash Equilibrium of $G(\infty)$. Then $U_i(\sigma^\star)\geq \underline v_i$.

**Definition: (Feasible Individually Rational Payoffs)** the Feasible Individually Rational Payoffs is defined as
$$
F^\star  = F\cap\{v\in \R^n | v_i\geq \underline v_i \forall i\in N\}
$$
**Claim: (Folk Theorem)** Suppose $F^\star$ has a non-empty interior in $R^n$. For all $v \in F^\star$, there exists a $\delta_0 \in (0, 1)$ such that for all $\delta ≥ \delta_0 $, $v$ can be supported by a SPE of the infinitely repeated game.

**Note:** For any feasible individually rational payoffs, we could define a SPE with appropriate $\delta$ by using a strategy profile with public randomization.



## Incomplete Information Game

### Static Games of Incomplete Information

**Definition: (Incomplete Information Bayesian Game)** A game of Incomplete Information Bayesian Game is defined as $(N,S,\Theta, u,p)$, where

- A set of players: $N = \{1, . . . , n \}$
- A set of pure action profiles: $S = \times_{i\in N} S_i $where $S_i$ is the set of player i’s pure actions
- A set of possible types $\Theta = \times _{i\in N} \theta_i $ where $\theta_i$ is the set of player i’s possible types
- A payoff function for each player: $u_i : S \times \theta → \R$
- A joint probability distribution $p$ over $\Theta$ such that $p(\theta_i) > 0$ for all $\theta_i \in \Theta_i$

**Definition: (Pure Strategy)** A Pure Strategy for player i is a mapping $s_i : \Theta_i \to S_i$ prescribing an action for each possible type of player i.

**Definition: (Pure Strategy Bayes-Nash Equilibrium)** A strategy profile $s : \Theta \to S$ is a Pure Strategy Bayes-Nash Equilibrium if $ \forall i \in N $and $\forall \theta_i \in \Theta_i$ we have that
$$
s_i(\theta_i) \in argmax_{ \hat s_i\in S_i} \sum_{ \theta_{-i}\in \Theta_{-i}} p(\theta_{−i} |\theta_i) u_i(\hat s_i , s_{−i}(\theta_{ −i}); \theta_i , \theta_{−i})
$$
**Claim: (BNE Existence)** Consider a finite game of incomplete information. Then a mixed strategy Bayes-Nash Equilibrium exists. 

**Claim: (Pure Strategy BNE Existence)** Consider a Bayesian game with continuous action spaces and continuous types. If action sets and type sets are compact, and payoff functions are continuous and concave in own actions, then there exists a pure strategy Bayes-Nash Equilibrium.



### Extensive-Form Equilibrium Refinements

#### Perfect Bayesian Equilibrium

**Definition: (Assessment)** Let $\mu_h(x)$ denote player $\iota(x)$’s belief that node $x \in h$ is reached conditional on information set $h \in H$ being reached. A system of beliefs $\mu = (\mu_h)_{h\in H}$ is a collection of beliefs such that $\forall h \in H, \mu_h \in \Delta(h)$. A pair$ (b, \mu) $ is called an Assessment.

**Note:** Given some information set $h \in H_i$ , we can evaluate player i’s expected utility $Eu_i( b|h ; \mu_h)$ from the continuation strategy profile $b|h$.

**Definition: (Conditional Probability)** For every node $x \in X$, let $P(x|b)$ denote the Probability that node $x$ is reached under the behavioral strategy profile $b$. We have $P(x|b) = \Pi_{a\in a^x}b(a)$, where $a^x$ is the path of actions leading from the initial node $x^0$ to the node $x$. And for every information set $h \in H$, let $P(h|b)$ denote the Probability that $h$ is reached under the behavioral strategy profile $b$. We have $P(h|b) = \Pi_{x\in h}P(x|b)$.

**Definition: (Perfect Bayesian Equilibrium)** An assessment $(b, \mu)$ constitutes a Perfect Bayesian Equilibrium of the game if $\forall h \in H$:

1. Sequential rationality is satisfied, i.e. the strategy $b_{\iota(h)}$ maximizes player $\iota(h)$’s expected continuation payoff, where the expectation is taken with respect to player $\iota(h)$’s belief: for every behavioral strategy $ b'_{\iota(h)}$,  we have $E_{u_\iota(h)}[b|h;\mu_h]\geq E_{u_\iota(h)}[b'_{\iota(h)},b_{-\iota(h)}|h;\mu_h]$
2. Bayes’ rule, i.e. whenever possible, beliefs are defined by Bayes’ rule: if $P(h|b) > 0$, then $\forall x \in h$, $\mu_h(x) = \frac{P(x|b)}{P(h|b)}$

**Note:** If $P(h|b) = 0$, PBE imposes no restriction on beliefs beyond sequential rationality. This is why this solution concept is sometimes called weak PBE.

**Claim: (PBE and NE)** If the assessment $(b, \mu)$ is a PBE, then the strategy profile $b$ is a NE.

**Note:** PBE imposes sequential rationality (in the sense of eliminating incredible threats) on path, but may fail to impose it off path, when beliefs are not defined by Bayes’ rule.

#### Sequential Equilibrium

**Definition: (Independence)** Beliefs must reflect that players choose their strategies independently.

**Definition: (Common Beliefs)** Players with identical information have identical beliefs.

**Definition: (Consistent)** An assessment $(b, \mu)$ is consistent if there exists a sequence of completely mixed behavioral strategies, $(b_n )$, converging to $b$, such that the associated sequence of Bayes’ rule induced systems of beliefs, $\mu_n$, converges to $\mu$.

**Definition: (Sequential Equilibrium)** An assessment $(b, \mu)$ constitutes a Sequential Equilibrium of the game $\Gamma$ if $\forall h \in H$:

1. Sequential rationality: the strategy profile $b$ is sequentially rational, given $\mu$
2. Consistency: the assessment $(b, \mu)$ is consistent.

**Claim: (PBE and SE)** If $(b, \mu)$ is a sequential equilibrium then $(b, \mu)$ is a Perfect Bayesian Equilibrium.

**Claim: (SPE and SE)** If the assessment $(b, \mu)$ is a sequential equilibrium, then the strategy profile $b$ is a SPE.

**Note:** If all information sets are reached, PBE and SE are equivalent. To circumvent the business of having to define your equilibrium concept, just use SE, as there is consensus as to its definition.

**Note:** If some information sets are not reached, use SE if feasible. If not, proceed with care, and it is not a refinement of SPE.



### Signaling Game

**Definition: (Signaling Game)** The Signaling game is defined as:

- Let $\theta = \{\theta_1, \theta_2, .., \theta_k\}$, denote the set of possible types of the sender
- Let $p \in \Delta(\theta)$ denote the common prior probability distribution over the type space
- Let$ M = \{m_1, m_2, ..., m_h\}$ denote the set of messages available to the sender
- Let $A = \{a_1, a_2, ..., a_l\}$ denote the set of actions available to the receiver
- If the sender is of type $\theta\in \Theta$, sends message $m \in M$ and the receiver takes action $a \in A$, their respective payoffs are denoted $u_S(m,a, \theta)$ for the sender and $u_R(m,a, \theta)$ for the receiver. Payoffs from mixtures are defined in the usual way

The extensive form game is as follows:

- First, Nature chooses sender’s type $\theta\in \Theta$ according to the probability distribution $p \in \Delta(\theta)$
- The sender privately observes her own type (i.e. the receiver does not). She then chooses a message $m \in M$
- The receiver observes the chosen message and chooses an action $a \in A$
- The payoffs at the corresponding terminal node are $u_S(m,a, \theta)$ and $u_R(m,a, \theta)$

**Definition: (PBE in Signaling Game)** A perfect Bayesian equilibrium of a signaling game is an assessment $(\sigma^\star , \rho^\star , \mu^\star )$ if

- Sequential rationality for the sender: for all $\theta\in \Theta$, we have $\sigma^\star (\theta) = argmax_{\sigma\in \Delta(M)} u_S(\sigma,\rho^\star, \theta)$
- Sequential rationality for the receiver: for all $m\in M $, we have $\rho^\star (m) = argmax_{\rho\in \Delta(A)} \sum_{\theta\in \Theta}\mu^\star (\theta|m)u_R(m,\rho, \theta)$
- Bayes Rule: for any $\theta, m$, if $\sum_{\theta'\in \Theta} p(\theta')\sigma^\star(m,\theta')>0$, we have $\mu^\star(\theta|m) = \frac{p(\theta)\sigma^\star(m|\theta)}{\sum_{\theta'\in \Theta}p(\theta')\sigma^\star(m|\theta')}$, and otherwise $\mu^\star$ is any probability distribution

**Claim: (Fudenberg and Tirole)** Consider a multi stage game of incomplete information with independent types. If either each player has at most two possible types, or there are two periods, then the set of PBE and SE of the game coincide with each other.

**Definition: (Pooling and Separating Solution)** Types that send messages that are different from those sent by any other types is called the Separating PBE, and  types that send messages that are also sent by other types are said to pooling PBE.

**Definition:(Intuitive Criterion)**

1. Fix an equilibrium of the signaling game
2. Fix an off path signal $m\in M$
3. For all types of sender, check if type $\theta$ loses from sending $m$, by comparing to the on path payoff for each possible undominated strategy that the receiver plays.
4. If yes, then $\theta \in J(m)$, the sure loser set of m
5. The belief for type $\theta $ has to be zero.
6. If every type is a sure loser or nobody is a sure loser, then the Intuitive Criterion is mute.



## Adverse Selection

### Adverse Selection

**Definition: (Insurance Model)** All agents, $i = 1, . . . , m,$ have the same VNM preferences with Bernoulli utility function $u(.)$ that is continuous, strictly increasing and strictly concave. There are two states of the world: one where an agent has wealth $w_g = w$ (the “good state”) and one where the agent suffer a loss L and so has wealth $w_b = w − L$. (Think of $L$ as the loss you incur if you have an accident, and of $\pi$ as your probability of having an accident. Agents differ in their probability πi of having the bad state (this is the only thing that differs across agents). Firms supplying insurance are risk-neutral profit maximisers, and there are no costs associated with providing insurance.

#### Full-Information Benchmark

**Assumption: (Full-Information Benchmark)** Suppose that the firms can somehow observe each agent’s probability $\pi_i$.

**Solution: (Full-Information Benchmark)**

Firms demand from agent i a premium $p_i$ in return for a payout $B_i$ in the event that the bad state occurs. In a competitive equilibrium, firms maximize:
$$
max\space  \pi_i u(w − L − p_i + B_i) + (1 − \pi_i) u(w − p_i) \\
s.t. \space p_i − \pi_iB_i \geq 0
$$
The solution to this problem is $B_i = L$ and $p_i = \pi_iL$.

**Note:** The risk-neutral firm carries all the risk — this is what you’d expect in bargaining between a risk-neutral an a risk-averse agent. No market failure.

#### Asymmetric Information

**Assumption: (Asymmetric Information)** Suppose the firms cannot observe an agent’s $\pi_i$. But suppose the firms know the distribution of the agents: $[\underline \pi, \overline \pi ]$.

**Solution: (Asymmetric Information)**

We would still have $B_i = L$. Type-$\pi$ agent will buy a full insurance policy at price $p$ if $u(w − p) ≥ \pi u(w − L) + (1 − \pi) u(w)$. So define $h(p) = \frac{u(w)-u(w-p)}{u(w)-u(w-L)}$. He will buy the insurance only if $\pi>h(p)$. The equilibrium price is $p^\star  = E[\pi|\pi\geq h(p^\star )]L$. Define $g(p)  = E[\pi|\pi\geq h(p )]L$.

Claim the equilibrium contract always exists.

$g(p)$ is an increasing function from $[\underline \pi L, \overline \pi L]$ to $[\underline \pi L, \overline \pi L]$. Moreover, $g(\underline\pi L) = E[\pi] × L$ (if $p = \underline \pi L$ all agents buy insurance since all were willing to buy at the actuarially fair price) and $g(\bar \pi L) \leq \bar \pi L$ (if $p = \bar \pi L$ at least the most risky type purchases insurance) Thus, $g$ has a fixed point.

**Note:** There might be market failure. 



### Signaling Game

#### Setup

**Assumption:(Setup)**

- Two types of consumers, with the probability of having a loss of L with probability of $\pi_L$ and $\pi_H$, with $\pi_L<\pi_H$
- Utility of the workers are $U_i(B,p) = \pi_iU(W-L-p+B)+ (1-\pi_i)U(W-p)$ for $i = L,H$
- Risk neutral Firm cannot observe the type of the consumer, with profit $\Pi = p - \pi_i B$
- The workers know their type, and make an offer $(B,p)$, and the firm decide to accept or not

**Assumption: (Single Cross Property)** The indifference curve of the consumers only cross once.

**Claim: (Benchmark)** Note that if the firm knows about the type of the customer, he will accept the offer from certain type if $p - \pi_i B\geq 0$ for $i = L,H$. Now assume the firm cannot observe the type, he will still accept all the offer if $p - \pi_H B\geq 0$.

**Claim: (Outside option)** The outside option of the two type customer is:

- For the high type: $B_H^{FI} = L, p_H^{FI} = \pi_H L$
- For the high type: $B_L = \tilde B_L, p_L = \pi_H \tilde B_L$, which solves: $max U_L(B,L)\space s.t.\space p - \pi_H B\geq 0$

#### Separating Equilibrium

**Claim: (Separating Equilibrium)** The Separating PBE of the model is:

- High type always choose $B_H = L, p_H = \pi_H L$

- Low type choose $(B_L,p_L)$ such that
  $$
  U_L(B_L,p_L) \geq U_L(\tilde B_L,\tilde p_L)  \space (IR_L)\\
  U_L(B_L,p_L) \geq U_L(B_H,p_H)  \space (IC_L)\\
  p_L - \pi_L B_L\geq 0 \space (Firm)
  $$

- Firm accept both offers and will reject any other offer, with the belief system: $\beta(i = H|(B_H,p_H)) =1$ and $\beta(i = H|(B_L,p_L)) =0$ on path, and  $\beta(i = H|(B,p)) =1$ off path. 

**Theorem: (Pareto Undominated PBE)** Among all the separating PBE, the PBE with $U_L(B_L,p_L) = U_L(B_H,p_H)  \space (IC_L)$ is the Pareto undominated PBE.

Proof: 

Consider a separating PBE with $U_L(B_L,p_L) > U_L(B_H,p_H)$, the firm and the high risk type’s payoff is not changed if move along the line $p_L - \pi_L B_L=\Pi_L$ but the utility of the low type is increasing. $\square$ 

**Definition: (Riley outcome)** The Riley outcome is defined as the best outcome in the Separating Equilibrium.

#### Pooling Equilibrium

**Claim: (Pooling Equilibrium)** The Separating PBE of the model is:

- Denote $\hat \pi = \alpha \pi_L+(1-\alpha) \pi_H$, then the two types will both choose $(B^\star,p^\star)$ such that
  $$
  U_H(B^\star,p^\star) \geq U_H(B_H^{FI},p_H^{FI})  \space (IR_H)\\
  U_L(B^\star,p^\star) \geq U_L(\tilde B_L,\tilde p_L)  \space (IR_L)\\
  p^\star - \hat \pi B^\star\geq 0 \space (Firm)
  $$

- Firm accept both offers and will reject any other offer, with the belief system:$\beta(i = H|(B_H,p_H)) =1$ and $\beta(i = H|(B_L,p_L)) =0$ on path, and  $\beta(i = H|(B,p)) =1$ off path. 

**Note:** To make sure the pooling equilibrium exist, we need $\hat \pi$ to be not too big.

**Note:** If the portion of the low type is large enough, then there are some pooling equilibrium that is strictly better than the best separating PBE. 

#### Intuitive Criterion

**Theorem: (Pooling PBE)** All the Pooling PBE do not satisfy intuitive criterion.

Proof:

Consider the off path signal $(B,p)$ such that $p-\pi_L B>0$, $U_L(B,p)>U_L(B^\star,p^\star)$ and $U_H(B^\star,p^\star)>U_H(B,p)$. This is a deviation that will not be profitable for the high risk type no matter whether the firm accept or not. So the high type is a sure loser, but the low type is not. So the belief system off path does not satisfies the intuitive criterion. $\square$ 

**Theorem: (Separating PBE)** Only the Riley outcome satisfy intuitive criterion.

Proof:

Consider the off path signal $(B_L,p_L)$ such that $p_L-\pi_L B_L>0$, $U_L(B_L,p_L)>U_L(B_L^\star,p_L^\star)$ and $U_L(B_H^\star,p_H^\star) \geq U_L(B_L,p_L)$. This is a deviation that will not be profitable for the high risk type no matter whether the firm accept or not. So the high type is a sure loser, but the low type is not. So the belief system off path does not satisfies the intuitive criterion. $\square$ 



### Screening

**Assumption:(Setup)**

- Two types of consumers, with the probability of having a loss of L with probability of $\pi_L$ and $\pi_H$, with $\pi_L<\pi_H$
- Utility of the workers are $U_i(B,p) = \pi_iU(W-L-p+B)+ (1-\pi_i)U(W-p)$ for $i = L,H$
- There are 2 firms in the market
- Risk neutral Firm cannot observe the type of the consumer, with profit $\Pi = p - \pi_i B$, so he post a menu of the offer to let the consumers to choose from

**Theorem: (Breakeven)** In Equilibrium the firm is breakeven.

Proof:

Assume that the firm do not offer at breakeven, i.e. they have positive profits. Consider 2 cases:

1. When there are choosing a separating equilibrium:

   Suppose the profit that the two firm can get in total to be $\Pi = \alpha(p_L^\star -\pi_LB^\star _L) + (1-\alpha) (p^\star_H - \pi_H B^\star_H)$. Without loss of generality, suppose the first firm’s profit is $\Pi_A$ and the second $\Pi_B $ and $\Pi_A\geq \frac{1}{2}\Pi\geq \Pi_B$. Then suppose firm B instead of using $(p_L^\star, B_L^\star, p_H^\star, B_H^\star)$, chooses to offer another bundle $(p_L^\star, B_L^\star+\epsilon_L ,p_H^\star, B_H^\star+\epsilon_H)$ such that the incentive constraint is still satisfied. Then since the profit is strictly positive, the new profit is still positive, and when $\epsilon$ is close to 0, the new profit is close to the old profit. Hence firm B can get the profit that is close to the entire market. So the firm can undercut each other such that the profit is zero.

2. When there are choosing a pooling equilibrium:

   Suppose the profit that the two firm can get in total to be $\Pi = p^\star -\pi B^\star$. Without loss of generality, suppose the first firm’s profit is $\Pi_A$ and the second $\Pi_B $ and $\Pi_A\geq \frac{1}{2}\Pi\geq \Pi_B$. Then suppose firm B instead of using $(p^\star, B^\star)$, chooses to offer another bundle $(p^\star, B^\star+\epsilon)$. Then since the profit is strictly positive, the new profit is still positive, and when $\epsilon$ is close to 0, the new profit is close to the old profit. Hence firm B can get the profit that is close to the entire market. So the firm can undercut each other such that the profit is zero. $\square$ 

**Theorem: (No pooling Equilibrium)** There is no pooling equilibrium in the screening model.

Proof:

Suppose in equilibrium the firms chooses $(p^\star, B^\star)$. Then one of the firm can offer $(p,B)$ such that $U_L(p,B)>U_L(p^\star,B^\star)$ and $U_H(p,B)\leq U_H(p^\star,B^\star)$. Then this firm can attract only the low type consumer, and gain positive profit. Hence it’s impossible to get a pooling equilibrium in the screening model. $\square$

**Theorem: (Unique PBE)** There is only one PBE in the screening setup and it will give the payoff of the Riley outcome.

Proof:

It’s trivial to show that for a high type the firms have to offer the bundle in full information. For the low type, If another bundle other than the Riley outcome is offered, one of the firm can always offer a new bundle $(p_L,B_L)$ such that $U_L(p_L,B_L)>U_L(p_L^\star,B_L^\star)$ and $U_H(p_L,B_L)\leq U_H(p_L^\star,B_L^\star)$. Then this firm can attract only the low type consumer, and gain positive profit. Hence the Riley outcome is the only PBE in the screening model. $\square$



### Principal Agent Model

#### Two-Type Model

**Assumption: (Setup)**

- One principal, the firm and one agent, the worker
- Worker has 2 types, H or L, denoted as $\theta \in \{\bar \theta,\underline \theta \}$, which is a private information for the worker, with probability of being a low type $v$
- The firm offers the worker a menu of contract $(W,q)$, and get the payoff $U(W,q,\theta) = S(q)-W$
- The worker choose one contract and produce according to the contract
- Type $\theta$ has a payoff function $U_\theta(W,q) = W-\theta q$
- Agent’s outside option is to not work, with payoff 0

**Claim:(Full Information Benchmark)** When the firm can observe the agent’s type, the firm will choose according to
$$
max \space S(q)-\theta q
$$
and the optimal bundle is $W =\theta q$ and $S(q) = \theta$.

**Solution: (Asymmetric Information)**

The firm’s problem is
$$
max \space v(S(\underline q) - \underline W) +(1-v)(S(\bar q) - \bar W) \\
s.t. \space \bar W - \bar \theta \bar q \geq 0 \space (IR_H) \\
\underline W - \underline\theta \underline q \geq 0 \space (IR_L) \\
\bar W - \bar \theta \bar q \geq \underline W - \bar\theta \underline q  \space (IC_H) \\
\underline W - \underline\theta \underline q \geq \bar W - \underline \theta \bar q \space (IC_L)
$$

1. Monotonicity: from $(IC_H)$ and $(IC_L)$ we can conclude that $(\bar \theta - \underline\theta)(\bar q- \underline q )\leq 0$.
2. $(IR_L)$ is slack. Notice that from $(IR_H)$ and $(IC_L)$ we have $\underline W - \underline\theta \underline q \geq \bar W - \underline \theta \bar q \geq (\bar\theta - \underline \theta )\bar q\geq 0$.
3. $(IR_H)$ and $(IC_L)$ binds. Since we need to maximize the objective function, which is a decreasing function of the wage, we need the $W$ variables to be as small as possible.

So the problem now become 
$$
max \space v(S(\underline q) - \underline W) +(1-v)(S(\bar q) - \bar W) \\
s.t. \space \bar W - \bar \theta \bar q = 0 \\
\underline W - \underline\theta \underline q = \bar W - \underline \theta \bar q
$$
which will give us that $S(\bar q) = \bar \theta +\frac{v}{1-v}(\bar \theta-\underline \theta)$ and $S(\underline  q) = \underline \theta$.

#### Continuum-Type Model

**Assumption: (Setup)**

- One principal, the firm and one agent, the worker
- Worker has type $\theta \in [\underline \theta, \bar \theta]$, with the PDF $f(\theta)$ and CDF $F(\theta)$
- The firm offers the worker a menu of contract $(W,q)$, and get the payoff $U(W,q,\theta) = S(q)-W$
- The worker choose one contract and produce according to the contract
- Type $\theta$ has a payoff function $U_\theta(W,q) = W-\theta q$
- Agent’s outside option is to not work, with payoff 0

**Solution: (Asymmetric Information)**

The firm’s problem is
$$
max \space \int _{\underline \theta}^{\bar \theta} [S(q(\theta))-W(\theta)]f(\theta)d\theta \\
s.t. \space  W(\theta) - \theta q(\theta) \geq 0 \space (IR) \\
W(\theta) - \theta q(\theta) \geq W(\tilde\theta) - \theta q(\tilde\theta)  \space (IC)
$$

1. Monotonicity: from $(IC_H)$ and $(IC_L)$ we can conclude that $ (\theta - \tilde\theta)( q(\theta)-q(\tilde \theta) )\leq 0$ i.e. we have $q'(\theta)\leq0$

2. Local IC constraint: we have $\theta  = argmax_x \{W(x) - \theta q(x)\}$. So the first order condition gives us: $W'(\theta) = \theta q'(\theta)$. Note that from monotonicity the second order condition is always satisfied: the second order derivative of the problem is $W''(\theta) - \theta q''(\theta)$, but from FOC we have $W'(\theta) = \theta q'(\theta)$, hence $W''(\theta) = q'(\theta)+\theta q''(\theta) < 0$ if $q'(\theta)<0$.

3. Integral the Local IC constraint: we have
   $$
   \int_{\tilde \theta}^\theta W'(x) - xq'(x) dx = 0 \\
   W(x)|_{\tilde \theta}^\theta =xq(x)|_{\tilde \theta}^\theta - \int_{\tilde \theta}^\theta q(x)dx \\
   W(x)-xq(x)|_{\tilde \theta}^\theta = -\int_{\tilde \theta}^\theta q(x)dx \\
   U(\theta) - U({\tilde \theta}) = -\int_{\tilde \theta}^\theta q(x)dx
   $$
   where $U(\theta) = W(\theta) - \theta q(\theta)$.

4. Global IC constraint: From the Local IC constraint and the Monotonicity we will have the global IC constraint. For $\tilde\theta>\theta$, $U(\theta) - U({\tilde \theta}) = -\int_{\tilde \theta}^\theta q(x)dx >0$ and for $\tilde\theta<\theta$, $U(\theta) - U({\tilde \theta}) = \int_{\tilde \theta}^\theta q(x)dx > 0$, hence $W(\theta) - \theta q(\theta) \geq W(\tilde\theta) - \theta q(\tilde\theta)$ for all $\tilde \theta$

Hence the firm’s problem can be rewritten as
$$
max \space \int _{\underline \theta}^{\bar \theta} [S(q(\theta))-W(\theta)]f(\theta)d\theta \\
s.t. \space  W(\theta) - \theta q(\theta) \geq 0 \space (IR) \\
W'(\theta) = \theta q'(\theta)  \space (IC) \\
q'(\theta)\leq 0 \space (Monotonicity)
$$
For now we ignore the monotonicity condition and solve the local IC constraint first. Notice from IR constraint, we have $W(\bar \theta) = \bar \theta q(\bar\theta) $, then for all the other $\bar \theta$ the IR constraint is satisfied. Plug in the IC and IR constraint back to the objective function, we have
$$
\int _{\underline \theta}^{\bar \theta} [S(q(\theta)) + \int_{\bar \theta}^\theta q(x)dx - \theta q(\theta)]f(\theta)d\theta\\
= \int _{\underline \theta}^{\bar \theta} [S(q(\theta))- \theta q(\theta)]f(\theta)d\theta + \int _{\underline \theta}^{\bar \theta} \int_{\bar \theta}^\theta q(x) f(\theta)dxd\theta \\
= \int _{\underline \theta}^{\bar \theta} [S(q(\theta))- \theta q(\theta)]f(\theta)d\theta +
\int _{\underline \theta}^{\bar \theta} \int_{x}^{\underline \theta} q(x) f(\theta)d\theta dx\\ 
=\int _{\underline \theta}^{\bar \theta} [S(q(\theta))- \theta q(\theta)]f(\theta)d\theta +
\int _{\underline \theta}^{\bar \theta} q(x) \int_{x}^{\underline \theta} f(\theta)d\theta dx\\
=\int _{\underline \theta}^{\bar \theta} [S(q(\theta))- \theta q(\theta)]f(\theta)d\theta -
\int _{\underline \theta}^{\bar \theta} q(x) F(x) dx\\
= \int _{\underline \theta}^{\bar \theta} [S(q(\theta))- \theta q(\theta)]f(\theta)d\theta -
\int _{\underline \theta}^{\bar \theta} q(\theta) \frac{F(\theta)}{f(\theta)} f(\theta) d\theta \\
=\int _{\underline \theta}^{\bar \theta} [S(q(\theta))- (\theta +\frac{F(\theta)}{f(\theta)})q(\theta)]f(\theta)d\theta
$$
This function holds for all $\theta$, so take FOC with respect to q, we have $S'(q(\theta)) = \theta +\frac{F(\theta)}{f(\theta)}$. Since $S(.)$ is a strictly concave function, as long as the hazard function of $\theta$ is decreasing in $\theta$, the monotonicity is satisfied.

**Definition: (Virtual Type)** Define the Virtual Type as $\theta +\frac{F(\theta)}{f(\theta)}$.

## Moral Hazard

### Moral Hazard

**Assumption: (Setup)**

- One Agent and one principal
- Principal is risk-neutral and would like agent to exert effort, and the agent is risk-averse, and dislikes effort
- Agent choose $e\in\{0,1\}$
- an  accident  results  in  losses  of $l\in L = \{0,1,...,L\}$, and realized losses  are observable by the principal
- The conditional probability: $\pi_l(e) >0$

**Assumption: (Monotone Likelihood Ratio Property)** Higher effort is more likely to result in lower losses in the following strong sense:

the likelihood ratio $\pi_l(0)/\pi_l(1)$ is strictly increasing.

**Theorem: (FOSD)** The realization of the loss under $e = 0$ stochastically dominates $e = 1$.

Proof:

Suppose $\pi_x(0)/\pi_x(1) < \pi_y(0)/\pi_y(1)$ if $x < y$. Taking aggregation over $x$ for all $x<y$ we have:
$$
\sum_{x =0}^{y}\pi_x(0) \pi_y(1) < \sum_{x =0}^{y} \pi_y(0) \pi_x(1) \\
\frac{P(l\leq y|0)}{P(l\leq y|1)}=\frac{\sum_{x =0}^{y}\pi_x(0)} {\sum_{x =0}^{y}  \pi_x(1)} < \frac{\pi_y(0)}{\pi_y(1)}
$$
Similarly taking aggregation over $y$ for all $x<y$ we have:
$$
\sum_{y =x}^{L}\pi_x(0) \pi_y(1) < \sum_{y =x}^{L} \pi_y(0) \pi_x(1) \\
\frac{\pi_x(0)}{\pi_x(1)}<\frac{\sum_{y = x}^{L}\pi_x(0)} {\sum_{y=x}^{L}  \pi_x(1)} = \frac{1-P(l\leq x|0)}{1-P(l\leq x|1)}
$$
Note that the about two inequalities holds for al $x$ and all $y$, so we have 
$$
\frac{P(l\leq z|0)}{P(l\leq z|1)} < \frac{1-P(l\leq z|0)}{1-P(l\leq z|1)} \\
P(l\leq z|0)<P(l\leq z|1)
$$
i.e. the realization of the loss under $e = 0$ stochastically dominates $e = 1$. $\square$

**Definition: (Full Information)** Suppose the principal could observe the effort of the agent. The principal solves the following problem:
$$
max_{\{p, B_l, e\}}\space p- \sum_{l=0}^L \pi_l(e)B_l \\
s.t. \sum_{l = 0}^L\pi_l(e)u(w-p-l+B_l) - d(e) \geq \bar u = \sum_{l = 0}^L\pi_l(e)u(w-l) - d(e)
$$
**Solution: (Full Information)**

First, fix $e$ and solve the problem for any e. Consider the Lagrangian problem, we have first order conditions:
$$
1- \lambda [\sum_{l = 0}^L\pi_l(e)u'(w-p-l+B_l)] = 0 \\
-\pi_l(e) + \lambda [\pi_l(e)u'(w-p-l+B_l)] = 0 \\
\sum_{l = 0}^L\pi_l(e)u(w-p-l+B_l) - d(e) \geq  \bar u
$$
Notice that combining all the equations in the second part we have the first FOC. So the first one is redundant. Plus, the constraint must bind, due to an argument of contradiction. Hence we have
$$
u'(w-p-l+B_l) = \frac{1}{\lambda}
$$
This is called the Borch optimal risk-sharing condition for the case where the principal is risk-neutral. It implies that $B_l-l$ must be constant, i.e. the agent is fully insured. Normalize $B_0 = 0$ we have $B_l = l$.

Now the principal’s problem become:
$$
max_{e\in\{0,1\}}\space p^{FI}(e)-\sum_{l=0}^L \pi_l(e)B_l(e)
$$
**Definition: (Moral Hazard)** Under asymmetric information, the principal cannot observe the effort chosen by the agent, so the principal’s problem now include the IC constraint:
$$
max_{\{p, B_l, e\}}\space p- \sum_{l=0}^L \pi_l(e)B_l \\
s.t. \sum_{l = 0}^L\pi_l(e)u(w-p-l+B_l) - d(e) \geq \bar u = \sum_{l = 0}^L\pi_l(e)u(w-l) - d(e) \\
\sum_{l=0}^L\pi_l(e) u(w−p−l+B_l) − d(e) ≥ \sum_{l=0}^L \pi_l(e') u(w−p−l+B_l)− d(e')
$$
**Solution: (Moral Hazard)**

First, fix $e$ and solve the problem for any $e$. 

1. Suppose the optimal $e = 0$, the firm can achieve the full information contract. To see this assume the principal offers the full information contract. By assumption we have $d(0)\leq d(1)$. Notice that by Monotone Likelihood Ratio Property we have $\sum_{l = 0}^L\pi_l(0)u(w-p^{FI}(0)-l+B_l^{FI}(0)) \geq \sum_{l = 0}^L\pi_l(1)u(w-p^{FI}(0)-l+B_l^{FI}(0)) $.

2. Suppose the optimal $e = 1$. We have the following first order conditions:

   
   $$
   1- \lambda [\sum_{l = 0}^L\pi_l(1)u'(w-p-l+B_l)] - \mu[\sum_{l = 0}^L(\pi_l(1) - \pi_l(0))u'(w-p-l+B_l)] = 0 \\-\pi_l(1) + \lambda [\pi_l(1)u'(w-p-l+B_l)] - \mu[(\pi_l(1) - \pi_l(0))u'(w-p-l+B_l)]  = 0 \\\sum_{l = 0}^L\pi_l(1)u(w-p-l+B_l) - d(1) \geq  \bar u \\\sum_{l=0}^L\pi_l(1) u(w−p−l+B_l) − d(1) ≥ \sum_{l=0}^L \pi_l(0) u(w−p−l+B_l)− d(0)
   $$
   Similarly, first we notice that from the second FOC we can get the first FOC. So the first one is slack. Rearrange the second FOC we have:
   $$
   \frac{1}{u'(w-p-l+B_l)} = \lambda +(1 - \frac{\pi_l(0)}{\pi_l(1)})\mu
   $$
   We can argue that $\lambda\neq 0$ and $\mu\neq 0$. Suppose $\lambda =0$, i.e. the IR constraint do not bind, then we can lower the payout to the agent such that the IC constraint still holds and it will give the principal a higher payoff. 

   Now suppose $\mu = 0$, Then the FOC will give the full information contract. But we just argued that with full information contract, the IC works for $e = 0$, not $e = 1$, so it’s a contradiction.

   Now we argue that $\lambda > 0$ and $\mu > 0$. 

   By $\pi_l(0)/\pi_l(1)$ to be increasing, there exists a state $l$ such that $\pi_l(0)/\pi_l(1)>1$, and hence $(1 - \frac{\pi_l(0)}{\pi_l(1)})\mu<0$. Note that $u'(.)$ is always positive, this means $\lambda>0$.

3. The optimal effort level the principal induces would have $\pi_0^{FI} = \pi_0^{MH}$ and $\pi_1^{FI} \geq \pi_1^{MH}$.



### Continuous Effort Levels Model

**Assumption: (Setup)**

- One Agent and one principal
- The employee’s output, $q$, can take two values: $q \in \{0, 1\}$
- The probability that $p(a) = P(q  =1| a)$ is strictly increasing and concave in $a$
- Principal is risk-neutral and would like agent to exert effort, and the agent is risk-averse, and dislikes effort, with utility function $v(q-w)$, with $v'(.)>0$ and $v''(.)<0$
- Agent choose $a\in[0,1]$, with utility function $u(w)$, with $u'(.)>0$ and $u''(.)<0$, and the cost of exerting $a$ is $c(a) = a$

**Claim: (Monotone Likelihood Ratio Property and FOSD)** Under the assumption that $p(a)$ is strictly increasing and concave, we have that the probability satisfy the Monotone Likelihood Ratio Property and FOSD.

**Definition: (Full Information)** Suppose the principal could observe the effort of the agent. The principal solves the following problem:
$$
max_{\{a, w_0,w_1\}}\space p(a)v(1-w_1)+ (1-p(a))v(-w_0) \\
s.t. p(a)u(w_1)+(1-p(a))u(w_0)-a\geq \bar u
$$
**Solution: (Full Information)**

Consider the Lagrangian problem, we have first order conditions:
$$
p'(a)(v(1-w_1)-v(-w_0) + \lambda(u(w_1)-u(w_0))) -\lambda = 0\\
- p(a)v'(1-w_1) + p(a)\lambda u'(w_1) = 0\\
- (1-p(a))v'(-w_0) + (1-p(a))\lambda u'(w_0) = 0\\
p(a)u(w_1)+(1-p(a))u(w_0)-a = \bar u
$$
Combine the first order conditions we have $\frac{v'(1-w_1)}{u'(w_1)} = \frac{v'(-w_0)}{u'(w_0)} = \lambda$. Combine the FOCs we can get the optimal solution to the problem.

**Definition: (Moral Hazard)** Under asymmetric information, the principal cannot observe the effort chosen by the agent, so the principal’s problem now include the IC constraint: 
$$
max_{\{a, w_0,w_1\}}\space p(a)v(1-w_1)+ (1-p(a))v(-w_0) \\
s.t. p(a)u(w_1)+(1-p(a))u(w_0)-a\geq \bar u \\
a\in argmax_{\hat a} \space p(\hat a)u(w_1)+(1-p(\hat a))u(w_0)-\hat a
$$
**Solution: (First Order Approach)**

The first order condition and the second order condition for the IC constraint gives us
$$
p'(a)(u(w_1)-u(w_0))-1 = 0 \\
p''(a)(u(w_1)-u(w_0))<0
$$
Put this into the constraint of the Lagrange function and we will get
$$
\frac{v'(-w_0)}{u'(w_0)} = \lambda -\mu \frac{p'(a)}{1-p(a)} \\
\frac{v'(1-w_1)}{u'(w_1)} = \lambda +\mu \frac{p'(a)}{p(a)} \\
p'(a)(v(1-w_1) - v(-w_0))+\lambda [p'(a)(u(w_1)-u(w_0))-1] + \mu p''(a) (u(w_1)- u(w_0)) = 0
$$
along with the IR and IC constraint. Notice that in the last FOC we have $p'(a)(u(w_1)-u(w_0))-1 = 0$ by IC constraint.

We could argue that $\mu>0$. Suppose not, then we have $w_0<w_0^{FI}< 1-w_1^{FI}< 1-w_1$. Now consider the last FOC with respect to $a$. We have $p'(a)(v(1-w_1) - v(-w_0)) + \mu p''(a) (u(w_1)- u(w_0)) = 0$ By assumption $p'(a)>0$ and $p''(a)<0$ so we have $\mu>0$. Contradiction. $\square$  



## Mechanism Design

### Auction

#### Second Price Auction

**Assumption: (Second Price Auction Setup)**

- $N$ players in total
- $v_i$ denotes player’s valuation
- $b_i$ is the bid of player $i$
- Denote $B_{-i} = max_{j\neq i}b_j$ and $N_{-i} = |\{k\neq i: b_k = b_{-i}\}|$
- Player $i$’s payoff is $u_i(b_i,b_{-i})= 0$ if $b_i<B_{-i}$, $u_i(b_i,b_{-i})= (v_i-B_{-i})/(N{-i}+1)$ if $b_i=B_{-i}$, and $u_i(b_i,b_{-i})= v_i-B_{-i}$ if if $b_i>B_{-i}$

**Definition: (Second Price Auction)** The Second Price Auction is defined as the following mechanism:

- The highest bidder wins the auction
- The winner pays the second highest bid

**Theorem: (Second Price Auction)** In a Second Price Auction, the strategy $b_i = v_i$ weakly dominates all other strategies.

Proof:

1. If we set the strategy to be $b_i = v_i$, then player $i$’s payoff is $u_i(v_i,b_{-i})= 0$ if $v_i<B_{-i}$, $u_i(v_i,b_{-i})= (v_i-B_{-i})/(N{-i}+1)$ if $v_i=B_{-i}$, and $u_i(v_i,b_{-i})= v_i-B_{-i}$ if if $v_i>B_{-i}$.

   If we set the strategy to be $b_i < v_i$, then player $i$’s payoff is $u_i(b_i,b_{-i})= 0$ if $b_i<B_{-i}$, $u_i(b_i,b_{-i})= (v_i-B_{-i})/(N{-i}+1)$ if $b_i=B_{-i}$, and $u_i(b_i,b_{-i})= v_i-B_{-i}$ if if $b_i>B_{-i}$.

   If we set the strategy to be $b_i > v_i$, then player $i$’s payoff is $u_i(b_i,b_{-i})= 0$ if $b_i<B_{-i}$, $u_i(b_i,b_{-i})= (v_i-B_{-i})/(N{-i}+1)$ if $b_i=B_{-i}$, and $u_i(b_i,b_{-i})= v_i-B_{-i}$ if if $b_i>B_{-i}$.

2. If $b_i< v_i< B_{-i}$, then $u_i(v_i,b_{-i})= 0 = u_i(b_i,b_{-i})$. 

   If $b_i< B_{-i} = v_i$, then $u_i(v_i,b_{-i})= (v_i-B_{-i})/(N{-i}+1)>0 = u_i(b_i,b_{-i})$.

   If $b_i< B_{-i} < v_i$, then $u_i(v_i,b_{-i})= v_i-B_{-i}>0 = u_i(b_i,b_{-i})$.

   If $b_i = B_{-i} < v_i$, then $u_i(v_i,b_{-i})= v_i-B_{-i}> (v_i-B_{-i})/(N{-i}+1)= u_i(b_i,b_{-i})$.

   If $B_{-i} < b_i< v_i$, then $u_i(v_i,b_{-i})= v_i-B_{-i}=v_i-B_{-i}= u_i(b_i,b_{-i})$.

   So $u_i(b_i,b_{-i})\leq u_i(v_i,b_{-i})$ is always true when $b_i< v_i$.

3. If $v_i< b_i< B_{-i}$, then $u_i(b_i,b_{-i})= 0 = u_i(v_i,b_{-i})$. 

   If $v_i< B_{-i} = b_i$, then $u_i(b_i,b_{-i})= (v_i-B_{-i})/(N{-i}+1)<0 = u_i(v_i,b_{-i})$.

   If $v_i< B_{-i} < b_i$, then $u_i(b_i,b_{-i})= v_i-B_{-i}<0 = u_i(v_i,b_{-i})$.

   If $v_i = B_{-i} < b_i$, then $u_i(b_i,b_{-i})= v_i-B_{-i}< (v_i-B_{-i})/(N{-i}+1)= u_i(v_i,b_{-i})$.

   If $B_{-i} < v_i< b_i$, then $u_i(b_i,b_{-i})= v_i-B_{-i}=v_i-B_{-i}= u_i(v_i,b_{-i})$.

   So $u_i(b_i,b_{-i})\leq u_i(v_i,b_{-i})$ is always true when $b_i > v_i$. So the strategy $b_i = v_i$ weakly dominates all other strategies. $\square$


**Theorem: (BNE in SPA)** $b_i = v_i$ is the unique BNE in weakly dominated strategies.

Proof:

By the lemma above we know that when the other player is playing according to $b_i = v_i$, it is a Nash equilibrium. By costruction it is the only BNE in weakly dominated strategies. $\square$ 

#### First Price Auction

**Assumption: (Second Price Auction Setup)**

- $n$ players in total
- $v_i$ denotes player’s valuation, each follows the same CDF $F(.)$ over $[0,1]$
- $b_i$ is the bid of player $i$,  $b_i(v) = b(v)$, it is differentiable and $b'(v)>0$

**Definition: (First Price Auction)** The First Price Auction is defined as the following mechanism:

- The highest bidder wins the auction
- The winner pays the highest bid

**Theorem: (BNE in FPA)** If all other player adhere to the BNE, then $b(v_i)$ is the best response for type $v_i$ for player $i$.

Proof:

The expected payoff to $v_i$ is $U_i(r,v_i) = P(b(r)>max_{j\neq i} b(v_j)) (v_i-b(r))$. This statement requires that the expected payoff satisfies:
$$
v_i = argmax_{r} U_i(r,v_i) = argmax_{r} U_i(r,v_i) \\
v_i = argmax_{r} P(b(r)>max_{j\neq i} b(v_j)) (v_i-b(r)) \\
v_i = argmax_{r} P(b(r)> b(max_{j\neq i}v_j)) (v_i-b(r)) \\
v_i = argmax_{r} P(r> max_{j\neq i}v_j) (v_i-b(r)) \\
v_i = argmax_{r} F(r)^{n-1} (v_i-b(r))
$$
Denote $G(r) = F(r)^{n-1}$ as the probability of the CDF of $max_{j\neq i}v_j$. The first order condition shows that $g(x)x = \frac{d}{dx}(G(x)b(x))$. Take the integral over both sides, we have $\int_0^{v_i} g(x)x dx = G(v_i)v_i- G(0)b(0)$. Notice that $b(0) = 0$. This indicates that
$$
b(v_i) = E[max_{j\neq i}v_j|max_{j\neq i}v_j<v_i]
$$
Notice that by FOC we have $\frac{\partial U}{\partial r} = (v_i-r)g(r)$. This implies that the SOC is satisfied. $\square$ 

**Claim: (Expected Payoff for Seller)** The expected payoff for the seller is the same. 



### Mechanism Design

**Assumption: (Setup)**

- There is one indivisible object, N potential risk neutral buyers, each has a private value $v_i$ 
- The buyer gets $v_i-p$ if she gets the object and gets $-p$ if not
- $v_i\in \Theta_i$ is a random variable with CDF $F_i$, with joint distribution as common knowledge to everyone

**Definition: (Mechanism)** A Mechanism is defined as $(S_i, P_i,C_i)_{i = 1}^N$ such that:

- $S_i$ denotes the strategies for player i
- $P_i:\times_{j =1}^N S_j \to [0,1]$ denotes bidder i’s probability of wining the object. Notice that $\sum_{i = 1}^N P_i(s)\leq 1$
- $C_i:\times_{j =1}^N S_j \to R$ denote the bidder i’s expected payment cost if $s \in S$ is played

**Definition: (Pure Strategy for Bidder)** A Pure Strategy for Bidder i is defined as $\sigma_i:\Theta_i\to S_i$.

**Definition: (Direct Selling Mechanism)** A Direct Selling Mechanism is if $S_i = \Theta_i $ for all i.

**Definition: (Truthful BNE)** a BNE $\sigma^\star$ in a direct selling mechanism is Truthful  if $\sigma^\star (v_i) = v_i$ for all $v_i\in \Theta_i$.

**Definition: (Equivalent BNE)** For two mechanism $(S_i, P_i,C_i)_{i = 1}^N$ and $(\hat S_i, \hat P_i,\hat C_i)_{i = 1}^N$, the BNE $\sigma^\star$ and $\hat \sigma^\star$ are called equivalent if for all $v\in \times_{i = 1}^N \Theta_i$, we have $P(\sigma^\star (v)) = \hat P(\hat \sigma^\star (v))$ and $C(\sigma^\star (v)) = \hat C(\hat \sigma^\star (v))$.

**Theorem: (Revelation Principle)** For all BNE of any mechanism, there is an equivalent truthful BNE of a direct selling mechanism.

Proof:

Consider $(S_i, P_i,C_i)_{i = 1}^N$ and a BNE $\sigma^\star$ for it. Construct the direct selling mechanism as

- $\hat S_i = \Theta_i$
- $\hat P_i(v) = P(\sigma^\star (v))$
- $\hat C(v) = C(\sigma^\star (v))$

Now we need to verify that there is a truthful BNE. By definition of $\sigma^\star$ being a BNE, we have 
$$
\int_{\Theta_{-i}}P_i(\sigma_i^\star(v_i),\sigma_i^\star(v_{-i}))v_i - C_i(\sigma_i^\star(v_i),\sigma_i^\star(v_{-i})) dv_{-i}\geq \int_{\Theta_{-i}}P_i(\sigma_i^\star(v'_i),\sigma_i^\star(v_{-i}))v_i - C_i(\sigma_i^\star(v'_i),\sigma_i^\star(v_{-i})) dv_{-i} \\

\int_{\Theta_{-i}}\hat P_i(v_i,v_{-i})v_i - \hat C_i(v_i,v_{-i}) dv_{-i}\geq \int_{\Theta_{-i}}\hat P_i(v'_i,v_{-i})v_i - \hat C_i(v'_i,v_{-i}) dv_{-i}
$$
Thus we verified that it is truthful. $\square$ 



### Incentive Compatible Direct Selling Mechanism

#### Incentive Compatible Direct Selling Mechanism

**Definition: (Interim Allocation and Payment)** Fix a mechanism $(P_i ,C_i)_{i=1}^N$, suppose all $j\neq i$ report truthfully, $r\in [0,1]$, then define the Interim Allocation and Payment as $ \bar P_i(r) = \int _{\Theta_{-i}}P_i(r, v_{-i})dv_{-i}$ and $ \bar C_i(r) = \int _{\Theta_{-i}}C_i(r, v_{-i})dv_{-i}$. If all the other players report truthfully, then agent i’s expected payoff from reporting r is $U_i(r,v_i) = \bar P_i(r)v_i-\bar C_i(r)$.

**Definition: (Incentive Compatible Direct Selling Mechanism)** The Incentive Compatible Direct Selling Mechanism is defined as a direct mechanism in which telling the truth is a BNE, i.e. $U_i(v_i,v_i)\geq U_i(r, v_i) $ for all r and $v_i$.

**Theorem: (IC Constraint)** A direct selling mechanism is incentive compatible if and only if:

1. $\bar P_i(r)$ is non decreasing
2. $\bar C_i(r) = C_i(0)+\bar P_i(v_i)v_i - \int _0^{v_i}\bar P_i(x)dx$

Proof:

1. Notice $U_i(v_i,v_i)\geq U_i(\tilde v_i, v_i) $ and $U_i(\tilde v_i,\tilde v_i)\geq U_i( v_i, \tilde v_i) $. Combine them we have $(v_i-\tilde v_i)(\bar P(v_i)-\bar P(\tilde v_i))\geq 0$.
2. The local IC constraint can be written as $v_i = argmax_r U_i(r, v_i)$. By firs order condition we have $\bar P'(v_i)v_i = \bar C_i(v_i)$. Integral over the first order condition, we have $\bar C_i(r)= C_i(0)+\bar P_i(v_i)v_i - \int _0^{v_i}\bar P_i(x)dx$.  Then combine the monotonicity with the first order condition, we have that the second order condition holds. $\square$

#### Revenue Equilvance

**Theorem: (Revenue Equilvance)** Consider 2 selling mechanisms, one BNE for each such that both BNE have the same $\bar C(0)$ and $\bar P_i(v_i)$ for all $v_i\in [0,1]$, then the expected revenue to the BNE of the selling mechanisms are the same.

Proof:

Suppose the two mechanisms are $(P_i, C_i)$ and $(\tilde P_i,\tilde C_i)$. Notice that the ex-ante revenue of the seller is 
$$
R = \int_{\Theta^N}\sum_{i=1}^N C_i(v)f(v)dv \\
 = \sum_{i=1}^N\int_{\Theta} \int_{\Theta^{N-1}} C_i(v)f_{-i}(v_{-i})dv_{-i} f_i(v_i)dv_{i} \\
 =  \sum_{i=1}^N\int_{\Theta} \bar  C_i(v_i) f_i(v_i)dv_{i} \\
$$
If both BNE have the same $\bar C(0)$ and $\bar P_i(v_i)$ for all $v_i\in [0,1]$, then the from the above theorem we have $\bar C_i(r)$ is the same. Hence expected revenue for the seller is the same. $\square$ 

#### Optimal Selling Mechanism Design

**Definition: (Virtual Valuation)** For any type $v_i$, player i’s Virtual Valuation is $\psi_i(v_i) = v_i - \frac{1-F_i(v_i)}{f_i(v_i)}$.

**Assumption: (Virtual Valuation)**

- We assume that $\psi_i'(v_i)>0$, i.e. $\frac{f_i(v_i)}{1-F_i(v_i)}$ is weakly increasing in $v_i$
- IR constraint is satisfied, i.e. $\bar P_i(v_i)v_i-\bar C_i(v_i)\geq 0$

**Theorem: (Mayson Theorem)** An ICDSM maximize seller’s expected revenue if and only if for all i and all $v_i$, we have 

- $\bar C_i(0) = 0$
- $ P_i(v_1,...v_N) = 1$ if $\psi_i(v_i)>\psi_j(v_j)$ and $\psi_i(v_i)>0$, and $P_i(v_1,...v_N) = 0$ otherwise.

Proof:

Note that the expected revenue for the seller for a given mechanism is 
$$
E[R] = \int_{\Theta}  \bar C_i(v_i) f_i(v)dv_{i} \\
= \sum_{i=1}^N \int_0^1  (C_i(0)+\bar P_i(v_i)v_i - \int _0^{v_i}\bar P_i(x)dx )f_i(v_i)dv_{i} \\
= \sum_{i=1}^N \int_0^1  (\bar P_i(v_i)v_i - \int _0^{v_i}\bar P_i(x)dx )f_i(v_i)dv_{i} \\
= \sum_{i=1}^N \int_0^1  \bar P_i(v_i)v_i f_i(v_i) dv_{i}- \int_0^1  \int _0^{v_i}\bar P_i(x) f_i(v_i)dxdv_{i} \\
= \sum_{i=1}^N \int_0^1  \bar P_i(v_i)v_i f_i(v_i) dv_{i}- \int_0^1  \int _x^1\bar P_i(x) f_i(v_i)dv_{i}dx \\
= \sum_{i=1}^N \int_0^1  \bar P_i(v_i)v_i f_i(v_i) dv_{i}- \int_0^1 \bar P_i(x) (1-F_i(x))dx \\
= \sum_{i=1}^N \int_0^1  (\bar P_i(v_i)v_i f_i(v_i) - \bar P_i(v_i) (1-F_i(v_i))dv_i \\
= \sum_{i=1}^N \int_0^1  (\bar P_i(v_i)v_i  - \bar P_i(v_i) (1-F_i(v_i)/f_i(v))f_i(v)dv_i \\
= \sum_{i=1}^N \int_0^1  (\bar P_i(v_i)\psi_i(v_i))f_i(v_i)dv_i \\
= \sum_{i=1}^N \int_0^1 \int_{\Theta^{N-1}} ( P_i(v_i, v_{-i})\psi_i(v_i))f(v)dv \\
$$
Hence we can choose the probability as in the theorem to maximize the expected revenue, we only need to show that such a probability function can induce an ICDSM, i.e. check that $\bar P(.)$ is monotonic. Notice that $\bar P_i(v_i) = 0$ if $\psi_i(v_i)\leq 0$ and $\bar P_i(v_i) = P(\psi_i(v_i)>max_{j \neq i} \psi_j(v_j))$ increases with $v_i$, so obviously the monotonicity is satisfied. $\square$ 

**Definition: (Constant Payment Rule)** After finding the optimal $P(.)$ we can construct the interim truth-telling mechanism $\bar C(.)$. Then the Constant Payment Rule is constructed by letting $C(v_i,v_{-j}) = \bar C_i(v_i)$.

**Definition: (Canonical Payment Rule)** After finding the optimal $P(.)$ we can construct the interim truth-telling mechanism $\bar C(.)$. Then the Constant Payment Rule is constructed by letting $C(v_i,v_{-j}) = P_i(v_i,v_{-i})v_i - \int _0^{v_i}P_i(v_i,v_{-i})dx$.