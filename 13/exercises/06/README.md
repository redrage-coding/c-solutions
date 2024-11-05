### Exercise 13.06
Write a function named `censor` that modifies a string by replacing every
occurrence of `foo` by `xxx`. For example, the string `"food fool"` would become
`"xxxd xxxl"`. Make the function as short as possible without sacrificing
clarity.

### Solution

```c
#include <stdio.h>


void censor(char *str);

int main(void)
{
char arr[] = "food fool fight foor";
censor(arr);

printf("%s", arr);

}


void censor(char *str)
{
    char *temp_str = str;

    while(*(temp_str + 2) != '\0'){
        if(*temp_str == 'f' && *(temp_str + 1) == 'o' && *(temp_str + 2) == 'o')
            *temp_str = *(temp_str + 1) = *(temp_str + 2) = 'x';
        temp_str++;
    }

}
```
