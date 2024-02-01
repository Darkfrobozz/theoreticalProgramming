## Introduction
Assume that this is a [[numeric_binary_search_tree]] :

These different queries can be proven to end up with $O(h)$ time where $h$ is the height :
- Minimum
- Maximum
- Successor
- Predecessor
## Minimum
The height is the longest route of links in the tree.
All [[node]]s to the left are lower in value to that of its parent.
Consequently we can simply take the left path at all times.
In the worst case that choice leads to the longest path.
## Maximum
In similar fashion to the minimum proof, we can prove that maximum runs in $O(h)$.
## Successor
We can use squeezing to our advantage for this.
A successor is the closest value after a certain value.
Thus, a successor is greater than but also closest to our value.

Thus, we reach two cases:
1. If the key of the node we are at is less then we should move to the right
2. If it is more we should move to the left.
3. If the keys are equal we should move to the right : we want the successor, which is greater than our target key.
This way we will always move towards the closest node as we are always taking the option that squeezes our target key in its range.
Another way to think about it is if we were to not do this then we can just guaranteed that the node we just left was the best node since we are moving away from the target.

After we are done with this we should end up with either a value that is higher or lower than our target key.
If it is indeed lower then we should reverse the walk to the first value that is higher than our target key.
By our contradiction proof this is indeed the closest successor value.
This is at most the height times two since we could have to reverse all the way back to the top!!
But then this is still in $O(h)$ time.
## Predecessor
This algorithm works exactly the same except part three is edited such that: 
- We always should move to the left since we now want a lower value.
- If we end up with a higher value we want to now reverse to a lower value.
And for the same reasons then it runs in $O(h)$ time.

