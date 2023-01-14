title: '[2021-03-27]P1957 口算练习题'
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 10:51:00
---
```cpp
include<iostream>
include<string>
using namespace std;
int i,z,c[100];bool flag;
int main(){

cin>>i;
string m;
for(int j=1;j<=i;j++){
    getline(cin,m);
    for(int i=0;i<m.length();i++){
        if(m[i]==' ') z++;
    }
    for(int j=0;j<m.length();j++){
        if(z=2&&m[j]!=' ') {
            c[j]=m
        }
    }
    
    
}
}
```