# EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

### Aim:
To write a C program to display stack elements using an array.
### Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
### Program:

```
void display() {
    if (top == -1) {
        printf("Stack is empty\n");
        return;
    }
    for (int i = top; i >= 0; i--) {
        printf(" %d \n", stack[i]);
    }
}
```

### Output:

<img width="675" height="883" alt="Screenshot 2026-07-29 035011" src="https://github.com/user-attachments/assets/a07a85ea-895f-4f65-b71f-a660250886c3" />


### Result:
Thus, the program to display stack elements using an array is verified successfully.
 

# EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
### Aim:
To create a C program to push the given element in to a stack using array.
### Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
### Program:

```
void push (float data)
{
    if (top == size-1 )
    {
    printf("stack is full\n");
    }
    else
    {
        top = top +1;
        stack[top] = data;
    }
}
```

### Output:

<img width="705" height="882" alt="image" src="https://github.com/user-attachments/assets/3c8ada45-2f06-417b-bf31-38a4e1e3766d" />


### Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
# EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
### Aim:
To write a C program to display queue elements using array

### Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
### Program:

```
void display()
{
    int i=1;
    if(front==-1||front>rear)
    printf("No elements to display\n");
    else
    {
        for(i=front;i<=rear;i++)
        {
            printf("%c ", queue[i]);
        }
    }
}
```

### Output:

<img width="1251" height="882" alt="image" src="https://github.com/user-attachments/assets/c59afa2f-097e-4056-84a8-166b7e16ea61" />


### Result:
Thus, the program to display queue elements using array is verified successfully.


 
# EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
### Aim:
To write a C program to insert elements in queue using array.

### Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

### Program:

```
void enqueue(float data)
{
    if (rear<size-1)
    {
        if(front==-1)
        front=0;
        rear+=1;
        queue[rear]=data;
    }
}
```

### Output:

<img width="1335" height="1584" alt="image" src="https://github.com/user-attachments/assets/03a3c8c5-49f0-4a0c-b495-e34daf4fee97" />


### Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
# EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



### Aim:

To create a function in C that deletes an element from a queue implemented using an array.

### Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.               
4.	End the Function.



### Program:

```
void deque() {
    if (front == -1) {
        printf("Queue is empty\n");
        return;
    }
    front++;
    if (front > rear) {
        front = rear = -1;
    }
}
```

### Output:

<img width="1332" height="1116" alt="image" src="https://github.com/user-attachments/assets/d6d35874-cd4e-495c-bc50-cd25d6a70626" />



### Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
