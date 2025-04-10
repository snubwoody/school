# Compositions & Inverses

## Composition of linear transformations

In many situations, we want to apply several linear transformations, one after another. Similar to calculus where, given two functions $f$ and $g$, it is possible to define a function $f \circ g = f(g(x))$, we can also define composite linear transformations.

Let $T:\mathbb{R}^n \rightarrow \mathbb{R}^p$ and $S:\mathbb{R}^p \rightarrow \mathbb{R}^m$ be linear transformations. The **composition** $S \circ T:\mathbb{R}^n \rightarrow \mathbb{R}^m$ is defined by 

```math
(S \circ T)(\textbf{v}) = S(T(\text{v}))
```

### Example

Let $T:\mathbb{R}^2 \rightarrow \mathbb{R}^4$ and $S:\mathbb{R}^4 \rightarrow \mathbb{R}^3$ be the linear transformations given by

```math
T\left(\begin{bmatrix}x \\ y \end{bmatrix}\right) = \begin{bmatrix}7y \\ -2y \\ 3x - 4y \\ x \end{bmatrix} \text{ and } S \left(\begin{bmatrix}x \\ y \\ z \\ w \end{bmatrix}\right) = \begin{bmatrix}x+y \\ 0 \\ z+w \end{bmatrix}
```

1. Find the image of the vector $\begin{bmatrix}-3 \\ 4 \end{bmatrix}$ under the composition $S \circ T$.

```math
\begin{split}
(S \circ T)\left(\begin{bmatrix}-3 \\ 4 \end{bmatrix}\right) 
&=  S\left(T\left(\begin{bmatrix}1 \\ 2 \end{bmatrix}\right)\right)
\\ &=  S\left(\begin{bmatrix}14 \\ -4 \\ -5 \\ 1 \end{bmatrix}\right)
\\ &=  \begin{bmatrix}10 \\ 0 \\ -4 \end{bmatrix}
\end{split}
```