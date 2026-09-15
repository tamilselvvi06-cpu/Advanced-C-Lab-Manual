## EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
### Aim:
To write a C program to search a given element in the given linked list.

### Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node{
    int data; 
    struct Node *next;
}*head;

void search(int data)
{
    struct Node *p;
    int item=data;
    int flag,i=0;
    p=head;
    if(p==NULL){
        printf("List is empty\n");
    }else{
        while(p!=NULL){
            if(p->data==item){
                printf("item %d found at location %d",item,i+1);
                flag=0;
            }i++;
            p=p->next;
        }
    }
    if(flag!=0){
        printf("Item not found\n");
    }
 
}
``` 

### Output:

<img width="940" height="567" alt="image" src="https://github.com/user-attachments/assets/ed0b1ede-f9ab-403c-a4fc-40e70f9fd93e" />


### Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
## EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
### Aim:
To write a C program to insert a node in a linked list.
### Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node{
    char data; 
    struct Node *next;
}*head;

void insert(int data)
{
    struct Node *n=(struct Node *)malloc(sizeof(struct Node));
    struct Node *temp;
    if(head==NULL)
    {
        head = n;
        head->data=data;
        n->next=NULL;
        return;
    }
    temp=head;
    while(temp->next!=NULL)
    {
        temp=temp->next;
    }
    n->data = data;
    n->next = NULL;
    temp->next= n;    
    
}

}
```

### Output:

<img width="559" height="578" alt="image" src="https://github.com/user-attachments/assets/7cb56621-4c64-462a-b128-4df0db6ff15a" />

 
### Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
## EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
### Aim:
To write a C program to traverse a doubly linked list.

### Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;

void display()
{
    struct Node *ptr;
    ptr=head;
    if(ptr==0){
        printf("EMPTY");
    }
    else{
        while(ptr!=0){
            printf("%d ",ptr->data);
            ptr=ptr->next;
        }
    }

    
}
```

### Output:

<img width="572" height="536" alt="image" src="https://github.com/user-attachments/assets/83bd1bea-6054-4436-b49c-e91781b0c71d" />


### Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



## EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
### Aim:
To write a C program to insert an element in doubly linked list

### Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head;

void insert(char data)
{
   struct Node *ptr,*temp;
   ptr = (struct Node *) malloc(sizeof(struct Node));
   if(ptr == NULL)
   {
       printf("OVERFLOW\n");
   }
   else
   {
        ptr->data=data;
       if(head == NULL)
       {
           ptr->next = NULL;
           ptr->prev = NULL;
           head = ptr;
       }
       else
       {
          temp = head;
          while(temp->next!=NULL)
          {
              temp = temp->next;
          }
          
          temp->next = ptr;
          ptr ->prev=temp;
          ptr->next = NULL;
          }

       }
    }
```

### Output:

<img width="590" height="529" alt="image" src="https://github.com/user-attachments/assets/a1e32cd5-141b-4e4b-b1ac-b10ef4569cb9" />


### Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




## EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

### Aim:
To write a C function that deletes a given element from a linked list.

### Algorithm:
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


### Program:


```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void delete()
{
    struct Node *ptr;
    if(head==NULL){
        printf("UNDERFLOW\n");
    }
    else if(head->next==NULL){
        head = NULL;
        free(head);
        printf("Node deleted\n");
    }
    else{
        ptr=head;
        head=head->next;
        head->prev=NULL;
        free(ptr);
        printf("Node deleted\n");
    }
    
    
    
}

```

### Output:

<img width="596" height="737" alt="image" src="https://github.com/user-attachments/assets/71c7aeb4-d9fd-4421-9d17-35717681f36a" />


### Result:
Thus, the function that deletes a given element from a linked list is verified successfully.
