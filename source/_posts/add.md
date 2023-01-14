title: '[2021-03-19]C++高精加法'
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 10:48:00
---
在老师电脑上敲代码的感觉好奇怪哦。（
```cpp
#include<iostream>
#include<string>
using namespace std;
int a[10001],b[10001],c[10001];
int main()
{
    string s1,s2;
    cin>>s1>>s2;
    int len1=s1.length(),len2=s2.length();
    for(int i=0;i<len1;i++)
    {
        a[len1-i]=s1[i]-'0';
    }
    for(int i=0;i<len2;i++)
    {
        b[len2-i]=s2[i]-'0';
    }
    int len=max(len1,len2);
    for(int i=1;i<=len;i++)
    {
        c[i]=a[i]+b[i];
        c[i+1]+=c[i]/10;
        c[i]%=10;
        if(c[len+1]>0) len++;
    }
    for(int i=len;i>=1;i--)
    {
        cout<<c[i];
    }
    return 0;
}
```