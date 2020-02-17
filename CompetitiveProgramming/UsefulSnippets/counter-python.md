# Factorial

```
from collections import Counter

def ransom_note(magazine, rasom):
    return (Counter(rasom) - Counter(magazine)) == {}
```

## Explanation
The result of counters' operator substraction is a counter that shows how many more values magazine is missing to match those present in rasom. When an empty dict is returned, every element in rasom is present enough times in magazine.

### References

* [HackerRank(Ransom Note)](https://www.hackerrank.com/challenges/ctci-ransom-note/forum/comments/192081?h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=dictionaries-hashmaps
)