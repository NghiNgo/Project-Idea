# Project Idea: Complete user’s Activities tracking with Remote Assistance

This Program is divided into two major modules one is for complete activity tracking and can even tell which activity is currently active on the user’s side.
Can also work as a Global Keylogger to log the text written by a user on any process window ( Only when Proper undertaking ).
The second module is for Remote Access which is widely used for Visual remote assistance and specially used on Industries, Colleges, Training Centers and many more. This project is fully based on Client-Server Architecture which is efficiently implemented using JAVA, C bridged by JNI.

# Features :
## First Module : Activity Tracking
### Server side:
It can track 100 clients at a time with simplest user interface with fast access to data .
This server program gives you choices to track user text on current activity from window handle to text init. (A-Z tracking)
Can even track Google chrome tabs to a text file located in FileSystem.
Uses Global key logger to log text typed by each of the users.
### Client side:
There is no UI for the client-side program.
It runs as a background process which runs on window’s startup or can be invoked by server process using RMI(remote method invocation).

## Second Module: Remote Visual Accessing
Master side:
It based on Master and slave architecture. Master’s side provides a visual Reflection of slave’s PC to provide a nice interface for remote access.
Master can control the slave’s machine completely from playing music to searching web.
It can only handle the slave at a time.
Slave side:
No user interface for Slave’s side its a background process.
Master’s actions are fully reflected on the slave’s machine.
A slave can be invoked by a Master machine at any time.

## Implementation Details:
No database used for the purpose of fast accessing of a large amount of data created per second.
For accessing Data we used nested TreeMap along with ArrayList for storing data in an efficient manner for fast access.
The concept behind using TreeMap is to fetch the data in Sorted order in O(logn) time complexity.
Small code snippet is given from implementation :

```
for (Map.Entry<String, TreeMap<String, TreeMap<String, ArrayList> > > en : tm.entrySet()) {
    System.out.print(en.getKey() + "-->");
    TreeMap<String, TreeMap<String, ArrayList> > tm1 = en.getValue();
    for (Map.Entry<String, TreeMap<String, ArrayList> > en1 : tm1.entrySet()) {
        System.out.print(en1.getKey() + "-->");
        TreeMap<String, ArrayList> tm2 = en1.getValue();
        for (Map.Entry<String, ArrayList> en2 : tm2.entrySet()) {
            System.out.print(en2.getKey() + "-->");
            ArrayList ar = en2.getValue();
                                for(int i=0;i");
        }
    }
}
```

# Tools/Programming Languages used:
Java
C
JNI
RMI
Notepad++

# RESEARCH WORK:
Deeply studied about JNI from web resources
RMI
Worked with Windows inbuilt functions using jni.
https://msdn.microsoft.com/en-us/library/windows/
Learned about Runtime class, Robot class, etc.
Special thanks to GEEKSFORGEEKS, StackOverflow.