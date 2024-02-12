A topological ordering can be thinking of never visiting a [[node]] before we visit a node that leads to this node.

This means that we are interested in dependencies, if we think of our [[acyclic_directed_graphs]] as if one [[node]] points to another then that [[node]] depends on that other node.

![[dependency.png]]
Here *A* is not dependent on anything. However, both *C* and *B* are dependent on *A*.

[[directed_graphs]] with cycles do not have topological orderings since [[node]] will need to have visited themselves before visiting themselves which is contradictory.

An example would be putting on yours clothes, a topological order would take into account dependencies :
- Boxers -> Pants -> Done - This is a topological order
- Pants -> Done This does not take into account the dependencies of pants in this context.

