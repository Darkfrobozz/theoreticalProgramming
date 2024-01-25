A probing [[hashtables]] is one that utilizes a probe function to handle collision.

The essential part of these [[hashtables]] is that if a collision occurs then we look further into the array to find the an empty slot.

This practices of trying to find the next empty slot is our probing and the reason we don't want our probing to be random is because we want to be able to exactly repeat what the inserting probe did when we are doing a lookup.

There are various ways to perform this search:
- Linear Probing: To look for the next index to search, we just add a constant to our current index.
- Quadratic Probing: To look for the next index to search, we add a quadratic value based on the amount of checks preformed.

These probing methods can also be augmented by providing a double hash, what this means is that we have a second hash function that calculates an alternative empty slot for the first collision and, then, uses the other probing techniques discussed.

The reason we have these different probing techniques is because they have various benefits. 
For example, linear probing can result in clustering of data that get the same key while quadratic probing avoids that.
However, quadratic probing increases the overhead as we now need to keep track of attempts, multiplying numbers and, so, on, which could add up over time.