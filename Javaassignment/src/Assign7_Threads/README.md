**Threads:**
--------------  
Threads topics covered below  
All Threads programs will find [here](https://github.com/mjalleda/Core_Java/tree/master/Javaassignment/src/Assign7_Threads)    

**Sub-Topics:**  
1: Thread Life Cycle OR Thread.start() method or threadobject.strat() method.   
2: Threads  
3: Diff b/w processor and thread:  
4: How to create threads:   
5: Some Threads  methods:   
6: Join VS Synchronized:   
7: Synchronization:  
8: Volitile vs Synchronization:   
9: Purpose of Volatile  
10 :Genericcs  
11: Difference between Synchronized and Volatile   
12: Difference between Threads & Processors  
13: Deamon threads:   
14: Deamon Deadlock  
15: Thread Group  
16: Thread wait, notify & notifyall


**1: Thread lifecycle:**

![alt tag](https://github.com/mjalleda/Core_Java/blob/master/Javaassignment/Screenshots/Thread_LifeCycle.png)  


**1: Thread Life Cycle OR Thread.start() method or threadobject.strat() method.**   
- When you execute this method for a thread ‘xyz’.  
- it creates a thread ‘xyz’ on JVM, and allocates some CPU memory in java heap memory.  
- And register the thread with ‘thread scheduler manager’ (which manages all threads in java’) later,   
- it runs the thread    
- Finally release the thread.  This is also called ‘thread life cycle’. See below diagram.

**2: Threads:**  
- Threads are like processors. That means, multitasking is possible with multiple threads.  
- Threads are nothing but a processors.  
- A small example: On OS, there are applications running like eclipse, gtalk…. so multiple processors are running at same time. That means OS allows you to do multitasking at same time. This is also same. With threads you can run multiple programs at same time. 
- But in java, you have to create multiple threads and you need to start.  
- Threads are more used for desktop applications.  These are not widely used on web applications since web sphere /tomcat already available to this so developers doesn’t like to create threads, so they use web sphere/tomcat.  
- Take an example:  Client have 1000 rows and he wants us to analyze his data within 4hours.     
- We have to connect to their applications, get data and insert into our servers and then analyze. So is it possible with in 4hours?     
- Yes, it is possible. Basically code can have 10 threads. From 1st thread, each thread asked to get 100 rows….to get data simultaneously. For ex:     
- 1st thread asked to get 1 to 100  
- 2nd thread asked to get 101 to 200  
- ..  
- ..  
- Nth thread asked to get last 1000  
- Which might take probably 1hour to get data.

**3: Difference between processor and thread:**  
- Processor doesn’t share memory with other processors, where each processor gets its own memory. Threads works on heap memory and they share their memory with other processors.   
- Processors wont die after they execute. But in Java, threads dies after their task is done.  
- Processor takes lot of memory where thread takes less memory and release it after it is done.

**4: How to create threads:**   
There are two types a thread can be created.   
- A class which extends Thread class  
- A class implements Runnable. 

**1: A class which extends Thread class:**   
If you extends another class, only one class can be extended. Another class can’t be extended. The disadvantage is another class can’t be extended.  
If you extends Thread class, you have to override Run method which is a rule.  

**2: A class which Implements runnable:**   
If you implements Runnable interface, the advantage is you have also extends another class. Which is not possible with ‘type 1’.

**5: Some Threads  methods:**   
1: Threads Priority:   
- We can define threads priority. Max is 10 and min is 1. Usually main thread gets priority 5.  
- We can change threads priority, high priority threads gets high priority and low priority threads get low priority.  

2: Threads setname and getname.   
- We can set threads name and also return threads name.  

**3: Thread Yield**   
Thread can pause for a while but how long we don’t know. But if thread has high priority along with yield, it doesn’t get paused.  If you want to pause thread for a while you can use yield on some threads.    

**4: Thread Join**  
If you want to continue only one thread and want to block another threads execution, then you can use this method on  thread which you want to execute. So all other theads completely gets stopped and they will start executed when your thread finished execution.   

**6: Join VS Synchronized:**   
Join completely blocks another threads execution and execute the thread which you used this method, the another threads wont even execute on any other methods until this thread get finished. Join works on threads.
Synchronized methods/blocks, you only allow one thread to execution at one time, that means all other threads get blocked on these methods, they get access when lock get released. Lock can be given to only one thread at one time. So synchronization work on methods/blocks.

**7: Synchronization:**  This is a keyword, that we can use it on both ‘Blocks (of code)’ and on Methods (both instance and static).  
- Why synchronization is introduced: To avoid data inconsistency problems. To Give more securities on methods/blocks, we use synchronization method.  
- if you use this code on block/method, at a time only one thread can access this. For instance methods/blocks, Object level will provided to first thread who access these. So when that thread release the lock, then only another thread gets the lock and access these methods.  
- On static block/method, a static level lock which also called ‘Class level lock’ will be provided to first thread who access these. So when that thread release the class lock, then only another thread get the lock and then access these methods.

**8: Volatile vs Synchronization:**  
- Volatile secures variables and synchronization secures methods/blocks.  
- Volatile only works on variables. Synchronization only works on methods/blocks.  
- Volatile gave a variable copy to each thread. At final, thread gives their final copy back to main copy.

**9: Purpose of Volatile:**    
- You have 5 threads, all these are accessing a variable int it. And each thread is modifying 50 times during execution. That means 50*5 = 250 times I get modified on main copy, so data incasistent problem will occur. To avoid this, Java introduced volatile keyword. Basically it protects variables if they are widely used by threads.   
- So each thread gets its own copy, at final they modify their copy on main copy.

**10: Generics:**  
- Basically if you know you are inserting only employee objects/data into one list, you can define that List as more generic, so return type would also be employee object type. So that means, you are avoiding typecasting while returning objects in Object type. These are more widely used. Generic doesn’t allow any other values except its own(ex: employee) objects.   
- But in raw type, you can have all types of values, but return type should need typecasted. 

**11: Difference between Synchronized and Volatile**   

| Synchronized methods/blocks        |      Volatile variable|
| ------------- |-------------|
|1: This only used for methods and blocks. |1.: This only used for variables. |
|2: This keyword used to allow only one thread to execute at one time. Basically protects statid and instance methods & blocks.  |2: This keyword gives separate copy for each thread. Basically protects variable|
|3: This is used to avoid data incosistency problems  |3: This is also used to avoid data inconsistency problems |


**12: Difference between Threads & Processors**    


| Threads        |      Processors|
| ------------- |-------------|
|1: All thread share same memory. |1.:Each process have thier own memory, they dont share memory most of the time|
|2: They use low CPU usage |2.They use high CPU usage |

**13: Deamon threads:**  
- Deamon threads run in the background. When you create deamon thread, after implementing it, you have to start it. 
- Most used deamon threads are used for garbage collectors and for security.  

**Garbage collectors:** For cleaning memory all the time, applications run  garbage collectors threads all the time.  For security purpose: If stopping attackers on web-based application, on background programmers run all threads to find if anybody is attacking.

**14: Deamon deadlock:**  
MutualTheadDeadlock: For ex: ThreadA has lock for ObjectA & threadB also have lock for ObjectA. Both holds lock but wait for another to release, but both don’t release. So deadlock happens. 

**15: ThreadGroup:**  
We can have multiple threads into one group.

**16: Thread wait, notify & notifyall.**   
Threads communicates to each other with wait, notify & notifyall.   
1: Wait: One thread notifies other threads that it is waiting for lock.  
2: notify: One thread notifies/tells one other thread that lock is released.  
3: notifyall:  One thread notifies/tells all other threads that lock is released.  
Example with threadA and threadB.: If threadA holds lock and thread waiting for the same lock. Then   
- ThreadB tells threadA that it is waiting for the lock  
- After execution, threadA notifies thread that lock is released.   
- After execution, threadA can tell all other threads (which are waiting for the same lock) that lock is released.  A question arises here: Lets say you have 10 threads, one holds lock and all other are waiting for the lock, when lock gets released which one gets the lock out of remaining nine. Basically, when multiple threads wait for the same lock, thread scheduler (manager) puts in the queue in priority, so no two threads get same priority. So when lock released, the next priority thread gets the lock.
