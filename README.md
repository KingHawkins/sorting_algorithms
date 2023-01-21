<h1>0x1B. C - Sorting algorithms & Big O</h1>
`C` `Algorithm` `Data Structure`

<img src="https://s3.amazonaws.com/intranet-projects-files/holbertonschool-low_level_programming/248/willy-wonka.png">

<h2>General</h2>
1. At least four different sorting algorithms
2. What is the `Big O notation` and how to evaluate the time complexity of an algorithm.
3. How to select the best sorting algorithm for a given input
4. What is a stable sorting algorithm

<h2>More Info</h2>
<h3>Data Structure and Functions</h3>
For this project you are given the following `print_array` and `print_list` functions:
1. `print_array` function


```c
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
```


2. `Print_list` function


```c
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}
```


3. Please use the following data structure for doubly linked list:


```c
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
```



