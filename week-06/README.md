[↑ Back](../README.md)

# Week #06 (Topic `B2`)

## Topics

Data structures and built-in functions #2 (strings, dynamic memory allocation)

## Agenda

1. Handling charter arrays and strings in the `main()` function.
1. Passing strings to functions.
1. Returning strings from functions.
1. The built-in functions for handling strings and characters (`string.h`, `ctype.h`, and `stdio.h`).

## Sample codes

1. [`test_string.c`](./samples/test_string.c)
1. [`test_ctype.c`](./samples/test_ctype.c)
1. [`test_malloc.c`](./samples/test_malloc.c)
1. [`test_calloc.c`](./samples/test_calloc.c)

## Exercises

### ProgCont exercises

1. [`PC200504` Sentence-ending punctuation](./exercises/PC200504.md)
1. [`PC200508` Counting Fruits](./exercises/PC200508.md)
1. [`PC200511` Counting Words](./exercises/PC200511.md)
1. [`PC200512` THE END](./exercises/PC200512.md)
1. [`PC200656` Pizzas](./exercises/PC200656.md)

### Permuted exercises

1. [`P1051` Strings - removing characters](./exercises/P1051/README.md)
1. [`P1052` Strings - duplicating characters](./exercises/P1052/README.md)
1. [`P1053` Strings - modifying characters](./exercises/P1053/README.md)

## Highlights

### Representation of strings

1. Language C represents strings as character sequences.
1. A character is represented by its ASCII code.
1. A string is identified by its start memory address.
1. A string is terminated by the `0` ASCII code (literal `'\0'`).

### Handling strings

1. Use the functions of header `string.h` if it is possible to manipulate strings and get their length.

### Functions

In this section, we list all the functions that should be known starting this week. You know a function if you can invoke it correctly using [the official C reference](https://arato.inf.unideb.hu/panovics.janos/stdc.pdf).

#### Functions of `stdio.h` for I/O handling

1. `char *gets(char *start)`
 
   * Reads the next line of the standard input to the memory address `start`.
   * Returns:

     * `NULL` if the case of `EOF`.
     * the memory address `start` otherwise

1. `int puts(char *start)`

   * Writes the string at memory address `start` to the standard output. Also prints a newline character.
   * Returns: *not important*

#### Functions of `stdlib.h` for data conversion

1. `double atof(char *s)` - Returns the `double` value of the given string.
1. `int atoi(char *s)` - Returns the `int` value of the given string.

### Functions of `string.h`

1. `size_t strlen(char *s)`

   * Counts the characters until the first `0` ASCII code.
   * Returns the length of parameter `s`.

1. `char *strcpy(char *left, char *right)`

   * Copies parameter `right` to the memory address of parameter `left`.
   * Returns the memory address of parameter `left`.

1. `char *strcat(char *left, char *right)`

   * Concatenates parameter `right` to the value of parameter `left`.
   * Returns the memory address of parameter `left`.

1. `int strcmp(char *left, char *right)`

   * Compares parameters `left` and `right` based on their alphabetical order. The ASCII values are used in the comparison.
   * Returns `0` if the two strings are equal.
   * Returns `<0` if the parameter `left` goes first in the order.
   * Returns `>0` if the parameter `right` goes first in the order.

1. `char *strchr(char *s, char c)`

   * Determines the first position of character `c` in string `s`.
   * Returns the memory address of the first occurrence of `c` in `s`.
   * Returns `NULL` if `s` does not contain `c`.

1. `char *strstr(char *s, char *p)`

   * Determines the first position of string `p` in string `s`.
   * Returns the memory address of the first occurrence of `p` in `s`.
   * Returns `NULL` if `s` does not contain `p`.

1. `char *strrchr(char *s, char c)`

   * Determines the last position of character `c` in string `s`.
   * Returns the memory address of the last occurrence of `c` in `s`.
   * Returns `NULL` if `s` does not contain `c`.

1. `char *strrstr(char *s, char *p)`

   * Determines the last position of string `p` in string `s`.
   * Returns the memory address of the last occurrence of `p` in `s`.
   * Returns `NULL` if `s` does not contain `p`.


### Allocating in the heap

1. By using static (classic) array declarations, all your allocated memory will be in the stack. These spaces will be de-allocated immediately after you return from the function. Thus, it is impossible to return their addresses from the functions (to be honest you can return them, but the values values cannot be used in the caller function).
1. You can reserve memory in the heap by using functions `calloc()` and `malloc()`. In this case, the de-allocation of the given memory segment is your responsibility too. Thus, it is mandatory to use the function `free()` for this reason.

### Functions

In this section, we list all the functions that should be known starting this week. You know a function if you can invoke it correctly using [the official C reference](https://arato.inf.unideb.hu/panovics.janos/stdc.pdf).

#### Functions of `stdlib.h` for data conversion

1. `double atof(char *s)` - Returns the `double` value of the given string.
1. `int atoi(char *s)` - Returns the `int` value of the given string.

### Functions of `stdlib.h`

1. `void *malloc(size_t size)`

   * Allocates a memory segment with the number of `size` bytes.
   * Returns the start memory address of the allocated memory segment.

1. `void *calloc(size_t number, size_t element_size)`

   * Allocates a memory segment for `number` elements, each having the size of `element_size` bytes.
   * Returns the start memory address of the allocated memory segment.

1. `void free(void *address)`

   * De-allocates the memory segment allocated for the given start memory address using `malloc()` and `calloc()` functions.

### Functions of `ctype.h`

The following functions return a logic value determining whether the given parameter belongs to a specific category of characters:

1. `int isalnum(char c)` - Returns whether character `c` is alphanumeric.
1. `int isalpha(char c)` - Returns whether character `c` is alphabetic.
1. `int iscntrl(char c)` - Returns whether character `c` is control.
1. `int isdigit(char c)` - Returns whether character `c` is a decimal digit.
1. `int isgraph(char c)` - Returns whether character `c` is a printable character.
1. `int islower(char c)` - Returns whether character `c` is lowercase.
1. `int ispunct(char c)` - Returns whether character `c` is neither a control nor an alphanumeric character.
1. `int isspace(char c)` - Returns whether character `c` is a whitespace character.
1. `int isupper(char c)` - Returns whether character `c` is uppercase.
1. `int isxdigit(char c)` - Returns whether character `c` is a hexadecimal digit.

The following functions return a character according to their description:

1. `int tolower(char c)` - Returns the lowercase version of character `c`.
1. `int toupper(char c)` - Returns the uppercase version of character `c`.

## Required skills

> [!IMPORTANT]
> The next lab will be based on the following expectations. Please ensure that you are aware of all the skills mentioned. Ask your questions using the available Q&A form in Moodle.

1. You must be able to declare strings and understand their representation.
1. You must be able to use the functions `gets()` and `puts()`.
1. You must be able to use the functions of header `string.h`.
1. You must be able to use dynamic memory allocation.
1. You must be able to use the mentioned functions of `stdlib.h`.
1. You must be able to use the mentioned functions of `ctype.h`.
