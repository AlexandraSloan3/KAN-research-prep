# Lecture 1 - The Geometry of Linear Equations

*MIT 18.06 (2010) — Prof. Gilbert Strang*

Original handwritten notes preserved in [`raw-scans/`](raw-scans/).

## Setup — a 3×3 system

$$A = \begin{bmatrix} 2 & -1 & 0 \\ -1 & 2 & -1 \\ 0 & -3 & 4 \end{bmatrix}, \quad b = \begin{bmatrix} 0 \\ -1 \\ 4 \end{bmatrix}$$

**Row picture** → each equation is a plane; the solution is the point where all planes meet.

**Column picture** → think of $Ax = b$ as a linear combination of the columns of $A$:

$$x\begin{bmatrix} 2 \\ -1 \\ 0 \end{bmatrix} + y\begin{bmatrix} -1 \\ 2 \\ -3 \end{bmatrix} + z\begin{bmatrix} 0 \\ -1 \\ 4 \end{bmatrix} = \begin{bmatrix} 0 \\ -1 \\ 4 \end{bmatrix}$$

By inspection: $x = 0, y = 0, z = 1$ solves it — you just want "one of these" (the third column matches $b$ directly). Otherwise, need a systematic method → **elimination**.

**Second example, different $b$:**

$$x\begin{bmatrix} 2 \\ -1 \\ 0 \end{bmatrix} + y\begin{bmatrix} -1 \\ 2 \\ -3 \end{bmatrix} + z\begin{bmatrix} 0 \\ -1 \\ 4 \end{bmatrix} = \begin{bmatrix} 1 \\ 1 \\ -3 \end{bmatrix}$$

Solution: $x=1, y=1, z=0$ — "took one of these and one of those" (combination of the first two columns).

## The big question

> Can we solve $Ax = b$ for **every** $b$? Equivalently: do linear combinations of the columns of $A$ fill all of 3-D space?

- **Good matrix** → non-singular / invertible → columns span the full space, every $b$ is reachable
- **Bad matrix** → if all 3 columns happen to lie in the same plane, any combination of them is stuck in that plane. If $b$ is outside that plane, it's **unreachable** → matrix is **singular / not invertible**

## Generalizing to $n$ dimensions

Same question in $n$ dimensions: does every $b$ get filled by combinations of the columns? Depends on whether the columns are **independent**.

- If a column is a combination of the others → it's **not independent**, it **contributes nothing new** to the space you can reach
- If independent → the columns really can fill out the whole $n$-dimensional space

## How matrix-vector multiplication actually works

**Way 1 — a column at a time** ("$Ax$ is a combination of the columns of $A$"):

$$Ax = b: \quad \begin{bmatrix} 2 & 5 \\ 1 & 3 \end{bmatrix}\begin{bmatrix} 1 \\ 2 \end{bmatrix} = 1\begin{bmatrix} 2 \\ 1 \end{bmatrix} + 2\begin{bmatrix} 5 \\ 3 \end{bmatrix} = \begin{bmatrix} 12 \\ 7 \end{bmatrix}$$

**Way 2 — a row at a time (dot product):**

Row $(2, 5)$ dotted with $(1, 2)$: $2 \times 1 + 5 \times 2 = 12$
Row $(1, 3)$ dotted with $(1, 2)$: $1 \times 1 + 3 \times 2 = 7$

**Two equivalent views:**
1. By columns → $Ax$ = combination of A's columns
2. By rows → each entry of $Ax$ = dot product of a row of $A$ with $x$

**★ Key thought:** $Ax$ is a combination of the columns of $A$.
