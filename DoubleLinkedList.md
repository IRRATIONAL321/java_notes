# DoubleLinkedList  
![DLL1.png](DLL1.png)
## Node
```java
public class Node {
    Object ele;
    Node next;
    Node prev;
    Node(Object ele)
    {
        this.ele=ele;

    }

    public Node(Node prev, Node next, Object ele) {
        this.prev = prev;
        this.next = next;
        this.ele = ele;
    }
}
```
# DoublyLinkedList  
```java
public class DoublyLinkedList {
    Node head;
    int count=0;
    Node tail;
    public void add(Object ele)
    {
        Node n=new Node(ele);
        if(head==null)
        {
            head=n;
            count++;
            tail=head;
            return ;
        }
        Node curr=head;
        while (curr.next != null) {
            curr=curr.next;
        }
        curr.next=n;
        n.prev=curr;
        tail=n;
        count++;
    }
    public int size(){
        return count;
    }
    public boolean isEmpty()
    {
        return count==0;
    }
    public void display(){
        Node curr=head;
        while (curr != null) {

            System.out.println(curr.ele);
            curr=curr.next;
        }

    }
    public void revdisplay(){
        Node curr=tail;
        while (curr != null) {

            System.out.println(curr.ele);
            curr=curr.prev;
        }
    }
    public boolean contains(Object ele)
    {
        Node curr=head;
        while (curr != null) {
            if(curr.ele.equals(ele))
                return true;
            curr=curr.next;
        }
        return false;
    }
    public void addIndex(Object ele,int index)
    {
        if (index < 0 || index > size()) {
            throw new IndexOutOfBoundsException();

        }
        if(index==0)
        {
            addFirst(ele);
        }
        if(index==size())
        {
            addLast(ele);
        }
        Node n=new Node(ele);
        Node curr=head;
        for(int i=1;i<index;i++)
        {
            curr=curr.next;
        }
        n.next=curr.next;
        n.prev=curr;
        curr.next.prev=n;
        curr.next=n;
        count++;
    }
    public void addLast(Object ele)
    {
        Node n=new Node(ele);
        tail.next=n;
        tail=n;
        count++;
    }
    public void addFirst(Object ele)
    {
        Node n=new Node(ele);
        n.next=head;
        head=n;
        count++;
    }
    public void removeFirst()
    {
        head=head.next;
        head.prev=null;
        count--;
    }
    public void remove(int index)
    {
        if(index<0||index>=size())
        {
            throw new IndexOutOfBoundsException();
        }
        if(index==0)
        {
            removeFirst();
        }
        if (index == size() - 1) {
            removeLast();
            return;
        }
        Node curr=head;
        for(int i=1;i<index;i++)
        {
            curr=curr.next;
        }
        curr.next.next.prev=curr;
        curr.next=curr.next.next;
        count--;
    }
    public void removeLast(){
        tail=tail.prev;
        tail.next=null;
        count--;
    }




}
```
