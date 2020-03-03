# APPROXIMATION ALGORITHM


## Theorem:
The function <img src="https://render.githubusercontent.com/render/math?math=f(\pi)"> defined in the stochastic maximization problem defined in formula *(8)* is adaptive submodular.

**Begin proof**
---

In order to prove adaptive submodularity, it is sufficient to prove that 
<img src="https://render.githubusercontent.com/render/math?math=\forall \Phi\subseteq\Phi' \forall r\in R-dom(\Phi')">
<img src="https://render.githubusercontent.com/render/math?math=\Delta(r|\Phi)\geq\Delta(r|\Phi')"> 
where <img src="https://render.githubusercontent.com/render/math?math=\Delta(.)"> denotes the Conditional Expected Marginal Benefit. Since each addition of node would only increase the coverage function, the requirement of sufficiency holds.

---
**End proof**
