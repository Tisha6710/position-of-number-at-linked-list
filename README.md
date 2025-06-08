# position-of-number-at-linked-list
I have make a  program to insert element at start and end.
package LinkedList;

public class insertelementatstart {
    public static class Node{
        int data;
        Node next;
        Node(int data){
            this.data=data;
        }
    }
    public static class linkedlist {
        Node head = null;
        Node tail = null;

        void insertAtEnd(int val) {
            Node temp = new Node(val);
            if (head == null) {
                head = temp;
                tail = temp;
            } else {
                tail.next = temp;
                tail = temp;
            }
        }

        void insertAtHead(int val) {
            Node temp = new Node(val);
            if (head == null) { //empty list
               head=tail=temp;
        }
        else{ //non empty list
            temp.next=head;
            head=temp;

        }
            System.out.println();
    }
        void display(){
            Node temp=head;
            while(temp!=null){
                System.out.println(temp.data+" ");
                temp=temp.next;

            }

        }
        int size() {
            Node temp=head;
            int count=0;
            while(temp!=null){
                count++;
                temp=temp.next;
            }
            return count;
        }
    }
    public static void main(String[] args) {
        linkedlist ll=new linkedlist();
        ll.insertAtEnd(4); //4
ll.display();
        ll.insertAtEnd(5);
        ll.display();
        ll.insertAtEnd(12);
        ll.display();
ll.insertAtHead(13); //13-4-5
        ll.display();
        System.out.println(ll.size());
    }
}

