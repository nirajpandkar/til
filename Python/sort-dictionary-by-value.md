# Sort dictionary by value

**Good to know**: It is not possible to sort a dictionary, only to get a representation of a dictionary that is sorted. Dictionaries are inherently orderless, but other types, such as lists and tuples, are not. So you need an ordered data type to represent sorted values, which will be a list—probably a list of tuples.


```
x = {1: 2, 3: 4, 4: 3, 2: 1, 0: 0}
sorted_by_value = sorted(x.items(), key=lambda y: y[1])
```

**Explanation**: Pass the value of the keys in the dictionary as a lambda function to the `key` parameter of `sorted()` function. Additionally you can set `reverse` parameter to `True` for descending order.

### References

[StackOverflow](https://stackoverflow.com/a/613218/4411757)