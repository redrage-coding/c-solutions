### Exercise 12.14
Assume that the following array contains a week's worth of hourly temperature
readings, with each row containing the readings for one day:

```c
int temperatures[7][24];
```

Write a statement that uses the `search` function (see Exercise 7) to search the
entire `temperatures` array for the value 32.

### Solution

```c
bool has32 = search(*temperatures, 7 * 24, 32);
```

### EXAMPLE CODE
```c
#include <stdio.h>
#include <stdbool.h>

bool search(const int a[], int n, int key);

int main(void)
{
int a[] = {1,2,3,4,5,6,7};

printf("%s\n", search(a, 7, 7) ? "True" : "False");


int temperatures[7][24] = {};
temperatures[3][0] = 32;
printf("%s\n", search(*temperatures, 7*24, 32) ? "True" : "False");


}

bool search(const int a[], int n, int key)
{
// int *p;
// p = a;

for(int i = 0; i < n; i++){
    if(*(a+i) == key)
        return true;

}
return false;

}
```
