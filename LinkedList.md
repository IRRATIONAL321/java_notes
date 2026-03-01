# Node
+ Container
+ value.next Node add  
![alt text](Singlelinkedlist.png)
## Node class  
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
## LinkedList  
```java
public class LinkedList {
	Node head;
	int count=0;
	public void add(Object ele)
	{
		Node n=new Node(ele);
		if(head==null) {
			head=n;
			count++;
			return;
		}
		Node curr=head;
		while(curr.next!=null)
		{
			curr=curr.next;
		}
		curr.next=n;
		count++;
	}
	public int size()
	{
		return count;
	}
	public void display()
	{
		Node curr=head;
		while(curr!=null)
		{
			System.out.println(curr.ele);
			curr=curr.next;
		}
	}public void addIndex(Object ele,int index)
    {
        if(index<0||index>size())
            throw new IndexOutOfBoundsException();
        if(index==0)
        {
            addFirst(ele);
            return ;
        }

        Node n=new Node(ele);
        Node curr=head;
        for(int i=1;i<index;i++)
        {
            curr=curr.next;
        }
        n.next=curr.next;
        curr.next=n;
        count++;

    }
    public void addFirst(Object ele)
    {
        Node n=new Node(ele);
        n.next=head;
        head=n;
        count++;
    }

}
```
