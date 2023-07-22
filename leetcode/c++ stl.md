## vector

```c++
vector<vector<int>> res(2, vector<int>(n, 0)); //里面的vector n 个数字都是0
```

## unordered_map

```C++
        unordered_map<int, int> hashtable;
        for (int i = 0; i < nums.size(); ++i) {
            auto it = hashtable.find(target - nums[i]);
            if (it != hashtable.end()) {
                return {it->second, i};
            }
            hashtable[nums[i]] = i;
        }
```

