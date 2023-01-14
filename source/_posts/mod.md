title: '[2021-05-14]模公式'
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 10:54:00
---
```cpp
#include<iostream>
using namespace std;
int main(){
    int a=5,b=7,k=3;
    cout<<(a*b)%k<<"///"<<((a%k)*(b%k))%k;
    cout<<(a+b)%k<<"///"<<((a%k)+(b%k))%k;
}
```