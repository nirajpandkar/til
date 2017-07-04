# Left/Right Rotation of array

```
vector<int> array_left_rotation(vector<int> a, int n, int k) {
    vector<int>::iterator it;
    for(int i=0;i<n-k;i++){
        it = a.begin();
        int element = a.back();
        a.pop_back();
        a.insert(it, element);
    }
    return a;
}
```

**Note**: Change the condition in the for loop accordinly for left or right rotation.
