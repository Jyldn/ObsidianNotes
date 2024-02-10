# Basics
Pointers allow us to ==access data by reference instead of by value==.

1. `int x = 4`
   **Translation:** 
	1. *Integer, whose name is **x**, is set to the value **4**.
2. `int * px = &x;`
   **Translation:**
	1. **Asterisk:** *modifies the type so that our variable is now a pointer to an integer.*
	2. **pNAME**: *This name is entirely optional and does not affect compilation. However, the standard way of naming a pointer is to prefix the original variable name with p in caps.*
	3. **&**: *The address of 'x'.*
---
# Using Pointers
Once a pointer is created, we can copy the value of *x* to a new variable using the pointer.

`int y = \*pX`

**Translation:**
*Integer 'y' is set to the thing **pointed to by** pX.*

**Explanation:**
==When an asterisk is used with a type declaration, it modifies the type.== When it is used alone, as shown here, the asterisk is called a **dereference**. ==The **dereference** means go to the address, pointed to by that pointer, and grab that value.==

Because *pX* points to *x*, the dereference will go and grab that value and set *y* equal to *x*.

When we see an asterisk alone with a variable, as opposed to used with a type, we can think of it as:
*The thing pointed to by.*  

---
# Why?
By using a pointer, we can pass around *x* by **reference instead of value**.

In functional programming, like in C, we break down functions based of the function that they perform. This means that, when programming functionally, the structure of data is often **outside the [[scope]]** of other functions. To solve this, we pass in the reference of a variable to get the memory address, rather than the variable, so that the function, which is outside of the variable scope, ==can now work on the value, stored in memory, that was declared with that original variable==.

Using pointers keeps code **clean** and **understandable**.

```C
#include <stdio.h>

struct Person {
	char name[64];
	int age;
};

void updateStruct(struct Person *p, int age) {
	p->age = age
}

int main(int argc, char **argv) {
	struct Person banana;
	updateStruct(&banana, 30);
}
```
## Static vs Dynamic Memory Allocation

### Static Allocation
Data that is known to have a fixed size at compile time.
A variable that goes onto the [[stack]]. A place that is always in scope for the function it is running in.
### Dynamic Allocation
Data that can be changed in size as the program runs.
Memory that comes from the [[heap]]. Memory taken from the heap is going to be a pointer to data that is outside of the current scope.
### Example
Here, 100 bytes is allocated to be pulled from the heap, but that 100 bytes could've come from user input or something else.
```C
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char**argv) {
	char *heapMemory = malloc(100);
	if (NULL == heapMemory) {
		perror("Malloc failed bruh.");
	}
	
	return 0;
}
```