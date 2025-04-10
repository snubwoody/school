# Linear independence

Vectors $\textbf{v}_1,...,\textbf{v}_k \in \mathbb{R}^n$ are said to be **linearly independent** if the only solution to the equation $c_1\text{v}_1+...+c_k\textbf{v}_k = 0$ is the trivial solution $c_1=...=c_k=0$.

## Checking for linear independence by row reducing

In general, to decide if vectors $\textbf{u}_1,...\textbf{u}_k \in \mathbb{R}^n$ are linearly independent

- put them into a matrix as columns
- find a row-echelon form of that matrix
- determine whether there is a leading entry in each column

### Example

To determine whether the vectors

$$
\textbf{u}_1 = \begin{bmatrix} 1 \\\ 2 \\\ 3 \\\ 4 \\\ 5 \end{bmatrix},
\textbf{u}_2 = \begin{bmatrix} 0 \\\ 1 \\\ 2 \\\ 3 \\\ 4 \end{bmatrix},
\textbf{u}_3 = \begin{bmatrix} 1 \\\ 2 \\\ 3 \\\ 2 \\\ 1 \end{bmatrix},
\textbf{u}_4 = \begin{bmatrix} 3 \\\ -2 \\\ 1 \\\ -2 \\\ 3 \end{bmatrix}
$$

are lineary independent, we form a matrix with the vectors as columns

$$
A=
\begin{bmatrix}
1 & 0 & 1 & 3 \\\
2 & 1 & 2 & -2 \\\
3 & 2 & 3 & 1 \\\
4 & 3 & 2 & -2 \\\
5 & 4 & 1 & 3 \\\
\end{bmatrix}
$$

$A$ has a row-echelon form given by

$$
\begin{bmatrix}
1 & 0 & 1 & 3 \\\
0 & 1 & 0 & -8 \\\
0 & 0 & -2 & 10 \\\
0 & 0 & 0 & 8 \\\
0 & 0 & 0 & 0 \\\
\end{bmatrix}
$$

which has a leading entry in every column, so the vectors $\textbf{u}_1,\textbf{u}_2,\textbf{u}_3$ are linearly independent.
