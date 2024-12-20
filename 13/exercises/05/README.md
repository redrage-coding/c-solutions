### Exercise 13.05
(a) Write a function named `capitalize` that capitalizes all letters in its
argument. The argument will be a null-terminated string containing arbitrary
characters, not just letters. Use arry subscripting to access the characters in
the string. *Hint*: Use the `toupper` function to convert each character to
upper case.

(b) Rewrite the `capitalize` function, this time using pointer arithmetic to
access the characters in the string.

### Solution
#### (a)

```c
#include <ctype.h>

void capitalize(char str[]) {
    int i = 0;
    while (str[i] != '\0') {
        if (isalpha(str[i]))  // Check if str[i] is an alphabetic character
            str[i] = toupper(str[i]);  // Assign the uppercase character back to str[i]
        i++;
    }
}
```

#### (b)

```c
#include <ctype.h>

void capitalize(char *str) {
    char *c = str;
    while (*c != '\0') {  // Dereference c to get the character
        if (isalpha(*c))  // Check if *c is an alphabetic character
            *c = toupper(*c);  // Convert *c to uppercase and assign back
        c++;
    }
}
```
