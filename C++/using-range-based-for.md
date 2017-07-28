# Ranged based `for`

* For **observing** elements 
  ```
  for (auto elem : container) 	//capture by value
  ```
* For **modyfing** elements
  ```
  for (auto& elem : container)	//capture by reference
  ```

### Example

* Printing values (Observing)
```
vector<int> v = {1, 3, 5, 7, 9};

for (auto x : v)
    cout << x << ' ';
```
_=> 1 3 5 7 9_


* Modifying values
```
vector<int> v = {1, 3, 5, 7, 9};
for (auto& x : v)	//Modifying values
    x *= 10;

for (auto x : v)	//Observing values
    cout << x << ' ';
```
_=> 10 30 50 70 90_


**Note**: Compile using g++ with the `-std=c++0x` flag.

For example, `g++ -std=c++0x program.cpp`.

### References

* [StackOverflow](https://stackoverflow.com/a/15927037/4411757)
* [Compiling using c++11](https://stackoverflow.com/a/26740283/4411757)