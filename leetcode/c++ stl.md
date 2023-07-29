## vector

```c++
vector<vector<int>> res(2, vector<int>(n, 0)); //里面的vector n 个数字都是0

vec.resize(n);
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

## priority_queue

```c++
struct cmp{
    bool operator()(const pair<int, int> &a, const pair<int, int> &b){
        return a.first>b.first; // 从小到大
    }
};
priority_queue<pair<int,int>, vector<pair<int,int>>, cmp> que; // 默认从大到小

que.push();
que.top();
que.pop();
```

