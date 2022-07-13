# Topics Covered in Project

This files contains the topic and definations covered in this Project.

---

## Table of Content
* Void Pointers
* Type conversion in C

---

## Void Pointers

> Void specifies that the pointer is "universal". That is the pointer is not associated with any data type.

Before using the pointer we have to typecast it.

```c
int n = 10;
void *pointer = &n;
printf("%d" , *(int *)pointer)
// Here the ..^ is dereferencing the pointer
```
<mark>
Note: 
1. The void cannot be used with the Variables.
2. We have to typecast every time to use void.
3. We use the _void pointer_  to return the void functions like _memset_, _memcpy_ ..etc. 
</mark>

A void pointer can point to a function, but not to a class member in C++


## Type Conversion in C

> A type cast is basically a conversion from one type to another. There are two types of type conversion:

### Implicit Type Conversion

> All the data types of the variables are upgraded to the data type of the variable with largest data type.

< img src ="https://www.geeksforgeeks.org/wp-content/uploads/Implicit-Type-Conversion-in-c.png" 
alt = "Conversion Stage" 
margin-right : 10px;/>

For example when __char__ converts to __short int__ when working on ASCII.

### Explicit Type Conversion

> The syntax in C: (type) expression

```c
int main()
{
    double x = 1.2;

    // Explicit conversion from double to int
    int sum = (int)x + 1;

    printf("sum = %d", sum);

    return 0;
}
```

## Use of size\_t 

> Points to remember

1. It is used to represent size of objects/variables in bytes.
2. sizeof returns this data type only.
3. It guarantee to be big enough to contain the size of the biggest object that system can handle.
   * If compiler is 32 bit: IT IS typedef of unsigned int
   * If compiler is 64 bit: IT IS typedef of unsigned long long.
4. It is never negative.
5. Standard functions use this type for count/number.
   * malloc (size\_t)
   * memcpy (destination, source, size\_t) 
   * size\_t strlen (const char * )
