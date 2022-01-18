---
title: 算法研究之快速排序
date: 2021-8-20 19:10:00
tags:
- 编程
- 算法
---
# 十大排序算法之快速排序

## 特性（雾）
时间复杂度 O(n log n)
不稳定 

## 原理 
一个数组，把第一个值设置为基础值，然后设置两个变量x，y。x在开头，y在结尾，x递加，找到比基础值大的数就和y换，y递减，进行同样的操作。
一个嵌套循环下来，基础值左面的都比基础值小，右面则反之。

看图![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1629458370000.png)
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1629458386000.png)
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1629458400000.png)
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1629458413000.png)
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1629458428000.png)
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1629458448000.png)
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1629458466000.png)
![](https://cdn.jsdelivr.net/gh/JesseJeson/file@master/1629458479000.png)

## 代码
```
#include <iostream>
#include <cstdlib>
#include <cstdio>
#include <cmath>
#include <ctype.h>
#include <cstring>
#include <algorithm>

using namespace std;

void Quick_sort(int lp[],int start , int over)
{
	if(start < over)
	{
		int x = start;
		int y = over;
		int key = lp[start];
		while(x < y)
		{
			while(x < y && lp[y] >= key)
			{
				y--;
			}
			lp[x] = lp[y];
			
			while(x < y && lp[x] <= key)
			{
				x++;
			}
			lp[y] = lp[x];
		}
		lp[x] = key;
		Quick_sort(lp , start , x - 1);
		Quick_sort(lp , x + 1,over);
	}
	return;
}

int main()
{
	int n = 0;
	cin >> n;
	int *lp = new int [n];
	for(int i = 0;i < n;i++)
	{
		cin >> lp[i];
	}
	Quick_sort(lp , 0 , n - 1);
	for(int i = 0;i < n;i++)
	{
		cout << lp[i] << " ";
	}
	delete []lp;
	return 0;
}
```
