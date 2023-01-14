title: '[2021-03-22]字符串练习'
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 10:49:00
---
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
    string s;
    int cnt=0;
    getline(cin,s);
    int len=s.length();
    for(int i=0;i<len;i++)
    {
        if(s[i]>='0'&&s[i]<='9'||s[i]>='a'&&s[i]<='z'||s[i]>='A'&&s[i]<='Z')
        cnt++;
    }
    cout<<cnt;
    return 0;
}
```