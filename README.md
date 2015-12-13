# c2stack
Stack implementation in C2. Stack is an data structure which follows
the LIFO model (Last In, First Out).
After downloading or cloning c2vector, it is advised to test
it with
```
c2c --test --checkOnly
```
in the the root directory of the c2vector repository

You can then try an example of usage of vector with
```
c2c
```
and running the test executable
```
./output/test/test
```
If no errors are thrown during the testing, everything works and you are good
to go.
## API
```
public type stack struct
{
    void** items;
    int32 capacity;
    int32 total;
}

public func void init(stack* v);
public func int32 total(stack* v);
public func void push(stack* v, void* item);
public func void* pop(stack* v);
public func void free(stack *v);
```
## Usage
First you start by creating a stack by using init function (import stdio as io; and import c2vector local; assumed)
```
stack st;
init(&st);
```
Then you can push symbols on the stack with push function
```
push(&st,item);
```
As with any stack, items are retrieved with
```
pop(&st);
```
The total() function returns the number of elements in a vector.
```
io.printf("%d\n, total(&st));
```
After you are finished working with a stack, free the memory with
```
free(&st);
```
## License
Lukas Hozda(luk.hozda@gmail.com, github.com/luciusmagn), (c)2015

Usage of the works is permitted provided that this instrument is retained with the works, so that any entity that uses the works is notified of this instrument.

DISCLAIMER: THE WORKS ARE WITHOUT WARRANTY. 
