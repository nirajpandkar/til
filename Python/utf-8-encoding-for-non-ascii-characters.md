# UTF-8 encoding for non ascii characters

**Problem**:  Unicode literals can only be written using the Latin-1 based encoding "unicode-escape". This makes the programming environment rather unfriendly to Python users who live and work in non-Latin-1 locales such as many of the Asian countries. Programmers can write their 8-bit strings using the favorite encoding, but are bound to the "unicode-escape" encoding for Unicode literals.

**Solution**: 

To define a source code encoding, a magic comment must be placed into the source files either as first or second line in the file, such as:

```
# coding=<encoding name>
```
or (using formats recognized by popular editors):

```
#!/usr/bin/python
# -*- coding: <encoding name> -*-
```

**Note**: Python will default to ASCII as standard encoding if no other encoding hints are given.

### References

* [Stackoverflow](https://stackoverflow.com/a/24221963/4411757)
* [Defining Python Source Code Encodings(Official)](https://www.python.org/dev/peps/pep-0263/#id8)