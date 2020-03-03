# APPROXIMATION ALGORITHM

## Theorem:
Let *U* be a universe set of regions and *S* be a subset of *U*. Function <img src="https://render.githubusercontent.com/render/math?math=f(.)"> which maps $S$ to a non-negative value is said to be submodular if given any <img src="https://render.githubusercontent.com/render/math?math=S\subseteq U">, it holds for any regions <img src="https://render.githubusercontent.com/render/math?math=x_1, x_2 \in U-S">  that  <img src="https://render.githubusercontent.com/render/math?math=f(S \cup \{x_1\}) + f(S \cup \{x_2\}) \geq f (S \cup \{x_1, x_2\}) + f(S)">.

**Begin proof**
---

we say <img src="https://render.githubusercontent.com/render/math?math=\sigma(.)"> is submodular if it satisfies the ``diminishing marginal gain" property.

The class of submodular functions is closed under non-negative linear combinations. Consider any submodular function <img src="https://render.githubusercontent.com/render/math?math= f_1,f_2,...,f_k"> and non-negative numbers <img src="https://render.githubusercontent.com/render/math?math=p_1,p_2,\ldots,p_k">. Then the function *g* defined by <img src="https://render.githubusercontent.com/render/math?math=g(S)=\sum_{i=1}^k p_i f_i(S)"> is submodular. Recall that <img src="https://render.githubusercontent.com/render/math?math=\sigma(.)"> indicates the expectation of the total weight of events influenced by the the selected regions, and the propagation of events is assumed to be independent, so <img src="https://render.githubusercontent.com/render/math?math=\sigma(.)"> can be expressed as

<img src="https://render.githubusercontent.com/render/math?math=\sigma(.) = \sum_{G=g}Pr(G=g)">

where <img src="https://render.githubusercontent.com/render/math?math=\sigma(.)"> is the number of influenced events when *g* occurs and *g* is a possible outcome of the joint distribution of the all the edges. Therefore, it is sufficient to prove that each function <img src="https://render.githubusercontent.com/render/math?math=f_i">, corresponding to each possible outcome, is submodular. For <img src="https://render.githubusercontent.com/render/math?math=f_i">, all the edges are associated with probability either *1* or *0*. We consider the following cases among <img src="https://render.githubusercontent.com/render/math?math=S , x_1"> and <img src="https://render.githubusercontent.com/render/math?math=x_2">: 

- There is a path from <img src="https://render.githubusercontent.com/render/math?math=x_1"> to *S*, a path from $x_2$ to *S*, all the events influenced by <img src="https://render.githubusercontent.com/render/math?math=x_1"> or <img src="https://render.githubusercontent.com/render/math?math=x_2"> are also influenced by *S*, so equality holds.
    
- There is a path from <img src="https://render.githubusercontent.com/render/math?math=x_1"> to *S*, no path from <img src="https://render.githubusercontent.com/render/math?math=x_2"> to *S*, <img src="https://render.githubusercontent.com/render/math?math=\sigma(S\cup x_1)=\sigma(S)">, and <img src="https://render.githubusercontent.com/render/math?math=\sigma(S\cup x_2)=\sigma(S)+\phi(x_2)">, where <img src="https://render.githubusercontent.com/render/math?math=\phi(x_2)"> denotes the total weight of events influenced by <img src="https://render.githubusercontent.com/render/math?math=x_2"> but not *S*. So <img src="https://render.githubusercontent.com/render/math?math=LHS = RHS = 2*\sigma(S)+\phi(x_2)">, so equality holds.
    
- There is no path from either <img src="https://render.githubusercontent.com/render/math?math=x_1"> or <img src="https://render.githubusercontent.com/render/math?math=x_2"> to *S*, then we consider two sub-cases: (1) there is a path from <img src="https://render.githubusercontent.com/render/math?math=x_1"> to <img src="https://render.githubusercontent.com/render/math?math=x_2">, then <img src="https://render.githubusercontent.com/render/math?math=\phi(x_1)=\phi(x_2)">, then <img src="https://render.githubusercontent.com/render/math?math=LHS=2*\sigma(S) + 2\phi(x_1)"> and <img src="https://render.githubusercontent.com/render/math?math=RHS=2*\sigma(S)+\phi(x_1)">. Since <img src="https://render.githubusercontent.com/render/math?math=\phi(x_1)>=0">, <img src="https://render.githubusercontent.com/render/math?math=LHS>=RHS">; (2) there is no path from <img src="https://render.githubusercontent.com/render/math?math=x_1"> to <img src="https://render.githubusercontent.com/render/math?math=x_2">, then <img src="https://render.githubusercontent.com/render/math?math=LHS=RHS=2*\sigma(S) + \phi(x_1)+\phi(x_2)">.
    
    
Therefore, we prove that <img src="https://render.githubusercontent.com/render/math?math=f_i"> is a submodular function for all *i*. Since submodluar functions are closed under non-negative linear combination, we complete the proof.
    
---
**End proof**
