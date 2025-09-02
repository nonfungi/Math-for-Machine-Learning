# Section 3: Matrix Operations

Matrices are the workhorses of machine learning. Here are the most fundamental operations you need to know.

### 1. Matrix Transposition

The **transpose** of a matrix, denoted as $A^T$, is an operation that flips the matrix over its main diagonal. In other words, the rows of the original matrix become the columns of the transposed matrix.

- **Example:**
If $A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \\ 5 & 6 \end{bmatrix}$, then its transpose is $A^T = \begin{bmatrix} 1 & 3 & 5 \\ 2 & 4 & 6 \end{bmatrix}$.

---

### 2. Matrix Addition and Scalar Multiplication

These operations are straightforward and work element by element, just like with vectors.

- **Matrix Addition:** You can only add two matrices if they have the **same dimensions**. The addition happens element-wise.
$$
\begin{bmatrix} a & b \\ c & d \end{bmatrix} + \begin{bmatrix} e & f \\ g & h \end{bmatrix} = \begin{bmatrix} a+e & b+f \\ c+g & d+h \end{bmatrix}
$$

- **Scalar Multiplication:** You multiply every element of the matrix by a single scalar number.
$$
k \cdot \begin{bmatrix} a & b \\ c & d \end{bmatrix} = \begin{bmatrix} ka & kb \\ kc & kd \end{bmatrix}
$$

---

### 3. Matrix Multiplication (The Most Important Operation)

Matrix multiplication is **not** element-wise. It's a process of combining two matrices to produce a third. It's the core operation in linear transformations and neural networks.

- **The Rule:** To multiply two matrices $A$ and $B$ (to get $C = AB$), the number of **columns** in matrix $A$ must be equal to the number of **rows** in matrix $B$.
- **Calculation:** Each element in the resulting matrix $C$ is the **dot product** of a row from matrix $A$ and a column from matrix $B$.

- **Example:**
Let $A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$ and $B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}$.
Then $C = AB$ is calculated as:
$$
C = \begin{bmatrix} (1 \cdot 5 + 2 \cdot 7) & (1 \cdot 6 + 2 \cdot 8) \\ (3 \cdot 5 + 4 \cdot 7) & (3 \cdot 6 + 4 \cdot 8) \end{bmatrix} = \begin{bmatrix} 19 & 22 \\ 43 & 50 \end{bmatrix}
$$

- **Critical Property:** Matrix multiplication is **not commutative**. This means that in most cases, $AB \neq BA$. The order matters!

---

### 4. Hadamard Product (Element-wise Product)

There is also an element-wise product, which is less common in transformations but used in some ML algorithms. It's denoted by the $\odot$ symbol.

- **Formula:**
$$
\begin{bmatrix} a & b \\ c & d \end{bmatrix} \odot \begin{bmatrix} e & f \\ g & h \end{bmatrix} = \begin{bmatrix} ae & bf \\ cg & dh \end{bmatrix}
$$
It's important not to confuse this with standard matrix multiplication.