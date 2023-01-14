title: '[2021-03-26]质数的简单判断'
author: Eicy
date: 2023-01-14 10:50:34
tags:
---
```cpp
#include<iostream>
#include<string>
#include<cmath>
using namespace std;
int a,g[101];
bool flag;
int main(){    
    cout<<2<<" ";
    for(int i=3;i<=100;i++)
    {
        for(int k=2;k<=sqrt(i);k++)
        {
            if(i%k==0)
            flag=1;
        }
        if(flag==0)
        cout<<i<<" ";
        flag=0;
    }
    return 0;
}
```