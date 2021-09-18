 # Chapter 3
## 3.1
Calculate (123 * 321 + 123) and print the result
```c
#include <stdio.h>

main ()
{
  printf("123 * 321 + 123 = %d\n",123 * 321 + 123);
}
```

# Chapter 4
## 4.1
Print this text
```
Are you going to Scarborough Fair?
Parsley, sage, rosemary, and thyme
Remember me to one who lives there
She once was a true love of mine
```
Answer:
```
#include <stdio.h>

int main()
{
    puts("Are you going to Scarborough Fair?");
    puts("Parsley, sage, rosemary, and thyme");
    puts("Remember me to one who lives there");
    puts("She once was a true love of mine");
}
```
## 4.2
Print this without using any variable:  
D:\[00] Upload\[00] Error\[PCCG-01351] "Shingeki no Kyojin" Original Soundtrack [24bit/48kHz].rar
```c
#include <stdio.h>

int main()
{
    printf("D:\\[00] Upload\\[00] Error\\[PCCG-01351] \"Shingeki no Kyojin\" Original Soundtrack [24bit/48kHz].rar");
}
```

# Chapter 5
## 5.1
Check whether 23 is divisible by 4
```c
#include <stdio.h>

int main()
{
    int result = 23 % 4;
    if(result == 0)
    {
        printf("23 is divisible by 4");
    }
    else
    {
        printf("23 is not divisible by 4");
    }
}
```
## 5.2
Print These Number:
```
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
## 5.3
Print These Number "Nicely":
```
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
# Chapter 14
## 14.1
Using struct to store data. 
This struct has 2 variables: 
 + Composer
 + Metadata  

Metadata is also a struct which has 3 variables:
 + Title
 + Catalog Number
 + Number of Tracks
Output:
```
Composer: Arai Ken
Catalog Number: VPCG-84988
Title: Kiseijuu Sei no Kakuritsu Original Soundtrack
Number of Tracks: 19
```
## 14.2
Find time difference using:
```
struct TIME
{
    int days;
    int hours;
    int minutes;
    int seconds;
};
```
Example
```
Input:
  Start: 9 days, 23 hours, 37 minutes, 58 seconds
  End: 14 days, 7 hours, 4 minutes, 27 seconds
Output:
  Time Difference: 4 days, 7 hours, 26 minutes, 29 seconds
```
Answer:
```c
#include <stdio.h>
#include <stdlib.h>

struct TIME
{
    int days;
    int hours;
    int minutes;
    int seconds;
};

struct TIME get_input(struct TIME time, char name[10])
{
    printf("%s.days = ", name);
    scanf("%d", &time.days);
    printf("%s.hours = ", name);
    scanf("%d", &time.hours);
    printf("%s.minutes = ", name);
    scanf("%d", &time.minutes);
    printf("%s.seconds = ", name);
    scanf("%d", &time.seconds);
    printf("~~~~~~~~~~~~~~~~~~~~~~~~~~~\n");

    return time;
}

void print_time(struct TIME time)
{
    printf("%d days, %d hours, %d minutes, %d seconds\n", time.days, time.hours, time.minutes, time.seconds);
}

struct TIME fix_format(struct TIME time)
{
    if(time.seconds >= 60)
    {
        time.seconds -= 60;
        time.minutes++;
    }

    if(time.minutes >= 60)
    {
        time.minutes -= 60;
        time.hours++;
    }

    if(time.hours >= 24)
    {
        time.hours -= 24;
        time.days++;
    }

    return time;
}

struct TIME calculate_diff(struct TIME start, struct TIME end)
{
    struct TIME temp;

    if(start.seconds > end.seconds)
    {
        end.seconds += 60;
        end.minutes--;
    }

    if(start.minutes > end.minutes)
    {
        end.minutes += 60;
        end.hours--;
    }

    if(start.hours > end.hours)
    {
        end.hours += 24;
        end.days--;
    }

    if(start.days > end.days)
    {
        printf("NANI KORE????");
        printf("\n~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
        exit(0);
    }

    temp.days = end.days - start.days;
    temp.hours = end.hours - start.hours;
    temp.minutes = end.minutes - start.minutes;
    temp.seconds = end.seconds - start.seconds;

    temp = fix_format(temp);

    return temp;
}

int main()
{
    // declare variables
    struct TIME start;
    struct TIME end;
    struct TIME diff;

    // get input
    start = get_input(start, "start");
    end = get_input(end, "end");

    // check the input
    start = fix_format(start);
    end = fix_format(end);

    // calculate time difference
    diff = calculate_diff(start, end);

    // display data
    printf("Start: ");
    print_time(start);
    printf("End: ");
    print_time(end);
    printf("Time Difference: ");
    print_time(diff);
    printf("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
}
```

# Chapter 15
## 15.1
Get a list of numbers from command line and calculate sum
Example:
```
  Input: 1 2 3
  Output: Sum = 6
```
Answer:
```c
#include <stdio.h>
#include <stdlib.h>

int i;

int main(int argc, char *argv[])
{
    int size = argc - 1;
    float sum;

    for (i = 0; i < size; i++)
    {
        sum += atof(argv[i + 1]);
    } 
    
    printf("Sum = %f", sum);
}
```
## 15.2
Get a list of numbers from command line and calculate Mean  
<img src="https://latex.codecogs.com/gif.latex?\dpi{120}&space;\bg_black&space;\huge&space;Mean&space;=&space;\frac{1}{N}\sum_{i=0}^{N}x_{i}" title="\huge Mean = \frac{1}{N}\sum_{i=0}^{N}x_{i}" />  
Example:
```
Input: 2 8 5 4 1 8
Output: 4.666667
```
Answer:
```
#include <stdio.h>
#include <stdlib.h>

int i;

int main(int argc, char *argv[])
{
    float sum;

    for (i = 0; i < argc - 1; i++)
    {
        sum += atof(argv[i + 1]);
    }

    printf("Mean = %f", sum / (argc - 1));
}
```
## 15.3
Get a list of numbers from command line and using the formula "Softmax function (stable)" to calculate:  
<img src="https://latex.codecogs.com/png.latex?\dpi{120}&space;\bg_black&space;\huge&space;m&space;=&space;max(x)" title="\huge m = max(x)" />  
<img src="https://latex.codecogs.com/png.latex?\dpi{120}&space;\bg_black&space;\huge&space;f(x_{i})&space;=&space;\frac{e^{(x_{i}-m)}}{\sum_{j}&space;e^{(x_{j}-m)}}" title="\huge f(x_{i}) = \frac{e^{(x_{i}-m)}}{\sum_{j} e^{(x_{j}-m)}}" />  
Example:
```
  Input:  1               2               3
  Output: 0.090031        0.244728        0.665241
```
Answer:
```c
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int i;

float max(float *X, int size)
{
    int result = X[0];
    for (i = 1; i < size; i++)
    {
        if (X[i] > result)
        {
            result = X[i];
        }
    }
    return result;
}

void stable_softmax(float *X, int size)
{
    double sum_exp;
    float exp[size];
    float maximum = max(X, size);

    for (i = 0; i < size; i++)
    {
        exp[i] = pow(M_E, X[i] - maximum);
        sum_exp += exp[i];
    }
    printf("\nResult:\n");
    for (i = 0; i < size; i++)
    {
        printf("%f\t", exp[i] / sum_exp);
    }
}

int main(int argc, char *argv[])
{
    int size = argc - 1;
    float arr[size];

    printf("Input:\n");
    for (i = 0; i < size; i++)
    {
        arr[i] = atof(argv[i + 1]);
        printf("%f\t", arr[i]);
    }
    stable_softmax(arr, size);
}
```

# Chapter 16
## 16.1
```c
#include <stdio.h>

int main()
{
    int a,b;
    float c;

    printf("Input the first value: ");
    scanf("%d",&a);
    printf("Input the second value: ");
    scanf("%d",&b);
    c = a/b;
    printf("%d/%d = %.2f\n",a,b,c);
    return(0);
}
```
## 16.2
```c
#include <stdio.h>

int main()
{
    int a,b;
    float c;

    printf("Input the first value: ");
    scanf("%d",&a);
    printf("Input the second value: ");
    scanf("%d",&b);
    c = (float)a/(float)b;
    printf("%d/%d = %.2f\n",a,b,c);
    return(0);
}
```
## 16.3
```c
#include <stdio.h>

typedef int stinky;

stinky main()
{
    stinky a = 2;

    printf("Everyone knows that ");
    printf("%d + %d = %d\n",a,a,a+a);
    return(0);
}
```
## 16.4
```c
#include <stdio.h>

int main()
{
    typedef struct id
    {
        char first[20];
        char last[20];
    } personal;

    typedef struct date
    {
        int month;
        int day;
        int year;
    } calendar;

    struct human
    {
        personal name;
        calendar birthday;
    };
    struct human president = {{"George","Washington"}, {2, 22, 1732}};

    printf("%s %s was born on %d/%d/%d\n",\
            president.name.first,
            president.name.last,
            president.birthday.month,
            president.birthday.day,
            president.birthday.year);
}
```
## 16.5
```c
#include <stdio.h>

void proc(void);

int main()
{
    puts("First call");
    proc();
    puts("Second call");
    proc();
    return(0);
}

void proc(void)
{
    int a;

    printf("The value of variable a is %d\n",a);
    printf("Enter a new value: ");
    scanf("%d",&a);
}
```
## 16.6
```c
#include <stdio.h>

void proc(void);

int main()
{
    puts("First call");
    proc();
    puts("Second call");
    proc();
    return(0);
}

void proc(void)
{
    static int a;

    printf("The value of variable a is %d\n",a);
    printf("Enter a new value: ");
    scanf("%d",&a);
}
```
## 16.7
```c
#include <stdio.h>

void half(void);
void twice(void);

int age;
float feet;

int main()
{
    printf("How old are you: ");
    scanf("%d",&age);
    printf("How tall are you (in feet): ");
    scanf("%f",&feet);
    printf("You are %d years old and %.1f feet tall.\n",age,feet);
    half();
    twice();
    printf("But you're not really %d years old or %.1f feet tall.\n",age,feet);
    return(0);
}

void half(void)
{
    float a,h;

    a=(float)age/2.0;
    printf("Half your age is %.1f.\n",a);
    h=feet/2.0;
    printf("Half your height is %.1f.\n",h);

}

void twice(void)
{
    age*=2;
    printf("Twice your age is %d.\n",age);
    feet*=2;
    printf("Twice your height is %.1f\n",feet);
}
```
## 16.8
```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

struct bot {
    int xpos;
    int ypos;
};

struct bot initialize(struct bot b);

int main()
{
    const int size = 5;
    struct bot robots[size];
    int x;

    srand((unsigned)time(NULL));

    for(x=0;x<size;x++)
    {
        robots[x] = initialize(robots[x]);
        printf("Robot %d: Coordinates: %d,%d\n",
               x+1,robots[x].xpos,robots[x].ypos);
    }
    return(0);
}

struct bot initialize(struct bot b)
{
    int x,y;

    x = rand();
    y = rand();
    x%=20;
    y%=20;
    b.xpos = x;
    b.ypos = y;
    return(b);
}
```
## 16.9
```c
#include <stdio.h>

int verify(int check);

int main()
{
    int s;

    printf("Enter a value (0-100): ");
    scanf("%d",&s);
    if(verify(s))
    {
        printf("%d is in range.\n",s);
    }
    else
    {
        printf("%d is out of range!\n",s);
    }
    return(0);
}

int verify(int check)
{
    enum { false, true };

    if(check < 0 || check > 100)
        return false;
    return true;
}
```
## 16.10
```c
#include <stdio.h>

int main()
{
    enum { SUN, MON, TUE, WED, THU, FRI, SAT };
    int day;

    printf("Enter a weekday number, 0 - 6: ");
    scanf("%d",&day);

    if( day < 0 || day > 6 )
    {
        puts("Invalid input");
    }
    else
    {
        switch(day)
        {
            case SUN:
                puts("Sunday");
                break;
            case MON:
                puts("Monday");
                break;
            case TUE:
                puts("Tuesday");
                break;
            case WED:
                puts("Wednesday");
                break;
            case THU:
                puts("Thursday");
                break;
            case FRI:
                puts("Friday");
                break;
            case SAT:
                puts("Saturday");
        };
    }
    return(0);
}
```
