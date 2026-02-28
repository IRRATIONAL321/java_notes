```java
public class ArrayList {

	Object []o=new Object[10];
	int count=0;
	public void add(Object ele)
	{
		if(count>=o.length)
			increase();
		o[count++]=ele;
	}
	public void increase() {
		Object []a=new Object[o.length+5];
		for(int i=0;i<o.length;i++)
		{
			a[i]=o[i];
			
		}
		o=a;
	}
	public int size()
	{
		return count;
	}
	public void addIndex(Object ele,int index) {
		if(index<0 ||index >=size())
			throw new IndexOutOfBoundsException();
		for(int i=size()-1;i>index;i--)
		{
			o[i+1]=o[i];
		}
		o[index]=ele;
		count++;
		
	}
	public void remove(int index)
	{
		if(index<0||index>size())
			throw new IndexOutOfBoundsException();
		for(int i=index;i<size();i++)
		{
			o[i]=o[i+1];
			
		}
		o[size()-1]=null;
		count--;
	}
	public void set(Object ele,int index)
	{
		if(index<0||index>size())
			throw new IndexOutOfBoundsException();
		o[index]=ele;
	}
	public boolean contains(Object ele)
	{
		for(int i=0;i<size();i++)
		{
			if(o[i]==ele)
				return true;
		}
		return false;
	}
}
```
