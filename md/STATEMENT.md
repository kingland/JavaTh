## If Statement
```java
if (condition){   
	//code if condition is true   
}
```
## If-Else Statement
```java
if (condition) {   
	//code if condition is true   
} else {   
	//code if condition is false  
}
```
```java
if (condition1) {   
	//code to be executed if condition1 is true   
} else if (condition2) {   
	//code to be executed if condition2 is true   
} else if (condition3) {   
	//code to be executed if condition3 is true   
} else {   
	//code to be executed if all the conditions are false   
}
```
## Switch Statement
```java
switch (expression) {         
	case value1:          
		//code to be executed;          
		break;  //optional       
	case value2:          
		//code to be executed;          
		break;  //optional      
	//......                  
	default:           
		//code to be executed if all cases are not matched;     
} 
```
## For Statement
**for (`initialization`;  `condition`; `incr/decr`)**
```java
for (int i=1;i<=10;i++){           
	System.out.println(i);   
}
```
## For Each Statement
**for (Type var : array)**
```java
int arr[]={12,23,44,56,78};
for(int i:arr){
	System.out.println(i);
} 
```
## Infinitive For Statement
```java
for(;;){      
	System.out.println("infinitive loop");   
}
```
## While Statement
**while(condition)**
```java
int i=1;   
while(i <= 10){    
	System.out.println(i);    
  i++;   
}
```
## Do-While Statement
```java
int i=1;   
do{       
	System.out.println(i);       
	i++;   
} while(i<=10);
```
## Break Statement
```java
for(int i=1; i<=10; i++){    
	if(i == 5){     
		break;    
	}    
	System.out.println(i);   
} 
```
## Continue Statement
```java
for(int i=1; i<=10; i++){ 
	if(i==5){
		continue;
	}
	System.out.println(i);
}
```
## Comment
* **Single Line**
```java
//This is single line comment 
```
* **Multi Line**
```java
/*      
 This is multi line comment      
 This is multi line comment     
 This is multi line comment     
 */ 
```
* **Documention**
```java
/**      
* This is document comment      
* @param str      
* @return      
*/ 
```
