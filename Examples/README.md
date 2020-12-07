# Memory Basics

## The Big Picture
| # | Subject | Description |
| --- | --- | --- |
| 1 | Arrays | Arrays and buffers are the same thing.  They point to [adjacent](https://www.merriam-webster.com/dictionary/adjacent) data streams located in memory and end with a NULL byte. (\x00). |
| 2 | Pointers | Pointers have [types](https://www.learnjavaonline.org/en/Variables_and_Types), just like variables.  Pointers are used to store to location of data in memory. |
| 3 | Strings | Strings are pointers to character arrays.  Strings point to the beginning of an array/buffer in memory to be read by a function like scanf(). |
| 4 | Typecasting | C/C++ is a Strongly Typed Language.  You need to use Typecasting to change the type of a variable or pointer.  Despite how the type was originally defined. |
| 5 | Vectors | Vectors are similar to arrays expect that they are used to store Object References instead of values with primative data types. |

## Primitive Data Types
| # | Subject | Description |
| --- | --- | --- |
| 1 | Signed Int | Stores a whole number. Numbers in C are defaultly signed. Meaning, they can be either positive or negative numbers. 32-bit signed integers max out at 2,147,483,647.
| 2 | Unsigned Int | Stores a whole number. Numbers that are unsigned can only be positive.  This means there is no [Twos Compliment](https://www.youtube.com/watch?v=lKTsv6iVxV4) and the least significant bit is not reserved. 32-bit unsigned integers max out at 4,294,967,295.
| 3 | Long | Store a whole number.  A long is bouble the memory size of an int, 8-bytes in 32-bit machines.  Used when an Int isn't big enough to store a value. |
| 4 | Short | Store a whole number.  A short is half the size of an Int. 2-Bytes in 32-bit machines. |
| 5 | Float | Stores numbers with decimal points.  4-Bytes in size on 32-Bit machines.  Used for values with 6 to 7 decimals. |
| 6 | Double | Stores numbers with decimal points. 8-Bytes in size on 32-Bit machines.  Used for values with up to 15 decimals.  |
| 7 | Char | 2 Bytes in size.  Chars are used to contain letters such as ASCII values. Strings are considered char arrays. |
| 8 | Boolean | Either a True or False.  1-Bit in size. |

## Endiannessness and Byte Ordering
| # | Subject | Description |
| --- | --- | --- |
| 1 | Big Endian | Bytes in there normal order. _"Most significant byte first"_  0x12345678 = \x12\x34\x56\x78 |
| 2 | Little Endian | Bytes in there reverse order. _"Least significant byte first"_  0x12345678 = \x78\x56\x34\x12 |

## Common Memory Bugs
| # | Bug | Description |
| --- | --- | --- |
| 1 | Buffer Overflow | Writing past the bounds of a buffer.  For example, writing to a buffer without an null byte (\x00) appended at the end, therefore the program doesn't know when to stop a user's input from writing to memory. |
| 2 | Dangling Pointers | When a pointer is pointing to an area of memeory that has already been freed.  Also known as, [Use-After-Free](http://phrack.org/issues/57/9.html). |
| 3 | Off-By-One Error | ... |
| 4 | Race Condition | When threads are in use.  If two or more threads can access shared data and try to change it at the same time.  |
| 5 | Format String Attack | ... |
| 6 | Integer Overflow | ... |
| 7 | Weak Encryption | Using weak Pseudo-random seeds, for example using time() to provide a cryptographical seed for encryption. |
