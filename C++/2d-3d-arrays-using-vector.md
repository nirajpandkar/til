# 2D/3D arrays using Vector

There are two major methods to create a 2D/3D array - using **vectors** or **pointers**.

Vectors are beneficial in the sense that they automatically remove the memory they use when they go out of scope.

You can also do some interesting things with dynamic multi-dimensional arrays with vectors. For example, if you only allocate the first dimension, then use the `push_back()` to add records to the 2nd dimension it's no longer a grid, but an array with a dynamically sized 2nd dimension.

2D Array with Vectors: 

```
#include <vector>
using std::vector;

#define HEIGHT 5
#define WIDTH 3

int main() {
  vector<vector<double> > array2D;

  // Set up sizes. (HEIGHT x WIDTH)
  array2D.resize(HEIGHT);
  for (int i = 0; i < HEIGHT; ++i)
    array2D[i].resize(WIDTH);

  // Put some values in
  array2D[1][2] = 6.0;
  array2D[3][1] = 5.5;

  return 0;
}
```

**Note**: `resize()` is the analogous step to allocating memory in C. It's a necessary step without which the code won't work. For examples on 3D arrays and pointers, visit the reference link.

### Reference

[CPlusPlus Forum Article](http://www.cplusplus.com/forum/articles/7459/)