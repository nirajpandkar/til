# LCM

```
typedef long long int ll;

ll lcm(vector<int> arr, int n){
    ll ans = arr[0];

    for(int i=1;i<n;i++){
        ans = (ans*arr[i])/(gcd(arr[i],ans));
    }
    return ans;
}
```

Refer to this [trick](./TricksAndTips/trick-to-find-lcm.md) for an explanation of above code and for an easier way to calculate lcm.
