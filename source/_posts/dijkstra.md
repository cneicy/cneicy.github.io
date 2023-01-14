title: dijkstra +
author: Eicy
tags:
  - 算法
categories:
  - 编程
date: 2023-01-14 11:02:00
---
```cpp
#include<iostream>
#include<queue>
using namespace std;
const int maxn=100007;
int first[maxn],next[maxn<<1],to[maxn<<1],tot,val[maxn<<1];
long long dis[maxn];
bool vis[maxn];
int n,m,s;
void add(int x,int y,int z)
{
    next[++tot]=first[x];
    first[x]=tot;
    to[tot]=y;
    val[tot]=z;
}
struct node
{
    int p,d;
    bool operator<(const node &a) const
    {
        return d>a.d;
    }
};
priority_queue<node>q;
void dijkstra(int s)
{
    dis[s]=0;
    q.push((node){s,0});
    while(!q.empty())
    {
        int a=q.top().p;
        q.pop();
        if(vis[a]==1) continue;
        vis[a]=1;
        for(int i=first[a];i;i=next[i])
        {
            int v=to[i];
            if(vis[v]==0&&dis[v]>dis[a]+val[i])
            {
                dis[v]=dis[a]+val[i];
                q.push((node){v,dis[v]});
            }
        }
    }
}
int main()
{
    cin>>n>>m>>s;
    for(int i=1;i<=n;i++) dis[i]=1e12;
    for(int i=1;i<=m;i++)
    {
        int x,y,z;cin>>x>>y>>z;
        add(x,y,z);
    }
    dijkstra(s);
    for(int i=1;i<=n;i++)
    cout<<dis[i]<<" ";
    return 0;
}
```