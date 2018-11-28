## Unary 
* **`postfix`** -> expr++,  expr--
* **`prefix`**  -> ++expr,  --expr,  +expr,  -expr,  !,  ~ 
```java
int x=10;   
System.out.println(x++); 
System.out.println(++x); 
System.out.println(x--); 
System.out.println(--x); 
```
```text
//output

```
```java
int a = 10;   
int b = -10;   
boolean c = true;   
boolean d = false;   
System.out.println(~a);//-11 (minus of total positive value which starts from 0)   
System.out.println(~b);//9 (positive of total minus, positive starts from 0)   
System.out.println(!c); 
System.out.println(!d); 
```
```text
//output

```
## Arithmetic
* **`multiplicative`** -> *,  /, %
* **`additive`** -> +, -
```java
int a = 10;   
int b = 10;   
System.out.println(a++ + ++a);   
System.out.println(b++ + b++);
```
```text
//output

```
```java
int a=10;   
int b=5;   
System.out.println(a+b);  
System.out.println(a-b); 
System.out.println(a*b); 
System.out.println(a/b); 
System.out.println(a%b); 
System.out.println(10*10/5+3-1*4/2); 
```
```text
//output

```
## Shift
* **shift** -> <<, >>, >>>
```java
System.out.println(10<<2);   
System.out.println(10<<3); 
System.out.println(20<<2); 
System.out.println(15<<4);
System.out.println(10>>2); 
System.out.println(20>>2);   
System.out.println(20>>3); 
//For positive number, >> and >>> works same   
System.out.println(20>>2);   
System.out.println(20>>>2);   
//For nagative number, >>> changes parity bit (MSB) to 0   
System.out.println(-20>>2);   
System.out.println(-20>>>2); 
```
```text
//output

```
## Relational
* **Comparison** -> <, >, <=, >=, instanceof 
* **Equality** -> ==, !=
## Bitwise
* **And** -> &
* **Exclusive Or** -> ^
* **Inclusive Or** -> |
## Logical
* **And** -> &&
* **Or** -> ||
```java
int a=10;   
int b=5;   
int c=20;   
System.out.println(a<b && a<c);  
System.out.println(a<b & a<c);
```
```text
//output

```
```java
int a=10;   
int b=5;   
int c=20;   
System.out.println(a<b && a++<c);   
System.out.println(a); //** 
System.out.println(a<b & a++<c); 
System.out.println(a); //** 
```
```text
//output

```
```java
int a=10;   
int b=5;   
int c=20;    
System.out.println(a>b || a++<c); 
System.out.println(a); //** 
System.out.println(a>b | a++<c); 
System.out.println(a); //** 
```
```text
//output

```
```java
short a=10;   
short b=10;   
a=a+b; 
System.out.println(a); 
```
```text
//output

```
```java
short a=10;   
short b=10;   
a=(short)(a+b); 
System.out.println(a);
```
```text
//output

```
## Ternary
* **Ternary** -> ?:
```java
int i = 0;
boolean t = t > 0 ? true : false;
System.out.println(t);
```
```text
//output

```
## Assignment
* **Assignment** -> =, +=, -=, /=, %=, &=, ^=, |=, <<=, >>=, >>>=
```java
int i = 10;
int j = 20;
i += j;
System.out.println(i);
```
```text
//output

```
