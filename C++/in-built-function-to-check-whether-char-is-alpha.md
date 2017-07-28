# In-built function to check whether character is alphabet

int isalpha ( int c );

>Checks whether _c_ is an alphabet.

```
#include<iostream>	//I/O
#include<ctype.h>	//isalpha()

using namespace std;

int main(){
    string str = "C++";
    for(auto &c:str){	//more info about range-based in the references
        if(isalpha(c))
            cout<<c<<" is an alphabet!\n";
        else
            cout<<c<<" isn't an alphabet!\n";
    }
    return 0;
}
```

**Output:**
```
C is an alphabet!
+ isn't an alphabet!
+ isn't an alphabet!
```

### References

* [Docs](http://www.cplusplus.com/reference/cctype/isalpha/)
* [Range-based for](./using-rang-baseed-for.md)