# Open Subsets of R and Continuous Functions

## Definition 1.1

A subset U of R (real numbers) is **open** if:

 around each point *p* of U there is an open interval *(p-h, p+h)* wholly contained in U.

 ```
 (p - h, p + h) ⊆ U
 ```

 You should think of an *open set* as containing none of the points at the edge of the set.

 ## Examples

 **Every open interval (a, b) is an open set in R**

 Proof:

 ```
 If p ∈ (a, b), let h be the distance from p to the nearest end point

 h = min(b - p, p - a)

 => (p - h, p + h) ⊆ (a, b)
 ```

 **R is open**

 **The empty set ∅ is vacuosuly open**

 A vacous truth is  conditional that is only true because the antecedent cannot be satisfied.

 **The closed interval [a, b] is not open in R**

 ```
 If you take p to be a, then every open interval (p - h, p + h) contains points outside of [a, b]
 ```

 **A singleton is not open in R**

 ```
 {a} = [a, a] => closed interval => not open
 ```
