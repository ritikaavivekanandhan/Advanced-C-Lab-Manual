EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST. 

Aim: To write a C program to display stack elements using linked list.

Algorithm:
```
Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
Declare a global variable head representing the starting node of the linked list.
Define a function display to print the elements of the linked list.
Declare a pointer p and initialize it with the head of the linked list.
Use a while loop to traverse the linked list:
Print the data of the current node.
Move to the next node using the next pointer.
```
Program:

```
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *temp;
    temp=head;
    while(temp!=NULL)
    {
        printf("%.3f\n",temp->data);
        temp=temp->next;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/a171a6d1-f7ef-44fa-81ba-5d56a3a493c1)

Result: Thus, the program to display stack elements using linked list is verified successfully.

EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST. 

Aim: To write a C program to pop an element from the given stack using liked list.

Algorithm:
```
Check for Empty Stack
If head is equal to NULL, Print "Stack is empty."
Else Proceed to the next step.
Set head to point to the next node in the stack.
```
Program:

```
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void pop()
{
    struct Node*temp;
    if(head==NULL)
    {
        printf("stack is empty\n");
    }
    else
    {
        temp=head;
        head=temp->next;
        free(temp);
    }
    
}
```
Output:

![image](https://github.com/user-attachments/assets/d31e1645-d3e1-4304-9e11-8558b3a33377)

Result: Thus, the program to pop an element from the given stack using liked list is verified successfully.

EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST. 

Aim: To write a C program to display queue elements using linked list.

Algorithm:
```

Check if Queue is Empty
Display Queue Elements
Print the data of the current node pointed to by front
Update front to point to the next node.
End the display function.
```
Program:

``` struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *temp;
    temp=front;
    if(rear==NULL)
    {
        printf("queue is empty");
    }
    else
    {
        while(temp!=NULL)
        {
            printf("%d\n",temp->data);
            temp=temp->next;
        }
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/5d5fb9aa-088b-4365-986f-84496d079b67)

Result: Thus, the program to display queue elements using linked list is verified successfully.

EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim: To write a C program to insert elements in queue using linked list

Algorithm:
```
Allocate Memory for New Node
Set Data and Next Pointer
Check if Queue is Empty
Set both front and rear to point to the new node p.
Set the next pointer of the current rear to point to the new node p.
End of Enqueue Operation
```
Program:

```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *newnode;
    newnode=(struct Node*)malloc(sizeof(struct Node));
    newnode->data=data;
    newnode->next=NULL;
    if(front==NULL && rear==NULL)
    {
        front=rear=newnode;
    }
    else
    {
        rear->next=newnode;
        rear=newnode;
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/83f11c95-9ef7-464d-b989-ca030a5991cb)

Result: Thus, the program to insert elements in queue using linked list is verified successfully.

EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.

Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:
```
Check if the queue is empty: o If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
Access the front element: o If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).
```
Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%d",front->data);
}
```
Output:

![image](https://github.com/user-attachments/assets/9404cfee-53b5-4f5a-b10b-9bd7508a553e)

Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.

