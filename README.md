# Chapter 3
## 3.1
```c
#include <stdio.h>

main ()
{
  printf("4 times 5 is %d\n",4*5);
  return(0);
}
```

# Chapter 4
## 4.1
```c
#include <stdio.h>

int main()
{
  puts("Don't bother me now. I'm busy.");
  return(0);
}
```
## 4.2
```c
#include <stdio.h>

int main()
{
   puts("I love displaying text!");
}
```
## 4.3
```c
#include <stdio.h>

int main()
{
    puts("Hickory, dickory, dock,");
    puts("The mouse ran up the clock.");
}
```
## 4.4
```c
#include <stdio.h>

int main()
{
    puts("Hickory, dickory, dock,");
    puts("The mouse ran up the clock.");
    puts("The clock struck one,");
    puts("The mouse ran down,");
    puts("Hickory, dickory, dock.");
}
```
## 4.5
```c
#include <stdio.h>

int main()
{
    puts("The secret password is:");
/*  puts("Spatula."); */
    return(0);
}
```
## 4.6
```c
#include <stdio.h>

int main()
{
    puts("The secret password is:");
    puts("Spatula."); 
    return(0);
}
```
## 4.7
```c
#include <stdio.h>

int main()
{
//  puts("The secret password is:");
    puts("Spatula.");
    return(0);
}
```
## 4.8
```c
#include <stdio.h>

int main()
{
    puts("This program goes BOOM!)
    return(0);
}
```
## 4.9
```c
#include <stdio.h>

int main()
{
    puts("This program goes BOOM!")
    return(0);
}
```
## 4.10
```c
#include <stdio.h>

int main()
{
    puts("This program goes BOOM!");
    return(0);
}
```
## 4.11
```c
#include <stdio.h>

int main()
{
    printf("I have been a stranger in a strange land.");
    return(0);
}
```
## 4.12
```c
#include <stdio.h>

int main()
{
    printf("Hickory, dickory, dock,");
    printf("The mouse ran up the clock.");
    printf("The clock struck one,");
    printf("The mouse ran down,");
    printf("Hickory, dickory, dock."); 
    return(0);
}
```
## 4.13
```c
#include <stdio.h>

int main()
{
    printf("Hickory, dickory, dock,\n");
    printf("The mouse ran up the clock.\n");
    printf("The clock struck one,\n");
    printf("The mouse ran down,\n");
    printf("Hickory, dickory, dock.\n"); 
    printf("\n~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
    return(0);
}
```
## 4.14
```c
#include <stdio.h>

int main()
{
    printf("\"Hey,\" said the snail, \"I said no salt!\"");
    printf("\n~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
}
```
## 4.15
```c
#include <stdio.h>

int main()
{
    puts("\"Hey,\" said the snail, \"I said no salt!\"");
    printf("\n~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
}
```
## 4.16
```c
#include <stdio.h>

int main()
{
    writeln("Another horrible mistake.");
    return(0);
}
```

# Chapter 5
## Bonus 1
```
Print These Number:
    short int si1 = -32768, si2 = 32767;
    unsigned short int usi = 65535;
    unsigned int ui = 4294967295;
    int i1 = -2147483648, i2 = 2147483647;
    long int li1 = -2147483648, li2 = 2147483647;
    unsigned long int uli = 4294967295;
    long long int lli1 = -9223372036854775807, lli2 = 9223372036854775807;
    unsigned long long int ulli = 18446744073709551615;
```
Output:
```
Range of short int: -32768 → 32767
Range of unsigned short int: 0 → 65535
Range of unsigned int: 0 → 4294967295
Range of int: -2147483648 → 2147483647
Range of long int: -2147483648 → 2147483647
Range of unsigned long int: 0 → 4294967295
Range of long long int: -9223372036854775809 → 9223372036854775807
Range of unsigned long long int: 0 → 18446744073709551615
```
Answer:
```
#include<stdio.h>

int main()
{
    short int si1 = -32768, si2 = 32767;
    unsigned short int usi = 65535;
    unsigned int ui = 4294967295;
    int i1 = -2147483648, i2 = 2147483647;
    long int li1 = -2147483648, li2 = 2147483647;
    unsigned long int uli = 4294967295;
    long long int lli1 = -9223372036854775808, lli2 = 9223372036854775807;
    unsigned long long int ulli = 18446744073709551615;

    printf("Range of short int: %hd %c %hd\n", si1, 26, si2);
    printf("Range of unsigned short int: 0 %c %hu\n", 26, usi);
    printf("Range of unsigned int: 0 %c %u\n", 26, ui);
    printf("Range of int: %d %c %d\n", i1, 26, i2);
    printf("Range of long int: %ld %c %ld\n", li1, 26, li2);
    printf("Range of unsigned long int: 0 %c %lu\n", 26, uli);
    printf("Range of long long int: %lld %c %lld\n", lli1, 26, lli2);
    printf("Range of unsigned long long int: 0 %c %llu\n", 26, ulli);
}
```
## 5.1
```c
#include <stdio.h>

int main()
{
    printf("The value %d is an integer.\n",986);
    printf("The value %f is a float.\n",98.6);
    return(0);
}
```
## 5.2
```c
#include <stdio.h>

int main()
{
    printf("%d\n%f\n%d\n%f\n",127,3.1415926535,122013,0.00008);
}
```
## 5.3
```c
#include <stdio.h>

int main()
{
    printf("%d\n%.2f\n%d\n%.1f\n",127,3.1415926535,122013,0.00008);
}
```
## 5.4
```c
#include <stdio.h>

int main()
{
    puts("Values 8 and 2:");
    printf("Addition is %d\n",8+2);
    printf("Subtraction is %d\n",8-2);
    printf("Multiplication is %d\n",8*2);
    printf("Division is %d\n",8/2);
    return(0);
}
```
