### Exercise 20.05

Write macros named `GET_RED`, `GET_GREEN` and `GET_BLUE` that, when given a
color as an argument (see Exercise 4), return its 8-bit red, green and blue
intensities.

### Solution

```c
#define GET_RED(color)   (((color) >> 16) & 0xFF)
#define GET_GREEN(color) (((color) >> 8) & 0xFF)
#define GET_BLUE(color)  ((color) & 0xFF)
```
