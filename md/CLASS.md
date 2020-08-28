## การตั้งชื่อ (Naming)
### ชื่อคลาส (Class Name)
* ควรเป็น `คำนาม` (noun) 
* ขึ้นต้นด้วยอักษรตัวใหญ่ 
* ตัวอย่าง **String**, **Color**, **Button**, **System**, **Thread** 
### ชื่ออินเทอร์เฟซ (Interface Name)
* ควรเป็น `คำคุณศัพท์` (adjective) 
* ขึ้นต้นด้วยอักษรตัวใหญ่ 
* ตัวอย่าง **Runnable**, **Remote**, **ActionListener** 
### ชื่อเมธอร์ด (Method Name)
* ควรเป็น `คำกริยา` (verb) 
* ขึ้นต้นด้วยตัวอักษรตัวเล็ก 
* ตัวอย่าง **actionPerformed()**, **main()**, **print()**, **println()** 
### ชื่อตัวแปร (Variable Name)
* ควรเป็นคำที่ขึ้นต้นด้วยตัวอักษรตัวเล็ก 
* ตัวอย่าง **firstName**, **orderNumber** 
### ชื่อแพ็คเกจ (Package Name)
* ควรเป็นคำที่ขึ้นต้นด้วยตัวอักษรตัวเล็ก 
* ตัวอย่าง **java**, **lang**, **sql**, **util** 
### ค่าคง (Contant Name)
* ควรเป็นอักษรตัวใหญ่ทั้งหมด 
* ตัวอย่าง **RED**, **YELLOW**, **MAX_PRIORITY** 
## ออปเจ็ค และ คลาส (Object & Class)
### ออปเจ็ค ทำไรบ้าง
* กำหนดสถานะ (state)
* กำหนดฟังก์ชันทำงาน (behavior)
* กำหนดไอดี (unique id)  ผู้ใช้งานโดยทัวไปจะไม่เห็นค่าดังกล่าว (hashcode)
### คลาส ประกอบด้วย
* **ฟิลด์** (Field) เก็บสถานะการทำงาน
* **เมธอร์ด** (Method) ฟังก์ชันการทำงาน
* **คอนทรัคเตอร์** (Constructor) เมธอร์ดที่มีชื่อเหมือนกันคลาส ใช้กำหนดค่าเริ่มต้นในการทำงาน
* **ฺบล็อค** (Block) บรรจุคำสั่งต่างๆ
* **เนทส์ คลาส** (Nested Class) 
* **อินเทอร์เฟซ** (Interface)
## คีย์เวิร์ด Static 
การประกาศตัวแปรแบบ static สามารถลดการใช้งานเมมโมรีลงได้ ส่วนที่จะนำ static ไปใช้ได้ประกอบด้วย
* **ตัวแปร** (variable)
* **เมธอร์ด** (method)
* **บล็อค** (block)
* **เนทส์ คลาส** (Nested Class)
### Static Method
* ถูกประกาศไว้ในคลาส
* สามารถเรียกใช้งานโดยไม่ต้องสร้างออปเจ็คของคลาส
* เข้าถึงและเปลี่ยนค่าตัวแปรที่เป็น static ได้
### Static Block
* กำหนดค่าเริ่มต้นให้ตัวแปร
* ถูกเรียกในงานในขั้นตอนโหลดคลาส (ก่อนมีการเรียกใช้เมธอร์ด main)
```java
public class Main{   
	static{       
		System.out.println("static block is invoked");       
		//System.exit(0);     
	}   
	static String str = "word";   
	public static void main(String[] args){     
		System.out.println(“Hello Java”);      
		System.out.println(Thread.currentThread().getName());   
	} 
} 
```
สามารถรันโปรแกรมโดยไม่มีเมธอร์ด main ในเวอร์ชันก่อน JDK 7 โดยใช้ static block
```java
class Main{     
	static{     
		System.out.println("static block is invoked");     
		System.exit(0);     
	}   
} 
```
## คีย์เวิร์ด This
* อ้างอิงถึงอินสแตนซ์ของออปเจ็คที่งานอยู่ในปัจจุบัน
* เรียกเมธอร์ดของอินสแตนซ์ปัจจุบันที่ทำงานได้
* เมธอร์ด this() เป็นการเรียกใช้งานคอนตรัคเตอร์
* เรียกเมธอร์ด ผ่าน this สามารถใส่ค่าอากิวเมนต์
* เรียกคอนตรัคเตอร์ ผ่าน this สามารถใส่ค่าอากิวเมนต์
* รีเทิร์น this รีเทิร์นอินสแตนซ์ของออปเจ็คที่งานอยู่ในปัจจุบัน (pass by reference)
## การสืบทอด Inheritance
เป็นกลไกในการนำส่วนที่ซ้ำกันของโปรแกรมมาใช้งาน (reuse) ลดความซ้ำซ้อน
### ทำไมต้องมี 
* เมธอร์ด โอเวอไรส์ (method overide)
* นำส่วนที่ซ้ำกันของโปรแกรมมาใช้งาน (reuse)
```java
class Employee {     
	float salary=40000;   
}   
 
class Programmer extends Employee {     
	int bonus = 10000;     
	public static void main(String args[]){      
		Programmer p = new Programmer();      
		System.out.println("Programmer salary is:"+p.salary);      
		System.out.println("Bonus of Programmer is:"+p.bonus);     
	}   
} 
```
## คีย์เวิร์ด Final
ส่วนที่สามารถนำไปใช้งาน
* **ตัวแปร** (Variable)
* **เมธอร์ด** (Method)
* **คลาส** (Class)
### Final variable
* ไม่สามารถเปลี่ยนแปลงข้อมุลได้หลังจากมีกำหนดค่าเริ่มต้น
* การกำหนดค่าสามารถทำได้ผ่านคอนทรัคเตอร์
* ถ้าเป็นตัวแปรแบบ static สามารถกำหนดค่าได้ผ่าน static block
```java
final int speedlimit=90; //final variable 
```
### Final method
* ไม่สามารถ overide เมธอร์ด
```java
//final method
final void run(){ System.out.println("running..."); }    
```
### Final class
* ไม่สามารถสืบทอดคลาส ไปยังคลาสอื่น
```java
//final class 
pubilc final class Bike9{
}
```
