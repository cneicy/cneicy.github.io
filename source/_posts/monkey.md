title: '[2021-03-26][洛谷]P1125 [NOIP2008 提高组] 笨小猴'
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 10:50:00
---
```cpp
#include<iostream>
#include<string>
#include<cmath>
using namespace std;
int maxn,minn=1e9,x;
int a[26];bool flag;
int main(){
    string s;cin>>s;
    int len=s.length();
    for(int i=0;i<len;i++){
        a[s[i]-'a']++;
    }
    for(int i=0;i<=25;i++)
    {
        if(a[i]!=0&&a[i]>maxn)
        {
            maxn=a[i];
        }
        if(a[i]!=0&&a[i]<minn)
        {
            minn=a[i];
        }
    }
    int ans=maxn-minn;
    if(ans==0||ans==1)
    {
        cout<<"No Answer"<<endl;
        cout<<0<<endl;return 0;
    }
    for(int i=2;i<=sqrt(ans);i++)
    {
        if(ans%i==0)
        {
            flag=1;break;
        }
    }
    if(flag==0)
    {
        cout<<"Lucky Word"<<endl;
        cout<<ans<<endl;
    }
    return 0;
}
```