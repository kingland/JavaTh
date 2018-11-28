## Exception Handling
กลไกในการจัดการโฟล์การทำงาน เมื่อเกิดข้อผิดพลาดที่ตอนรันไทม์ (run time)
### Checked Exception
คลาสในกลุ่มนี้จะสืบทอดจากคลาส **Throwable** แต่จะยกเว้น คลาส **RuntimeException** และ **Error** ที่ไม่ได้อยู่ในกลุ่ม จะถูกตรวจสอบข้อผิดพลาดตอนคอมไฟล์ (compile time)
### Unchecked Exception
คลาสในกลุ่มนี้จะสืบทอดจากคลาส **RuntimeException** ข้อผิดพลาดจะถูกตรวจสอบตอนรันไทม์ (runtime)
### Error
คลาสในกลุ่มจะสอบทดสจากคลาส **Error** เมือเกิดข้อผิดพลาดจะส่งผลให้ระบบหรือโปรแกรมต้องหยุดการทำงาน (irrecoverable)
## Example Exception
### ArithmeticException
```java
int a = 50/0; //ArithmeticException
```
### NullPointerException
```java
String s=null;   
System.out.println(s.length()); //NullPointerException   
```
### NumberFormatException
```java
String s="abc";    
int i=Integer.parseInt(s); //NumberFormatException
```
### ArrayIndexOutOfBoundsException
```java
int a[]=new int[5];   
a[10]=50; //ArrayIndexOutOfBoundsException 
```
## Try-Catch
```java
public class TryCatch{ 
    public static void main(String args[]){ 
        try{  
            int data=50/0;      
        }
        catch(ArithmeticException e){
            System.out.println(e);
        }     
        System.out.println("rest of the code..."); 
    }   
}
```
```java
public class MultipleCatch{     
    public static void main(String args[]){ 
        try{ 
            int a[]=new int[5];  
            a[5]=30/0;  
        }
        catch(ArithmeticException e){
            System.out.println("task1 is completed");	
        }
        catch(ArrayIndexOutOfBoundsException e){
            System.out.println("task 2 completed");
        } 
        catch(Exception e){
            System.out.println("common task completed");
        }
        System.out.println("rest of the code...");
    }   
} 
```
## Exception propagation 
ข้อผิดพลาด (Exception) จะถูกส่งผ่านจากด้านบนสุดของ สแต๊ค (stack) ไปเรื่อยจะกว่าจะถึงด้านล่างสุด หรือจนกว่าจะมีการจัดการกับข้อผิดพลาด
```java
class TestExceptionPropagation{ 
    void m(){
        int data=50/0;     
    }   

    void p(){
        try{
            n();
        } catch(Exception e) {
            System.out.println("exception handled");
        }
    }    
    public static void main(String[] args) {
        TestExceptionPropagation obj = new TestExceptionPropagation();
        obj.p();
        System.out.println("normal flow..");
    }
}
```
## Throws Exception
```java
import java.io.IOException;

public class ThrowsException {
    void m() throws IOException{
        //checked exception
        throw new IOException("device error");
    }

    void n() throws IOException {
        m();
    }

    void p() {
        try{
            n();
        } catch (Exception e){
            System.out.println("exception handle");
        }
    }

    public static void main(String[] args) {
        ThrowsException obj = new ThrowsException();
        obj.p();
        System.out.println("normal flow...");
    }
}
```
```java
import java.io.IOException;

class Method {
    void method() throws IOException {
        throw new IOException("device error");
    }
}

public class ThrowsException {
    public static void main(String[] args) {
        try{
            Method m = new Method();
            m.method();
        } catch (Exception e){
            System.out.print("exception handle");
        }

        System.out.print("normale flow");
    }
}
```
## Exception VS MethodOverride 
ซุปเปอร์คลาส (superclass) ไม่มีการโยนข้อผิดพลาด (exception) ออกมาจากฟังก์ชัน ฟังก์ชั่นเดียวกันของซับคลาส (subclass) จะต้องไม่กำหนดการโยนข้อผิดพลาด (exception) หรือกำหนดได้แต่ต้องไม่เป็นประเภท checked exception
```java
import java.io.IOException;

class Parent {
    void msg(){
        System.out.println("parent");
    }
}

class Child extends Parent {
    //compile time exception
    void msg() throws IOException{
        System.out.println("child");
    }

    public static void main(String[] args) {
        Parent p = new Child();
        p.msg();
    }
}
```
```java
class Parent {
    void msg(){
        System.out.println("parent");
    }
}

class Child extends Parent {
    void msg() throws ArithmeticException{
        System.out.println("child");
    }

    public static void main(String[] args) {
        Parent p = new Child();
        p.msg();
    }
}
```
ซุปเปอร์คลาส (superclass) ไม่มีการโยนข้อผิดพลาด (exception) ออกมาจากฟังก์ชัน ฟังก์ชั่นเดียวกันของซับคลาส (subclass) ควรจะมีการโยนข้อผิดพลาด (exception) เหมือนกับ ซุปเปอร์คลาส (superclass) หรือ ไม่มีก็ได้
```java
class Parent {
    void msg() throws ArithmeticException{
        System.out.println("parent");
    }
}

class Child extends Parent {
    //compile time error
    void msg() throws Exception{
        System.out.println("child");
    }

    public static void main(String[] args) {
        Parent p = new Child();
        p.msg();
    }
}
```
```java
class Parent {
    void msg() throws ArithmeticException{
        System.out.println("parent");
    }
}

class Child extends Parent {
    void msg(){
        System.out.println("child");
    }

    public static void main(String[] args) {
        Parent p = new Child();
        p.msg();
    }
}
```
```java
class Parent {
    void msg() throws Exception{
        System.out.println("parent");
    }
}

class Child extends Parent {
    void msg() throws ArithmeticException{
        System.out.println("child");
    }

    public static void main(String[] args) {
        Parent p = new Child();
        p.msg();
    }
}
```
## Custom Exception 
สร้าง Exception ที่ใช้งานเฉพาะได้ดังนี้
```java
class InvalidAgeException extends Exception {
    InvalidAgeException(String str){
        super(str);
    }
}

class CustomException {
    static void validate(int age) throws InvalidAgeException {
        if(age < 18){
            throw new InvalidAgeException("not valid");
        } else {
            System.out.println("Welcome to vote");
        }
    }
    public static void main(String[] args) {
        try {
            validate(13);
        } catch(Exception e){
            System.out.println("Exception occured: "+e);
        }
        System.out.println("reset of the code");
    }
}
```
