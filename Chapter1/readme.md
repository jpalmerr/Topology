# Open Subsets of R and Continuous Functions

## Definition 1.1

A subset *U* of *R* (real numbers) is **open** if:

 around each point *p* of *U* there is an open interval *(p-h, p+h)* wholly contained in *U*.

 ```
 (p - h, p + h) ⊆ U
 ```

------------------------
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

 **The empty set ∅ is vacuously open**

----------------
 A vacous truth is  conditional that is only true because the antecedent cannot be satisfied.

 **The closed interval [a, b] is not open in R**

 ```
 If you take p to be a,
 then every open interval (p - h, p + h) contains points outside of [a, b]
 ```

 **A singleton is not open in R**

 ```
 {a} = [a, a] => closed interval => not open
 ```

## Definition 1.8

Continuity:

Let *S* be an open subset of *R*.

A function `f:S -> R` is **continuous** on S <=> for each *a ∈ S* and each *ε > 0* there is a *δ > 0* such that

```
|x - a| < δ => |f(x) - f(a)| < ε
```

Speaking very loosely:

*f* is **continous** at *a* if *f(x)* is close to *f(a)* when *x* is close to *a*.

## Definition 1.10

Let `f: A -> B` be a function.

- If *T* is a **subset** of *B*
- then the **inverse image** of *T* **under** *f* is:
- the subset of *A* consisting of all the elements of *A* that *f* maps into *T*

```
a ∈ f^-1(T) <=> f(a) ∈ T
```

## Example

If `f:R -> R` is defined by `f(x) = x^2` then

```
f^-1([0,9]) = (-3, 3)

f^-1([-5, -4]) = ∅

f^-1(R) = R
```

## Theorem 1.12

Let S be an *open* subset of R.

A function f: S -> R is *continous* <=> the *inverse* image f^-1(U) under f of each open set U is *open*

Proof:

=>

```
Suppose f is continuous and let U be open.

No reason f^-1(U) can't be the empty set (also open).

If a ∈ f^-1(U) then f(a) ∈ U.
But U is open so
(f(a) - ε, f(a) + ε) ⊆ U

By continuity:

|x - a| < δ => |f(x) - f(a)| < ε

=> (a - δ, a + δ) ⊆ f^-1((f(a) - ε, f(a) + ε))
                  ⊆ f^-1(U)

Therefore f^-1(U) is open
```

<=

```
Suppose the inverse image of each open set is open

Let a ∈ S

(f(a) - ε, f(a) + ε) is open => f^-1(f(a) - ε, f(a) + ε) is open

By open set: contains (a - δ, a + δ) so

|x - a| < δ => x ∈ (a - δ, a + δ)
            => x ∈ f^-1((f(a) - ε, f(a) + ε)
           <=> f(x) ∈ (f(a) - ε, f(a) + ε)
           <=> |f(x) - f(a)| < ε

=> f is continuous at a           
```

If *f* is not continuous one can find an open subset U in the codomain of *f* such that the inverse image f^-1(U) of U under f is not open.

## Theorem 1.15

Let `f: R -> R`

and `g: R -> R` be continuous.

Then `g o f: R -> R` is also continuous.

## Definition 1.16

Let *S* be an open subset of *R*. A function `f: S -> R` is called **open** if the image of every open subset *V* of *S* is open in **R**

-----------
Note that **not every continuous map is open**.

For example: `f(x) = 7` is not an open map.

## Thereom 1.19

Let τ be the collection of all open subsets in *R*. Then

1. τ contains *R* and the empty set ∅

2. τ is **closed** under arbitrary unions

3. τ is **closed** under finite intersections
