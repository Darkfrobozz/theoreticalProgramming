Using our new found definition of [[types]], we can explore how we can use types.

One way to use types is to let the language do everything behind the scenes, this means the programmer does not have to give the type.

Rather, the language finds the type at runtime and matches it to the appropriate functions.

The weakness of this is that it requires more overhead and it is often unclear which function the data is actually going to go into as the programmer does not know.

This is called dynamic typing.
The opposite is static typing and that is when the programmer manually has to add the types, this removes the bad parts of dynamic typing but it adds manual overhead as now we have to make the types and they need to make sense, which requires planning.