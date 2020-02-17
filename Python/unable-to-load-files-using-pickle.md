# Unable to load files using pickle

**Problem**:  Objects pickled in one module/file/place wouldn't load in another. Gives the following error - 
```
AttributeError: Can't get attribute '<some-function-name>' on <module '__main__' from 'main.py'>
```

**Good to know**: 

The issue is that you're pickling objects defined in one module by actually running that module/function/main, then you're trying to unpickle the objects from a different module.
Remember that pickle doesn't actually store information about how a class/object/function is constructed, and needs access to the class/function when unpickling.

In my case, `TfIdfVectorizer` was using a custom tokenizer function called `process_text`. When I pickled the tfidf object to use again in another script, it couldn't get the attribute `process_text` on module main.

**Solution**:
To solve this, I created another file with only the function definition of `process_text` in it, and imported the function from the file into the script where I needed to load the pickle. Voila!


### References

* [A more detailed (probably more accurate :P) explanation on StackOverflow](https://stackoverflow.com/a/27733727/4411757)
* [Pickle Wiki](https://wiki.python.org/moin/UsingPickle)