## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
### Aim:
To write a C program to display stack elements using linked list.

### Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *p;
    p=head;
    while(p!=NULL){
        printf("%.2f\n",p->data);
        p=p->next;
    }
}

```

### Output:

<img width="622" height="526" alt="image" src="https://github.com/user-attachments/assets/23139631-fb3a-4d2d-bb89-9265882d30db" />


### Result:
Thus, the program to display stack elements using linked list is verified successfully. 



## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
### Aim:
To write a C program to pop an element from the given stack using liked list.

### Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>
struct Node   
{  
int data;  
struct Node *next;  
}*head;  
void pop() {
    struct Node *ptr;
    if(head==NULL){
        printf("stack is empty");
    }
    else{
        ptr=head;
        head=ptr->next;
        free(ptr);
    }
}

```

### Output:

<img width="989" height="654" alt="image" src="https://github.com/user-attachments/assets/4a79d58a-e8e9-4f26-8267-dcf7985ba8fe" />



### Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
### Aim:
To write a C program to display queue elements using linked list.
### Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display() {
    if (front == NULL) {
        printf("queue is empty\n");
        return;
    }
    struct Node *temp = front;
    while (temp != NULL) {
        printf("%d\n", temp->data); 
        temp = temp->next;
    }
}
```

### Output:

<img width="643" height="570" alt="image" src="https://github.com/user-attachments/assets/b4f68d7b-d2ef-4ac2-9e70-1aea879ad588" />


### Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

### Aim:
To write a C program to insert elements in queue using linked list

### Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float value) {
    struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
    if (newNode == NULL) {
        printf("Queue Overflow\n");
        return;
    }
    newNode->data = value;
    newNode->next = NULL;

    if (rear == NULL) {   
        front = rear = newNode;
    } else {
        rear->next = newNode;
        rear = newNode;
    }
}
```

### Output:

<img width="687" height="578" alt="image" src="https://github.com/user-attachments/assets/9a707f53-b571-46a5-9376-3e9958bdde4e" />


### Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


### Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

### Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

### Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek() {
    if (front == NULL) {
        printf("Queue is empty\n");
    } else {
        printf("%c\n", front->data);  
    }
}

```

### Output:

<img width="583" height="601" alt="image" src="https://github.com/user-attachments/assets/12003cf8-13ed-4d1e-a70e-a356f7ef75f7" />


### Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.
