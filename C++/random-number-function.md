# Random number function

**int rand(void);**

> Generates a pseudo-random number in the range between 0 and RAND_MAX.

**Note**: Here RAND_MAX is library-dependent and it's least value is 32767 on any standard library implementation.

#### Example
```
v1 = rand() % 100;         // v1 in the range 0 to 99
v2 = rand() % 100 + 1;     // v2 in the range 1 to 100
v3 = rand() % 30 + 1985;   // v3 in the range 1985-2014 
```

**Note**: You'll have to include `stdlib.h` and `time.h` libraries. Also initialize random seed before using `rand()` by including `srand(time(NULL));`.

### Reference

[CPlusPlus](http://www.cplusplus.com/reference/cstdlib/rand/)