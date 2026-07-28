# EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
### Aim:
To write a C program print the lowercase English word corresponding to the number
### Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
### Program:

```
#include <stdio.h>
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
switch (n) {
    case 1:
       printf("One\n");
       break;
    case 2:
       printf("Two\n");
       break;
    case 3:
       printf("Three\n");
       break;
    case 4:
       printf("Four\n");
       break;
    case 5:
       printf("Five\n");
       break;
    case 6:
       printf("Six\n");
       break;
    case 7:
       printf("Seven\n");
       break;
    case 8:
       printf("Eight\n");
       break;
    case 9:
       printf("Nine\n");
       break;
    case 10:
       printf("Ten\n");
       break;
    case 11:
       printf("Eleven\n");
       break;
    case 12:
       printf("Twelve\n");
       break;
    case 13:
       printf("Thirteen\n");
       break;
    default:
       printf("Greater than 13\n");
       break;
}
return 0;
}
```



### Output:

<img width="424" height="229" alt="image" src="https://github.com/user-attachments/assets/0f2b146d-24cd-4900-a2f7-b7d13d954e75" />



### Result:
Thus, the program is verified successfully
 
# EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
### Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
### Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
### Program:
```
#include <stdio.h>
int main() {
    char a[50];
    int i, h, c;
    printf("Enter a string of digits: ");
    scanf("%s", a);
    for (h = 0; h <= 3; h++) {
        c = 0;
        for (i = 0; a[i] != '\0'; i++) {
            if (a[i] - '0' == h) {
                c++;
            }
        }
        printf("%d ", c);
    }

    printf("\n");
    return 0;
}
```
### Output:


<img width="224" height="122" alt="image" src="https://github.com/user-attachments/assets/40947c6d-5b9b-4d97-a3b2-a5d81e304815" />


### Result:
Thus, the program is verified successfully

# EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
### Aim:
To write a C program to print all of its permutations in strict lexicographical order.

### Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
### Program:

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

void swap_ptr(char **a, char **b) { char *t = *a; *a = *b; *b = t; }

int next_permutation(int n, char **s) {
    int i = n - 2;
    while (i >= 0 && strcmp(s[i], s[i + 1]) >= 0) i--;
    if (i < 0) return 0;
    int j = n - 1;
    while (strcmp(s[j], s[i]) <= 0) j--;
    swap_ptr(&s[i], &s[j]);
    for (int l = i + 1, r = n - 1; l < r; l++, r--)
        swap_ptr(&s[l], &s[r]);
    return 1;
}

int cmp(const void *a, const void *b) {
    return strcmp(*(char **)a, *(char **)b);
}

int main(void) {
    char **s;
    int n;
    scanf("%d", &n);
    s = calloc(n, sizeof(char *));
    for (int i = 0; i < n; i++) {
        s[i] = calloc(11, sizeof(char));
        scanf("%10s", s[i]);
    }
    qsort(s, n, sizeof(char *), cmp);   // required for full enumeration
    do {
        for (int i = 0; i < n; i++)
            printf("%s%c", s[i], i == n - 1 ? '\n' : ' ');
    } while (next_permutation(n, s));
    for (int i = 0; i < n; i++)
        free(s[i]);
    free(s);
    return 0;
}
```



### Output:


<img width="170" height="180" alt="image" src="https://github.com/user-attachments/assets/4c4a6d66-f586-4656-8c82-e7697cbd822f" />

### Result:
Thus, the program is verified successfully
 
# EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
### Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
### Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
### Program:

```
#include <stdio.h>
int main() {
    int n, i, j, len, min;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    len = n * 2 - 1;
    for (i = 0; i < len; i++) {
        for (j = 0; j < len; j++) {
            min = (i < j) ? i : j;
            min = (min < len - i - 1) ? min : len - i - 1;
            min = (min < len - j - 1) ? min : len - j - 1;
            printf("%d ", n - min);
    }
    printf("\n");
 }
 return 0;
}
```



### Output:

<img width="223" height="248" alt="image" src="https://github.com/user-attachments/assets/55e80578-ebcd-4468-9792-ca2c2574beba" />




### Result:
Thus, the program is verified successfully

# EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

### Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

### Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

### Program:

```
#include <stdio.h>
int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}
int main() {
   int result = square();
   printf("The square of the number is: %d\n", result);
   return 0;
}
```



### Output:


<img width="211" height="101" alt="image" src="https://github.com/user-attachments/assets/8e571de5-43c9-40b7-856f-e651cbbbf4f1" />



### Result:

Thus, the program is verified successfully



























