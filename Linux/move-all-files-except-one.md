# Move all files except one


When you want to move all the files in a particular folder say `A` into a subfolder in `A`, say `a` you cannot just use `mv ~/A/* a/`. This doesn't work because you are essentially recursively moving subfolder `a` into itself. So you have to move everything _except_ `a` into `a`.

**Aim**: To convert this file structure..
```
A
-- a
-- file1
-- file2
```

into - 

```
A
-- a
	-- file1
	-- file2
```


This can be done in the following manner -  

```bash
$ mv `ls -1 ~/A| grep -v a` ~/A/a/
```

**Note**: -v option in grep excludes the result, it's like take everything except Tux.png


### References

* [StackOverflow](https://stackoverflow.com/a/41300731/4411757)
