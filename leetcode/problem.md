# 经典问题

## 最大公约数

a*b = (a和b的最大公约数) * (a和b的最小公倍数)

可以从：用尽可能大的正方形填补矩形的角度来理解：[辗转相除法介绍 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/324578532)

```c++
int gcd(int a,int b){
    if(a<b) swap(a,b);
    int r=b;
    while(r!=0){
        r=a%b;
        a=b;
        b=r;
    }
    return a;
}
```



# 独立问题

## 众数（多数元素

问题：给定数组，返回数组中出现次数大于$\lfloor n/2 \rfloor$的元素，保证一定有

题解：Boyer-Moore（多数投票算法）；时间复杂度：O(n)；空间复杂度：O(1)

```c++
遍历数组，对数组中元素x，
如果 count 的值为 0，我们先将 x 的值赋予 candidate

如果 x 与 candidate 相等，那么计数器 count 的值增加 1；
如果 x 与 candidate 不等，那么计数器 count 的值减少 1；

返回 candidate
```



