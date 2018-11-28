## Type of Variable
* **local variable** ประกาศตัวแปรภายในเมธอร์ด
* **instance variable** ประกาศตัวแปรภายในคลาสแต่จะอยู่ด้านนอกเมธอร์ด
* **static varibale**  ตัวแปรที่ประกาศตัวคีย์เวิร์ด static
## Data Type in Java
### Primitive
Type | Default  | Bit Width
------ | -------| --------
boolean | false | 1
char   | \u0000 | 16
byte   | 0 | 8
short | 0 | 16
int  | 0 | 32
long  | 0 | 64
float | 0.0f | 32
double | 0.0f | 64
### Non Primitive
Type  |  Desc
------ | --------
String | ข้อความ
Array  | อาร์เรย์
All Class | คลาสอืนๆทุกคลาส
### Example
```java
int a = 10;
int b = 10;
System.out.println(a + b);
```
```text
//output

```
```java
int a = 10;   
float b = 20.0f;  
b = a; 
System.out.println(a + b);   
```
```text
//output

```
```java
int a = 10;   
float b = 20.0f; 
a = b;  
System.out.println(a + b);
```
```text
//output

```
```java
int a = 10;   
float b = 20.0f; 
a = (int) b;  
System.out.println(a + b); 
```
```text
//output

```
## Unicode System
จาวาใช้รหัสแบบ Unicode ทำให้สามารถรองรับได้หลายภาษา
* **`ASCII`** -สหรัฐ
* **`ISO 8859-1`** -ยูโรป
* **`KOI-8`** -รัสเซีย
* **`GB18030`** และ **`BIG-5`** -จีน
