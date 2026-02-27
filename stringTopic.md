```java 
public class demo1{

	public static void main(String[] args) {
		
		String s1=new String("abc");
		System.out.println(s1);
		String s2="abc";
		System.out.println(s2);
		System.out.println(s1==s2);//false
		System.out.println(s1.equals(s2));//true
	}

}
```
## String methods
|return type|method|
|--------|---------------|
|int|length|
|char|charAt(int index)|
|int|indexOf(char c)//return -1 if not available,-1 posi if multiple|
|int|indexOf(char c,int startsearch)|
|int|indexOf(String s,int startsearch)|
|int|lastIndexOf(char c)|
|int|lastIndexOf(String s)|  
  
  ```java
  public static void main(String[] args) {
		
		String s1="javadeveloper";
		System.out.println(s1.length());//13
		System.out.println(s1.charAt(5));//e
		System.out.println(s1.indexOf('e'));//5
		System.out.println(s1.indexOf("dev"));//4
		System.out.println(s1.indexOf("ab"));//-1
		System.out.println(s1.indexOf('e',8));//11
		System.out.println(s1.lastIndexOf('a'));//3
	}
```
```java
char[]a=s1.tocharArray();
		for(char c:a)
		{
			System.out.println(c);
		}
```
## Immutable
1.String is immutable type  
2.Once the String obj is created the same obj value cant be changed  
3.If we try to change String obj, a new obj will be created and returned  

 	