EX-16-LEFT-SHIFT-OPERATION
~~~
AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

ALGORITHM
1.Start the program.
2.Assign values of a and b as 44 and 3.
3.Use left shift operator (<<) and shift the value of a three times.
4.Display the result.
5.Stop the program.
~~~
PROGRAM
#include <stdio.h>

int main() { int num = 44; // Initialize the number

// Perform left shift by 3 positions
int result = num << 3;

// Print the result
printf("Original number: %d\n", num);
printf("After left shifting by 3 positions: %d\n", result);

return 0;
}
~~~
OUTPUT
~~~
Original number: 44 After left shifting by 3 positions: 352
~~~
RESULT
~~~
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.
~~~
EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT
AIM
Write a C Program to check whether the two numbers are equal or not using simple if statement.

ALGORITHM
1.Start the program.
2.Read two numbers.
3.If first number is equal to second number, display both are equal.
4.Otherwise display both are not equal.
5.Stop the program.
~~~
PROGRAM
#include <stdio.h>

int main() { int a, b;

// Input two numbers
printf("Enter first number: ");
scanf("%d", &a);

printf("Enter second number: ");
scanf("%d", &b);

// Check if the numbers are equal
if (a == b) {
    printf("The numbers are equal.\n");
} else {
    printf("The numbers are not equal.\n");
}

return 0;
}
~~~~
OUTPUT
~~~
Enter first number: 10 Enter second number: 10 The numbers are equal.
~~~
RESULT
~~~
Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
~~~
EX-18-STRING-LOWERCASE-CONVERSION
AIM
Write a C Program to convert the given string into lowercase.

ALGORITHM
1.Start the program.
2.Read a string variable.
3.Using tolower( ) function convert the given string into its lowercase.
4.Display the result.
5.Stop the program.
~~~
PROGRAM
#include <stdio.h> #include <ctype.h> // For tolower() function

int main() { char str[100];

// Input the string
printf("Enter a string: ");
fgets(str, sizeof(str), stdin);  // Use fgets for safe input (handles spaces)

// Convert the string to lowercase
for (int i = 0; str[i] != '\0'; i++) {
    str[i] = tolower(str[i]);  // Convert each character to lowercase
}

// Output the result
printf("String in lowercase: %s\n", str);

return 0;
}
~~~
OUTPUT
~~~
Enter a string: Hello World! String in lowercase: hello world!
~~~
RESULT
~~~
Thus the program to convert the given string into lowercase has been executed successfully
~~~
EX-19-COUNT-OF-WORDS-IN-A-STRING
AIM
Write a C Program to count the total number of words in a given string using do While loop.

ALGORITHM
1.Start the program.
2.Read a string variable.
3.Using for loop, inspect the string character by character.
4.Whenever a space is encountered increment count by 1.
5.Display the result.
6.Stop the program.
~~~
PROGRAM
#include <stdio.h>

int main() { char str[100]; int i = 0, wordCount = 0;

// Input the string
printf("Enter a string: ");
fgets(str, sizeof(str), stdin);  // Use fgets to handle spaces

// Use a do-while loop to count words
do {
    // Skip any spaces
    while (str[i] == ' ' && str[i] != '\0') {
        i++;
    }

    // If we encounter a non-space character, it's the start of a word
    if (str[i] != ' ' && str[i] != '\0') {
        wordCount++;

        // Skip through the rest of the word
        while (str[i] != ' ' && str[i] != '\0') {
            i++;
        }
    }
} while (str[i] != '\0');  // Continue until we reach the end of the string

// Output the total word count
printf("Total number of words: %d\n", wordCount);

return 0;
}
~~~
OUTPUT
~~~
Enter a string: Hello world! This is a test. Total number of words: 6
~~~
RESULT
~~~
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
~~~
EX -20 -COMPARING TWO STRINGS
AIM
write a Program to compare two strings without using strcmp().

ALGORITHM
~~~
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable flag and initialize it to 0, and i for indexing.
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered (i.e., can include spaces).
 Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no spaces in the second string).
 Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string): • If c1[i] is not equal to c2[i], set flag = 1. • Increment i by 1.
 Step 7: After the loop, check the value of flag: • If flag == 0, print "strings are same". • Otherwise, print "strings are not same".
 Step 8: End the program.
~~~
~~~
PROGRAM
#include <stdio.h>

int main() { char str1[100], str2[100]; int i = 0, flag = 0;

// Input two strings
printf("Enter first string: ");
fgets(str1, sizeof(str1), stdin);

printf("Enter second string: ");
fgets(str2, sizeof(str2), stdin);

// Compare strings character by character
while (str1[i] != '\0' && str2[i] != '\0') {
    if (str1[i] != str2[i]) {
        flag = 1;  // Set flag if strings are not equal
        break;
    }
    i++;
}

// Check if strings are equal
if (flag == 0 && str1[i] == str2[i]) {
    printf("Strings are equal.\n");
} else {
    printf("Strings are not equal.\n");
}

return 0;
}
~~~
OUTPUT
~~~
Enter first string: Hello Enter second string: Hello Strings are equal.
~~~
RESULT
~~~
Thus the C Program to compare two strings without using strcmp() has been executed successfully.
~~~
