# Difference between size() and capacity()

`capacity()` is the maximum characters a string can hold without having to grow. `size()` is the number of characters currently existing in the string.

**Reason:** Allocating memory is generally inefficient. So allocation is done as rarely as possible by grabbing more memory than is actually needed at a time.
Many data structures use a "doubling" method where, if they hit their capacity of `N` and need more space, they will allocate `2*N` space, to avoid having to reallocate again any time soon.
