EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

```
float stack[100];
int top;
void display()
{
    if(top==-1)
    {
        printf("Stack is empty\n");
    }
    for(int i=top;i>=0;i--)
    {
        printf("%.1f ",stack[i]);
    }
}
```
Output:

![Screenshot 2025-04-25 220519](https://github.com/user-attachments/assets/8a9804a6-71cc-4e31-961a-8351556cd443)



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
float stack[100];
int size=3,top=1;
void push (float data)
{
    if (top ==size-1 )
    {
        printf("stack is full\n");
    }
    else
    {
        top+=1;
        stack[top] = data;
    }
}
```
Output:

![Screenshot 2025-04-25 220639](https://github.com/user-attachments/assets/ab5dfc55-47b7-41d8-97f5-d91874a8db42)




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
int queue[50];
int rear, front,i;
void display()
{
    if(front==-1||front>rear)
    {
        printf("No elements to display\n");
    }
    else
    {
        for(i=front;i<=rear;i++)
        {
            printf("%d\n",queue[i]);
        }
    }
}
```
Output:

![Screenshot 2025-04-25 220757](https://github.com/user-attachments/assets/e74599b6-66b7-4856-abda-081017758c57)


Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
float queue[50];
int front=-1,rear=-1;
int size=10;
void enqueue(float data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear=rear+1;
        queue[rear]=data;
    }
}
```
Output:
![Screenshot 2025-04-25 220920](https://github.com/user-attachments/assets/674599b0-92d1-422e-8787-12c7eba2d773)


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
```
int queue[50];
int front, rear;
void dequeue()
{
    if(front==-1||front>rear)
    {
        printf("No elements to display");
    }
    else
    {
        front=front+1;
    }
}
```
Output:

![Screenshot 2025-04-25 221041](https://github.com/user-attachments/assets/f3a7a0c2-5781-4517-acee-a170c0ca5b54)


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
