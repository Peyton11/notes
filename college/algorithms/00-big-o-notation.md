# Ch 0: Big-O Notation

## Asymptotic Complexity

- Running time of an algorithm as a function of input size *n* **for large n**.
- Expressed using only the **highest-order term** in the expression for the exact running time.
    - Instead of exact running time, say $O(n^2)$.
- Describes behavior of function in the limit. 
- Written using **Asymptotic Notation**. 

## Examples/Terminology

### Big O is for the upper bound (worst case).  

If $T(n) = O(\log{n})$, $T(n) \leq \log{n}$.

T(n) is the time complexity.


### Big Omega is for the lower bound (best case).  

$T(n) \geq 1$

$\Omega(1)$ 
