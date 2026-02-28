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
Max ele ,min ele in 2D array.
  
  ```java
  public void maxminElemenst(int[][]a)
	{
		int max=a[0][0];
		int min=a[0][0];
		for(int i=0;i<a.length;i++)
		{
			for(int j=0;j<a[i].length;j++)
			{
				if(a[i][j]>max)
					max=a[i][j];

				if(a[i][j]<min)
					min=a[i][j];
			}
		}
		System.out.println("max="+max);
		System.out.println("min="+min);
	}
```
Pascal number  
```java
public class pascal {
	public static void ispascal(int [][]a)
	{
		for(int i=0;i<a.length;i++)
		{
			a[i]=new int[i+1];
			for(int j=0;j<a[i].length;j++)
			{
				if(j==0||i==j)
				{
					a[i][j]=1;
				}
				else
					a[i][j]=a[i-1][j-1]+a[i-1][j];
			}
		}
	}

	public static void main(String[] args) {
		int n=7;
		int space=n-1;
		int [][]a=new int[n][];
		ispascal(a);
		for(int i=0;i<a.length;i++)
		{
			for(int j=1;j<=space;j++)
				System.out.print(" ");
			for(int k=0;k<a[i].length;k++)
			{
				System.out.print(a[i][k]+"  ");
			}
			System.out.println();
			space--;
		}

	}

}
```
TransposeMatrix  
```java
public static void main(String[] args) {
		
		int [][]a= {{1,2,3},
					{4,5,6},
					{7,8,9}};
		int [][]b=new int[a.length][a.length];
		for(int i=0;i<a.length;i++)
		{
			for(int j=0;j<a.length;j++)
			{
				b[i][j]=a[j][i];
			}
		}
		for(int i=0;i<a.length;i++)
		{
			for(int j=0;j<a.length;j++)
			{
				System.out.print(b[i][j]+" ");;
			}
			System.out.println();
		}
		
	}
```
Print the sum of two diagonals of a matrix.  
```java
public static void main(String[] args) {
		
		int [][]a= {{1,2,3},
					{4,5,6},
					{7,8,9}};
		int sum=0;
		for(int i=0;i<a.length;i++)
		{
			for(int j=0;j<a.length;j++)
			{
				if(i==j||i+j==a.length-1)
					sum+=a[i][j];
			}
		}
		System.out.println(sum);
	}
```

Spiral Matrix
```java 
public static void main(String[] args) {
		int n=5;
		int row=0;
		int col=-1;
		char dir='r';
		int [][] a=new int [n][n];
		for(int i=1;i<=n*n;i++)
		{
			switch(dir) {
			case 'r':
			{
				col++;
				a[row][col]=i;
				if(col==a.length-1||a[row][col+1]!=0)
				{
					dir='d';
				}
			}
			break;
			case 'd':
			{
				row++;
				a[row][col]=i;
				if(row==a.length-1||a[row+1][col]!=0)
				{
					dir='l';
				}
			}
			break;
			case 'l':
			{
				col--;
				a[row][col]=i;
				if(col==0||a[row][col-1]!=0)
				{
					dir='u';
				}
			}
			break;
			case 'u':
			{
				row--;
				a[row][col]=i;
				if(a[row-1][col]!=0)
				{
					dir='r';
				}
			}
			break;
			}
		}
		for(int[]m:a)
		{
			for(int num:m)
				System.out.print(num+"\t");
			System.out.println();
		}
		

	}
```
Matrix multipication
```java
public static void main(String[] args) {
		
		int [][]a= {{1,2,3},
					{3,2,1},
					{1,2,1}};
		int [][]b= {{1,3,1},
					{2,2,1},
					{1,6,1}};
		int [][]c=new int[a.length][a.length];
		for(int i=0;i<a.length;i++)
		{
			for(int j=0;j<a[i].length;j++)
			{
				for(int k=0;k<a[i].length;k++)
				{
					c[i][j]+=a[i][k]*b[k][j];
				}
			}
		}
		for(int[]m:c)
		{
			for(int num:m)
				System.out.print(num+" ");
			System.out.println();
		}
		
	}
```
