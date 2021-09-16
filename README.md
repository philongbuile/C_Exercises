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
```c
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
## Bonus 2
```
Print These Number "Nicely":
    int i1 = -92233720368;
    int i2 =  92233720368;
```
Output:
```
-2 039 407 152
2 039 407 152
```
Answer:
```c
#include <stdio.h>

void print_with_space(int num)
{
    int temp = 0;
    int scale = 1;
    if (num < 0)
    {
        printf("-");
        num = -num;
    }

    while (num >= 1000)
    {
        temp = temp + scale * (num % 1000);
        num /= 1000;
        scale *= 1000;
    }

    printf("%d", num);

    while (scale != 1)
    {
        scale /= 1000;
        num = temp / scale;
        temp = temp % scale;
        printf(" %03lld", num);
    }

    puts("");
}

int main()
{
    int i1 = -92233720368;
    int i2 =  92233720368;

    print_with_space(i1);
    print_with_space(i2);
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
## 5.5
```c
#include <stdio.h>

int main()
{
    printf("456.98 + 213.4 = %f",456.98 + 213.4);
}
```
## 5.6
```c
#include <stdio.h>

int main()
{
    printf("8 * 14 * 25 = %d",8 * 14 * 25);
}
```
## 5.7
```c
#include <stdio.h>

int main()
{
    int result = 0 + 50 * 1 - 60 - 60 * 0 + 10;
    printf("0 + 50 * 1 - 60 - 60 * 0 + 10 = %d", result);
}
```
## 5.8
```c
#include <stdio.h>

int main()
{
    printf("The total is %d\n",16+17);
    return(0);
}
```
## 5.9
```c
#include <stdio.h>

int main()
{
    printf("The total is %d\n", 16.0 + 17);
    printf("The total is %f\n", 16.0 + 17);
    return(0);
}
```
## 5.10
```c
#include <stdio.h>

int main()
{
    printf("The total is %.1f\n", 16.0 + 17.0);
    return(0);
}
```
## 5.11
```c
#include <stdio.h>

int main()
{
    printf("%d/%d=%d\n",2,5,2/5);
    return(0);
}
```
## 5.12
```c
#include <stdio.h>

int main()
{
    printf("%d/%d=%f\n",2,5,2/5);
    return(0);
}
```
## 5.13
```c
#include <stdio.h>

int main()
{
    printf("%d/%d = %f\n", 2, 5, 2.0/5.0);
    return(0);
}
```

# Chapter 14
## 14.1
```c
#include <stdio.h>

struct player
{
    char name[32];
    int highscore;
}xbox;

int main()
{
    printf("Enter the player's name: ");
    scanf("%s",xbox.name);
    printf("Enter their high score: ");
    scanf("%d",&xbox.highscore);

    printf("Player %s has a high score of %d\n", xbox.name, xbox.highscore);
}
```
## 14.2
```c
#include <stdio.h>

struct player
{
    char name[32];
    int highscore;
    float hours;
}xbox;

int main()
{
    printf("Enter the player's name: ");
    scanf("%s",xbox.name);
    printf("Enter their high score: ");
    scanf("%d",&xbox.highscore);
    printf("Enter the hours played: ");
    scanf("%f",&xbox.hours);

    printf("Player %s has a high score of %d\n", xbox.name, xbox.highscore);
    printf("Player %s has played for %.2f hours\n", xbox.name, xbox.hours);
}
```
## 14.3
```c
#include <stdio.h>

int main()
{
    struct president
    {
        char name[40];
        int year;
    };
    struct president first = {
        "George Washington",
        1789
    };

    printf("The first president was %s\n",first.name);
    printf("He was inaugurated in %d\n",first.year);
}

```
## 14.4
```c
#include <stdio.h>

int main()
{
    struct president
    {
        char name[40];
        int year;
    }first = {
        "George Washington",
        1789
    };

    printf("The first president was %s\n",first.name);
    printf("He was inaugurated in %d\n",first.year);
}
```
## 14.5
```c
#include <stdio.h>

int main()
{
    struct president
    {
        char name[40];
        int year;
    }   first  = {"George Washington", 1789},
        second = {"John Adams", 1897};

    printf("The first president was %s\n",first.name);
    printf("He was inaugurated in %d\n",first.year);
    printf("The second president was %s\n",second.name);
    printf("He was inaugurated in %d\n",second.year);
}
```
## 14.6
```c
#include <stdio.h>

struct scores
{
    char name[32];
    int score;
} player[4];

int main()
{
    int x;

    for(x = 0; x < 4; x++)
    {
        printf("Enter player %d: ", x + 1);
        scanf("%s", player[x].name);
        printf("Enter their score: ");
        scanf("%d", &player[x].score);
    }

    puts("Player Info");
    printf("#\tName\tScore\n");
    for(x = 0; x < 4; x++)
    {
        printf("%d\t%s\t%5d\n", x+1, player[x].name, player[x].score);
    }
    return(0);
}
```
## 14.7
```c
#include <stdio.h>

struct scores
{
    char name[32];
    int score;
} player[4], temp;

int main()
{
    int x;
    int a;
    int b;

    // input
    for(x = 0; x < 4; x++)
    {
        printf("Enter player %d: ", x + 1);
        scanf("%s", player[x].name);
        printf("Enter their score: ");
        scanf("%d", &player[x].score);
    }

    // sort
    for(a = 0; a < 3; a++)
    {
        for(b = a + 1; b < 4; b++)
            {
                if(player[a].score < player[b].score)
                {
                    temp = player[a];
                    player[a] = player[b];
                    player[b] = temp;
                }
            }
    }

    // display
    puts("\nPlayer Info");
    printf("#\tName\tScore\n");
    for(x = 0; x < 4; x++)
    {
        printf("%d\t%s\t%5d\n", x+1, player[x].name, player[x].score);
    }
}
```
## 14.8
```c
#include <stdio.h>
#include <string.h>

int main()
{
    struct date
    {
        int month;
        int day;
        int year;
    };
    struct human
    {
        char name[45];
        struct date birthday;
    } president = {"George Washington", {2, 22, 1732}};

    printf("%s was born on %d/%d/%d\n",
            president.name,
            president.birthday.month,
            president.birthday.day,
            president.birthday.year);
}
```
## 14.9
```c
#include <stdio.h>
#include <string.h>

int main()
{
    struct id
    {
        char first[20];
        char last[20];
    };
    struct date
    {
        int month;
        int day;
        int year;
    };
    struct human
    {
        struct id name;
        struct date birthday;
    }president = {{"George", "Washington"}, {2, 22, 1732}};

    printf("%s %s was born on %d/%d/%d\n",
            president.name.first,
            president.name.last,
            president.birthday.month,
            president.birthday.day,
            president.birthday.year);
}
```
