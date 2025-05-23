# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
int main() {
    int num = 44;
    int shifted;
    shifted = num << 3; 
    printf("Original number: %d\n", num);
    printf("After left shift by 3 positions: %d\n", shifted);
    return 0;
}

```

## OUTPUT


![image](https://github.com/user-attachments/assets/b237efa1-65b7-4c30-9fe8-9729fe8a7b50)






## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>
int main()
{
    int a,b;
    scanf("%d%d",&a,&b);
    if(a==b)
    printf("Numbers are Equal");
    else
    printf("Numbers are not Equal");
    
    
}
```


## OUTPUT
![image](https://github.com/user-attachments/assets/6a408d82-0ce6-46d0-94da-78ad83a49f02)

           
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main(){
    char str[100];
    int i;
    scanf("%s",str);
    for(i=0;str[i]!=0;i++){
        str[i]=tolower(str[i]);
    }
    printf("Lower case String is:%s",str);
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/2be359e9-9177-445e-9ed5-b652f53a6990)





## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int main() {
    char str[100];
    int i = 0, wordCount = 0;
    int inWord = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    str[strcspn(str, "\n")] = '\0';
    do {
        if (isspace(str[i]) || str[i] == '\0') {
            if (inWord) {
                wordCount++;
                inWord = 0;
            }
        } else {
            inWord = 1;
        }
        i++;
    } while (str[i - 1] != '\0');
    printf("Total number of words: %d\n", wordCount);
    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/0055f7fe-ada9-4aba-b72a-e824f3d72eea)





## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    int rows;
    printf("Enter a string: ");
    scanf("%s", str);
    printf("Enter number of rows: ");
    scanf("%d", &rows);
    int len = strlen(str);
    int index = 0;
    for (int i = 1; i <= rows; i++) {
        for (int j = 0; j < rows - i; j++) {
            printf(" ");
        }
        for (int j = 0; j < i; j++) {
            printf("%c", str[index % len]);
            index++;
            if (j != i - 1) {
                printf(" ");
            }
        }
        printf("\n");
    }
    return 0;
}
```


## OUTPUT

![image](https://github.com/user-attachments/assets/8544cd5b-8868-47af-845a-4efbe7b83637)

 

## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

