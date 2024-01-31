A name space grabs some pattern and associates it to some computer representation.

For example,
```rust
fn main {

}
```
Associates the name space *main* with a function.

This is incredibly useful for making code maintainable and readable since referring to for example line numbers does not say anything even though the computer could infer based on that information alone.

It also connects our abstract thinking into the computer representation of things. For example,
this:
1010 1100
might not mean much to us but for a computer it is a easily readable binary number.

To represent it we could tie it to its purpose in the program. 
For example, we might call it index to be used in a loop.