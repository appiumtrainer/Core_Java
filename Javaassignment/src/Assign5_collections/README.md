Collections:
==============   
Collections topics you will find below.   
All Collections programs are covered [Here](https://github.com/mjalleda/Core_Java/tree/master/Javaassignment/src/Assign5_collections)  

**Sub-Topics:**  
1: Collection Interface  
2: All Lists Classes  
3: All Sets classes  
4: All Maps Classes  
5: All Others:  
- Collection Class/API  
- Generics  
- String Tokenizer  
- Locale Class  
- Date API  
- Timer  
- Calendar  
- Comparator  
- Cursors.

*****************************************************************************
**1: Collection Interfaces.**
-------------------------  

**1: Layers in most of programming applications:**

![alt tag](https://github.com/mjalleda/Core_Java/blob/master/Javaassignment/Screenshots/Application_Layer.JPG)  


**2: Collections:**  
Collection is nothing but collection of objects OR set of objects. 
Basically, collection contains all objects.  If you look into the below diagram you understand that Collection is the superclass for all. Where List & Set are subclasses of Collection (Actually, if you look into any collection hierarchy they don’t show AbstractList).  ArrayList, Vectors, LinkedList are subclasses of List.  HashSet and sorted set are subclasses of SetInterface.   The last level you can see in below diagram.   
1: Collection is a interface it can contain only abstract methods. 

Here is a hierarchy of Collection Interfaces:  
**Interfaces:** are:  
- Collection  
- Lists  
- Sets  
- Sorted Set  
- Map  
- Sorted Hash Map    

**Classes:** are:   
- ArrayList  
- LinkedList  
- Vector  
- Stack  
- HashSet  
- LinkedHashSet  
- TreeSet  
- HashMap  
- Weak hashMap  
- Identity HashMap  
- TreeMap  
- Hashtable.

Maps represent mappings rather than true collections. However, these interfaces contain collection-view operations, which allow them to be manipulated as collections.

![alt tag](https://github.com/mjalleda/Core_Java/blob/master/Javaassignment/Screenshots/Collections_Hirarchy..JPG)  


*****************************************************************************				  
**2: All Lists Classes**
-------------------------

**Sub-Topics:**  
1: Lists & Diagram :    
2: Difference between Lists & Sets  
3: What is the purpose of Lists & Sets.   
4: Memory management:  
5: performance  
6: Random access interface  
7: Difference between all three. ArrayList, LinkedList and Vector.


**1: Lists & Diagram:**  

![alt tag](https://github.com/mjalleda/Core_Java/blob/master/Javaassignment/Screenshots/AllList_Classes.png)

In Lists,   
Interfaces are: Lists  
Classes are:  ArrayList, LinkedList, Vector & Stack.

1: List is a Interface which implements Collection Interface methods.  
2: Lists are index based. Means, each value get a position. For searching, we can use index/position to retrieve a value.  
3: The following are ListInterface methods.   
- 1.boolean add(Object obj)  
- 2.boolean add(int index,Object o)  
- 3.boolean addAll(Collection c)  
- 4.boolean addAll(int index,Collection c)  
- 5.boolean remove(object o).  remove the first occurrence of this object  
- 6.boolean removeAll(Collection c)  
- 7.int indexOf(Object o). return the index of first occurrence. returns -1 if there is no such object  
- 8.int lastIndexOf(Objetc o)  
- 9.Object get(int index). there is no get method in the collection interface  
- 10.Object set(int index , Object o)  
- 11.ListIterator listIterator()  
- 12.Object remove(int index)

4: AbstractList is a abstract class, which extends both Collections & LinkedList interfaces. Then implements body for some methods of collections and Lists. Why some methods only? Let say for ex: Collection have 10 methods, LinkedList have 8 methods, Total 18 methods should be implemented by below classes.   
- ArrayList  
- VectorList  
- LinkedList  
- Stack    

But for ex: if all above classes implemented some methods, let say if 6 methods in same manner (no change at all, and output also same) then why to write in four classes, write it in one location and access it from there. So that common location is AbstractList class.  
5: Remember Collection,List & Sets are Interfaces. AbstractClass is a abstract class & all others are regular classes.    
6. Most commonly used are Lists are     
ArrayList  
Vectors  
LinkedList    
Stack.    
7. Size (arrayList, linked list, vector list and stack) grows dynamically for collections unlike concrete classes.   8: Even, List & sets share common methods like Iterator.    
9: All lists & sets holds objects, by default its size is 10 but JVM dynamically grows its size.    
10: List & Sets can have, wrapper class object, Object class object, another class (for ex: employee) class object and also directly primitive values are allowed. For theory we say, primitives are not allowed in Collections, but if you initialize some primitive values in array list, JVM in the background it runs autoboxing and autounboxing mechanism and convert them into wrapper classes.  
11: you need to import to all Lists and Sets and collections. For ex:   
. import java.util.ArrayList;  
. import java.util.LinkedList;  
. import java.util.Enumeration;  
. import java.util.Vector;  
. import java.util.ListIterator;


**2. Difference between List & Set.**

| Lists        |      Sets      |
| ------------- |-------------|
|Both are used to transfer set of values (using objects) in between layers like control, service or DEO.| |
|Both are used to search values on an Object (of set of values).| |
|But Lists allows duplicate values to print/add. |Set Doesn’t allow duplicate values. It removes duplicate while retrieving. |
|List allow multiple null values to be in the list.| But Set doesn’t allow more than one null value. It only return one null values if it has multiple.|
|List returns the order of values in the order they are initialized.|In set order is preserved( except LinkedHashSet). |
|Widely used are Lists.|If you don’t want duplicates then use sets. |
|List uses both For and Foreach. Because it is index based.|Since set is not index based it doesn’t allow forloop. Only allows foreach loop.|

**3: What is the purpose of Lists & Sets:** Usually, in most of the projects there would be some requirements like transferring set of values. You can insert all those values into one array and pass that array in between layers. So all these are different types of arrays. Some allow duplicates some doesn’t. In some order is preserved in some order is not preserved. So main purpose is: To transfer a set of values in between layers, we use Lists & Sets. 

**4: Memory management:** In arrayList & vector, if you change/update/modify any value, JVM will create a new Object inside memory location and update there and removes the existing one. Hence, memory management is not poor in Array list & Vector. But in LinkedList case, it doesn’t happen. JVM doesn’t create a new object, it just updates the existing one. So it manages memory well in LinkedList.  
Summary: So, ArrayList & vector manages memory better than LinkedList.

**5: Performance:** Since vector is very old, it doesn’t allow multiple threads to access its methods. For ex: addmethod can be used by one user/thread at one time. But this is opposite in ArrayList & LinkedList, since they are not legacy classes, they allow multiple threads at one time to access one method.  
Summary: ArrayList & LinkedList are preffered than Vectors.  

**6: Random access Interface:** Since this mechanism is implemented on ArrayList & Vector, so user can rapidly access/search values, since this is not implemented on LinkedList, user can’t do rapid search for values in LinkedList.   
Summary: ArrayList & LinkedList are better. 

**7: Difference between all three. ArrayList, LinkedList and Vector.**  

|  ArrayList |Vector |LinkedList|
| ------------- |-------------| -----|
|Memory Management Doesn't manage well: Update/modify: If you update a value in the ArrayList, JVM will create a new memory for the ArrayList and point it to that one, later it will remove the old memory location. Memory allocation is poor in Array list   | Memory Management Doen't manage well:Update/modify: If you update a value in the Vector, JVM will create a new memory for the Vector and point it to that one, later it will remove the old memory location. Memory allocation is poor in Vector|Memory Management: Manages well:Update/modify: If you update A value in the LinkedList, JVM will not create a new memory for the linkedList, it updates existing one. So memory management is better on LinkedList.|
|Performance on accessing values are better:  Array list are better since it allows multiple threads to access same method at same time. For ex: If 10 users want to access addmethod in ArrayList, it allow all 10 users at same time.   | Performance: Doesn't access well :Performance wise Vector are not preffered since it doesn't allow multiple threads to access same method at same time. For ex: If 10 users want to access addmethod in Vector, it allow 1 user at one time.|Performance wise LinkedList are better: Performance wise Linked list are better since it allows multiple threads to access same method at same time. For ex: If 10 users want to access addmethod in LinkedList, it allow all 10 users at same time.|
| Search criteria: ArrayList are better for searching values. For searching ArrayList are better. Since 'random access' interface is implemented on it, so this mechanism allow user to search values rapidly on Arraylist  | Search criteria: Vector are better for searching a value. For searching Vector are preffered. Since 'random access' interface is implemented on this also, so this mechanism allow user to search values rapidly on Vector.|Search criteria: LinkedList is bad to search for an item. For searching LinkedList  is veryBAD. Since 'random access' interface is NOT implemented on this, so JVM takes lot of time to search a value on LinkedList.|
| You can use for & for each loop. Since all lists are index based.  |You can use for & for each loop. Since all lists are index based. |You can use for & for each loop. Since all lists are index based.|
| All three are used to transfer set of values (in a object) from one layer to another layer. Or from one place to another place. For ex: transferring from DEO to Service layer.  | ||
| ArrayList is not legacy class  | Vector is a legacy class|LinkedList is not legacy class|

******************************************************************************  
**3: All Sets Classes**  
-------------------------

**Sub-Topics:**  
1: Sets & Hirarchy.  
2: Difference between Hashset & ListHashSet  
3: How HashSet/Linked Hashset removes duplicates & compare   
4: Diff between System.identityHashcode  and hashcode.  
5: How SortedSet & TreeSet removes duplicates & sorts?

**1: Sets & Hirarchy**  
In Sets,   
Interfaces are:  Set & Sorted Set   
Classes are: HashSet & LinkedHashSet & TreeSet.

![alt tag](https://github.com/mjalleda/Core_Java/blob/master/Javaassignment/Screenshots/AllSet_Classes.png)


1: Sets is a interface which implements collection interface  
2: Sets: In the map:  
- Collection is a interface  
- Set is interface which implements Collection  
- HashSet is a class which implements collection & set interfaces.  
- SortedSet is a interface which implements Set & Collection interfaces.  
- LinkedHasSet is a class which extends HashSet.  
- Again Treet Set is a class which extends SortedSet.  

3: Purpose is of Sets is same as Lists : the only difference is, it doesn’t allow duplicates. 

**2: Difference between Hashset & ListHashSet**    

|  HashSet |LinkedHashSet |
| ------------- |-------------|
| Both are from Sets  | |
| HashSet is parent for LinkedHashSet.   | |
|LinkedHashSet - order is not preserved. It return values based on value hashcode.   |LinkedHashSet - order is not preserved. It retunr values in the order they are initialized. |

**3: How HashSet/Linked Hashset removes duplicates & compare?**  
- JVM needs to compare values in order to know if that value is duplicated or not ? For ex: a(=1) & b(=1). JVM needs to compare if a equal to b or not. For this, JVM uses Object.equals method. So you can say by default it uses equals method.   
- Equals method – Compare two values based on their hashcode. If a’s hashcode is 123@skfFedl  & b’s hashcode is 344@9FKajh.  So equal method works based on  hashcode concept.    
- What is hashcode – JVM returns Object’s memoryLocation address in hexadecimal format. Basically each object located in separate memory location. Hashcode represents that memory location address.    
- All Set classes, by default they use hashcode method to compare values. If they find a value is same/duplicated, then Set classes don’t allow the second duplicate value.   
- JVM knows how to use Object.equals method on predefind, Wrapper, String/string buffer. But how it doesn’t know how to compare user-defined Objects like Employee & EmpSalary. So what is the solution.    
- Solution is: Override equals & hashcode method, in such a way that, ask them to compare your objects OR your object fields. What ever you want. Override concept is also very simple. Below one example.   
- You have Employee class with fields empNo, empName & empSal. Now you created two objects for two employees.  You want to compare below two employee objects with empNO.    
  Employee e1 = new Employee(1, “Sajta”, 1000)  
  Employee e2 = new Employee(2, “Sajta”, 1000)   
- Solution is, override hashcode method to compare the content of empNo. If they match return 1 otherwise 0.    Override equals methods to use above override hashcode method. If value is 1 then duplicated, if it is 0 then not duplicated.   
- Keep all these in the same class where you have your Set class is (it may be hashSet, LinkedHashSet or Sorted Hashset).  
- So override equals method in the same class, later your set class calls only that method.   
- While adding values to Set, it checks if this value is duplicated with help of equals method. If so, it doesn’t allow. You can print and check.  
- For ex::   
- 1: Return Students from database table ‘student’ and remove duplicate student names and return all students in random order– Best to use Hashset.  You have two requirements. Avoid duplicates + return in the random order.  
- 2: Return Students from database table ‘student’ and remove duplicate student names and return all students in the same order – Best to use Linked Hashset.  You have two requirements. Avoid duplicates + return in the order.

**4: Diff between System.identityHashcode  and hashcode.**  
Both are for representing hashcodes only. But identity Hashcode is the original hashcode, where hashcode contains programmatic hashcode format. Both represents in hexadecimal format only. For some purposes JVM introduced hashcode concept when identity Hashcode exists. 

**5: How SortedSet & TreeSet removes duplicates & sorts?**  
1: Tree Set is child of SortedSet. TreeSet is a class and SortedSet is Interface. So Tree Set extends SortedSet.   
2: Basically SortedSets/TreeSet are used for sorting values. For ex: 1: Return Students from database table ‘student’ and remove duplicate student names and return students based on “StudentId in ascending order”. You have two requirements. Avoid duplicates + return in StudentId Asc order –so, best to use TreeSet.   
3: By default JVM returns in ascending order on Treeset.   
4. How JVM sort items?  JVM by default it implements comparable interface and returns items in ascending order. That means, it sorts all pre-defined like ‘primitive’, Wrapper and String/String buffer.     
5.Comparable interface have method compare to. It is something like ‘How equals method uses hashcode method’.   
6:What if you need to sort custom/user defined Objects. Solution is: Override comparable & compareTo methods, in such a way that, ask them to compare your objects OR your object fields. What ever you want. Override concept is also very simple. Below one example.   
- You have Employee class with fields empNo, empName & empSal. Now you created two objects for two employees.  You want to sort below two employee objects with empNO.    
- Employee e1 = new Employee(1, “Sajta”, 1000)  
- Employee e2 = new Employee(202, “Sajta”, 1000)   
- Employee e2 = new Employee(2, “Sajta”, 1000)   
- Employee e2 = new Employee(33, “Sajta”, 1000)   
- Solution is, override compareTo method to compare the content of empNo. Return 1, -1 and 0 for >, < & ==.    
Override comparable method to use above override compareTo method. If value is 1 then keep it in the front, if value is -1 then place it back, if value is 0(means duplicated) then remove it.   
- Keep all these in the same class where you have your TreeSet.  
- While executing values to TreeSet, it checks if this value is duplicated & sort , if duplicated then remove it, if value is big then keep it in the front, if value is small then keep it in the back.  
 
7: Only one null value is allowed if it is first value. Otherwise null is not allowed anywhere except at beginning.  8: Remember only one null value is allowed. Multiple null not allowed. Since it replaces existing null values.  Sorted Set: This is just an interface – there is nothing much to learn about it.  
Tree Set: is the mostly used.  


******************************************************************************
**4: All Maps Classes**  
-------------------------

**Sub-Topics:**  
1: Maps & diagram:  
2: HashSet VS hash map:   
3: LinkedHashSet vs Linked hash map:  LinkedHashSet  
4: TreeSet and TreeMap:  
5: Null values on Hash map, on Linked Hash map, on HashTable and on TreeMap:   
6: Hash table:   
7: Iterators/retrievable mechanism:

1: All Map Classes & Hirarchy:   
Interfaces: Maps & SortedHashMap  
Classes: HashMap, Weak hashMap, Identity HashMap, TreeMap & Hashtable.

![alt tag](https://github.com/mjalleda/Core_Java/blob/master/Javaassignment/Screenshots/AllMap_Classes.png)


1: If you have student class and student names. For ex: Class is Math, Sci and Comp.   
And you have total 30 student names. 10 for each class. Now you can put all of them in single map and access the map as key value pair. 
For ex:

| Key  |Value |
| ------------- |-------------|
| Math  | Sajta, sarita, kavita|
| Sci  |Ravi, ram, raju|
|  Comp |John, albert, Robert, david |

2: But collection class can contain only values no keys.  The main difference between collections and maps are  
- Collection are collection of individual objects, where maps are key-value pairs.    
- In collections >>  sets don’t allow duplicate values. Where in maps    
      1: Duplicate keys overrides existing keys.  
      2: Duplicate values are not allowed.    

3: Maps somehow looks similar to Collection Sets. Since both have similar classes. Like,  
- hash set and hash map  
- LinkedHashSet and LinkedHashMap  
- Hashtable   
- TreeSet and TreeMap. 

**2: Hash Set vs hash map:**  HashSet prints the value in random order. Same as hashmap it prints the key-value pair in random order.

**3: Linked Hash Set vs Linked Hash map:**  LinkedHashSet prints the value in the same order as they defined. Same as Linked hash map it prints the key-value pair in the same order as they defined.  
LinkedHashSet is child of HashSet, same as LinkedHashMap it is child of HashMap.

**4: TreeSet and TreeMap:**  Tree set sorts values and prints them in some sorting manner, Same as TreeMap it also prints the key-value pair in some sorting manner. Both, TreeSet and TreeMap, uses both comparable and comparator methods. Both don’t allow null values.  
TreeSet is child or SortedTreeSet &   
TreeMap is child of SortedTreeMap.

**5: Null values on Hash map, Linked Hash map, HashTable and TreeMap:**  
- HashMap and LinkedHashMap allows null values more than once.   
- Where TreeMap allow null values only once.  
- HashTable doesn’t allow null value at least once. 

**6: Hash table:**  
- This is a legacy class something like vectors.   
- Which doesn’t do sorting but doesn’t allow null values more than once. But all methods inside this are synchronized methods.  
- All methods inside this are synchronized that means they don’t allow multiple threads to access at same time. So these are suitable for ‘multiple thread accessible’ projects. .   
- If any developer allow multiple users to access same form/object at same time, there might be data loss and data in-consistency. A user address might enter into different user’s account. To avoid these type of situation, developers don’t use hashMap & linkedHashMap, since they allow multiple users to access them. So developers uses HashTable. If we go in deep,   
- They declare in such   a way that each objects/form declare declare as hashtable, that means hashtable is not declared as globally. Just to the local object/form. So each form can be accessed by one user and one user enters his data. That means, multiple users are not accessing the same form/object. 

**7: Iterators/retrievable mechanism:** There are three iterators in Maps.    
KeySet  
EntrySet  
Values.

**1: KeySet:** This method return type should be sets. That means, you have to create a object type of set and then execute KeySet on Maps.   
Purpose: This iterate on map and return key-value pairs.

**2: EntrySet :** This method is also return type should be sets. That means, you have to create a object type of set and then execute EntrySet on keys.   
Purpose: This iterate the keys and return the values. 

**3: Values.** This method is also return type should be value. That means, you have to create a object type of Collection and then execute Values on Maps.   
Purpose: This iterate on each map and return only values not keys. This will also return duplicate values since the return type is collection (it should be lists but don’t know why sun declared return type as collection. Since lists allows duplicates. But if you say collections, that means it includes sets too which is not correct).  

Entry set and values look similar but they aren’t. Because, entry set works on each key and return its value. But Values works on each map and return values from maps.  
Common: All three uses same iterator method inside to iterate each key-value.

******************************************************************************  
**5: All Others: Collection Class/API, Generics, String Tokenizer, Locale Class, Date API, Timer, Calendar, Comparator & Cursors.**  
-------------------------

**Sub-topics:**  
1: Collection class VS collection interfaces:   
2: Generics VS Raw classes (Lists, Sets and Maps):  
3: String tokenizer:    
4: LocaleClass :   
5: SimpleDateformat:   
6: Timer: 
7: Calendar VS date:    
8: Comparator.  
9: Cursors.  

**1:Collection class VS collection interfaces:**     
- Collection class is a class which is different from collection interface. Where collection interface have its own sub sets like Lists and Sets. but collection class is just like a API class something like Class, Object or System classes.    
- Collection class have some methods like sort, search, binary search, linear search, synchronized…all these can be used in collection interface objects. i.e., we can use them in Lists, Sets & Maps.    
- If you are using any collection method, then you have to extends collection interface.    
- Ex: public className extends Collection.   
- A question is:  When all Lists, Sets and Maps classes required all sorting mechanism and searching mechanism, why these methods are not directly implemented on them ? why we have to extends Collection class for these?    
- Answer is:  all these are common methods which are used in all Lists, Sets and Maps. Hence they given in  on e API (that means Collection class) and every time we access them from that API.    

**2: Generics VS Raw classes (Lists, Sets and Maps):**   
Generics are more used than raw classes. i.e.,    
Generic is ArrayList <Employee> AL1 = <Employee> new ArrayList();   
Raw type is ArrayList AL1 = new ArrayList();   

**3: String tokenizer:** To separate strings by using    
- space “ “  or   
- any characters or multiple characters   
- separate strings by removing characters   

**4: LocaleClass :** This is used for localization. To get any    
- country code/ID, its language and ISOCountries and their languages.     
- Ex: India’s population. 1,000,000. Italy population is 1.000.000    
- To get a country’s numbering format. For ex: display population, area, number of units.    
- To get a country’s currency format. India’s is Rs.1,000, US is $1,000.    
- To get a country’s date format. For ex: In india date comes first. DD/MM/YYYY, but US Month comes first MM/DD/YYYY.  
- To get all above in locale class,  we also use different APIs, date, time, calendar, NumberFormat, SimpleDateFormat, DateFormat classes. 

How to change the text format : How to change text from language to another language. Change Hello to “Hola” in Mexico. Store a text file with “Hola” string. Then call with getInstance() method then ask variables to change to Spanish when input string = “hello” By using locale class. Country code:  locale l = new locale(“Mexico”);

**5: SimpleDateformat:** This is used to for setting/getting date formats.

**6: Timer:** This is just like schedulers in windows, basically you can schedule task(s) at particular time. so it runs automatically at that time.    
For this you need to create tasks (which you want to run) + schedulers (when you want to run).

**7: Calendar VS date:**       
Date: has very limited set of methods and it doesn’t have wide range of properties like calendar. So calendar got introduced for this purpose. Using date, you can print current date, month, year, hour, mm and ss. But using calendar date you can print day of a week, week of month,  isLeapYear?    

**8: Comparator:** This is similar to Comparable method. Where it uses compare() method. Remember    
- Comparable uses compareto() method    
- Comparator uses compare() method.    
There is no much difference between comparable & comparator. Except that, comparable used in same class where your Treeset is defined but Comparator defined in different class where your treeset is defined. Otherwise both can be overide and used for sorting values/objects.     

**9: Cursors:** There are three types of cursors.     
- Iterators ( used by all collection classes)    
- ListIterator (used by List implemented classes)    
- Enumerator (used only by legacy classes)    

**9.1: Iterators:** Iterators are defined in collection interface. So these can be used by both Lists and Sets.     Which has limited number of methods.     
- hasNext    
- next    
- remove.     

**9.2: ListIterator:** ListIterator is defined in List class, so it can be used by ArrayList, LinkedList, Vector and Stack. It has total 9 methods. But it also inherits Object API class methods.    
- add(e)    
- hasNext()    
- hasPrevious()    
- next()    
- nextIndex()    
- previous()    
- previousIndex()    
- remove()    
- set(e)    

**9.3: Enumerator:** Which is used only for legacy classes like Hashtable, hashcode and Vector class. It has the following methods.    
- hasMoreElements()     
- nextElement()    

**9.4: Difference between Iterator, ListIterator and Enumerator.**  

|Iterator   |ListIterator |Enumerator|
| ------------- |-------------| -----|
|  1: Iterator is defined in collection interface, so Iterator can be used in any collection implemented classes | ListIterator only implemented in List, so it can be used only in ListImplemented classes.|Enumerator only used in legacy classes, like hashcode, hashtable and vector. |
|  Iterator has three main methods. hasnext, next and remove. | It has total 11 methods.|It has also many, but the important and not used one is element.|

























