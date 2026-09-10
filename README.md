# C Language – Complete Turbo C 
---

## PHASE 1: BASICS

### 1. Introduction to C / Program Structure

**Example 1 – Sabse pehla program**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    clrscr();
    printf("Hello, World!");
    getch();
}
```

**Example 2 – Comments ka use**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    clrscr();
    // Ye ek single line comment hai
    /* Ye multi line
       comment hai */
    printf("Comments seekh rahe hain");
    getch();
}
```

**Example 3 – Multiple statements**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    clrscr();
    printf("Line 1\n");
    printf("Line 2\n");
    printf("Line 3");
    getch();
}
```

---

### 2. Variables aur Data Types

**Example 1 – Basic variables**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int age = 20;
    float height = 5.9;
    char grade = 'A';
    clrscr();
    printf("Age: %d\n", age);
    printf("Height: %f\n", height);
    printf("Grade: %c", grade);
    getch();
}
```

**Example 2 – Double aur sizeof**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    double pi = 3.14159265;
    clrscr();
    printf("Pi value: %lf\n", pi);
    printf("Size of int: %d bytes\n", sizeof(int));
    printf("Size of float: %d bytes", sizeof(float));
    getch();
}
```

**Example 3 – Multiple variable declaration**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=5, b=10, c=15;
    clrscr();
    printf("a=%d b=%d c=%d", a, b, c);
    getch();
}
```

**Example 4 – Unsigned aur long**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    unsigned int u = 300;
    long l = 123456789;
    clrscr();
    printf("Unsigned: %u\n", u);
    printf("Long: %ld", l);
    getch();
}
```

---

### 3. Input/Output (printf, scanf)

**Example 1 – Ek number input**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int num;
    clrscr();
    printf("Enter a number: ");
    scanf("%d", &num);
    printf("You entered: %d", num);
    getch();
}
```

**Example 2 – Name aur age**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    char name[20];
    int age;
    clrscr();
    printf("Enter name: ");
    scanf("%s", name);
    printf("Enter age: ");
    scanf("%d", &age);
    printf("Name: %s, Age: %d", name, age);
    getch();
}
```

**Example 3 – Do numbers ka sum**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a, b;
    clrscr();
    printf("Enter two numbers: ");
    scanf("%d%d", &a, &b);
    printf("Sum = %d", a+b);
    getch();
}
```

---

### 4. Operators

**Example 1 – Arithmetic operators**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=15, b=4;
    clrscr();
    printf("Add: %d\n", a+b);
    printf("Sub: %d\n", a-b);
    printf("Mul: %d\n", a*b);
    printf("Div: %d\n", a/b);
    printf("Mod: %d\n", a%b);
    getch();
}
```

**Example 2 – Relational aur Logical operators**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=10, b=20;
    clrscr();
    printf("a>b: %d\n", a>b);
    printf("a<b: %d\n", a<b);
    printf("a==b: %d\n", a==b);
    printf("AND: %d\n", (a<b)&&(a>0));
    printf("OR: %d\n", (a>b)||(a>0));
    getch();
}
```

**Example 3 – Bitwise operators**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=5, b=3;
    clrscr();
    printf("AND: %d\n", a&b);
    printf("OR: %d\n", a|b);
    printf("XOR: %d\n", a^b);
    printf("Left shift: %d\n", a<<1);
    printf("Right shift: %d\n", a>>1);
    getch();
}
```

**Example 4 – Ternary operator**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int num=7;
    clrscr();
    (num%2==0) ? printf("Even") : printf("Odd");
    getch();
}
```

---

### 5. Type Conversion aur Type Casting

**Example 1 – Implicit conversion**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=5;
    float b=2.5;
    clrscr();
    printf("Result: %f", a+b);   // int automatically float ban jata hai
    getch();
}
```

**Example 2 – Explicit type casting**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    float f=9.7;
    int i;
    clrscr();
    i = (int)f;
    printf("After casting: %d", i);
    getch();
}
```

**Example 3 – Integer division problem fix**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=7, b=2;
    clrscr();
    printf("Without cast: %d\n", a/b);
    printf("With cast: %f", (float)a/b);
    getch();
}
```

---

## PHASE 2: CONTROL FLOW

### 6. Conditional Statements (if, if-else, switch)

**Example 1 – Simple if-else**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int num;
    clrscr();
    printf("Enter a number: ");
    scanf("%d", &num);
    if(num%2==0)
        printf("Even number");
    else
        printf("Odd number");
    getch();
}
```

**Example 2 – Nested if (largest of 3 numbers)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a,b,c;
    clrscr();
    printf("Enter 3 numbers: ");
    scanf("%d%d%d", &a, &b, &c);
    if(a>b)
    {
        if(a>c)
            printf("%d is largest", a);
        else
            printf("%d is largest", c);
    }
    else
    {
        if(b>c)
            printf("%d is largest", b);
        else
            printf("%d is largest", c);
    }
    getch();
}
```

**Example 3 – Switch case (grade calculator)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    char grade;
    clrscr();
    printf("Enter grade (A/B/C): ");
    scanf(" %c", &grade);
    switch(grade)
    {
        case 'A':
            printf("Excellent");
            break;
        case 'B':
            printf("Good");
            break;
        case 'C':
            printf("Average");
            break;
        default:
            printf("Invalid grade");
    }
    getch();
}
```

**Example 4 – Simple calculator using switch**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a,b;
    char op;
    clrscr();
    printf("Enter num1 operator num2: ");
    scanf("%d %c %d", &a, &op, &b);
    switch(op)
    {
        case '+': printf("%d", a+b); break;
        case '-': printf("%d", a-b); break;
        case '*': printf("%d", a*b); break;
        case '/': printf("%d", a/b); break;
        default: printf("Invalid operator");
    }
    getch();
}
```

---

### 7. Loops (for, while, do-while)

**Example 1 – for loop (1 se 10 tak print)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int i;
    clrscr();
    for(i=1; i<=10; i++)
        printf("%d ", i);
    getch();
}
```

**Example 2 – while loop (table print karna)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int n=5, i=1;
    clrscr();
    while(i<=10)
    {
        printf("%d x %d = %d\n", n, i, n*i);
        i++;
    }
    getch();
}
```

**Example 3 – do-while loop (sum of digits)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int num, sum=0, digit;
    clrscr();
    printf("Enter a number: ");
    scanf("%d", &num);
    do
    {
        digit = num%10;
        sum = sum+digit;
        num = num/10;
    } while(num!=0);
    printf("Sum of digits = %d", sum);
    getch();
}
```

**Example 4 – Nested loop (pattern printing)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int i,j;
    clrscr();
    for(i=1; i<=5; i++)
    {
        for(j=1; j<=i; j++)
            printf("* ");
        printf("\n");
    }
    getch();
}
```

---

### 8. break, continue, goto

**Example 1 – break statement**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int i;
    clrscr();
    for(i=1; i<=10; i++)
    {
        if(i==6)
            break;
        printf("%d ", i);
    }
    getch();
}
```

**Example 2 – continue statement**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int i;
    clrscr();
    for(i=1; i<=10; i++)
    {
        if(i%2==0)
            continue;
        printf("%d ", i);
    }
    getch();
}
```

**Example 3 – goto statement**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int i=1;
    clrscr();
    start:
        printf("%d ", i);
        i++;
        if(i<=5)
            goto start;
    getch();
}
```

---

## PHASE 3: FUNCTIONS

### 9. Functions Basics

**Example 1 – Function without parameters**
```c
#include<stdio.h>
#include<conio.h>
void greet();
void main()
{
    clrscr();
    greet();
    getch();
}
void greet()
{
    printf("Hello from function!");
}
```

**Example 2 – Function with parameters aur return value**
```c
#include<stdio.h>
#include<conio.h>
int add(int a, int b);
void main()
{
    int result;
    clrscr();
    result = add(5, 10);
    printf("Sum = %d", result);
    getch();
}
int add(int a, int b)
{
    return a+b;
}
```

**Example 3 – Function to check prime**
```c
#include<stdio.h>
#include<conio.h>
int isPrime(int n);
void main()
{
    int num;
    clrscr();
    printf("Enter a number: ");
    scanf("%d", &num);
    if(isPrime(num))
        printf("Prime number");
    else
        printf("Not a prime number");
    getch();
}
int isPrime(int n)
{
    int i;
    if(n<2) return 0;
    for(i=2; i<n; i++)
    {
        if(n%i==0)
            return 0;
    }
    return 1;
}
```

---

### 10. Call by Value vs Call by Reference

**Example 1 – Call by value (original change nahi hota)**
```c
#include<stdio.h>
#include<conio.h>
void change(int x);
void main()
{
    int a=10;
    clrscr();
    change(a);
    printf("Value in main: %d", a);
    getch();
}
void change(int x)
{
    x = 100;
}
```

**Example 2 – Call by reference (pointer ke through)**
```c
#include<stdio.h>
#include<conio.h>
void change(int *x);
void main()
{
    int a=10;
    clrscr();
    change(&a);
    printf("Value in main: %d", a);
    getch();
}
void change(int *x)
{
    *x = 100;
}
```

**Example 3 – Swap two numbers using call by reference**
```c
#include<stdio.h>
#include<conio.h>
void swap(int *a, int *b);
void main()
{
    int x=5, y=10;
    clrscr();
    printf("Before: x=%d y=%d\n", x, y);
    swap(&x, &y);
    printf("After: x=%d y=%d", x, y);
    getch();
}
void swap(int *a, int *b)
{
    int temp = *a;
    *a = *b;
    *b = temp;
}
```


---

### 11. Recursion

**Example 1 – Factorial using recursion**
```c
#include<stdio.h>
#include<conio.h>
long fact(int n);
void main()
{
    int num;
    clrscr();
    printf("Enter a number: ");
    scanf("%d", &num);
    printf("Factorial = %ld", fact(num));
    getch();
}
long fact(int n)
{
    if(n==0) return 1;
    return n*fact(n-1);
}
```

**Example 2 – Fibonacci using recursion**
```c
#include<stdio.h>
#include<conio.h>
int fib(int n);
void main()
{
    int i, n=10;
    clrscr();
    for(i=0; i<n; i++)
        printf("%d ", fib(i));
    getch();
}
int fib(int n)
{
    if(n==0) return 0;
    if(n==1) return 1;
    return fib(n-1)+fib(n-2);
}
```

**Example 3 – Sum of natural numbers using recursion**
```c
#include<stdio.h>
#include<conio.h>
int sum(int n);
void main()
{
    clrscr();
    printf("Sum = %d", sum(10));
    getch();
}
int sum(int n)
{
    if(n==0) return 0;
    return n+sum(n-1);
}
```

---

### 12. Storage Classes

**Example 1 – auto (default)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    auto int a=10;
    clrscr();
    printf("Auto value: %d", a);
    getch();
}
```

**Example 2 – static (value yaad rehta hai)**
```c
#include<stdio.h>
#include<conio.h>
void counter();
void main()
{
    clrscr();
    counter();
    counter();
    counter();
    getch();
}
void counter()
{
    static int count=0;
    count++;
    printf("Count = %d\n", count);
}
```

**Example 3 – global aur extern**
```c
#include<stdio.h>
#include<conio.h>
int x = 50;   // global variable
void display();
void main()
{
    clrscr();
    display();
    getch();
}
void display()
{
    extern int x;
    printf("Global x = %d", x);
}
```

---

## PHASE 4: ARRAYS AUR STRINGS

### 13. Arrays (1D, 2D)

**Example 1 – 1D array (numbers store aur print)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[5], i;
    clrscr();
    for(i=0; i<5; i++)
    {
        printf("Enter element %d: ", i+1);
        scanf("%d", &arr[i]);
    }
    printf("Array elements: ");
    for(i=0; i<5; i++)
        printf("%d ", arr[i]);
    getch();
}
```

**Example 2 – Array me largest number dhoondhna**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[5] = {12, 45, 3, 67, 21};
    int i, max=arr[0];
    clrscr();
    for(i=1; i<5; i++)
    {
        if(arr[i]>max)
            max = arr[i];
    }
    printf("Largest number = %d", max);
    getch();
}
```

**Example 3 – 2D array (matrix print)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int mat[2][3] = {{1,2,3},{4,5,6}};
    int i,j;
    clrscr();
    for(i=0; i<2; i++)
    {
        for(j=0; j<3; j++)
            printf("%d ", mat[i][j]);
        printf("\n");
    }
    getch();
}
```

**Example 4 – Two matrices ka addition**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a[2][2]={{1,2},{3,4}}, b[2][2]={{5,6},{7,8}}, c[2][2], i, j;
    clrscr();
    for(i=0; i<2; i++)
    {
        for(j=0; j<2; j++)
            c[i][j] = a[i][j]+b[i][j];
    }
    printf("Result matrix:\n");
    for(i=0; i<2; i++)
    {
        for(j=0; j<2; j++)
            printf("%d ", c[i][j]);
        printf("\n");
    }
    getch();
}
```

---

### 14. Strings aur String Functions

**Example 1 – String input aur length (strlen)**
```c
#include<stdio.h>
#include<conio.h>
#include<string.h>
void main()
{
    char str[50];
    clrscr();
    printf("Enter a string: ");
    gets(str);
    printf("Length = %d", strlen(str));
    getch();
}
```

**Example 2 – strcpy aur strcat**
```c
#include<stdio.h>
#include<conio.h>
#include<string.h>
void main()
{
    char str1[50]="Hello ", str2[50]="World", str3[50];
    clrscr();
    strcpy(str3, str1);
    strcat(str3, str2);
    printf("Copied+Concatenated: %s", str3);
    getch();
}
```

**Example 3 – strcmp (do strings compare karna)**
```c
#include<stdio.h>
#include<conio.h>
#include<string.h>
void main()
{
    char s1[20]="apple", s2[20]="banana";
    clrscr();
    if(strcmp(s1,s2)==0)
        printf("Strings are equal");
    else
        printf("Strings are not equal");
    getch();
}
```

**Example 4 – String ko reverse karna**
```c
#include<stdio.h>
#include<conio.h>
#include<string.h>
void main()
{
    char str[50];
    clrscr();
    printf("Enter a string: ");
    gets(str);
    strrev(str);
    printf("Reversed string: %s", str);
    getch();
}
```

---

## PHASE 5: POINTERS (C ka core concept)

### 15. Pointer Basics

**Example 1 – Address-of aur dereference operator**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=10;
    int *p;
    clrscr();
    p = &a;
    printf("Value of a = %d\n", a);
    printf("Address of a = %u\n", p);
    printf("Value using pointer = %d", *p);
    getch();
}
```

**Example 2 – Pointer se value change karna**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=5;
    int *p = &a;
    clrscr();
    *p = 50;
    printf("New value of a = %d", a);
    getch();
}
```

**Example 3 – NULL pointer**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int *p = NULL;
    clrscr();
    if(p==NULL)
        printf("Pointer is NULL, kisi ko point nahi karta");
    getch();
}
```

---

### 16. Pointer Arithmetic

**Example 1 – Pointer increment**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[5]={10,20,30,40,50};
    int *p = arr;
    clrscr();
    printf("First: %d\n", *p);
    p++;
    printf("Second: %d\n", *p);
    p++;
    printf("Third: %d", *p);
    getch();
}
```

**Example 2 – Pointer se poora array print karna**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[5]={1,2,3,4,5};
    int *p = arr, i;
    clrscr();
    for(i=0; i<5; i++)
    {
        printf("%d ", *(p+i));
    }
    getch();
}
```

**Example 3 – Difference between two pointers**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[5]={1,2,3,4,5};
    int *p1 = &arr[0];
    int *p2 = &arr[3];
    clrscr();
    printf("Difference = %d", p2-p1);
    getch();
}
```

---

### 17. Pointers aur Arrays ka Relation

**Example 1 – Array name khud ek pointer hai**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[3]={100,200,300};
    clrscr();
    printf("arr = %u\n", arr);
    printf("&arr[0] = %u\n", &arr[0]);
    printf("*arr = %d", *arr);
    getch();
}
```

**Example 2 – Array element access dono tareeko se**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[4]={5,10,15,20};
    int i;
    clrscr();
    for(i=0; i<4; i++)
        printf("arr[%d]=%d  *(arr+%d)=%d\n", i, arr[i], i, *(arr+i));
    getch();
}
```

**Example 3 – Character array aur pointer**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    char str[]="HELLO";
    char *p = str;
    clrscr();
    while(*p != '\0')
    {
        printf("%c", *p);
        p++;
    }
    getch();
}
```

---

### 18. Pointers to Pointers

**Example 1 – Double pointer basics**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=10;
    int *p = &a;
    int **pp = &p;
    clrscr();
    printf("a = %d\n", a);
    printf("*p = %d\n", *p);
    printf("**pp = %d", **pp);
    getch();
}
```

**Example 2 – Double pointer se value change**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int a=5;
    int *p=&a;
    int **pp=&p;
    clrscr();
    **pp = 99;
    printf("New a = %d", a);
    getch();
}
```

---

### 19. Function Pointers

**Example 1 – Simple function pointer**
```c
#include<stdio.h>
#include<conio.h>
int add(int a, int b) { return a+b; }
void main()
{
    int (*fp)(int, int);
    clrscr();
    fp = add;
    printf("Sum = %d", fp(5,10));
    getch();
}
```

**Example 2 – Function pointer array (calculator)**
```c
#include<stdio.h>
#include<conio.h>
int add(int a,int b){ return a+b; }
int sub(int a,int b){ return a-b; }
void main()
{
    int (*ops[2])(int,int) = {add, sub};
    clrscr();
    printf("Add: %d\n", ops[0](10,5));
    printf("Sub: %d\n", ops[1](10,5));
    getch();
}
```

---

### 20. Dynamic Memory Allocation (malloc, calloc, realloc, free)

**Example 1 – malloc se array banana**
```c
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
void main()
{
    int *p, i, n=5;
    clrscr();
    p = (int*)malloc(n*sizeof(int));
    for(i=0; i<n; i++)
        p[i] = i+1;
    for(i=0; i<n; i++)
        printf("%d ", p[i]);
    free(p);
    getch();
}
```

**Example 2 – calloc (zero-initialized memory)**
```c
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
void main()
{
    int *p, i, n=5;
    clrscr();
    p = (int*)calloc(n, sizeof(int));
    printf("Calloc se initial values (sab zero): ");
    for(i=0; i<n; i++)
        printf("%d ", p[i]);
    free(p);
    getch();
}
```

**Example 3 – realloc (memory size badalna)**
```c
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
void main()
{
    int *p, i;
    clrscr();
    p = (int*)malloc(3*sizeof(int));
    for(i=0; i<3; i++) p[i]=i+1;
    p = (int*)realloc(p, 5*sizeof(int));
    for(i=3; i<5; i++) p[i]=i+1;
    for(i=0; i<5; i++)
        printf("%d ", p[i]);
    free(p);
    getch();
}
```

---

## PHASE 6: STRUCTURES AUR UNIONS

### 21. Structures

**Example 1 – Basic structure (student record)**
```c
#include<stdio.h>
#include<conio.h>
struct Student
{
    char name[30];
    int roll;
    float marks;
};
void main()
{
    struct Student s1;
    clrscr();
    printf("Enter name: ");
    scanf("%s", s1.name);
    printf("Enter roll: ");
    scanf("%d", &s1.roll);
    printf("Enter marks: ");
    scanf("%f", &s1.marks);
    printf("\nName: %s\nRoll: %d\nMarks: %.2f", s1.name, s1.roll, s1.marks);
    getch();
}
```

**Example 2 – Structure with function**
```c
#include<stdio.h>
#include<conio.h>
struct Point { int x, y; };
void display(struct Point p);
void main()
{
    struct Point p1 = {10, 20};
    clrscr();
    display(p1);
    getch();
}
void display(struct Point p)
{
    printf("x=%d, y=%d", p.x, p.y);
}
```

**Example 3 – Nested structure**
```c
#include<stdio.h>
#include<conio.h>
struct Date { int day, month, year; };
struct Employee
{
    char name[20];
    struct Date doj;
};
void main()
{
    struct Employee e1 = {"Ravi", {15, 8, 2020}};
    clrscr();
    printf("Name: %s\n", e1.name);
    printf("Date of Joining: %d/%d/%d", e1.doj.day, e1.doj.month, e1.doj.year);
    getch();
}
```

---

### 22. Unions

**Example 1 – Basic union**
```c
#include<stdio.h>
#include<conio.h>
union Data
{
    int i;
    float f;
    char c;
};
void main()
{
    union Data d;
    clrscr();
    d.i = 10;
    printf("i = %d\n", d.i);
    d.f = 22.5;
    printf("f = %.2f (ab i ki value bigad gayi)", d.f);
    getch();
}
```

**Example 2 – sizeof union vs structure**
```c
#include<stdio.h>
#include<conio.h>
union U { int a; float b; char c; };
struct S { int a; float b; char c; };
void main()
{
    clrscr();
    printf("Size of union: %d\n", sizeof(union U));
    printf("Size of structure: %d", sizeof(struct S));
    getch();
}
```

---

### 23. Structures with Pointers, Array of Structures

**Example 1 – Structure pointer**
```c
#include<stdio.h>
#include<conio.h>
struct Student { char name[20]; int roll; };
void main()
{
    struct Student s1 = {"Amit", 101};
    struct Student *p = &s1;
    clrscr();
    printf("Name: %s\n", p->name);
    printf("Roll: %d", p->roll);
    getch();
}
```

**Example 2 – Array of structures**
```c
#include<stdio.h>
#include<conio.h>
struct Student { char name[20]; int marks; };
void main()
{
    struct Student s[3] = {{"A",80},{"B",90},{"C",70}};
    int i;
    clrscr();
    for(i=0; i<3; i++)
        printf("%s scored %d\n", s[i].name, s[i].marks);
    getch();
}
```

---

### 24. typedef aur enum

**Example 1 – typedef ka use**
```c
#include<stdio.h>
#include<conio.h>
typedef unsigned int uint;
void main()
{
    uint age = 25;
    clrscr();
    printf("Age = %u", age);
    getch();
}
```

**Example 2 – enum basics**
```c
#include<stdio.h>
#include<conio.h>
enum Day {Mon, Tue, Wed, Thu, Fri, Sat, Sun};
void main()
{
    enum Day today;
    clrscr();
    today = Wed;
    printf("Day number = %d", today);
    getch();
}
```

---

## PHASE 7: FILE HANDLING

### 25. File Operations (fopen, fclose, fread, fwrite, fprintf, fscanf)

**Example 1 – File me likhna (fprintf)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    FILE *fp;
    clrscr();
    fp = fopen("data.txt", "w");
    fprintf(fp, "Hello, ye file handling hai!");
    fclose(fp);
    printf("File me data likh diya gaya");
    getch();
}
```

**Example 2 – File se padhna (fscanf)**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    FILE *fp;
    char data[100];
    clrscr();
    fp = fopen("data.txt", "r");
    fscanf(fp, "%[^\n]", data);
    printf("File se data: %s", data);
    fclose(fp);
    getch();
}
```

**Example 3 – File me append karna**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    FILE *fp;
    clrscr();
    fp = fopen("data.txt", "a");
    fprintf(fp, "\nYe naya line hai");
    fclose(fp);
    printf("Naya data add ho gaya");
    getch();
}
```

---

## PHASE 8: ADVANCED / LOW-LEVEL CONCEPTS

### 26. Preprocessor Directives (macros)

**Example 1 – #define ka use**
```c
#include<stdio.h>
#include<conio.h>
#define PI 3.14
void main()
{
    float r=5;
    clrscr();
    printf("Area = %.2f", PI*r*r);
    getch();
}
```

**Example 2 – Macro with parameters**
```c
#include<stdio.h>
#include<conio.h>
#define SQUARE(x) ((x)*(x))
void main()
{
    clrscr();
    printf("Square of 6 = %d", SQUARE(6));
    getch();
}
```

**Example 3 – Conditional compilation**
```c
#include<stdio.h>
#include<conio.h>
#define DEBUG 1
void main()
{
    clrscr();
    #if DEBUG
        printf("Debug mode ON");
    #else
        printf("Debug mode OFF");
    #endif
    getch();
}
```

---

### 27. Bitwise Operations aur Bit Manipulation

**Example 1 – Check if number is even/odd using bitwise**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int n=15;
    clrscr();
    if(n & 1)
        printf("Odd number");
    else
        printf("Even number");
    getch();
}
```

**Example 2 – Ek bit set karna**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int n=5;
    clrscr();
    printf("Before: %d\n", n);
    n = n | (1<<1);   // 2nd bit set karna
    printf("After: %d", n);
    getch();
}
```

**Example 3 – Number ke bits count karna**
```c
#include<stdio.h>
#include<conio.h>
void main()
{
    int n=13, count=0;
    clrscr();
    while(n)
    {
        count += n & 1;
        n >>= 1;
    }
    printf("Set bits count = %d", count);
    getch();
}
```

---

### 28. Command Line Arguments (argc, argv)

**Example 1 – Arguments count aur print karna**
```c
#include<stdio.h>
#include<conio.h>
void main(int argc, char *argv[])
{
    int i;
    clrscr();
    printf("Total arguments = %d\n", argc);
    for(i=0; i<argc; i++)
        printf("Argument %d: %s\n", i, argv[i]);
    getch();
}
```

**Example 2 – Do numbers command line se add karna**
```c
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
void main(int argc, char *argv[])
{
    int a, b;
    clrscr();
    if(argc==3)
    {
        a = atoi(argv[1]);
        b = atoi(argv[2]);
        printf("Sum = %d", a+b);
    }
    else
        printf("2 numbers do command line par");
    getch();
}
```

---

### 29. Linked List (Data Structure in C)

**Example 1 – Simple linked list create aur print karna**
```c
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
struct Node
{
    int data;
    struct Node *next;
};
void main()
{
    struct Node *head, *second, *third;
    clrscr();
    head = (struct Node*)malloc(sizeof(struct Node));
    second = (struct Node*)malloc(sizeof(struct Node));
    third = (struct Node*)malloc(sizeof(struct Node));

    head->data = 10;
    head->next = second;
    second->data = 20;
    second->next = third;
    third->data = 30;
    third->next = NULL;

    struct Node *temp = head;
    while(temp != NULL)
    {
        printf("%d -> ", temp->data);
        temp = temp->next;
    }
    printf("NULL");
    getch();
}
```

**Example 2 – Linked list me naya node insert karna (beginning me)**
```c
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
struct Node { int data; struct Node *next; };
struct Node *head = NULL;
void insert(int val)
{
    struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = val;
    newNode->next = head;
    head = newNode;
}
void main()
{
    struct Node *temp;
    clrscr();
    insert(30);
    insert(20);
    insert(10);
    temp = head;
    while(temp != NULL)
    {
        printf("%d -> ", temp->data);
        temp = temp->next;
    }
    getch();
}
```

---

### 30. Compilation Process (Concept)

**Example – Compilation ke steps samajhne ke liye program**
```c
#include<stdio.h>
#include<conio.h>
/*
   Compilation 4 steps me hoti hai:
   1. Preprocessing - #include, #define resolve hote hain (.i file)
   2. Compiling     - C code Assembly code me convert hota hai (.s file)
   3. Assembling    - Assembly code Machine/Object code banta hai (.obj file)
   4. Linking       - Object code + libraries jud ke Executable banta hai (.exe file)
*/
void main()
{
    clrscr();
    printf("Ye program khud ek example hai ki upar wale 4 steps se guzarta hai");
    getch();
}
```

---

## Extra Tips (Padhaane ke liye)

- Har program compile karke turant run karwayein — output dekhna sabse zyada samajh deta hai.
- `getch()` aur `clrscr()` sirf **Turbo C** me kaam karte hain. Modern compiler (GCC, Code::Blocks, VS Code) me inki jagah `system("pause")` ya kuch nahi bhi use kar sakte, aur `void main()` ki jagah `int main()` + `return 0;` likhna hoga.
- Pointers aur recursion do baar padhayein — ek baar concept ke liye, doosri baar sirf practice ke liye.
- Har phase ke baad chhota quiz ya coding test lein taaki concept clear hue ya nahi pata chale.

---
*Document banaya gaya: C Language sikhane/padhane ke liye complete roadmap, Turbo C style examples ke saath.*
