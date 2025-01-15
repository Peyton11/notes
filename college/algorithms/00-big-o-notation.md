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

### Time Complexity for Binary Search

$T(n) \leq f(n) = \log{n} \Rightarrow T(n) = O(\log{n})$

## Asymptotic Notation

$\Theta, O, \Omega, o, \omega$

O "$\leq$"

$\Omega$ "$\geq$"

$\Theta$ "="

o "<"

$\omega$ ">"

The notations $(\Theta, O, \Omega, o, \omega)$ describe different rate-of-growth relations between the defining function and the defined set of functions.

The quotes are necessary around the comparison operators due to the possibility of constants.

## O-notation

**O-notation Definition**:  
For function g(n), we define O(g(n)), big-O of n, as the set:  
O(g(n)) = {f(n): $\exists$ positive constants c and $n_{0}$, such that $\forall_{n} \geq n_{0}$, we have $0 \leq f(n) \leq cg(n)$ }

f(n) = T(n) is the run time of an algorithm.  
*Intuitively*: Set of all functions whose rate of growth is the same or lower than that of g(n).

Technically, $f(n) \in O(g(n))$  
Older usage, $f(n) = O(g(n))$

**g(n) is an *asymptotic upper bound* for f(n).**

### Examples

To justify use $\exists, c, n_{0}, s.t.$

- $O(n^2)$
    - $n^2 + 1$  
        Is this $== O(n^2)$?  
        $n^2 + 1 \leq cn^2 = 2n^2 = n^2 + n^2$  
        If pick $c = 2, n_{0} = 0 \Rightarrow $ ???

    - $n^2 + n$  
        Is this $== O(n^2)$? Yes, it is.

    - $1000n^2 + 1000n$
        Yes, this is $O(n^2)$  
        You must show that $1000n^2 + 1000n \leq cn^2, \forall n \geq n_{0}$  
        Proof:  
        $1000n^2 + 1000n \leq cn^2 = 2000n^2 = 2000n^2 = .000n^2 + 10000n^2, then$ $\forall n \geq 1$

    - $n^{1.999}$
    - $n^2 / \log{n}$
    - $n^2 / \log{\log{\log{n}}}$

Example:  

$T(n) = 3n^3 + 2 = O(n^2)?$  
There are no $c, n_{0}, s.t.$  
$3n^3 + 2 \leq cn^2$  

Assuming $\exists c, n_{0}, s.t.$:  
$3n^3 \leq 3n^3 + 2 \leq cn^2$. Now,  

$3n \leq c$ (divide each side by n)  
$n \leq c/3$
This is not true because if n > c/3. Therefore, $3n^2 + 2 \neq O(n^2)$

## $\Omega-notation$

For function g(n), we define $\Omega(g(n))$, big-Omega of n, as the set:  
$\Omega(g(n))$ = {$f(n) : \exists$ positive constants c and $n_{0}, s.t. \forall n \geq n_{0}$, we have 0 $\leq cg(n) \leq f(n)$}

*Intuitively*: Set of all functions whose *rate of growth* is the same as or higher than that of g(n).

**g(n) is an *asymptotic lower bound* for f(n).**

### Examples

- $n-10^6 = \Omega(n)$  
    Yes, that means $\exists$ c > 0, $n_{0}$, s.t.  
    $n-10^6 \geq$ cn, $\forall n \geq n_{0}$.  
    True if c = 1/2.  
    $n-10^6 \geq 1/2n$

    $n-10^6 = 1/2n + 1/2n - 10^6 \geq 1/2n$  
    This would be true if $n_{0} = 2 * 10^6$  
    $1/2 * 2 * 10^6 - 10^6 = 0 \geq 0$  

- You create a search algorithm = $\sqrt{n} - 10$. Assume all records are sorted. Is this sort better than binary search?  

    $\sqrt{n}$ "$\leq$" $\log{n} \Leftrightarrow \log{n}$ "$\geq$" $\sqrt{n}$
