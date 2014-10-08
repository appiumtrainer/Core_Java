OOPS (Object Oriented Programming)
------  
All OOPS topics are covered below.  
All OOPS programs are covered [Here](https://github.com/mjalleda/Core_Java/tree/master/Javaassignment/src/Assign3_OOPS)  

**Sub-Topics:**  
1: Class API & Object APIs.  
2: Encapsulation  
3: Abstraction  
4: Inheritance  
5: Polymorphism  
6: Constructor

******************************************************************************
**1: Class API & Object API**  

**Class:** Class is nothing but a blueprint, it represents a house, person, animal. Which has specifications saying that it needs to have properties and methods.  
How java code gets into memory:   
- Any class contains either static variables/methods or instance variables/methods or both.   
- For static methods, Memory should be allocated when they get executed.  
- Instance variables can be executed only with an object. In java, you can’t directly execute/call instance variables/method. First you need to create object and then call/execute instance variables/methods. Memory should be allocated when object is created that means instance variables are getting to memory thru object not just by themselves like static variables/methods.  
- That means, java codes gets into memory in two ways. Thru static variables/methods or Objects (for storing instance variables/methods).

**Object:** Is an actual reference for all variables/methods in memory.

******************************************************************************
**2: Abstraction:**  
- Hiding variables/methods/implementation of a class is called Abstraction, means everything should be defined as private.  
- This just a concept and there is no keyword for it  
- Basically most of the files in finance application should be abstracted. 

******************************************************************************
**3: Encapsulation**  
This also a concept not a keyword.  
- If all variables/methods in a class are declared as private, that class is called tightly encapsulated.  
- Encapsulation is tide with class not with variables/methods. If a class contains both private and public/protected/default, that class is called is not completely encapsulated.

******************************************************************************
**4: Inheritance**  
1: Creating a new class from existing class is called Inheritance.   
- This is a concept + we use keyword extends to inherit properties from parent.  
- You can extend one class but not multiple classes.  
- API classes can be accessible everywhere.  
- Levels of inheritance.   
- ParentClass > ChildClass extends ParentClass  > GrandChild c extends Parent.  
  That means,  ChildClass access all properties/methods of Parent.  
  But GrandChild can access all properties/methods of both ‘Parent’ & ‘ChildClass’.

**2: Difference between Extends keyword and parent reference/object.**  
- Main difference is you can’t override methods with our inheritance/extends.  
- Only you can access parent class methods/variable by parent reference not by child reference. With extend keyword, child reference also access parent’s variables/methods.

**************************** *************************************************
**5: Polymorphism (Method overloading and overriding)**    

**Sub-Topics:**  
1: Understanding some overloading scenarios:  
2: Understanding some Override scenarios:  
3: Polymorphism  
4: Overloading:   
5: Overriding:   
6: Override method access specifiers:   
7: Override method return types:   
8: Co-variant:  
9: What is Method hiding.  
10: Why final methods can’t override?

Any programs created: Yes  
Program Names:   
PolymorphismOverrideDatatypeSuperclass.java  
PolymorphismOverrideDatatypeSubclass is subclass.java  
PolymorphismOverrideObjecttypesSubclass.java  
PolymorphismOverrideObjecttypesSuperclass.java  
PolymorphismOverrideReturntypesSubclass is subclass.java  
PolymorphismOverrideReturntypesSuperclass is parent.java   
PolymorphismOverrideReturntypesSuperclassAnimal.java  
PolymorphismOverrideReturntypesSuperclassMonkey.java

**1: Understanding some Overloading scenarios:**  
**Scenario1:**  
Do method overloading and create error scenarios.  
ProgramName: PolymorphismNameAmbiguity. 

**Scenario2:** Do constructor overloading and call them.  
ProgramName: PolymorphismConstructorsOverload. 

**Scenario3:** Use API classes as method arguments and call the methods.  
ProgramName: PolyOLWithAPIClasses. 

**Scenario4:** Call var arguments in method and call the methods.  
ProgramName: PolymorphismVarArguements. 

**2: Understanding some Override scenarios:**  
**Override Scenario1:**  
Override focus on Object type class. Some programs created for this: They are,  
- PolymorphismOverrideObjecttypesSuperclass.java  
- PolymorphismOverrideObjecttypesSubclass.java

**Override Scenario2:**  How to write datatypes in method overriding  
Try all access specifiers (increase a level up OR same level).Declarations & object type calling & Error conditions generating. Some programs created for this: They are,  
- PolymorphismOverrideDatatypeSuperclass.java  
- PolymorphismOverrideDatatypeSubclass is subclass.java

**Override Scenario 3:** how to write return types in method overriding  
Try to use return types of API classes or examples of parent-child relationship. (same level or a level below). How to return object of these classes. Some programs created for this: They are,  
- PolymorphismOverrideReturntypesSuperclass is parent.java  
- PolymorphismOverrideReturntypesSubclass is subclass.java  
- PolymorphismOverrideReturntypesSuperclassAnimal.java  
- PolymorphismOverrideReturntypesSuperclassMonkey.java

**3: Polymorphism:**  In greek, poly means “any”, morphism means “forms/formats”. That is, any forms/formats. That means, you can create one methods in any number of forms/formats.  
Two rules apply for polymorphism:   
- Method name should be the same.   
- Number of arguments/order of arguments/ arguments type should be different.   
- It doesn’t matter if return type is same or different. Or if there is no return type.  
- Overloading feature focuses on reference type & Override focuses on objective type.    
- Let’s take an example of ClassA and ClassB. i.e.,     
  ClassB obj1 = new ClassA();  
  Obj1 is reference type & Constructor is objective type.

**4: Overloading:**  
1: Inside/outside of a class, you can change the signature(except method name) and extend a method, that means you can overload a method with a same name.   
2: In case of overloading, it go based on the reference type. For example, if you have a method m1() in both classes Super & Sub. And you have two objects for both Super & sub when you overload a method, complier will execute on reference type. For ex: you have below three objects in subclass,   
Parent p1 = new parent();  // parent reference type & parent object type  
Parent p2 = new child();     // parent reference type & child object type  
Child c1 = new child();     // child reference type & child object type

P1.m1 // it calls parent method since reference type is parent   
P2.m1 // it also calls parent method since reference type is parent  
C1.m1 // it calls child method since reference type is parent.  
Note: Second case will behave differently in override feature.

**5: Overriding:**   
1: You can do this only in subclass not in superclass.  
2: You shouldn’t change signature (method name + arguments)  
3: If you want to have a different implementation for a same class, you can override it.  
For ex: If you are not satisfied with java api methods, you can override them.  
4: Reverse triangle icon shows next to override method in subclass.  
5: In case of overriding, it goes based on the object type. For example, if you have a method m1() in both classes Super & Sub. And you have two objects for both Super & sub when you override a method, complier will execute on object type. For ex: you have below three objects in subclass,   
Parent p1 = new parent();  // parent reference type & parent object type  
Parent p2 = new child();     // parent reference type & child object type  
Child c1 = new child();     // child reference type & child object type

P1.m1 // it calls parent method since object type is parent   
P2.m1 // it calls child method since object type is parent  
C1.m1 // it calls child method since object type is parent.  
Note: Second case will behave differently in override feature.

**6: Override method access specifiers:**   
1: We use access specifiers/modifiers in method overriding, basically we need learn “what access specifier a parent method is using, if subclass method can use same access specifier or one level above “  
2: Rule1:  If parent method has a access modifier (ex: default), subclass method can have same level of modifier (ex: default) or can go up to high levels (which are public and protected) but can’t use below levels of default which is private.


| Access Modifiers        |      A method in Super class      |  Override method in subclass  |
| ------------- |-------------| -----|
|Public|If it is public| It can be public only.|
|Protected|If it is protected|it can be either public or protected. but can't be default/private|
|Default|If it is default| it can be either public or protected or default, can't be private|
|private|If it is private| Can't be visible outside of the class|
|Final|If it is final| It can be visible but can’t be accessible since it is final.|
|static|If it is static| It should be static only|
|Abstract|If method is abstract| It can be non abstract|
|not fianl|If a method is not final method|It can be final in subclass. |
|synchronized|If a method is synchronized|It can be either synchronized or non-synchronized.|

**7: Override method return types:**  
1: We use return types in method overriding, basically we need to learn “what return types a parent method is using, if subclass method can use same return type or levels below/above?“  
2: Rule1:  If parent method has return type as Object API, subclass method can have same level of return type or can go level below (math API, String API) but can’t go level above.  
Ex: Object and Class are at same level but String is one level below.

**8: Co-variant:** Parent method return type & Child method return type should have parent-child relationship, it is called Co-variant.

**9: What is Method hiding.** In method overriding concept: Lets say you have a static method in superclass & you did static method override in subclass.  
When you create an object in subclass, if you call static method, the reference type static method get called not object type.  
Usually, in method overriding method, all methods are called based on object type. Even though if a method is override, static methods are always called based on reference type.

**10:Why final methods can’t be override:**  
Final methods means final implementation. You shouldn’t override it. But if you extend a class where final method is defined, then that final method can be visible in subclass.   
So subclass cant contain a method which is similar to final method name and signature. 	Since complier thinks that you are overriding final method and it will not allow you to do 	that.

******************************************************************************
**6: Constructor**  
Any Programs created: Yes  
Program Names: HowtoUseConstructors

**Sub-Topics:**  
1: Constructor  
2: Main purpose   
3: Default constructor   
4: Parameterized constructor   

**1: Constructor:** There are two types of constructors. Default constructor and parameterized constructor. 

**2: Main purpose:**   
Basically to initialize instance variables before object is created. Let’s take a real time example. You want to pass username and password to make a connection to database before actual object is created, you can pass them in constructor. So before object is created, compiler will execute the constructor to make db connection with uname and password.

**3: Default constructor:** Basically if you don’t create any constructor or a default constructor, compiler will create a default constructor when you create an object. 

PublicA Obj1  = new PUBLICA // PUBLICA is constructor & PublicA is classname. New is operator and obj1 is object name.

One class can have multiple parametrized constructors with different arguments ( could be different number or Same number with different datatype arguments).  
For ex:    
1: PublicA(int a, int b) { }  
2: PublicA(int c, char d) {}   
3: PublicA(int a, int b, intc) {}  
4. PublicA(int c, int d) {}

At one time, 1,2 & 3 are allowed..  
But at one time 1 & 2 are not allowed because they have same number of arguments + same number of datatype arguments.

**4: Parameterized constructor:** means you can pass parameters/arguments in a constructor.   
**Difference between method and constructor:**   
- Method has return type void/int/char but Constructor has no return type.   
- You can’t use methods before main but you can use before main.
	


	

