# Linear transformations

## Transformations

Let $m$ and $n$ be positive integers. A **transformation** $T$ from $\mathbb{R}^n$ to $\mathbb{R}^m$ written
$$T: \mathbb{R}^n \rightarrow \mathbb{R}^m$$
is a rule that assigns each vector $\textbf{v}$ in $\mathbb{R}^n$ exactly one vector $T(\textbf{v})$ in $\mathbb{R}^m$. A transformation is also called a **map** or a **function**. 
We say that $T(\textbf{v})$ is the **image** of $\textbf{v}$ under $T$.
We call $\mathbb{R}^n$ the **domain** of $T$ and $\mathbb{R}^m$ the **codomain** of $T$. The subset $\{T(\textbf{v}) | \textbf{v} \in \mathbb{R}^n\}$ of $\mathbb{R}^m$ consisting of all images under $T$ of vectors in $\mathbb{R}^n$ is the **range** (or image) of $T$.^transformation-definition.

### Example

Consider the following transformation
```math
\begin{split}
&T:\mathbb{R}^2 \rightarrow \mathbb{R}^3 \\
&\begin{bmatrix}x \\ y\end{bmatrix}\rightarrow
\begin{bmatrix}2x \\ 0 \\ x + y\end{bmatrix}
\end{split}
```

The image of the vector $[5,-8]$ in $\mathbb{R}^2$ under $T$ is

```math
\begin{split}
T\left(\begin{bmatrix}5 \\ -8 \end{bmatrix}\right) 
&=\begin{bmatrix}2(5) \\ 0 \\ (5-(-8) \end{bmatrix} \\
&=\begin{bmatrix}10 \\ 0 \\ -3 \end{bmatrix}
\end{split}
```

## Linear transformations

There is a special kind of transformation called a **linear transformation**. These are special transformations which preserve the vector space structure of the domain.

A transformation $T:\mathbb{R}^n \rightarrow \mathbb{R}^m$ is said to be a **linear transformation** if the following conditions hold:
**(LT1)** $T(\textbf{u} + \textbf{v}) = T(\textbf{u}) + T(\textbf{v})$ for all $\textbf{u},\textbf{v} \in \mathbb{R}^n$
**(LT2)** $T(c\textbf{u}) = cT(\textbf{u})$ for all $\textbf{u} \in \mathbb{R}^n$ and all scalars $c \in \mathbb{R}$
^linear-transformation-definition

A linear transformation $T: \mathbb{R}^n \rightarrow \mathbb{R}^m$ is called a **linear operator** on $\mathbb{R}^n$.

Condition **(LT1)** says that a linear transformation **preserves vector addition**, while condition **(LT2)** says that a linear transformation **preserves scalar multiplication**.

###### Example
Consider the map $T$ defined below:

```math
\begin{split}
&T: \mathbb{R}^2 \rightarrow \mathbb{R}^3 \\
&\begin{bmatrix}x \\ y\end{bmatrix} \rightarrow
\begin{bmatrix}2x \\ 0 \\ x - y\end{bmatrix}
\end{split}
```

a) Is $T(\textbf{u} + \textbf{v}) = T(\textbf{u}) + T(\textbf{v})$, for $\textbf{u} = [-3,1]$ and $\textbf{v} = [2,4]$?

```math
\begin{split}
T\left(
\begin{bmatrix}-3 \\ 1\end{bmatrix} + 
\begin{bmatrix}2 \\ 4\end{bmatrix}
\right) 
&= T\left(\begin{bmatrix}-1 \\ 5\end{bmatrix}\right) \\
&= \begin{bmatrix}-2 \\ 0 \\ 4\end{bmatrix} \\
T\left(\begin{bmatrix}-3 \\ 1\end{bmatrix}\right) + 
T\left(\begin{bmatrix}2 \\ 4\end{bmatrix}\right) 
&= \begin{bmatrix}-6 \\ 0 \\ -2\end{bmatrix} + 
\begin{bmatrix}4 \\ 0 \\ 6\end{bmatrix} \\
&= \begin{bmatrix}-2 \\ 0 \\ 4\end{bmatrix}
\end{split}
```

Therefore, for $\textbf{u} = [-3,1]$ and $\textbf{v} = [2,4]$, we have $T(\textbf{u} + \textbf{v}) = T(\textbf{u}) + T(\textbf{v})$. 

### Proving linear transformations

To show that a map $T: \mathbb{R}^n \rightarrow \mathbb{R}^m$ is a linear transformation, we verify that both of the conditions (LT1) and (LT2) hold arbitrary vectors in $\mathbb{R}^n$ and arbitrary scalars.

###### Example

Show that the map 
```math
\begin{split}
&T: \mathbb{R}^n \rightarrow \mathbb{R}^m \\
&\begin{bmatrix}x \\ y\end{bmatrix} \rightarrow \begin{bmatrix}2x \\ 0 \\ x + y\end{bmatrix}
\end{split}
```
is a linear transformation.

**(LT1):** Let $\textbf{u} = \begin{bmatrix}a \\ b\end{bmatrix}$ and $\textbf{v} = \begin{bmatrix}c \\ d\end{bmatrix}$ be vectors in $\mathbb{R}^2$. Then

```math
\begin{split}
T(\textbf{u} + \textbf{v}) 
&= T\left(
\begin{bmatrix}a \\ b\end{bmatrix}
+ \begin{bmatrix}c \\ d\end{bmatrix}
\right) \\
&=T\left(
\begin{bmatrix}a + c \\ b + d\end{bmatrix}
\right) \\
&=\begin{bmatrix}2(a + c) \\ 0 \\ a + c +b + d\end{bmatrix}
\end{split}
```

and 

```math
\begin{split}
T(\textbf{u}) +T(\textbf{v}) 
&= T\left(
\begin{bmatrix}a \\ b\end{bmatrix}
\right) + 
T\left(
\begin{bmatrix}c \\ d\end{bmatrix}
\right) \\
&=
\begin{bmatrix}2a \\ 0 \\ a + b\end{bmatrix} + 
\begin{bmatrix}2c \\ 0 \\ c + d\end{bmatrix} \\
&=\begin{bmatrix}2a + 2c \\ 0 \\ a + b + c + d\end{bmatrix} \\
&=\begin{bmatrix}2(a + c) \\ 0 \\ a + c + b + d\end{bmatrix}
\end{split}
```

Therefore (LT1) holds.

**(LT2):** Let $\textbf{v} = \begin{bmatrix}a \\ b\end{bmatrix}$ and $k \in \mathbb{R}$. Then 

```math
\begin{split}
T(k\textbf{v}) 
&= T\left(
k\begin{bmatrix}a \\ b\end{bmatrix}
\right) \\
&= T\left(
\begin{bmatrix}ka \\ kb\end{bmatrix}
\right) \\
&=\begin{bmatrix}2(ka) \\ 0 \\ ka + kb\end{bmatrix}
\end{split}
```

and

```math
\begin{split}
kT(\textbf{v}) 
&= kT\left(
\begin{bmatrix}a \\ b\end{bmatrix}
\right) \\
&=k \begin{bmatrix}2a \\ 0 \\ a + b\end{bmatrix} \\
&=\begin{bmatrix}2(ka) \\ 0 \\ ka + kb\end{bmatrix}
\end{split} 
```

Therefore (LT2) holds. Thus since both (LT1) and (LT2) hold, $T$ is a linear transformation.