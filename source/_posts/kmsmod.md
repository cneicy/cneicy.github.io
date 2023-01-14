title: '[2021-05-14]P1226 快速幂取余'
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 10:56:00
---
```cpp
#include<iostream>
using namespace std;
int b,p,k;
long long ksm(long long a,int b,int k)
{
    long long s=1;
    while(b>0)
    {
        if(b%2==1)
        {
            s=(s%k)*(a%k)%k;
        }
        b=b/2;
        a=(a%k)*(a%k)%k;
    }
    return s;
}
int main()
{
    cin>>b>>p>>k;
    if(p==0){
        cout<<b<<"^"<<p<<" mod "<<k<<"="<<1%k;
    }else{
        cout<<b<<"^"<<p<<" mod "<<k<<"="<<ksm(b,p,k);
    }
    return 0;
}
```