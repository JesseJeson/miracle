---
title: st表代码
date: 2022-1-18 11:15:56
tags:
- 编程
- 代码
---
```
#include<iostream>
#include<cstdio>
#include<cstdlib>
#include<algorithm>
#include<cmath>

using namespace std;

const int N = 200010,M = 18;
int st[N][M];
int w[N];
int n,m;

void init()
{
    for(int j = 0;j < M;j++)
    {
        for(int i = 1;i + (1 << j) - 1 <= n;i++)
        {
            if(j == 0)
            {
                st[i][j] = w[i];
            }
            else
            {
                st[i][j]=max(st[i][j - 1],st[i + (1 << (j - 1))][j - 1]);
            }
        }
    }
}

int query(int l ,int r)
{
    int k = log2(r-l+1);
    return max(st[l][k],st[r - (1 << k) + 1][k]);
}

int main()
{
    cin >> n;
    for(int i = 1;i <= n;i++) scanf("%d",&w[i]);
    
    init();
    
    cin >> m;
    while(m--)
    {
        int l,r;
        cin >> l>>r;
        cout << query(l,r) << endl;
    }
    return 0;
}
```