# Clone a specific git branch

```
git clone -b <branch> <remote_repo>
```
Example:
```
git clone -b my-branch git@github.com:user/myproject.git
```
Alternative (no public key setup needed):
```
git clone -b my-branch https://git@github.com/username/myproject.git
```
With Git 1.7.10 and later, add --single-branch to prevent fetching of all branches. Example, with OpenCV 2.4 branch:
```
git clone -b 2.4 --single-branch https://github.com/Itseez/opencv.git opencv-2.4
```

### References

* [StackOverflow](https://stackoverflow.com/a/4568323/4411757)