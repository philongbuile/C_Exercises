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
## Bonus 3
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

# Chapter 15
## 15.1
 ```c
 #include <stdio.h>

int main(int argc, char *argv[])
{
    if(argc>1)
        printf("Greetings, %s!\n",argv[1]);
    return(0);
}
```
## 15.2
```c
#include <stdio.h>

int main(int argc, char *argv[])
{
    printf("You typed %d arguments.\n",argc);
    return(0);
}
```
## 15.3
```c
#include <stdio.h>

int main(int argc, char *argv[])
{
    printf("You typed %d arguments.\n",argc);
    printf("Argument one is %s.\n",argv[0]);
}
```
## 15.4
```c
#include <stdio.h>

int main(int argc, char *argv[])
{
    int i;

    for(i = 0; i < argc; i++)
    {
        printf("Arg[%d] = %s\n", i + 1, argv[i]);
    }
}
```
## 15.5
```c
#include <stdio.h>
#include <stdlib.h>

void sub(void);

int main()
{
    puts("This program quits before it's done.");
    sub();
    puts("Or was that on purpose?");
}

void sub(void)
{
    puts("Which is the plan.");
    exit(0);
}
```
## 15.6
```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("Press Enter to clear the screen:");
    getchar();
    system("cls");
    puts("That's better");
    return(0);
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
