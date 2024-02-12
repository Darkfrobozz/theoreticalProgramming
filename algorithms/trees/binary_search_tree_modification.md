## Introduction
Assume that this is a [[numeric_binary_search_tree]] :

We want to support the following two modification actions :
- Insertion
- Deletion
## Insertion

Let's think about the fact that the [[inorder_tree_walk]] property must be preserved. 
Therefore, we can use [[binary_search_tree_queries]] to find the place by looking for a predecessor or a successor, note that there is a collision we will just overwrite.
Moreover, if the predecessor or successor is not a leaf, we will have to insert our node in between its corresponding direction.
Either way we would find this collision since by design since both predecessor and successor moves towards the target node.

Thinking about this visually, we should be able to place our insertion node either to the right of its predecessor or to the left of its successor for our [[inorder_tree_walk]] to be maintained.
## Deletion
First we can use our search from [[binary_search_tree_queries]] to lookup the suggested node.
Then, we have three cases
1. 0 children - simply remove and set its parents link to it to null.
2. 1 child - simply remove and let the child take its place.
3. 2 children - Harder because the children can't take its place as it will gain a new child!

### The Two Children

We need to find a candidate for this *x* and that candidate must be a leaf since then it can handle two new children.
To solve this we should look at the [[inorder_tree_walk]]. 
To maintain this, the successor and the predecessor can take the role as the [[inorder_tree_walk]] would be maintained if the new key was either of them.
Moreover, since all values to the left of our [[node]] *x* are to the left of the predecessor (except itself) and all values to the right are to the right of the predecessor we have that the order is maintained. 

However, while this indeed then makes a good candidate, we need to ensure that it is a leaf, is this always the case?
Well obviously the predecessor can have children to its left but if it has a child to its right than that would be the predecessor since it is a greater value that is still less by the order property than the key of *x*.
A similar line of reasoning can be applied to successor.

Well then, we cannot prove that it is a leaf.
But, deleting a node with only one child was an easy process!
So let's delete the predecessor and then instead of deleting *x*, overwrite it with the predecessor.
We can do the same with the successor.

In conclusion, we can delete a [[node]] with two children by using our ability to delete a node with one child to move the predecessor or successor to replace *x*.