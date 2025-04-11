# Linear independence
Vectors $\textbf{v}_1,...,\textbf{v}_k \in \mathbb{R}^n$ are said to be **linearly independent** if the only solution to the equation $c_1\text{v}_1+...+c_k\textbf{v}_k = 0$ is the trivial solution $c_1=...=c_k=0$.

## Checking for linear independence by row reducing
In general, to decide if vectors $\textbf{u}_1,...\textbf{u}_k \in \mathbb{R}^n$ are linearly independent
- put them into a matrix as columns
- find a row-echelon form of that matrix
- determine whether there is a leading entry in each column

### Example
To determine whether the vectors
```math
\textbf{u}_1 = \begin{bmatrix} \end{bmatrix}
```
