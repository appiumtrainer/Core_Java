EXCEPTIONS:
==============  
Exceptions topics you will find below.   
All exceptions programs are covered [Here](https://github.com/mjalleda/Java/tree/master/Javaassignment/src/Assign4_exceptions)

**Index**  
**1: Exceptions:**  
1. What is exception:  
2. Exception Hierarchy:  
3. Calling an object with their superclass names  
4. Types of exceptions: Errors & Exceptions.  
5. Checked & Unchecked exceptions.  
6. How to generate unchecked exceptions:   
7. Checked exceptions are:  
8. Custom exceptions:   
9. Purpose/Example of custom exceptions  

**2: Throw & Throws.**  
1. Throws:   
2. Purpose of Throws:  
3. Throw:   
4. Throws with Method Overrding :   
5. Throws with Constructor Overrding :   
6. Difference between Catch and Throws  
7. Difference between Throws & Throw  

**3: Try, Catch & Finally**  
1. Try and catch block:   
2. Catch block  
3. Finally block  
4. Valid & Invalid combination scenarios  
5. What is the purpose of having multiple catches :   
6. Rule

*****************************************************************************
**1:: Exceptions:**  
**1: What is exception:**  
- 1: Unwanted unexpected event occurred while running, this is called exception.  
- 2: When exception occurs, runtime will stop execute the code where execution occurs.   
- 3: So we need to catch the exception and tell the complier to continue with next lines of the code.  
- 4: Every time JVM returns exception, it definitely return below parameters
Exception name, description and position.  
- 5: Exception looks like - Exception in thread "main" java.lang.ArithmeticException: / by zero at com.sample.exercise5_exceptions.exercise1_exception_arithmeticone.main(exercise1_exception_arithmeticone.java:12). In above example, Name is   Exception in thread "main" java.lang.ArithmeticException: / 
Description is by zero at com.sample.exercise5_exceptions.exercise1_exception_arithmeticone.m
Position is exercise1_exception_arithmeticone.java:12).  
- 6: Usually, java maintains a runtime stack to display printing statements on console. Whenever it runs code it runs from this stack and after running it empties the stack. For any reason, stack get full it stops the code execution and return stack overflow error.  
- 7: Since JVM maintains runtime stack so it displays exceptions on console.   
- 8: There are two different types of exceptions – Errors & Exceptions. Errors are non-recoverable & Exceptions are recoverable.

**2: Exception Hierarchy:**


**3: Calling an object with their superclass names**  
- 1: In this diagram Object is a superclass.  
- 2: Throwable is subclass of Object class  
- 3. Errors & Exceptions are subclass of throwable  
- 4. VMError, leakage error and assertion errors are subclass of throwable.  
- 5. out of memory errors and stack overflow memory error are subclasses of VMerror, etc. So, Out of memory error > VMerror > Error > Throwable > Object. If you want to call Out of memory error you can also call with its parents. For ex:
you can call Out of memory error object O with its superclasses also.   
Catch (Out of memory error O) { }; OR  
Catch (VMerror O) { }; OR  
Catch (Error O) { }; OR    
Catch (Throwable O) { }; OR  
Catch (Object O) { };

**4: Types of exceptions:**  
**Errors & Exceptions.**  
1: Are also called non-recoverable, that means you can’t catch them. That means, if non-recoverable error occurs, code will stop executing it ( may be it will crash ).  
2: Exception: are also called re-coverable, that means you can write catch them. But exception again  two types. Checked & Unchecked.

**5: Checked & Unchecked exceptions.**
Checked: Complier checks if any exceptions occurred and it immediately tells the user there is an checked exception. 
Unchecked: The exception will not checked by compiler are called unchecked exception. Basically, runtime will catch these exceptions and prints exception in console.

**6: How to generate unchecked exceptions:**  
1: Arithmetic exception: 10/0 – which is not possible, it returns arithmetic exception  
2: Nullpointer exception: Without completing object creation process, you can’t initialize an object. It returns nullpointer exception.  
3: IllegalstateException:  
4: IllegalArgumentException:  
5: ClasscastException:  
6: IndexOutofBoundException:  is two types.   
- ArrayIndexOutOfBound  
- StringIndexOutofBound: 

**7: Checked exceptions:** Are,  
1: SQL Exception  
2: Remote exception  
3: ClassnotFoundException  
4: IO Exception exception – it is three types:   
- EndofFile  
- Filenotfound  
- InteruptedIO

**8: Custom exceptions:**  
1: user defined exceptions are called custom exceptions.   
2: We can inherit/extend java defined exceptions.   
3: Custom exceptions always contains constructors with parametrized type.   
4: You can only pass String datatype as arguments, you can’t pass anyothers.  
5: Why string type only: Since basically, you want to replace the exception description with your custom message, message takes String Datatype not int, float..or others. So we use only String Datatype.  
6: You can write custom exception in a class type and call them in different classes.  
7: important exception methods are   
- e.printstacktrace – to print all exception message  
- e.getmessage – to print only exception description  
- e.String – to print position and position description. 

**9: Purpose/Example of custom exceptions**      
For ex: In banking application, customer should always maintain $500  minimum balance. For ex: while doing internal transaction you want to check if a/c minimum balance after transaction is done. If not, throw a exception. So,  you need to write a custom exception for it and throw a message “a/c should have minimum $500 and can’t process this transaction”.

******************************************************************************					
**2:  Throw & Throws**
**1: Throws:**  
1: Throws is used only with exceptions.    
2: we use throws keyword at signature level and not inside method. That means, we use throws for class, method and constructor signatures.  
3: When exception occurs, we either have to catch Or tell the method caller to catch it.   
4: So we use try/catch block to catch exceptions, but throws is used to tell the method caller to catch it and handle it.  
5: We use throw & throws with custom exceptions too.

**2: Purpose of throws:**  
When exception occurs, we either have to catch it or tell the method caller to catch it. So we use try/catch block to catch exceptions, but throws is used to tell the method caller to catch it and handle it.  
If you aren’t sure if exception occurs or not, in that case you can use throws keyword. Basically tell the compiler to handle the exception at caller level.

**3: Throw:** Throws is a keyword used inside method. Basically to throw custom exceptions. We can call custom exceptions by creating an object to its class (where custom exception is defined). So this is not used at signature level.  These are also used with in methods.    
In two ways, we can use these.   
1: Either write throw in try block and handle it in catch block.   
OR  
2: If you are not putting in try&catch block, then add throws to method signature. Since when throw occurs, it can be returned inside a method it can't go outside, either you have to catch it or tell somebody to throw it outside. Hence we use throws keyword to throw a custom exception out of the method.

**4: Throws with Method Override:**  
Lets say you have two classes, parent and child. And child is going to override method which is defined in parent class.  
When you throws in both classes, then it should be:  
Subclass throws exception class can be either at same level/co-variant(parent-child) relationship of superclass’s throws exception class.  
Ex: My superclass is ClassA, child class is ClassB  
In classA  
Int m1(int a, int b) throws Exception { //code  }, then child class should be 

In classB:  
Int m1(int a, int b) throws Exception { //code } OR //Same level  
Int m1(int a, int b) throws Arithmetic Exception { //code } OR // co-variant level with parent’s exception

**5: Throws with Constructor Override :**  
Lets say you have two classes, parent and child. Lets say both have constructors.  
When you throws in both classes, then  
Rule is:  Subclass throws exception class can be either at same level/a level up (child-parent) relationship of superclass’s throws exception class.  
Ex: My superclass is ClassA, child class is ClassB  
In classA  
classA() throws Arithmetic Exception { //code  }, then child class should be   
In classB:  
ClassB() throws Arithmetic Exception { //code } OR //Same level  
ClassB() throws Exception { //code } OR //A level above.

Yes, it is opposite with method overriding.


**6: Difference between Catch and Throws**

| Catch        |      Throws      |
| ------------- |:-------------:|
|When exception occurs in try block, control jumps to catch block and handle the exception over here.|If a method/class is defined with throws keyword, then control goes to the caller who called this parent/method.|
|After handling the exception in catch block, control executes next lines of code|Here, if none of parent classes are not handling the generated exception, then JVM will stop executing the code at line where the exception occurred.|
|Basically, catch wants to handle the exception|Here, parent/method says I don’t want to handle it, who ever calls me, let them handle it.|
|Basically, next lines of code will execute since you are handling it in catch block|The next lines of code will break if caller doesn’t handle it|

**7: Throws VS Throw.**

| Throws        |      Throw      |
| ------------- |-------------|
|Throws is used while defining method signature or class signature. That means, who ever calls this method/class, they have to handle the exception, if JVM is the caller then JVM needs to handle it.|Throw is mostly used to throw custom exceptions. Basically if this happens throw my own exception.  It can also return predefined exception but what is the use, jvm also returns predefined exceptions.|
||1: Either write throw in try blcok and handle it in catch block.OR 2: If you are not putting in try&catch block, then add throws to method signature. Since when throw occurs, it can be returned inside a method it can't go outside, either you have to catch it or tell somebody to throw it outside. Hence we use throws keyword to throw a custom exception out of the method.|
|This works only with method/class.|This is only used inside a method|
|For ex: Public parent throws Exception|throw e;|
|Both are used only with exceptions Exception|Both are used only with exceptions

******************************************************************************   					
**Try, catch & Finally**

**1: Try and catch block:** If you know some code generates exception write that danger code in try block and if that code returns any exception capture that in catch block. Basically after catch block, control goes to next line of catch block.

**2: Catch block:** If any exception occurs in try block, then only control goes to catch block otherwise it won’t go to catch block. If code has no catch block then it continues to the next line after try.

**3: Finally block:** If code has all three try, catch & finally. It doesn’t matter if try block has exception or not, when control goes to try block, it will definitely go to finally block. So opposite to catch block since if try block has exception then only control goes to catch block.

**4: Valid & Invalid Combinations:**  
If code has,  
- Only try block – not valid  
- Only catch block – not valid  
- Only finally block – not valid

**4.1: Try with single catch**  
- Combination1: try & catch block – valid  
- Combination2: try & finally block –valid  
- Combination3: All three try, catch & finally –valid  
- Combination4: catch & finally  - not valid.

**4.2: Try with multiple catches**  
- Combination1: try & multiple catches blocks – valid  
- Combination2: try, multiple catches & finally –valid  
- Combination3: try & multiple finally blocks – not valid

**4.3: Order of Try, catch & Finally.**  
- Order1: Try --> catch --> finally – is valid  
- Order 2: Try --> catch1 --> catch2 --> catch3--> finally – Valid  
- Order 3: Try --> finally  --> catch1 --> catch2 --> catch3  – NOT valid  
- Order 4: Try --> catch1 --> catch2 --> finally --> catch3 –  NOT Invalid

**4.4: Order with allowed exceptions** (relation should be parent to child “co-variant”)  
For above orders:  
**Order1:**   
try --> Arithmetic catch block 1 --> nullpointerCatchblock 2 == Is valid (since they both are defined at same level in library, since both are children for Exception)

**Order2:**   
try --> ExceptionCatchblock1 --> Arthemetch catch block 2 --> nullpointerCatchblock 3 == Is valid (since they both are defined as “co-variant” level, parent first and then children)

**Order3:**   
try -->  Arithmetic catch block 1 --> ExceptionCatchblock1 == Is NOT valid (since they both are not defined as “co-variant” level or same level. Child(arithmetic Exception) is coded before Parent (Exception).)

**5: What is the purpose of having multiple catches :**   
1: This is widely used   
2: Scenario1: We are not sure if the code in try block returns nullpointer or arithmetic or arrayIndex….so when you don’t know what it returns, so how would you catch multiple exceptions ? So you need multiple catch blocks. One for nullpointer, one for arithmetic and one for arrayIndex..  
2.1: You may ask instead of writing all three catches, you can write a single catch with Exceptions (since this is parent for all three) ? Yes, it is valid, if you don’t know what will return, you can write a single catch with Exceptions.  
3: Scenario 2: We are not sure if the code in try block returns nullpointer or arithmetic or arrayIndex….so when you don’t know what it returns, so how would you catch multiple exceptions ? So you need multiple catch blocks. One for nullpointer, one for arithmetic and one for arrayIndex. For ex: When control gets to arithmetic catch block, you want to extend the code (from try block) inside arithmetic catch block. If you want to do this for all three exception, it might not be possible to put all three in one single Exception catch block, so it is better to code three catch blocks, one for each exception.   
3.1: You may ask instead of extending the logic in all three catches, you can write a single catch with Exception (since this is parent for all three) ? No. For ex: if nullpointer exception not occurred but you extended logic for it, it might break the code somewhere else. If you want to extend the logic better to write its own catch block for that exception.

**6: Rule:** If you have multiple catches, control execute them in the order (top to bottom).   
For ex:  You have three catch blocks (for arithmetic, nullpointer and arrayIndex). Let’s say their order is   
Try {}     
catch (nullpointerexception e) {}  
catch (arrayIndexexception e3) {}   
catch (arithmetic e) {}   
Lets say, try block has some danger code and it generated arithmetic exception.   
First control goes to first catch block, and it finds its not arithmetic exception catch block.  
Later control goes to second catch block, it finds its is not arithmetic exception catch block.  
Later control goes to third catch block, it finds it finds it is arithmetic exception catch block and executes the code.
