# Clone git repository with a specific revision sheet

There are two methods to achieve the same result - 
* Without pulling everything from the remote repo.
* Pulling everything which includes other branches too. (Not a good option for large repos)

#### Without pulling everything from the remote repo

```
# make a new blank repository in the current directory
git init

# add a remote
git remote add origin url://to/source/repository

# fetch a commit (or branch or tag) of interest
# Note: the full history of this commit will be retrieved
git fetch origin <sha1-of-commit-of-interest>

# reset this repository's master branch to the commit of interest
git reset --hard FETCH_HEAD
```

#### Pulling everything which includes other branches too
```
$ git clone $URL
$ cd $PROJECT_NAME
$ git reset --hard $SHA1
```
To again go back to the most recent commit
```
$ git pull
```

### References

1. [StackOverflow](https://stackoverflow.com/a/3489576/4411757)
2. [StackOverflow](https://stackoverflow.com/a/14091182/4411757)