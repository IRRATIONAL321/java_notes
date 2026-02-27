# 2-D Array  
datatype[][]ref=new datatype[row][col]  
int[][] a=new int[3][3]  
  
Sop(a[0])  print the first array address  
```java
public static void main(String[] args) {
		int [][]a=new int [2][2];
		a[0][0]=10;
		a[0][1]=20;
		a[1][0]=30;
		a[1][1]=40;
		
		for(int i=0;i<a.length;i++)
		{
			for(int j=0;j<a.length;j++)
			{
				System.out.print(a[i][j]+" ");
			}
			System.out.println();
		}
		
	}
```
In 2D array rowcount and colcount is different then the array is called as `jagged` array  
```java
int [][]a=new int[3][];
	a[0]=new int[1];
	a[1]=new int[3];
	a[2]=new int[2];
	
	a[0][0]=10;
	a[1][0]=20;
	a[1][1]=30;
	a[1][2]=40;
	a[2][0]=50;
	a[2][1]=60;
	
	for(int i=0;i<a.length;i++)
	{
		for(int j=0;j<a[i].length;j++)
		{
			System.out.print(a[i][j]+" ");
		}
		System.out.println();
	}

}  

10 
20 30 40 
50 60 
```
int [][] a={{1,2,3},{4,5,6}};  
```java
public static void main(String []args) {
	int [][] a= {{1,2,3},
				{4,5,6},
				{8,9,10}};
	for(int[]n:a)
	{
		System.out.println(Arrays.toString(n));
	}


[1, 2, 3]
[4, 5, 6]
[8, 9, 10]
```
Print even number in given 2D array.
```java
for(int i=0;i<a.length;i++)
	{
		for(int j=0;j<a[i].length;j++)
		{
			if(a[i][j]%2==0)
				System.out.println(a[i][j]);
		}
	}
```
