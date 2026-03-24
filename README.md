EX-21-POINTERS
# AIM:
Write a C program to convert a 15.5 into 15 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (15.5).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 15.0.
4.	Print the modified value.

## PROGRAM:
```
#include <stdio.h>
int main() {
    float num;
    float *p;
    int result;
    scanf("%f", &num);
    p = &num;
    result = (int)(*p);
    printf("the integer equivalent of %.2f =%d", *p, result);
    return 0;
}
```
<img width="922" height="565" alt="image" src="https://github.com/user-attachments/assets/9eb2ac03-b429-42ea-8518-1da196da4e5e" />

## OUTPUT:
<img width="869" height="297" alt="image" src="https://github.com/user-attachments/assets/b2b1eb39-b40c-4a5d-b426-47bdd5bad99b" />












## RESULT:
Thus the program to convert a 15.5 into 15 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
```
#include <stdio.h>
long long int product(int n) {
    if (n == 1)
        return 1;   
    else
        return n * product(n - 1);  
}
int main() {
    int n = 12;
    long long int result = product(n);
    printf("Product is = %lld\n", result);
    return 0;
}
```
<img width="971" height="652" alt="image" src="https://github.com/user-attachments/assets/35527f3c-f7da-4ede-90fa-7efa8812cbd5" />

## OUTPUT:
<img width="653" height="249" alt="image" src="https://github.com/user-attachments/assets/4b22ea72-651e-454b-a9c4-3c101ed942b8" />
 		
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row and column of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Inside the loop, calculate the sum of the elements in each column.
5.	Print the sum for each row.

## PROGRAM:
```
#include <stdio.h>
int main() {
    int a[10][10], rows, cols, i, j, sum;
    scanf("%d %d", &rows, &cols);
    for(i = 0; i < rows; i++) {
        for(j = 0; j < cols; j++) {
            scanf("%d", &a[i][j]);
        }
    }
    for(i = 0; i < rows; i++) {
        sum = 0;
        for(j = 0; j < cols; j++) {
            sum += a[i][j];
        }
        printf("The Sum of Elements of a Row in a Matrix:  %d\n", sum);
    }
    for(j = 0; j < cols; j++) {
        sum = 0;
        for(i = 0; i < rows; i++) {
            sum += a[i][j];
        }
        printf("The Sum of Elements of a Column in a Matrix:  %d\n", sum);
    }
    return 0;
}
```
<img width="1086" height="608" alt="image" src="https://github.com/user-attachments/assets/5f76285a-7c70-4ee9-9d72-609b46e1483b" />



## OUTPUT
<img width="1139" height="537" alt="image" src="https://github.com/user-attachments/assets/d08752a7-aef6-4892-b833-d76d1e633494" />


 
 

 ## RESULT
 Thus,the program has been executed successfully.


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    int num_rows, len, i, j, k;
    scanf("%s", str);
    scanf("%d", &num_rows);
    len = strlen(str);
    for(i = 1; i <= num_rows; i++) {
        int midpoint = (2 * num_rows - 1) / 2;
        for(j = 0; j < (2 * num_rows - 1); j++) {
            if(j >= midpoint - (i - 1) && j <= midpoint + (i - 1)) {
                k = (j - (midpoint - (i - 1))) % len;
                printf("%c", str[k]);
            } else {
                printf(" ");
            }
        }
        printf("\n");
    }
    return 0;
}
```

 ## OUTPUT
<img width="959" height="626" alt="image" src="https://github.com/user-attachments/assets/77ad5df0-4340-4088-b93a-b7d0f60a532c" />

 

## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.

## PROGRAM
```
#include <stdio.h>
int main() {
    int arr[10];
    int *parr = arr;
    int n = 6, i;
    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", parr + i);
    }
    printf("The elements of the array are:\n");
    for(i = 0; i < n; i++) {
        printf("%d ", *(parr + i));
    }
    printf("\n");
    return 0;
}

```
## OUTPUT
<img width="939" height="626" alt="image" src="https://github.com/user-attachments/assets/a0734727-50bf-40f8-8303-8abe21eb23fe" />

 

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


