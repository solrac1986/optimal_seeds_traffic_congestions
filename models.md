# MODELS AND PROBLEM DEFINITIONS

Begin proof
---

**The J-KEY-Region problem is NP-hard for the *Independent Cascade (IC) model***


To reach the NP-hardness of the J-KEY-Region problem, it is sufficient to prove that one special instance of J-KEY-Region is NP-hard. We define such a special instance as follows. Set all the weight <img src="https://render.githubusercontent.com/render/math?math=w_{v_i} = 1, p_{(u,v)}\in \{0,1\}"> and assume every region only contains one event (<img src="https://render.githubusercontent.com/render/math?math=f(t) = r"> is one to one mapping). Then we give the decision problem as follows. Given a traffic event network *G(V, E)*, an non-negative integer *l*, we want to find a set *S* of regions such that <img src="https://render.githubusercontent.com/render/math?math=|S| = l and \sigma(T) \geq B">,   <img src="https://render.githubusercontent.com/render/math?math=\forall t \in T, f(t)\in R">.

Consider an instance of the NP-complete problem, \emph{Set Cover}. Given a universe <img src="https://render.githubusercontent.com/render/math?math=U={u_1, u_2, ..., u_n}"> and a collection of m subsets 
<img src="https://render.githubusercontent.com/render/math?math=C= {S_1, S_2, ..., S_m}">. We want to verify whether there exists a subset <img src="https://render.githubusercontent.com/render/math?math=C' \subseteq C"> so that <img src="https://render.githubusercontent.com/render/math?math=|C'| \leq k"> and <img src="https://render.githubusercontent.com/render/math?math=\cup_{S\in C'} S= C">.

We reduce the Set Cover to our J-KEY-Region problem as follows. We construct a set *V* of vertices and a set *E* of edges. Initially, *V* and *E* are set to be empty sets. For each element <img src="https://render.githubusercontent.com/render/math?math=u_i"> in *U*, create a vertex <img src="https://render.githubusercontent.com/render/math?math=v_{u_i}"> and insert to *V*. For each subset <img src="https://render.githubusercontent.com/render/math?math=S_j"> in C, create a vertex <img src="https://render.githubusercontent.com/render/math?math=v_{S_j}"> and insert to *V*. For each element <img src="https://render.githubusercontent.com/render/math?math=u_i in S_j">, construct a directed edge <img src="https://render.githubusercontent.com/render/math?math=e(v_{S_j}, v_{u_i})"> and insert to *E*. Finally, we obtain a directed graph *G = (V, E)*. Clearly, the aforementioned reduction runs in polynomial time. 

We show that the set cover problem is equivalent to the special instance of the J-KEY-Region problem, where <img src="https://render.githubusercontent.com/render/math?math=l = k and B = |U|">+ *k*. In other words, if the set cover problem has a yes-certificate (i.e., there are *k* subsets of C that cover U), then the corresponding set *S* of regions can influence at least <img src="https://render.githubusercontent.com/render/math?math=|U|">*+ k* events. Hence we have a yes-certificate for the J-KEY-Region problem. If the J-KEY-Region has a yes-certificate, then all the vertices <img src="https://render.githubusercontent.com/render/math?math=v_{u_i}"> must be influenced, which indicates $k$ subsets cover the corresponding universe. Therefore, the NP-hardness holds.

---
End proof
