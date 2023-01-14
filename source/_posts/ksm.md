title: '[2021-05-14]快速幂'
author: Eicy
date: 2023-01-14 10:56:04
tags:
---
```cpp
#include<iostream>
using namespace std;
int b,p;
long long ksm(int a,int b)
{
    long long s=1;
    while(b>0)
    {
        if(b%2==1)
        {
            s*=a;
        }
        b=b/2;
        a*=a;
    }
    return s;
}
int main()
{
    cin>>b>>p;
    cout<<ksm(b,p);
    return 0;
}
```