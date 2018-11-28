## I/O
### Stream
ลำดับข้อมูล(ไบท์)ที่เรียงกัน 
* **`System.out`** ส่งข้อมูลออก โดยดีฟอลต์จะออกที่จอภาพ
* **`System.in`** รับข้อมูลเข้า
* **`System.err`** แสดงข้อผิดพลาด
```java
System.out.println("simple message");
System.err.println("error message");
```
### OutputStream
โปรแกรมจาวาใช้งาน **OutputStream** ในการเขียนข้อมูล เช่น ไฟล์, อาร์เรย์, ซ็อกเก็ต (socket)

### InputStream
โปรแกรมจาวาใช้งาน  InputStream ในการอ่านข้อมูล เช่น ไฟล์, อาร์เรย์, ซ็อกเก็ต (socket)

### FileOutputStream
การส่งออกข้อมูลพื้นฐาน (primitive value) หรือ ข้อมูลที่เป็นไบท์ (byte oriented) เขียนไฟล์ (ข้อมูลตัวอักษร (character oriented) จะใช้ **FileWriter** ในการเขียนไฟล์)

### FileInputStream
การนำเข้าข้อมูลพื้นฐาน (primitive value) หรือ ข้อมูลที่เป็นไบท์ (byte oriented) จากไฟล์ (ข้อมูลตัวอักษร (character oriented) จะใช้ **FileReader** ในการนำเข้า)

### BufferedOutputStream
เพื่อประสิทธิภาพที่ดีกว่าในการเขียนข้อมูล จาวามีคลาส **BufferedOutputStream** ช่วยทำบัฟเฟอร์ (buffer) ซึ่งดีกว่าเขียนข้อมูลโดยตรง

### BufferedInputStream
เพื่อประสิทธิภาพที่ดีกว่าในการอ่านข้อมูล  จาวามีคลาส **BufferedInputStream** ช่วยทำบัฟเฟอร์ (buffer) ซึ่งดีกว่าอ่านข้อมูลโดยตรง

### SequenceInputStream
อ่านข้อมูลจากหลาย Stream แต่จะทำงานตามลำดับ

### ByteArrayOutputStream
คลาสช่วยเขียนไฟล์หลายไฟล์พร้อมกัน ข้อมูลถูกเขียนในรูปแบบไบท์อาร์เรย์ (byte array) ก่อนที่ส่งให้ Stream อื่นๆ

### ByteArrayInputStream
คลาสช่วยในการอ่านข้อมูลไบท์อาร์เรย์ (byte array) ในรูปแบบ Stream

### DataOutputStream
คลาสที่ช่วยในการเขียนข้อมูลพื้นฐาน (primitive value) และเป็นอิสระไม่ขึ้นกับระบบ (machine independent)

### DataInputStream
คลาสที่ช่วยในการอ่านข้อมูลพื้นฐาน (primitive value) และเป็นอิสระไม่ขึ้นกับระบบ (machine independent)

### Console
คลาสที่ช่วยอ่านค่าข้อมูลจาก คอนโซล ซึ่งเตรียมฟังก์ชันที่ใช้ในการอ่าน ข้อความ (text) และ รหัสผ่าน (password)

### FilePermission
คลาสที่ช่วยอ่าน Permission (read, write, execute) จากไฟล์หรือไดเรคทอรี่

### FileWriter
การส่งออกข้อมูลที่เป็นตัวอักษร (charecter oriented) เขียนไฟล์ 

### FileReader
การอ่านข้อมูลที่เป็นตัวอักษร  (charecter oriented)

### BufferWriter
เพื่อประสิทธิภาพที่ดีกว่าในการเขียนข้อมูลประเภทตัวอักษร (charecter oriented) จาวามีคลาส **BufferWriter** ช่วยทำบัฟเฟอร์ (buffer) ซึ่งดีกว่าเขียนข้อมูลโดยตรง

### BufferReader
เพื่อประสิทธิภาพที่ดีกว่าในการอ่านข้อมูลประเภทตัวอักษร (charecter oriented) จาวามีคลาส **BufferReader** ช่วยทำบัฟเฟอร์ (buffer) ซึ่งดีกว่าอ่านข้อมูลโดยตรง

### CharArrayReader
คลาสช่วยในการอ่านข้อมูล คาเรคเตอร์อาร์เรย์ (character array) ในรูปแบบ Stream

### CharArrayWriter
คลาสช่วยเขียนไฟล์หลายไฟล์พร้อมกัน ข้อมูลถูกเขียนในรูปแบบคาเรคเตอร์อาร์เรย์ (byte array) มีการสร้างบัฟเฟอร์ (buffer) ให้อัตโนมัติก่อนที่ส่งให้ Stream

### PrintStream
คลาสช่วยเขียนไฟล์ไปยัง Stream อื่น PrintStream จะทำการ ฟลัชข้อมูลในอัตโนมัติ โดยไม่ต้องเรียกฟังก์ชัน flush()

### PrintWriter
คลาสช่วยเขียน ข้อความ ไปยัง text-output Stream

### StringReader

### StringWriter


