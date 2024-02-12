# Problem
In programming, we want to structure our data.
We could have everything at the same place but another approach is to structure it so that we create a so called environment for different procedures.
This is because we only want those procedures to be able to access components related to that procedure and we only want to allocate memory for those components when that procedure is being run.
There are many ways to organize our data but one of the key concepts necessary is navigation and connectedness.
If we can't navigate back to our initial environment and if environments are disconnected we won't be able to access allocated data.

# Theoretical Solution
Thus, at a bare minimum we define that an environment is either empty or consists of a sequence of frames.
A frame is like a plaque, a table where we can store bindings for [[name_spaces]].
We can proceed to the enclosing environment of a frame by following a pointer.
All frames have an enclosing environment except the global one.
# Practice
In practice these means we need three operations on environments:
- lookup symbol value
- extend environment
- assign symbol value

We also to properly use this will need a way to extend environment by scanning for incoming declarations.