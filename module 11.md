## EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

## Aim:
To write a C program to create a function to find the greatest number

## Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables a, b, c, d and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
## Program:
```
#include <stdio.h>
int max_of_four(int a, int b, int c, int d)
{
    int max;
    max=(a>b && a>c && a>d)?a:(b>a && b>c && b>d)?b:(c>b && c>a && c>d)?c:d;
    return max;
}

int main()
{
    int w,x,y,z;
    scanf("%d %d %d %d",&w,&x,&y,&z);
    int res=max_of_four(w,x,y,z);
    printf("%d",res);
}

```

## Output:

<img width="723" height="416" alt="image" src="https://github.com/user-attachments/assets/5ece956c-61d2-42b2-a476-13b777443831" />


## Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS

## Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

## Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
## Program:
```
#include <stdio.h>
void calculate_the_maximum(int n,int k)
{
    int x=0,y=0,z=0;
    
    for(int a=1;a<=n;a++)
    {
        for(int b=a+1;b<=n;b++)
        {
            int val1= a&b ,val2 = a|b ,val3= a^b;
            
            if(val1 < k && val1 >x)  x=val1;
            if(val2 < k && val2 >y)  y=val2;
            if(val3 < k && val3 >z)  z=val3;
            
        }
    }
    printf("%d\n",x);
    printf("%d\n",y);
    printf("%d\n",z);
    
}

int main()
{
    int n,k;
    scanf("%d %d",&n,&k);
    calculate_the_maximum(n,k);
}

```

## Output:

<img width="514" height="403" alt="image" src="https://github.com/user-attachments/assets/4dead749-0a9f-4d1b-8cea-0538c43b8e5e" />


## Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

## Aim:
To write a C program to write the logic for the requests

## Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
## Program:

```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int noshel, noque;
    
  
    scanf("%d %d", &noshel, &noque);

  
    int **shelarr = (int **)malloc(noshel * sizeof(int *));
    int *nobookarr = (int *)calloc(noshel, sizeof(int));

  
    for (int i = 0; i < noshel; i++) {
        shelarr[i] = NULL; 
    }

    int k, c;

   
    for (int q = 0; q < noque; q++) {
        int type;
        scanf("%d", &type);

        if (type == 1) {
        
            int shelf_no, pages;
            scanf("%d %d", &shelf_no, &pages);

            nobookarr[shelf_no]++;  
            int count = nobookarr[shelf_no];

           
            shelarr[shelf_no] = realloc(shelarr[shelf_no], count * sizeof(int));
            shelarr[shelf_no][count - 1] = pages;
        }

        else if (type == 2) {
            
            int shelf_no, book_no;
            scanf("%d %d", &shelf_no, &book_no);

            printf("%d\n", shelarr[shelf_no][book_no]);
        }

        else if (type == 3) {
           
            int shelf_no;
            scanf("%d", &shelf_no);

            printf("%d\n", nobookarr[shelf_no]);
        }
    }

 
    for (int i = 0; i < noshel; i++) {
        free(shelarr[i]);
    }
    free(shelarr);
    free(nobookarr);

    return 0;
}

```

## Output:

<img width="354" height="476" alt="image" src="https://github.com/user-attachments/assets/ca70581d-bdad-4458-be16-0c1fbf314ee4" />


## Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

## Aim:
To write a C program print the sum of the integers in the array.

## Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



## Program:

```
#include <stdio.h>
int main()
{
  int n;
  scanf("%d",&n);
  
  int a[n],sum=0;
 
  for (int i=0;i<n;i++)
  {
    scanf("%d",&a[i]);
    sum+=a[i];
  }
  printf("%d",sum);

}
 ```

## Output:

<img width="296" height="567" alt="image" src="https://github.com/user-attachments/assets/941bda99-5486-46c7-8af1-9830d6ab48bc" />



## Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



## Aim:

To write a C program that counts the number of words in a given sentence.

## Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



## Program:
```
#include <stdio.h>

int Count_TotalWords(char *str);

int main()
{
    char str[100];
    int totalwords;
    scanf("%[^\n]", str);

    totalwords = Count_TotalWords(str);

    printf("%d\n", totalwords);

    return 0;
}

int Count_TotalWords(char *str)
{
    int i, totalwords = 0;
    while (*str == ' ')
        str++;

    for (i = 0; str[i] != '\0'; i++)
    {
        if ((str[i] == ' ' || str[i] == '\t') &&
            (str[i + 1] != ' ' && str[i + 1] != '\t' && str[i + 1] != '\0'))
        {
            totalwords++;
        }
    }
    if (str[0] != '\0')
        totalwords++;

    return totalwords;
}

```

## Output:

<img width="1140" height="271" alt="image" src="https://github.com/user-attachments/assets/9b62dcca-abce-427d-b3ff-b0ba0c47803a" />




## Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
