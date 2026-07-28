# EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
## Aim:
To write a C program to search a given element in the given linked list.

## Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
## Program:

```
struct Node
{
    char data;
    struct Node *next;
}*head;
void search(char data)
{
   struct Node *temp;
   temp=head;
   int loc=1,flag=0;
       while(temp!=NULL)
       {
          if(temp->data == data)
          {
              flag=1;
              break;
          }
          else
          {
              temp=temp->next;
              loc++;
          }
       }  
}
if(flag==0)
{
    printf("Item not found");
}
else
{
    printf("item %c found at location %d",data,loc);
}
}
```

## Output:

<img width="1371" height="834" alt="image" src="https://github.com/user-attachments/assets/b60feec7-497b-4cbb-8aa1-070a9582a97c" />



## Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
# EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
## Aim:
To write a C program to insert a node in a linked list.
## Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
## Program:

```
struct Node{
    int data;
    struct Node *next;
}*head;
void insert(int data)
{
     struct Node *newnode,*temp;
     newnode=(struct Node *)malloc(sizeof(struct Node));
     newnode->data=data;
     newnode->next=NULL;
     if(head==NULL)
     {
       head=newnode;
     }
     else
     {
       temp=head;
       while(temp->next != NULL)
       {
            temp=temp->next;
       }
       temp->next=newnode;
     }
}
```

## Output:

<img width="855" height="882" alt="image" src="https://github.com/user-attachments/assets/a6cbd1d7-82bc-4cd1-a5b1-f917ffe960e2" />


 
## Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
# EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
## Aim:
To write a C program to traverse a doubly linked list.

## Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
## Program:

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head;
void display()
{
    struct Node *temp=head;
    while(temp!=NULL)
    {
        printf("%c ",temp->data);
        temp=temp->next;
    }
}
```

## Output:

<img width="687" height="885" alt="image" src="https://github.com/user-attachments/assets/7f97b410-1dca-4cd5-854e-40109af153de" />


## Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



# EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
## Aim:
To write a C program to insert an element in doubly linked list

## Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
## Program:

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;
void insert(int data)
{
    struct Node *temp,*newnode=(struct Node*)malloc(sizeof(struct Node));
    newnode->data=data;
    newnode->next=NULL;
    newnode->prev=NULL;
if(head==NULL)
{
    head=newnode;
}
else
{
   temp=head;
   while(temp->next!=NULL)
   {
    temp=temp->next;
   }
temp->next=newnode;
newnode->prev=temp;
}
}
```

## Output:

<img width="855" height="882" alt="image" src="https://github.com/user-attachments/assets/ae68a723-6006-49b7-8dda-c8c77b0cae76" />



## Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




# EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




## Aim:
To write a C function that deletes a given element from a linked list.

## Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


## Program:

```
struct Node
{
    struct Node *next;
    int data;
}*head;
void delete(int data) {
    struct Node *current, *prev;

    if (head == NULL) {
        printf("List is empty\n");
        return;
    }

    if (head->data == data) {
        current = head;
        head = head->next;
        free(current);
        printf("Element %d deleted\n", data);
        return;
    }

    prev = head;
    current = head->next;
    while (current != NULL) {
        if (current->data == data) {
            prev->next = current->next;
            free(current);
            printf("Element %d deleted\n", data);
            return;
        }
        prev = current;
        current = current->next;
    }

    printf("Element %d not found in the list\n", data);
}
```

## Output:

<img width="456" height="426" alt="image" src="https://github.com/user-attachments/assets/05f8ddb1-e533-4a55-a446-692e609d02ac" />

<br>
<br>

<img width="909" height="402" alt="image" src="https://github.com/user-attachments/assets/9b54c30f-eefb-4ed1-a653-aa27817870a2" />



## Result:

Thus, the function that deletes a given element from a linked list is verified successfully.





