title: '[2021-07-05]floyed'
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 11:01:00
---
```cpp
0 3 4 
5 0 8
3 2 0
g[1][2]=3

for(int i=1;i<=n;i++)
{
    for(int j=1;j<=n;j++)
    {
        for(int k=1;k<=n;k++)
        {
            if(i!=j&&i)
            {
                if(f[i][j]>g[i][k]+g[k][j])
                {
                    f[i][j]=g[i][k]+g[k][j];
                }
            }
        }
    }
}
```