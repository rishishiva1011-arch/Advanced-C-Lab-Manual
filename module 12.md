# EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display stack elements using linked list.

## Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
## Program:

```
struct Node   
{  
int data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *ptr;  
    ptr=head;  
    while(ptr!=NULL)  
    {  
        printf("%d\n",ptr->data);  
        ptr=ptr->next;  
    }  
}  
```

## Output:

<img width="164" height="196" alt="image" src="https://github.com/user-attachments/assets/1bbb064e-f8b3-4845-895c-49e9eb4e2412" />



## Result:
Thus, the program to display stack elements using linked list is verified successfully. 



# EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
## Aim:
To write a C program to pop an element from the given stack using liked list.

## Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
## Program:

```
struct Node
{
char data;
struct Node *next;
}*head;
void pop()
{
     struct Node *temp;
     if(head==NULL){
        printf("stack is empty");
     }else{
       temp=head;
       head=head->next;
       free(temp);
}
}
```

## Output:

<img width="407" height="256" alt="image" src="https://github.com/user-attachments/assets/7e8b6c72-23b2-43d5-b855-fdb559cf5978" />


## Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
# EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display queue elements using linked list.
## Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
## Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
   if(front==NULL)
   {
      printf("queue is empty\n");
   }
   else
   {
      printf("queue elements:\n");
      struct Node *temp=front;
      while(temp->next!=NULL)
      {
          printf("%0.2f\n",temp->data);
          temp=temp->next;
      }
      printf("%0.2f\n",temp->data);
   }
}
```

## Output:

<img width="265" height="221" alt="image" src="https://github.com/user-attachments/assets/0d2bcc36-0465-47d6-8832-64c9c5147ee5" />


## Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
# EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

## Aim:
To write a C program to insert elements in queue using linked list

## Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
## Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
   struct Node *newnode=(struct Node*)malloc(sizeof(struct Node));
   newnode->data=data;
   newnode->next=NULL;
   if(front==NULL&&rear==NULL){
   front=rear=newnode;
}else{
   rear->next=newnode;
   rear=newnode;
}
}
```

## Output:

<img width="266" height="220" alt="image" src="https://github.com/user-attachments/assets/c86c2d19-8f95-486d-a22e-90e1463fe483" />


## Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



# EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


## Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

## Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

## Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%.2f",front->data);
}
```
## Output:

<img width="196" height="232" alt="image" src="https://github.com/user-attachments/assets/cba73817-7b9c-4bde-81d6-fda8a5647694" />




## Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


