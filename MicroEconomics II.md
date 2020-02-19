# Microeconomics II

## Static Games of Complete Information

### Normal Form Games

**Definition: (Strategic Form Game)** A Strategic Form Game, G, is defined as a triplet: $G = \{N,S,u\}$. It is consisted of the following:

- A finite set of players: $N = \{1,2,...,n\}$
- A finite set of actions: For each $i\in N$, let $S_i$ denote the set of players $i$'s pure strategies, and call $s_i$ a typical element of $S_i$
- A pure strategy profile $s = (s_1, s_2,..., s_n)$ lists one pure strategy for each player, and the set of pure strategy proles is $S = (\times_{i\in N}S_i)$
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

**Theorem: (Equivalent Strict Dominance)** If the pure strategy $s_i$ is strictly (weakly) dominated then any mixed strategy that plays $ s_i$ with positive probability is also strictly (weakly) dominated.

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



#### Second Price Auction

**Assumption: (Second Price Auction Setup)**

- $N$ players in total
- $v_i$ denotes player’s valuation
- $b_i$ is the bid of player $i$
- Denote $B_{-i} = max_{j\neq i}b_j$ and $N_{-i} = |\{k\neq i: b_k = b_{-i}\}|$
- Player $i$’s payoff is $u_i(b_i,b_{-i})= 0$ if $b_i<B_{-i}$, $u_i(b_i,b_{-i})= (v_i-B_{-i})/(N{-i}+1)$ if $b_i=B_{-i}$, and $u_i(b_i,b_{-i})= v_i-B_{-i}$ if if $b_i>B_{-i}$

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

1. $\Sigma$ is a compact and convex set. Note that $N$ and $S_i$ are finite, Remember \Sigma_i = \Delta(S_i) is the $|S_i|-1$ dimensional simplex, which is compact and convex. Hence $\Sigma = \times_{i\in N}\Sigma_i$ is also compact and convex.
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

**Definition: (Continuity at Infinity)**  Let$ h, h' \in H$ be two infinite-horizon histories. A game is Continuous at Infinity if for every $i\in N$, if
$$
lim_{t\to \infty} sup_{(h,h')|h_t=h_t'}|u_i(h)-u_i(h')|=0
$$
**Note:** If continuity at infinity is satisfied then OSD can still work.



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

4. Combine these two inequalities and use the fact that $M_i\geq m_i$, we have $m_j=M_j$. Thus in every subgame where player i makes the offer, the SPE payoff is unique. Hence the SPE is unique.