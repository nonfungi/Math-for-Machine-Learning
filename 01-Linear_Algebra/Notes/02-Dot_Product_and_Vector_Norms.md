# Section 2: Dot Product and Vector Norms

To fully understand the dot product, we first need to learn about the "magnitude" or "length" of a vector. This concept is called the **Norm**.

### 1. Vector Norm

The norm of a vector represents its length or its distance from the origin. The most common type is the **$L_2$ Norm**, or the Euclidean distance, denoted by the symbol $\|v\|$.

- **Formula:** For a vector $v = [v_1, v_2, ..., v_n]$, the $L_2$ norm is calculated as follows:
$$
\|v\| = \sqrt{v_1^2 + v_2^2 + \cdots + v_n^2} = \sqrt{\sum_{i=1}^{n} v_i^2}
$$
- **Example:** If we have a vector $a = [3, 4]$, its length is:
$\|a\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5$



---

### 2. Dot Product

The dot product of two vectors returns a single **scalar** number that represents the relationship between their directions and magnitudes.

#### Algebraic Definition
This is how we calculate the dot product.
- **Formula:** For two vectors $a = [a_1, a_2]$ and $b = [b_1, b_2]$:
$$
a \cdot b = a_1b_1 + a_2b_2
$$

#### Geometric Definition
This definition gives a better intuition for what the dot product means.
- **Formula:**
$$
a \cdot b = \|a\| \|b\| \cos(\theta)
$$
Here, $\theta$ is the angle between the two vectors. This formula tells us that the dot product is equivalent to projecting one vector onto the other and multiplying their lengths.



#### What does the Dot Product's result mean?
The sign of the dot product tells us if the vectors are pointing in similar directions:
- **If $a \cdot b > 0$ (Positive):** The angle between the vectors is less than 90°. They are pointing in roughly the same direction.
- **If $a \cdot b = 0$ (Zero):** The vectors are orthogonal (perpendicular). The angle between them is exactly 90°.
- **If $a \cdot b < 0$ (Negative):** The angle between the vectors is greater than 90°. They are pointing in roughly opposite directions.

---

### 3. Cosine Similarity

Now that we understand the dot product and vector norms, **Cosine Similarity** is a direct and very important application. This metric measures **only the similarity in direction** between two vectors, ignoring their magnitudes.

By rearranging the geometric formula for the dot product, we get the formula for cosine similarity:

- **Formula:**
$$
\cos(\theta) = \frac{a \cdot b}{\|a\| \|b\|}
$$

- **Use in ML:** This metric is widely used to measure the similarity between text documents, recommend products to users (Recommendation Systems), and more. In these applications, the direction of the vector (the "meaning") is more important than its magnitude (e.g., the length of the text).

- **Interpreting the Values:**
    - **1:** The vectors are pointing in the exact same direction (maximum similarity).
    - **0:** The vectors are orthogonal (no similarity).
    - **-1:** The vectors are pointing in opposite directions (maximum dissimilarity).