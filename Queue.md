## Node
```java
public class Node {
Object ele;
Node next;
Node(Object ele)
{
this.ele=ele;
}
public Node(Object ele, Node next)

    {
        this.ele=ele;
        this.next=next;
    }
}
```
## Queueclass
```java
public class Queue {
    Node head;
    int count=0;
    public void add(Object ele)
    {
        Node n=new Node(ele);
        if (head == null) {
            head=n;
            count++;
            return;
        }
        Node curr=head;
        while (curr.next != null) {
            curr=curr.next;
        }
        curr.next=n;
        count++;
    }
    public int size(){
        return count;
    }
    public boolean isEmpty()
    {
        return count==0;
    }
    public Object peek(){
        return head.ele;
    }
    public Object poll(){
        Object key=head.ele;
        head=head.next;
        count--;
        return key;
    }
}

```
## Queue using ArrayList

```java
public class QueueArrayList {
    Object []o=new Object[10];
    int count=0;
    public void add(Object ele)
    {
        if(o.length==size())
        {
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
    public int size(){
        return count;
    }
    public boolean isEmpty()
    {
        return size()==0;
    }
    public Object peek(){
        return  o[0];
    }
    public Object poll(){
        Object key=o[0];
        for(int i=0;i<o.length-1;i++)
        {
            o[i]=o[i+1];
        }
        return key;
    }

}

```


