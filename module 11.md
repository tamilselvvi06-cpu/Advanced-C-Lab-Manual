## EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
### Aim:
To write a C program to create a function to find the greatest number

### Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
### Program:

```
#include <stdio.h>

int max_of_four(int n1, int n2, int n3, int n4) {
    int max = n1;
    
    if(n2 > max) max = n2;
    if(n3 > max) max = n3;
    if(n4 > max) max = n4;
    
    return max;
}

int main() {
    int n1, n2, n3, n4, greater;
    
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);
    
    greater = max_of_four(n1, n2, n3, n4);
    
    printf("Greatest number: %d\n", greater);
    
    return 0;
}
```

### Output:
<img width="531" height="377" alt="image" src="https://github.com/user-attachments/assets/2da8301b-983b-43c7-a6d7-da023a4b2ae2" />


### Result:
Thus, the program  that create a function to find the greatest number is verified successfully.

 
 
## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
### Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

### Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
### Program:

```
#include<stdio.h>
int main(){
    int n,k;
    scanf("%d%d",&n,&k);
    int max_and=0,max_or=0,max_xor=0;
    for(int i=1;i<=n;i++){
        for(int j=i+1;j<=n;j++){
            if((i&j)<k&&(i&j)>max_and)
                max_and=i&j;
            if((i|j)<k&&(i|j)>max_or) 
                max_or=i|j; 
            if((i^j)<k&&(i^j)>max_xor)
                max_xor=i^j; 
        }
    }
    printf("%d\n",max_and);
    printf("%d\n",max_or); 
    printf("%d\n",max_xor); 
    return 0;
}
```

### Output:
<img width="654" height="419" alt="image" src="https://github.com/user-attachments/assets/8f709080-e0f5-4269-82f2-2e3e6c893b1a" />


### Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
### Aim:
To write a C program to write the logic for the requests

### Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int total_number_of_shelves;
    scanf("%d", &total_number_of_shelves);

    int total_number_of_queries;
    scanf("%d", &total_number_of_queries);

    int** shelves = (int**)malloc(total_number_of_shelves * sizeof(int*));
    int* shelf_sizes = (int*)malloc(total_number_of_shelves * sizeof(int));

    for(int i = 0; i < total_number_of_shelves; i++) {
        shelves[i] = NULL;
        shelf_sizes[i] = 0;
    }

    while(total_number_of_queries--) {
        int type_of_query;
        scanf("%d", &type_of_query);

        if(type_of_query == 1) {
            int x, y;
            scanf("%d %d", &x, &y);

            shelf_sizes[x]++;
            shelves[x] = realloc(shelves[x], shelf_sizes[x] * sizeof(int));
            shelves[x][shelf_sizes[x] - 1] = y;
        }

        else if(type_of_query == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", shelves[x][y]);
        }

        else if(type_of_query == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", shelf_sizes[x]);
        }
    }

    for(int i = 0; i < total_number_of_shelves; i++) {
        free(shelves[i]);
    }

    free(shelves);
    free(shelf_sizes);

    return 0;
}

    

```

### Output:

<img width="528" height="283" alt="image" src="https://github.com/user-attachments/assets/863a3f45-c518-49e2-a0eb-18fc4b11417f" />

### Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
### Aim:
To write a C program print the sum of the integers in the array.

### Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



### Program:

```
#include<stdio.h>
int main(){
    int n,sum=0;
    scanf("%d",&n);
    int a[n];
    for(int i=1;i<=n;i++){
        scanf("%d",&a[i]);
    }
    for(int i=1;i<=n;i++){
        sum+=a[i];
    }
    printf("%d",sum);
}
```

### Output:

<img width="503" height="262" alt="image" src="https://github.com/user-attachments/assets/43e6f2c9-77d3-43ff-aef1-75b58fecfdae" />


### Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



### Aim:

To write a C program that counts the number of words in a given sentence.

### Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



### Program:

```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    fgets(str,sizeof(str),stdin);
    int len=sizeof(str);
    int count=1;
     for(int i=0;i<len-1;i++){
         if(str[i]==' ')
         count++;
         
     }
     printf("Total number of words in the string is :%d",count);
    return 0;
}

```

### Output:

<img width="922" height="127" alt="image" src="https://github.com/user-attachments/assets/b1552f83-61ef-4ef7-904d-7f6905116f70" />


### Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
