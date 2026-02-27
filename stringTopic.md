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