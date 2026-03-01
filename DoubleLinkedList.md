# DoubleLinkedList  
![DLL1.png](DLL1.png)
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
