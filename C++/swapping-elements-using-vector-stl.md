# Swapping elements using vector STL

Can be done using `swap()` or `iter_swap()` in `<algorithm>`.

* Based on object contents (Swap v[0] and v[1])-
```
swap(v[0], v[1]);
```

* Based on underlying iterators -
```
iter_swap(v.begin(), v.begin()+1);
```

### References

* [StackOverflow](https://stackoverflow.com/a/22514812/4411757)
