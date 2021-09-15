---
title: DP
categories:
  - ACM
  - 模板
---






### 状压DP

- 枚举子集

  ``` cpp
  for(int S1 = S: S1 != 0; S1 = (S1 - 1) & S)
  {
      S2 = S ^ S1;
  }
  ```

  $S1$ 是 $S$ 的所有按二进制从大到小顺序枚举的子集. $S2$ 是补集.

- 枚举 $n$ 元集合的 $k$ 元子集

  ``` cpp
  void GospersHack(int k, int n)
  {
      int cur = (1 << k) - 1;
      int limit = (1 << n);
      while (cur < limit)
      {
          int lb = cur & -cur;
          int r = cur + lb;
          cur = ((r ^ cur) >> __builtin_ctz(lb) + 2) | r;  // __builtin_ctz 判断末尾0的个数
      }
  }
  ```

  







### SOS DP

有重叠枚举子集	





``` cpp
```

