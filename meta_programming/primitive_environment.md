To tie together [[boot_strapping]] and [[environment]], we can create in our [[meta_circular_evaluator]] a global environment in which we can apply the things that are already implemented in the language and, then, develop new functionality by extending to a new [[environment]] on top of that.

We call this the primitive environment and it is often filled with primitive functions.