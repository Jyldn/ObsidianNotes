A [[type]] used to represent the **size of an object**, or more generally, **any type**. The size is chosen to be large enough to represent the largest possible object of the platform being used.

- It is an unsigned integer (can only store positives and 0).
- On a 64-bit system, the size is 64 bits wide.
- Using this type ensures that the code can handle objects of any size that the system can support.