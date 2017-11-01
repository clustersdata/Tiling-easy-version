# Tiling-easy-version

Tiling easy version

Problem Description

有一个大小是 2 x n 的网格，现在需要用2种规格的骨牌铺满，骨牌规格分别是 2 x 1 和 2 x 2，请计算一共有多少种铺设的方法。

Input

输入的第一行包含一个正整数T（T<=20），表示一共有 T组数据，接着是T行数据，每行包含一个正整数N（N<=30），表示网格的大小是2行N列。

Output

输出一共有多少种铺设的方法，每组数据的输出占一行。

Sample Input

3 2 8 12

Sample Output

3 171 2731

代码：

#include<stdio.h>

main()

{

	int t,n,i,a[31];
  
	a[1]=1;
  
	a[2]=3;
  
	for(i=3;i<=31;i++)
  
		a[i]=2*a[i-2]+a[i-1];
    
	scanf("%d",&t);
  
	while(t--)
  
	{
  
		scanf("%d",&n);
    
		printf("%d\n",a[n]);
    
	}
  
}
