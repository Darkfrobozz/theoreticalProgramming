The in order tree walk is an algorithm called on ordered [[tree]]s.
It relies on following recursively each of a [[node]]s [[link]]s in some order.
This algorithm runs in O(n) time.
This can be proven by first reasoning of an empty binary tree:
$$
T(0) = c, c > 0
$$
Then assuming $k$ is the amount of [[node]]s in the left subtree, postulating the scenario in a recursive manner:
$$
T(n) \leq T(k) + T(n - k - 1) + d, d > 0
$$
Where $d$ is a constant that reflects how much time it takes to make the two calls the subtrees.
Now we only need to prove that the right side runs in $O(n)$ time.
We will now use the [[substituion_method]] to prove that it is $O(n)$:
We now assume that:
$$
T(n) \leq (c + d)n + c \tag{1}
$$
For $T(0) = (c+d) \cdot 0 + c = c$, we have that it is true.
Now for assume subtree *k* is true then by (1):

$$
\begin{align}
T(n) &\leq (c+d)k + c + (c+d)(n - k - 1) + c +d  \\
&\leq (c + d)n - (c + d) + 2c + d \\
&\leq (c + d)n + c  \\
\end{align}
$$
Thus, completing the proof. $\square$