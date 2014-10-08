java.lang
=========   
Here, you will find java.lang API classes & their details.   
All java.lang programs are covered [Here](https://github.com/mjalleda/Java/tree/master/Javaassignment/src/Assign2_javalang)

**java.lang APIs**  
[1: Class  API & Object API]  
[2: Enum]  
[3: String API]  
[4: string buffer API and StringBuilder API]  
[5: Cleanable and Comparable]  
[6: Wrapper APIs/Classes]   
[7: Math Class/API]
[8: Autoboxing and Autounboxing]  
[9: System API/class]

*****************************************************************************  
**1: Class API & Object API**  
1: Multiple Inheritance  
2: HashCode  
3: “Class” class OR “Class API”:  
4: Why do we need to create an object in order to return a class’s methods or properties.   
5: What is the difference between a class and Class API:  
6: Create a method with classname.

**1: Multiple inheritance:**  Object is a super class of any java class .All the predefined classes are user defined classes. They either directly or indirectly extends java.lang.objectclass.  
For every class parent class in object class. Take below example. A is child and B is parent class. Where A is extending B class. But B extends Object class directly/indirectly. That means, java supports multilevel inheritance.  
Object Class > Class B > Class A.  

       Class A extends B {  
       // code   
       }
       Class B extends Object {  
       // code   
       }


**2: Hashcode:** In generally, all objects/variables/all stores in memory. System provides an id to each object in memory for identification. This id is called hashcode. All objects/classes/variables contains hashcode. 

| 1234444        |      34333      |  4444888 | 9843549 |
| ------------- |-------------| -----|------------|
| Obj1 | obj2 |obj3 | obj4 |

The following are called hashcodes. 1234444,  34333,  4444888 & 9843549.  
Object.hashcode – to return hashcode for a object  
Object.string – the string representation of hashcode of an Object  
Object.clone – to make a copy of object  
Object.Equal – to compare hashcodes of two objects and return Boolean results true or false  
Object.finalize – to clean up the garbage collection.

Note: Here, Object is a class and all above are methods. You can also override these methods. For ex:  
Equal only compares hashcodes of two objects. It doesn’t compare two object properties and methods.   
So if you need it to compare values then you need to override Equal() method.

**3: “Class” Class OR “Class API”:** Java also have an API for “Class”. It has many properties and methods.   
Rule1: You need to tell this API  for which class you want to return methods/properties.  For ex: If you create classA, classB and so on…Provide classname to Class Class. i.e.,  
Class s = Class.forName(“classA”);  // Class is a return type and Class is JAVA API    
s.getPackage();  
s.getClass();  
s.getFields();  
s.getInterfaces(); // if any interface this class implements.  
s.IsAbstract(); r // return if class is abstract class. True or false

**4: Why do we need to create an object in order to return a class’s methods or properties.**  Basically in order to return a class properties and methods, we need to first store them in memory and should point a reference to that memory location. So here object points to that memory location and returns the properties and methods of a class.

Note: you need to add the below code to method where are you create an object for the Class API.  
throws ClassNotFoundException  
For ex:    
        public static void  main(String args[]) throws ClassNotFoundException {    
         Class c = Class.forName("Remove");  
         System.out.println(c.getPackage());  
         String abc = c.getName();  
         System.out.println(abc);  
        }

**5: What is the difference between a class and Class API:** class is a keyword to declare/create a class. for ex: public class PublicA {}  
But Class API is a Java API which has properties and methods like any other class but which are defined by sun not by user. But in class user can declare all his properties and behaviors.

**6: Create a method with classname.**  
Every time method should tell what is the return type whether it is void or int or char. So it can also  tell the return type is a classt ype, that means the method returns an object for that class.

        Public classA {   // class A   
         int a;  
         char name;  
         int id;  
        }

        Public classB { // Class B  
         classB method() { // creating a method of classtype (this return an object)  
          classA Obj1 = new classA(); // creating object for classA  
          obj1.a = 10; 			// initializing values  
          obj1.name = ‘n’;  
          obj1.id = 100;  
          return obj1;		// returning object. A single obj contains 							multiple values.	  
        }

       Public static void main(String args[]) // Main method inside classB  
       {  
        ClassB obj2 = new ClassB;  		//creating object for classB   
        classA obj1 = obj2.method();		// calling classB method, that means you want to hold method’s behavior and           properties in obj1.   
        System.out.println(obj1.id+””+obj1.name+””+obj1.id);  
      }

It should print   
10  
N  
100

******************************************************************************
**2: ENUM**  
1: Enum is collection of constants. For ex: If I want to define to get/store input/output data, I can provide filepath/variable as a constant that never changes. For ex: if I have the same kind of requirement 20 times, instead of writing all 20 variables, I can just define them in one Enum variable and call that variable everywhere in my classes (with classname.enum.constant).  
2: We can create Enum constructor also.   
3: There are multiple methods are implemented on enum like iterator, hasNExt, values, getenum.   
4: Enum is widely used in switch class.

********************************* *************************************
**3: Strings & 4: string buffer,StringBuilder**    

Sub-Topics:  
1: String API:  
2: Difference between: String constant pool and Heap memory.   
3: How they uses memory:  
4: Difference between String API and string buffer API.   
5: Why to use String buffer why not String?  
6: What is mutable:   
7: Why String builder is introduced when String and string buffer are there:

**1: String API:**  There are three different types of String APIs. String API, string buffer API and String Builder API. Don’t get confuse between String API and regular datatype String. Both are different.  
We can create objects of string type. For ex:  
String s = new String(“laxmi”);  //  Here s is object, with this object you can get all String API methods.  
Or you cal also define  
String s = “laxmi”. Here you are not using primitive String datatype not API class. Here s1 is not object so you won’t get String API methods with S1 variables.  
Why do we need String API methods. For ex: If you want to compare, concatenate, equal two strings first you need to create objects for them and then can use all these methods. 

String is nothing but collection of characters. It is an API class so it has some methods. We can use them.   
All three APIs get stored into heap memory only.  
Syntax:  
String s = new String(“laxmi”);  
string buffer sb = new string buffer(“laxmi”);  
Stringbuilder sbd = new Stringbuilder(“laxmi”);

**2: Difference between: String constant pool and Heap memory.**   
Java uses both String constant pool and heap memory. String API objects uses heap memory and regular string variables uses String constant pool memory.   
1: String s = new String(“laxmi”);  
2: String s1 = “Laxmi”.   
1st one stores in heap memory with reference s.   
2nd stores in string constant pool memory. 

**3: How they uses memory:** Take a scenario with 4 variables/objects.  
String S1 = new String(“laxmi”);  
String S2 = new String(“Laxmi”);

String S3 = “Laxmi”;  
String s4 = “Laxmi”;  

**4: Difference between String API and string buffer API.** Both are string API classes only both are stored in heap memory only. But when you modify String object, JVM will create a new object in the memory and garbage collect the old one. In case of string buffer JVM will modify the existing object the new object is not created whenever string buffer object is modified. That’s why it is advisable to use string buffer if you keep change/modify string values, because it will not create new object every time, just modify the existing object.  Indirectly for better memory management use string buffer not String.

**5: Why to use String buffer why not String?** If you are constantly modifying string value, so it is advisable to use string buffer not string type. Since there are two advantages with string buffer
Better memory management
String is immutable where string buffer is mutable.

**6: What is mutable:** you can modify an object value within same memory location instead of creating a new object in memory. 

**7: Why String builder is introduced when String and string buffer are there:**  
String and String buffer are not synchronized but where String builder is synchronized  
Multiple processor can’t access string buffer objects at same time

The behavior of these three APIs are very different when you apply API methods on it. For ex: Equal method. Please check assignment for it.

***************************************************************************
**5: Cloneable And Comparable**   
Comparable: We are going to learn this in Sets & Maps.  
Cloneable:   
Cloneable is a interface, a class needs to implement this interface in order to use this.
This is used to clone a object and its methods and properties. Basically creating another object of an object. There are so many methods that we can execute on cloneable. 

***************************************************************************
**6: Wrapper APIs**    

Any Assignment created: Yes  
Program name:   
Javalang_WrapperClass.java  
Javalang_StringToPrimitiveToWrapper.java

**1: Why java introduced Wrapper classes:**
Primitive data types are not object oriented programming., as they used in other nonOOPs  languages like C.
For serialization. (What is serialization: Refer to audio of Jan19th).  
There are not programming methods to conversion in primitive types. Where wrapper classes have good conversion methods.

**2: What is serialization:**  If you two difference machines on a network and you want to send java code to another machine.  You need to send this thru files. For that you need to create objects cant send variables directly. So you can’t use primitive datatypes. When you collect all objects into a file and send it to another machine is called serialization and when the 2nd end machine receives the file, it de-serialize the file and gets the data in form objects.

**3: Diagram Explanation:**   
1: Primitive --> String  & String -->  Primitive  
2: String --> Wrapper  & Wrapper --> Primitive  
3: Primitive --> Wrapper  & Wrapper --> Primitive

Note: Before 1.5, java didn’t support on converting primitive to wrapper and wrapper to primitive.  In java 1.5 you can directly convert primitive to wrapper classes & wrapper to primitive type.  But in cases 1 & 2, you still have to use methods only.

*****************************************************************************
**7: Math class api**   
API Index: http://docs.oracle.com/javase/1.4.2/docs/api/index.html  
1: The Math class serves as a grouping of mathematical functions and constants.  
2: It is interesting to note that all the variables and methods in Math are static, and  the Math class itself is final.   
3: This means you can’t derive new classes from Math. Additionally, you can’t instantiate the Math class

*****************************************************************************
**8: AutoBoxing & AutoUnBoxing**   
AutoBoxing: Automatic conversion by the compiler from primitive type to the corresponding object form/wrapper form is called AutoBoxing.  
Ex: int i=10; //Compile time error in 1.4 but valid in 1.5  
Integer I=i;   
Compiler first constructs the integer object and then assigned that object to the variable.  

**AutoUnBoxing:**  
Automatic conversion from wrapper class object to primitive type by the compiler is called AutoUnBoxing.  
Ex: Integer I= new Integer(10);  
int i= I; //CTE :1.4  
// valid in 1.5s

*****************************************************************************
**9: System class**      
1: Both classes System and Runtime provides runtime environment resources(properties & behaviors) for your programs  2: Like Math API, System class is also final and is entirely composed of static variables and methods.   
3: The System class basically provides a system-independent programming interface to system resources. Examples of system resources include the standard input and output streams, System.in and System.out, which typically model the keyboard and monitor.  
4: When runtime system first starts up, the system properties are initialized to contain information about the runtime environment like the current user, the current version of the Java runtime, and even the character used to separate components of a filename.  
5: System properties only define inside a method not at class level.
Below is a complete list of the system properties you get when the runtime system first starts up and what they mean: 

**Key Meaning**  
file.separator --------- File separator (e.g., "/")  
java.class.path--------- Java classpath  
java.class.version ------Java class version number  
java.home -------------Java installation directory  
java.vendor ------------Java vendor-specific string  
java.vendor.url ---------Java vendor URL  
java.version ------------ Java version number  
line.separator -----------Line separator  
os.arch -----------------Operating system architecture  
os.name --------------- Operating system name  
path.separator --------Path separator (e.g., ":")  
user.dir ---------------User's current working directory  
user.home -------------User home directory  
user.name--------------User account name  
