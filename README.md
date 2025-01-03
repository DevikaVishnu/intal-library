# Library for Integers of an Arbitrary Length

An integer of an arbitrary length (intal) is an object pointed to by a ```void*``` pointer. An intal can be created by ```intal_create()``` by providing a ```char``` string of a nonnegative integer provided in decimal digits. Some intals are created out of some functionalities like ```intal_add()```.

The responsibility of destroying the created intals lies with the client, using the ```intal_destroy()```, which will free whatever memory that was allocated during the creation of the intal.

There is no theoretical limit to the size of the integer, except for memory limitations of the process (Operating System).

The operations that can be done on intals are-

- Addition
- Subtraction
- Multiplication (Karatsuba algorithm)
- Division
- Exponent
- Comparison
- Increment and decrement by 1


## Usage:
1. To run a sanity check:
```
$ gcc -c intal_sanity_check.c
$ gcc -Wall intal.c intal_sanity_check.o -lm -lrt -o intal.out
$ ./intal.out
```

2. Running a client file:
```
$ gcc -c client.c
$ gcc -Wall intal.c client.o -lm -lrt -o intal.out
$ ./intal.out
```
