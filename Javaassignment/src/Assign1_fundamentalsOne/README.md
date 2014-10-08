Core Java Fundamentals
======================
I only covered core java topics here. In this page, you will topics of Fundamentals chapter.     
You will find all fundamentals programs [Here](https://github.com/mjalleda/Core_Java/tree/master/Javaassignment/src/Assign1_fundamentalsOne)

**Fundamentals:**  
___________________  
1: DataTypes  
2: Identifiers:  
3: Literlas:  
4: Java Keywords:  
5: Variable types & thier scope:  
6: Arrays:  
7: Operators & Assignments:  
8: TypeCasting  
9: FlowControl or statements  
10: Coding Standards  
11: imports,package  
12: mainMethod,args  
13: Access Modifiers  
14: var-argMethod  
15: Abstract Class  
16: GarbageCollection  
17: Inner class  
18: Interface  
19: Assertions  
20: java execution flow  
21: super,this

******************************************************************************  
**1-3: DataTypes, Identifiers & Litersls:**  
Any programs created? Yes:
Program Name: Exer1_DataTypes.java

byte, short, int, long, char, float, double & Boolean. These are primitive datatypes regular datatypes which are used in other languages also. Since Java uses these too so java is not considered pure OOPS language. 
How java uses them: There are some wrappers are available they make primitive datatypes into objective datatypes. The wrappers are:
- Byte, Short, Integer, Long, Float, Double, Char and Boolean.   
- short, byte, int and long are also called numerical datatypes.  
- Float/double: If you don’t add ‘f’ at end of float value, java consider that value as double.  
- It is not possible to convert double to float but float to double is possible  

Default values  
- int – 0  
- boolean – false  
- char – space  
Char can only take single characters.   
- char my = ‘c’; /valid  
- char my = ‘char’ /not valid  
- String my = “char” /valid  
- String my = “c”; /valid  
String is not primitive data type. it is a class/API.  

Datatypes, identifies and literals.  
Int aim = 1000; Here,    
- Datatype is int  
- Identifier is aim  
- value/literal is 1000   

**2: Identifiers:**  
How to declare/define a identifier and its rules.  
Assignments: NO

**3: Literals:**   How to initialize a value/literal to all datatypes and their conversion  
Any programs created? No
******************************************************************************
**4: Java Keywords:**  
Keywords of each category.  
Any programs created? No  
**Break:** This is used to break the loop and come out of the loop. Basically, control goes out of the loop and start execute the next line out of the loop.  
**Continue:** Continue says, don’t execute next lines of the code inside this loop but go to first line of the code in the loop and start execute from there. Basically if you want to check the loop condition in between loop, you can use continue.

*****************************************************************************
**5: Variable types & their scope:**  
Any programs created? Yes  
1: Exer5_VariablesAndMethods_BothStaticAndInstance
2: Exer5_BothStaticInstanceVariablesAndMethodsSuperclass
3: Exer5_BothStaticInstanceVariablesAndMethodsSubclass

**Instance, static and Local & Final variables:**    
**Static variables:** will be declared only in class level not in method block, you can’t change static variable value but can access in both static and non static method

**Final variables:** If you prefix variable with final, then you can’t change its value later.   
final int m =100; // So this is also instance variable.

| Static|Instance|Local|
|-------------|-------------|-------------|
| Declared only at class level. Can't be declared in method level/block.| Declared at class level.| Declared only with in a block/method|
| Value of variable can't be changed|Value of variable can be changed| Variable can't be accessed without block so value cant be changed|
|Value of variable can't be changed | Value of variable can be changed|Variable can't be accessed without block so value cant be changed |  
|Can access everywhere including in static and non static methods | Can access only in non static methods. Static methods can't use instance variable.|Local variable can be used with in a block. Can't be accessed outside of a block |  
| It can be accessed directly, or by using object to that class, or by using classname.|To access instance variable outside the block. You need help of classname or object of that class. You can't call it directly. |it can't be accessed outside of the block. |  
|1: No need to initialize while declaring it, by default it get null/0 value. 2: Final static variables must be initialized before class loaded into memory. otherwise compile time error. i.e we can perform initialization for the final static variables at one of the following places. 1. at the time of declaration. 2. 2. inside the static initialization block. Example: final static int I; static{ int i=30; } | 1:  No need to initialize while declaring it, by default it get null/0 value. 2: But For the final instance variables ,we should perform initialization other wise compile time error. The final instance variable must be initialization before constructor compiles.i.e at the time of declaration or inside instance initialization block or inside constructor. Example: final int i; public static void main(String arg[]) { Sample s=new Sample() System.out.println(s.i); // invalid }| value needs to initialized before using it otherwise it will get CTE error|

******************************************************************************
**6: Arrays:**  
Arrays: declaration, initialization, construction  
Any programs created: yes  
Program Name: Exer6_ArraysDeclaration

*****************************************************************************
**7: Operators & Assignments:**  
Any programs created: No  
• equality(==,!=)  
• relational  
• bit-wise  
• short-circuit  
• instanceof  
• cast  
• conditional(?)  
• new  
• [ ]  
• Compound


****************************************************************************
**8. TYPE CASTING**  
**TypeCasting:** There are two types of typecasting.
  1: Primitive and  
  2: Objective.  
Both have again two types of categories. Implicit and explicit.   
Implicit means, JVM will take care while execution.  
Explicit means, you have to tell JVM when you code it.

**1: Primitive type casting:**  
byte --> short --> int --> long --> float --> double   
char --> int --> long --> float --> double  
That means, byte can directly convert into int. In above two diagram, jvm converts forward typecasting. That means, byte --> short, byte --> int, int --> float but not long --> int or int --> byte.

******************************************************************************
**9: Flow controls or statements:**    
Any programs created: No  
1: Selection statement : If-else & Switch  
2: Iteration statement : For, For-each, While, Do-while  
3: Transfer statement : Break, continue, return, try-catch-finally & assertion  
4: Do-while vs While: They are quite opposite  
5: While: As usual like others, it will check the condition first then execute the statement.  
6: Do-while: It is opposite to while. it executes the statement then checks the condition.

******************************************************************************
**10: Coding standards:**   
How to define name of classes, objects, variables,packages…  
Any programs created: No

******************************************************************************
**11: Import package:**     
Any programs created: No  
Basically here we talk about java source structure, the order is  
- Package statement  
- Import statement    
- Class/interface/enum declaration  
For ex:   
Package com.sample.one  
Import java.math;  
Public class superclass()  
{  
}  
Superclass inside “one”, One is inside “sample”, sample is inside “com”.  
Com > sample > one > Superclass.  
Superclass wants to inherit all math classes so it is importing.

******************************************************************************
**12: Main method**    
**Main method** : public static void main(String args[])  
Any programs created: No  
Public static void main(String args[])  
{  
}  
**Public:** We use public to give access to outsider of main. Since Java programs  
executed from main line, so JVM has to access main method, that means outsiders needs to access this. So main always should be public.  
**Static:** Using static we allocate some memory for main method. So it should be
always static. In any program language the code should be saved into memory with some references. In java, objects does this task, basically they allocate memory for methods/variables.  Since main method has no object so Static allocates memory for main method.    
**Void:** We don’t return anything from main, so its always void.  
**String args[]** : It means, main method is expecting array of strings. That means, for ex: if you are creating a website, then you want to user to enter dynamic values every time, then you can give array of strings.   
Create below class and then right click > run as > run configuration > arguments > enter 10 30 > then apply> then it will print 10 & 20 as output. 

	Class super  
         {
                Public static void main (String args[])
                {
      			System.out.println(args[0]);
      			System.out.println(args[1]);
    		}
		}

Output:  
10  
20

What if you don’t pass dynamic values: JVM will pass empty array or null.  
  System.out.println(args[0]);  
Output:  
Java.lang.string@1...9


******************************************************************************
**13: Access Modifiers/Access Specifiers**    
Below are called Access Modifiers:  
Public, Private, Protected, Default, static, final, abstract, strictfp, native  
Notes:   
- The allowed modifiers for the Top level classes are : 1.public 2.default 3. final 4.abstract 5. Strictfp, 6: Abstract    
- The allowed modifiers for the method level are 1.public 2.default 3. Private 4.protected 5. Final, 6: static 7: Abstract  
- The allowed modifiers for the variables  
- Final, public, protected, default, private and static.
For ex: Package 1 have class1 and class2. Package 2 contains : Class3 & Class4.

**1: Public:** Accessed everywhere (refer to diagram in the notes).   If public defined in class1, it can be accessed in class2, packag1, and all classed in packag2. 

**2: Private:** If it is defined in class1, it can be accessed only to class1, not to class2, or packag2. 
It is accessible within the block/class/method. Private not allowed for top level class.  That means, only for variable/methods. 

**3: Default:** By default, variables/methods/classes are available to within the package, not outside the package. If a class declared as the default ,we are allowed to access that class only with in the current package.outside package can’t access this. If a method declared as the default ,that member is visible with in the current package only.

**4: Protected:** This is accessible within the package + subclasses. It is not defined at class level. That means, only members/methods can define as protected.  

**5: Final:** Final means, you are making methods/classes as constants, that means you can’t override/extend them.  
**5.1: Rule1/Final class:** You can’t use extend keyword in subclass/other classes to call Final class. For ex: if Final class contains final methods, subclass don’t extend Final class, so that means there is no relationship between final class and subclass, so subclass can contain same signatures/methods of final methods in subclass. Here, we realized that final class can’t be extended in other classes.

**5.2: Rule 2/Final methods:** For ex, if concrete class ‘A’ contains final methods, if subclass ‘b’ extends class ‘A’, then it can’t override ‘final methods of A in B’. It will get an error. That means, you can’t override final methods. Here we realized that, a concrete class can contain final methods.   

**5.3: Rule 2/Final variables:** For ex, if concrete class ‘A’ contains final variables, if subclass ‘b’ extends class ‘A’, then it can’t re-initialize/override ‘final variables of A in B’. (Usually, you re-produce this error by 
Creating a parent reference in sub class, then try access final variables using the object, then it will show you the error.

So you don’t extend final class , then subclass may contain same signatures o

**5.4: Final Methods :** if you add final in front of methods, that method becomes constant and in other subclasses, these can be accessible but can’t be overide.

**5.5: Final classes:** If you add final in front of class, that class becomes constant and in other sub classes, these can be accessible by objects, but can’t create the child class.
We can implement security by final.

**6: Abstract**  
**6.1: Abstract with static method is not valid. Why?** 
Because, static means constant and you can’t change, but abstract means you can’t do implementation with in the method, so if you do implementation in different class first you need to access the method, since it is static you can’t change it. SO ABSTRACT STATIC METHOS IS NOT POSSIBLE.

**6.2: Abstract with final method is not valid. Why?**   
If a class declared as the abstract ,we should create the child class to provide implementation for abstract methods.  
If a class declared as the final ,you are not allowed to create the child class.Hence final and abstract combination is illegal for classes.

**7: Static:** The keyword static can be use for classes,methods, variables  
We can not apply static keyword for the top level classes,but we can apply inner classes.  
For every object a separate copy of instance variables will be created but in the case of static variables a single copy will be created at the class level and shared by all the objects of that class.

**8: Native:** Native means, you can use c/c++ code with in java class by making some configuration changes. But how to write c/c++ code in java.  For ex: There is a requirement that we need add Client API/Classes/code into our code, so our application can analyze client's data. But client code is in c/C++ and ours is in Java. How is it possible?
Basically, java allow a method called ‘addLibrary’. If you keep the client code in local machine, then you can add that api into our java program by ‘addLibrary’ method.  
If you know a method exists in C/C++ api, then you can define that method with native. 

**9: Strictfp:** Basically you are strictly maintaining a structure for floating point variables.   
Why it is introduced? : Before java 1.4, floating point variables to take 32 bits if OS is 32 bit OS, otherwise it takes 64bits if OS is 64bit OS. Code may not run if you run the 32 bit code on 64 bit and vise versa.
To avoid this problem, java introduced Strictfp. Basically we define Strcitfp for classes not for methods or variables. Inside that class, all floating point variables take same number of decimal points that you have. Basically it goes by IEEE standards.


******************************************************************************
**14: Variable argument method**  
Any programs created: NO  
This is 1.5 feature. variable argument methods (var-arg methods)allow us to specify that a method can take multiple arguments of the same type and allows the number of arguments to be variable.  

        Void m1(int..i)  
		{  
			….  
		}
	 	Public static void main (String args[])
                {
                	System.out.println(args[0]);
                	System.out.println(args[1]);
                }
		}

******************************************************************************
**15: Abstract Classes & Abstract Methods**  
Any programs created: Yes  
Programs:   
AbstractPublicA  
concreteUseAbstractA

**1: Abstract:**  
-	We can’t create objects for abstract class.   
-	We can have abstract class and abstract methods. But not possible to have abstract variables.     
-	Abstract class can have both instance methods and abstract methods.    
-	A abstract class can have 0 abstract methods and N concrete methods.  
-	A abstract class can have N abstract methods and 0 concrete methods.  
-	But a concrete class can’t contain abstract methods.  
-	You can’t create objects for abstract class but you can access abstract class by extending abstract class.  
-	Abstract methods can only have signature not implementation. That’s the reason we should not keep curly 		braces at end.  Abstract class/methods are used only for specifications. So child class is responsible 		to provide the implementation for the parent class abstract methods.  
-	A regular class can’t contain abstract methods. If a class contain at least one abstract method we should 		have to declare that class as abstract other wise compile time error.

**2: What is the difference between abstract & public?** Public is a access modfier with it you can specify if variable/method/class is public type or not? But abstract is not a access modifier so the purpose of abstract class is to create specification/signatures. But there are two rules in abstract  
	1: Abstract class may be either public or default  
	2: But methods may be three types: Public, default and protected. Not private because if you create a 			private method with signature you can’t access this method to do implementation in other class. 
	Some of java books says abstract is a access modifier since you can create methods/classes of abstract type. 	Even though if a class/method is abstract type you need to pass access modifier like public, protected, private 		(if you don’t pass any, that means default).

**3: Why there is an option have creating Abstract checkbox while creating classes when there is no difference between public and abstract classes?**  See, the purpose of abstract class is to provide specification no implementation. For ex: you know the variables take public, protected, methods will be default and protected….then you can write all these by creating a abstract class by selecting 
Abstract check box + Public radio button.

**4: We can’t create objects for abstract class. Why?** You don’t implementation in abstract methods, if you try to create a object for abstract class and you call abstract methods with help of object, JVM doesn’t know what to do since there is no implementation for abstract methods but call is made, so it will be crashed. That’s why Java not allow to create object for abstract class.


******************************************************************************
**16:GARBAGE COLLECTION**  
Any programs created: NO  
In java, garbage collections runs in background. For better memory management, java uses garbage collections.  In java we set some memory for heap and when we create objects, they take place in heap memory. When it occupies 80% of heap memory, in the background java runs the garbage collectors clean up the heap memory. Other wise you can run below line. You can run this only inside block/method not at class level.
System gc();

******************************************************************************
**17: INNER CLASSES**  
Any programs created:Yes  
Programs names:   
Exer17_Inner class.java  
Exer17_Inner classes.java  
Exer17_StaticInner class.java  
Exer17_MethodLocalInner class.java  
Exer17_AnonymousInner classA.java  
Exer17_AnonymousInner classB.java  
Exer17_AnonymousInner classC.java

There are 4 types of Inner Classes:  
-	Inner classes  
-	Static inner classes    
-	Method Local Inner classes  
-	Anonymous classes

**1: Inner class:**  
How to create > How to call > Generate errors (including create both variables and call them)  
Access modifiers, Purpose of Inner classes with example.  
	1: Are also called Instance inner classes.  
	2: inner classes are completely different from static Inner class.   
	3: Since instance methods/variables only be called by object, so Instance Inner classes are also called by 		object. That means, you can’t call them before creating an object.   
	4: Inside a main method, after creating an object for a class you have to create an object for this inner 		class and then call it OR Inside static main method, if you directly create an object for this class 		before creating an object for the mainclass is not possible.   
	5: In this class, you can define both static and instance variables.  

**Purpose of inner class:** For ex:  If a class has 10 methods and 10 variables. Every time you are calling these 10 variables in 10 different methods individually.  
**Disadvantage:** time consuming, number of lines of code increased.  
**Solution:** Better to create a inner class and define all these variables inside inner class and call inner class only in 10 different methods. 

**2: Static inner class:**   
How to create > How to call > Generate errors (including create both variables and call them)  
Purpose of static classes with example.  
StaticInner class.java  
1: Static inner classes are completely different from Inner class.   
2: Since static is directly called without an object so Static Inner classes are directly callable without object. Inside main method, before creating an object for a class you can directly call static inner class.   
3: In this class, you can define only static variables.   
4: If you have instance variables inside static inner class, you can’t call them before creating an object. For any instance variable you have to create an object in order to call them.

**3: Method Local Inner class:**  How to code this class, how to access it, how you can’t access it.  MethodLocalInner class.java  
**Method local classes:** Are defined only inside a method which are not accessible from outside of that method. Obviously not accessible from outside of a class. 

**4: Anonymous Inner class:**   
How to declare, its structure, error generation.  
Purpose – Override methods on concrete class  
Purpose – aslo implements methods of abstract class/Interfaces  
Relationships:   
AnonymousInner classA.java  
AnonymousInner classB.java  
AnonymousInner classC.java
1: Are the most used anonymous inner classes  
2: We can use these Inner class to overiride methods, implementing abstract methods, implementing interfaces.  
3. Anonymous class contain the classname of method’s classname. Since there are not keywords for it.  
4. 4: These classes don’t look like a class template, they have the same name as classname and ; will be placed at the end body. Basically you create a object for the class and use that object as anonymous inner classes.

**4.1: Why Anonymous classes were introduced:** In older versions of java, it doesn’t allow to extend multiple classes, we can’t override methods without extending their classes.  
So, java introduced Anonymous Inner class. With this class, you no need to extend a class but you can override that class methods. Lets take an example.     
You have three classes ClassA, ClassB and ClassC.   
	ClassB extends ClassA for some reasons  
	ClassA can’t extend ClassC since multiple classes can’t be extended in java  
	But ClassB wants to override ClassC methods. 

**4.2: Old versions of java** - It was not possible.  
Newer versions of java: In classB, you can create a Anonymous class for ClassC & can extends ClassC methods inside AnonymousClass. 

**5: General:**   
Priority of Inner classes are:   
Anonymous classes > Inner classes > Static Inner classes > and then Method Inner classes  
1: Anonymous classes are mostly used, very few times we use inner classes, very rarely static classes, very very rarely we use method local classes.  
2: None of these are accessed from outside.  
3: By default all Inner classes are private, even if you define them as public there will be no use, since they are not allowed from outside.  
**Disadvantage:** You can’t access any Inner class from outside of the class.


******************************************************************************
**18: Interfaces**      
Any programs created: No  
Programs:
InterfaceA,   
InterfaceB,   
SubInterface,   
ClassImplementsInterfaceAInterfaceB are related.

**1: Interfaces:** The main purpose of interfaces to define specifications. That means  
	1: It can only have abstract methods no instance(regular/concrete) methods are allowed  
	2: So only signature is allowed due to abstract classes. So interface class can’t have actual 			 	implementation.  
	3: In interface when you write method, no need to mention abstract infront of methods, by default they are 		abstract methods  
	4: Regular classes can’t extend interface classes, but they can implement the interface class by using 			keyword ‘implement’. 
	For ex:  
	public regular class implement interfaceclass
	{
	}  
	5: Other interface class can extend more than one interface class.   
	For ex: public interfaceclassone extend interfaceclasstwo interfaceclassthree  
	{  
	}  
	A class can extend only one class at a time .But a interface can extend any number interfaces.  
	A class can implement any number of interfaces at a time.But interface never implement another interface.  
	6:Later in classes, If you want to provide implementation for any interface method ,it must be declared as 		public .  
	7: The first concrete class which implements an interface must provide implementation for all the interface 	methods otherwise the class must declared as abstract. 

**2: Interface variables:** are by default public static final. Public is you can access anywhere, static means you can access in both static & in concrete methods. Final means you can re-initialize the value.

**3: Interface methods:** are by default Public Abstract. Public means you can access this from anywhere, abstract means only signature is allowed not implementation. 


******************************************************************************				     
**19:Assertions**  
Any programs created: No  
**Assertions:** Assertions are not used in any logic, those are not useful at all. Instead of using system.out.println, we can use assertions. For ex: if you want to delete system.out.println, then how to delete them if they are in different places. So this is possible with assertions. So print with assertions every where, and configure some where to delete them by one configuration.    
There is no difference using assertions and system out println.


******************************************************************************
**20: Java execution Flow, Instance and Static Blocks & Methods.**  
Any programs created: Yes  
Programs Names:   
Exer20_JavaFlowBothStaticAndInstanceExecution  
Exer20_JavaFlowBothStaticAndInstanceExecutionSubclass  
Exer20_JavaFlowBothStaticAndInstanceExecutionSuperclass  
Exer20_JavaFlowInstanceExecution  
Exer20_JavaFlowStaticExecution

1: Java execution flow:  
2: What are static blocks and instance blocks.   
3: Java execution flow order should be: 

1: In java if you have static blocks, instance blocks, constructors and main method. Java first runs  
	Static blocks, later instance block, later constructor finally main method.   
	Static blocks > Instance blocks > Constructor > finally main class.

2: What are static blocks and instance blocks.  
These are just blocks not methods, basically they can also have arguments/variables.   
But these should be defined outside of main class. Not only top level of class, you can define them anywhere but outside of main class. 

        Public sample()    
        Int I;  
        Int j;  
        
        Sample(int I, int j) // this is constructor  
        {  
        	Print “ This is constructor”  
        }

         
        Static m1() // this is static block  
        {  
        	Print (“ The project starts here”);  
        }

        Int M2() // this is instance blcok  
        {  
        	Print ”This is the project name”;   
        	K=i+j;  
        	Int k;  
        }

        Public static void main(String args[])  
        {  
        	Sample s = new Sample(10,20);    
        	s.m2();    
        }

Basically, in above program, control first goes to static block and it will print value from there, later it create object, when it create object it immediately execute the instance block and also create constructor and execute the constructor too.  
Constructor is nothing but: It will contain same name as classname. But it will declared outside main, this is used to create objects. It logic will be executed when object is created.  For more information about this please refer to audio file. 

        public class Initialization  // a class  
        {  
        	Private static String msg(String msg) // static Method  
        	{  
        	System.out.println(msg); return msg;  
        	}  
        	static String m=msg(“1”); // static variables  
        	static   
        	{		// static block  
        		m=msg(“3”);  
        	}  
        	{  				// Instance block  
			m=msg(“2”);  
			}  
			public static void main(String a[])  // Main method  
			{  
			Object o=new Object();
			}
		}

**3: Java execution flow order should be:** Priority order start from 
Static variables > then it goes to static block > then it goes to  Instance variables > then it goes to  Instance block >  then it goes to  Constructor >  then it goes to  others like main method.  
1: static variable wants to print msg(“1”)  --> it goes to method msg() and prints : 1   
2: static block wants to print msg(“3”) --> it goes to method msg() and prints: 3  
3: There is no instance variables  
4. Instance block wants to print msg(“2”) --> it goes to method msg() and prints : 2  
5. The constructor “object” is not created, so nothing will print.


One more program:  

        public class Myclass //class name  
        {  
        public static void main(s[] a) // Main method  
        {  
        Myclass obj= new Myclass(l);  
        }

        static int i=5; // static variables   
        static int l; 	// static variables  
        int j=7; int k; // Instance variables.  
        public Myclass(int m)  		// constructor  
        {  
        System.out.println(i+”,”+j+”,”+k+”,”+l+”,”+m);  
        }  
        {                 			 //Instance initialize block  
        J=70; l=20;   
        }  
        Static 					 //static Initialize block  
        {  
        i=50;  
        }   
        }


*****************************************************************************
**21: Super & This**  
Any programs created: Yes  
Programs Names:   
Exer21_SuperThisClassA  
Exer21_SuperThisClassB

**Super:** super is a keyword which is used to refer the super class from a sub class. -- You can only refer to superclass Instance variables, Installable blocks, Instance methods and constructors	  
You can’t refer to superclass’s static methods and variables.

**This:** This is a keyword which is used within the same class.  
-	You can only refer to this class’s Instance variables, instance blocks, Instance methods and constructors.
-	You can’t refer to this class static variables, static blocks and static methods
