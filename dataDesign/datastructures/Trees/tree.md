Let's construct a tree, a tree is a sorted [[node_network]].
![[dataset.png]]

Then step 2 is choosing a start node, notice the one in red.
![[dataset-tree.png]]
A tree starts with a head [[node]], this node is then connected with the rest of the tree using [[link]].

How these [[link]] are created is up to the designer of the tree. 
However, the reasons should not be at random, if they are, we will not be able to get the benefit of our data structure.
Moreover, most [[tree]] require at least some time adding more than one link per node.
The reason for this is that [[tree]] usually don't look like sticks.
And we have another name for such data structures, a [[list]].
Then we might as well stop at step 2.

Each [[node]] in our dataset has a number value and the order is that if the number is bigger we look to the right otherwise to the left.

So step 3 is from the treenode making our tree:
![[bin_tree_numbers.png]]
