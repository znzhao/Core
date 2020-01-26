# Microeconomics II

## Static Games of Complete Information

### Static Games

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

**Theorem: (Mixed Strategy Nash Equilibrium)** If $\sigma^\star$ is a Nash equilibrium in non-degenerate mixed strategies, i.e. there exist $s_i, s'_i \in S_i$ such that $\sigma^\star _{i}(s_i)>0$ and $\sigma^\star _{i}(s_i)>0$, it must be that $U_i(s_i,\sigma_{-i}^\star) = U_i(s'_i,\sigma_{-i}^\star)$.

Proof:

Suppose the claim is incorrect. With out loss of generality, suppose $U_i(s_i,\sigma_{-i}^\star) > U_i(s'_i,\sigma_{-i}^\star)$, we have
$$
U_i(\sigma_i^\star,\sigma_{-i}^\star) = \sum_{s\neq  s'_i} \sigma_i^\star (s)u_i(s,\sigma_{-i}^\star)+ \sigma_i^\star(s'_i)U_i(s'_i,\sigma_{-i}^\star)< \sum_{s\neq  s'_i} \sigma_i^\star (s)u_i(s,\sigma_{-i}^\star)+ \sigma_i^\star(s'_i)U_i(s_i,\sigma_{-i}^\star) = U_i(\hat \sigma_i,\sigma_{-i}^\star)
$$
where $\hat \sigma_i$ is a profitable deviation of $\sigma_i^\star$, with probability $\hat \sigma_i(s) = \sigma_i^\star(s)$ if $s\neq s_i$ and $s\neq s'_i$, $\hat \sigma_i(s) = \sigma_i^\star(s_i)+\sigma_i^\star(s'_i)$ if $s= s_i$, and  $\hat \sigma_i(s) = 0$ if $s = s'_i$, which is impossible, because  $\sigma^\star$ is a Nash equilibrium and there is no profitable deviation. Contradiction. $\square$ 

#### Rationalizability

**Definition: (Never a Best Response)** $ \sigma_i \in \Sigma_i$ is never a best response if there exists no $ \sigma_{-i} \in \Sigma_{-i}$ for which $ \sigma_i$ is a best response. 

**Theorem: (Never a Best Response and Strictly Dominated Strategies)** if a strategy is strictly dominated then it is never a best response.

Proof:

If $\sigma_i$ is strictly dominated by $\hat\sigma_i$, then the best response of any given $\sigma_{-i}$ would be $\hat\sigma_i$ or some other strategies. So it can never be a best response. $\square$ 

**Note:** The inverse of this statement is not true.

**Definition: (Rationalizability)** Rationalizability is the iterated deletion of strategies that are never a best response.