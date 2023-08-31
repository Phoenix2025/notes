## vector

```c++
vector<vector<int>> res(2, vector<int>(n, 0)); //里面的vector n 个数字都是0
// push_back(ele)	创建新元素再添加
// emplace_back(ele)	直接添加
// pop_back()	删除

vec.resize(n);
```

## unordered_map

```C++
unordered_map<int, int> hashtable;
// erase(key)	删除指定键值对
// count(key)	查找键值是否存在

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

