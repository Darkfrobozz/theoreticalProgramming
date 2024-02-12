This is algorithm for performing a [[topological_ordering]] sort.

What we do is repeatedly remove [[node]]s from the graphs that have no dependencies left, then we filter away those that depended on that node.

There are therefore three steps :
1. Find a node with no dependencies in graph *A*
	1. If we can find no such node we return the queue
2. Enqueue that node in a result queue 
3. Produce a new graph *B* that does not have the removed node
4. return the queue from, send that new graph *B* and the result queue to the kahn algorithm

Thus, we have to implement :
- Finding a node with no dependencies : 
	- We can do this by coloring all found nodes as black : and only removing white nodes in the end requiring at least one white node.
- A queue to enqueue our nodes in.
- Producing a new graph by removing a node from a graph.
	- We can easily use filter for this