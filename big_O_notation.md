To analyze algorithms and data structures we can use big O notation, it is used to quickly describing its performance quality.

From Math we have to import the idea of growth, some [[function]]s grow faster than others.
For example using [[discrete_limits]] with conditionals,
$$
\lim_{ n \to \infty } (n^2 > n)
$$
In fact, this is a proof that $n^2$ grows quicker than $n$.
Big O notation takes the most significant component of a concepts performance as $n \to \infty$ and rates the concepts proficiency as that component.

For example, let's say it takes for every element added to the data structure, the bytes increase by $n + n^2$

Consequently, we would say that the space complexity of that data structure is $O(n^2)$.

If we are talking about speed, we would instead talk about time complexity.