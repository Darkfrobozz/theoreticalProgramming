This is a type of [[tree]], a visual example of such a [[tree]] can be found below:
![[bin_tree_numbers.png]]
The search part implies that the [[tree]] is to be sorted for searching and the binary part tells us that once a [[node]] is introduced it can at most extend the [[tree]] with two more [[link]]s.

This part with [[link]]s using [[big_O_notation]] leads to some interesting properties of a binary tree.

Afterall, if each [[node]] leads to two more [[node]]s, we can in a perfect world fit $2^n$ amount of nodes within a binary tree of depth $n$.

Consequently, navigating to a [[node]] in a perfect world would only take $n$ links with $2^n$ nodes.
So to get the time complexity to navigate to a [[node]] in a perfect tree would follow:
$$
O(\log_{2}{2^n})
$$

However, as been continually stated, this is only in a perfect world.
If each [[node]] only create one new [[node]], then we would need at least $\frac{n}{2}$ links on average to navigate to any one [[node]]. This of course grows a lot faster.

How a binary tree tries to solve this problem is not an inherent common denominator of trees.
But that this has an effect on the search speed is inherent in all [[binary_search_trees]].