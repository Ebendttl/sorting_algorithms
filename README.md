## C - Sorting algorithms & Big O
- C
- Algorithm
- Data structure

## Resources
- Sorting algorithm
- Big O notation
- Sorting algorithms animations
- 15 sorting algorithms in 6 minutes (WARNING: The following video can trigger seizure/epilepsy. It is not required for the project, as it is only a funny visualization of different sorting algorithms)
- CS50 Algorithms explanation in detail by David Malan
- All about sorting algorithms

## Learning Objectives
- At the end of this project, I am expected to be able to explain to anyone, without the help of Google:

## General
- At least four different sorting algorithms
- What is the Big O notation, and how to evaluate the time complexity of an algorithm
- How to select the best sorting algorithm for a given input
- What is a stable sorting algorithm

## Requirements
- Allowed editors: vi, vim, emacs
- All my files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All my files should end with a new line
- A README.md file, at the root of the folder of the project, is mandatory
- My code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- I am not allowed to use global variables
- No more than 5 functions per file
- Unless specified otherwise, I am not allowed to use the standard library. Any use of functions like printf, puts, … is totally forbidden.
- In the following examples, the main.c files are shown as examples. I can use them to test my functions, but I don’t have to push them to my repo (if I do they won’t be taken into account). ALX will use our own main.c files at compilation. Their main.c files might be different from the one shown in the examples
- The prototypes of all my functions should be included in my header file called sort.h
- All my header files should be include guarded
- A list/array does not need to be sorted if its size is less than 2.
- GitHub

### More Info
- Data Structure and Functions
- For this project I am given the following print_array, and print_list functions:

``` bash
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

- My files print_array.c and print_list.c (containing the print_array and print_list functions) will be compiled with your functions during the correction.
- Please declare the prototype of the functions print_array and print_list in your sort.h header file
- Please use the following data structure for doubly linked list:
``` bash
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
- Please, note this format is used for Quiz and Task questions.

- O(1)
- O(n)
- O(n!)
- n square -> O(n^2)
- log(n) -> O(log(n))
- n * log(n) -> O(nlog(n))
- n + k -> O(n+k)
- …
- Please use the “short” notation (don’t use constants). Example: O(nk) or O(wn) should be written O(n). If an answer is required within a file, all your answers files must have a newline at the end.

### Tests
#### Here is a quick tip to help you test your sorting algorithms with big sets of random integers: Random.org
