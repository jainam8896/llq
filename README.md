import java.util.*;

public class llq {

        node head;

        static Scanner sc = new Scanner(System.in);

        class node{

             

            int data;

            node next;

            

            node()

            {

                System.out.println("Enter The Data:-");

                data=sc.nextInt();

                next=null;

            }

        }

        

        public void enq()

        {

            node nn = new node();

            if(head==null)

            {

                head=nn;

                return;

            }

            node temp=head;

            while(temp.next!=null)

            {

                temp=temp.next;

            }

            temp.next=nn;

        }

        

        public void deq()

        {

            if(head==null)

            {

                System.out.println("Q Is Empty");

                return;

            }

            System.out.println("Delete Element Is "+head.data);

            head = head.next;

        }

        

        public void display()

        {

            if(head==null)

            {

                System.out.println("Q Is Empty");

                return;

            }

            node temp=head;

            while(temp.next!=null)

            {

                System.out.print("<-"+temp.data);

                temp=temp.next;

            }

            

        }

        

        public static void main(String[] args) {

        

            llq ob = new llq();

            int ch;

            do{

                System.out.println("\nOperation");

                System.out.println("\n1.Enq");

                System.out.println("\n2.Dq");

                System.out.println("\n3.Display");

                System.out.println("\nEnter Your Choice");

                ch=sc.nextInt();

                

                switch(ch)

                {

                    case 1:

                        ob.enq();

                        break;

                        

                    case 2:

                        ob.deq();

                        break;

                        

                    case 3:

                        ob.display();

                        break;

                        

                    case 4:

                        System.out.println("\nExit");

                        break;

                        

                    default:

                        System.out.println("\nInvalid Choice");

                        break;

                }

            }while(ch!=4);

    }

}
