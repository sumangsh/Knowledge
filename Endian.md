# BIG ENDIAN And SMALL ENDIAN

**There are two ways of ordering the data while storing it into memory.**
- Big Endian
- Little Endian

* __Big Endian:__ Most significant Byte stored first in the memory and Least significant Byte stored at last in memory

_Example:_ 

We want to store data 0x12345678 starting at address 0x1000. Here total data is 16 byte

|12|34|56|78|
|-----|------|-----|----|
|4byte|4byte|4byte|4byte|

In Big endian, Lower Address holds higher byte of data and Higher Address holds lower byte of data

Data stored in below way for Big Endian

|Address|Data|
|------|-------|
|1000H|12H|
|1001H|34H|
|1002H|56H|
|1003H|78H|


__Little Endian:__ Most significant Byte stored last in the memory and Least significant Byte stored at first in memory

In Little endian, Lower Address holds lower byte of data and Higher Address holds higher byte of data

Data stored in below way for Little Endian

|Address|Data|
|------|-------|
|1000H|78H|
|1001H|56H|
|1002H|34H|
|1003H|12H|


Advantages in Big Endian
Easier to determine the sign
Easier to compare two number
Easier to divide two number
Easier to print


Advantages in Little Endian
Easier for Multiplication and Addition of multiprecision number



# Convert Bytes to unsigned int


### General Mathematical formula for an array of bytes B of length N:
  
\[
\text{Value} = \sum_{i=0}^{N-1} B_i \times 256^{k}
\]

* **For Little Endian**
\[ \text{Value} = B_0 \times 256^0 + B_1 \times 256^1 + ... + B_{N-1} \times 256^{N-1} \]

_Example (4 bytes)_
\[ \text{Value} = B[0] + (B[1] \times 256) + (B[2] \times 65536) + (B[3] \times 16777216) \]

* **For Big Endian**  
\[ \text{Value} = B_0 \times 256^{N-1} + B_1 \times 256^{N-2} + ... + B_{N-1} \times 256^0 \]

_Example (4 bytes)_  
\[ \text{Value} = (B[0] \times 16777216) + (B[1] \times 65536) + (B[2] \times 256) + B [3] \]