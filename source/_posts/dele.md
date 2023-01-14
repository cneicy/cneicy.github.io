title: '[2021-03-31]高精度减法'
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 10:51:00
---
```cpp
#include<iostream>
#include<string>
using namespace std;
string a,b;
int z[11001],d[11001],c[11001];
int main()
{
    cin>>a>>b;
    int len1=a.length(),len2=b.length();
    if(len1<len2)
    {
        cout<<"-";swap(a,b);swap(len1,len2);
    }
    else
    {
        if(len1==len2)
        {
            if(a<b)
            {
                cout<<"-";swap(a,b);swap(len1,len2);
            }
        }
    }
    for(int i=0;i<len1;i++)
    {
        z[len1-i]=a[i]-'0';
    }
    for(int i=0;i<len2;i++)
    {
        d[len2-i]=b[i]-'0';
    }
    for(int i=1;i<=len1;i++)
    {
        c[i]=z[i]-d[i];
        if(c[i]<0)
        {
            c[i]=c[i]+10;
            c[i+1]-=1;
        }
    }
    while(c[len1]==0&&len1>1) len1--;
    for(int i=len1;i>=1;i--)
    {
        cout<<c[i];
    }
    return 0;
}
```