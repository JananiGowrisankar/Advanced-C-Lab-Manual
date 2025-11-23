## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

## Aim:
To write a C program to display stack elements using linked list.

## Algorithm:
1.	Define a structure Node with two members: data to store the float value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer ptr and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
## Program:
```
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *ptr;  
    ptr=head;  
    while(ptr!=NULL)  
    {  
        printf("%.2f\n",ptr->data);  
        ptr=ptr->next;  
    }  
}

```

## Output:

<img width="899" height="550" alt="image" src="https://github.com/user-attachments/assets/e391aa2f-17ab-48cf-aba5-1141151e7d84" />



## Result:
Thus, the program to display stack elements using linked list is verified successfully. 



## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.

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
    struct Node *ptr;  
    if(head==NULL)  
    {  
        printf("stack is empty");  
    }  
    else  
    {  
        ptr=head;  
        head=ptr->next;  
        free(ptr);  
    }  
}  

```

## Output:


<img width="1187" height="618" alt="image" src="https://github.com/user-attachments/assets/d0286fa8-c2a7-46e3-bdec-07ce6c8f8c65" />



## Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

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
    struct Node *ptr;
    ptr=front;
    
    if(ptr==NULL) printf("queue is empty");
    else
    {
        printf("Queue elements:\n");
    while(ptr!=NULL)
    {
       printf("%.3f\n",ptr->data);
       ptr=ptr->next;
    }
    }
}

```

## Output:

<img width="995" height="581" alt="image" src="https://github.com/user-attachments/assets/7277c149-6431-40de-a23e-8eda2f478798" />


## Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

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
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(char data)
{
   struct Node *newNode;
   newNode=(struct Node*)malloc(sizeof(struct Node));
   newNode->data=data;
   newNode->next=NULL;
   if(front==NULL)
   {
      front=rear=newNode;
   }
   else
   {
      rear->next=newNode;
      rear=newNode;
   }
}



```

## Output:

<img width="771" height="502" alt="image" src="https://github.com/user-attachments/assets/6f22d92a-2f0b-402b-9069-af6213c97c3f" />


## Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


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
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
if(front==NULL && rear==NULL)  printf("Queue is empty");

void peek()
{
    printf("%d",front->data);
}
```

## Output:

<img width="575" height="608" alt="image" src="https://github.com/user-attachments/assets/555ed50f-0d56-45fb-9773-21029c3edb17" />




## Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.
