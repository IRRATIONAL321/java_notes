# stack
+ push
+ pop
+ isEmpty
+ size
+ peek
## Node  
```java
public class Node {
	Object ele;
	Node next;
	Node(Object ele)
	{
		this.ele=ele;
	}
	public Node(Object ele,Node next)
	
	{
		this.ele=ele;
		this.next=next;
	}

}
```  
## StackClass Using LinkedList
```java 
public class Stack {
    Node head;
    int count=0;
    public void push(Object ele)
    {
        Node n=new Node(ele);
        if (head == null) {
            head=n;
            count++;
            return;
        }
        n.next=head;
        head=n;
        count++;
    }
    public int size()
    {
        return count;
    }
    public boolean isEmpty()
    {
        return count==0;
    }
    public Object peek(){
        return head.ele;
    }
    public Object pop()
    {
        if(head==null)
        {
            throw new IndexOutOfBoundsException();
        }
        Object key=head.ele;
        head=head.next;
        count--;
        return key;
    }
}
```
## Stack using ArrayList
```java
public class StackArrayList {
    Object[]o=new Object[10];
    int count=0;
    public void push(Object ele)
    {
        if (count == o.length) {
            increase();
        }
        o[count]=ele;
        count++;
    }
    public void increase()
    {
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
    public boolean inEmpty(){
        return count==0;
    }
    public Object peek()
    {
        return o[count-1];
    }
    public Object pop(){
        if (count == 0) {
            throw new EmptyStackException();
        }
        Object key=o[count-1];
        o[count-1]=null;
        count--;
        return key;
    }
}
```

