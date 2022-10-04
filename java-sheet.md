Garbage Collection: Garbage collection is the technique through which Java programs maintain their memory automatically. Java programs are compiled into bytecode that may be executed by a Java Virtual Machine, or JVM. Objects are produced on the heap, which is a part of memory devoted to the Java application, while it runs on the JVM. Some objects will become obsolete over time. To free up memory, the garbage collector detects these useless objects and deletes them.

finalize method: It’s a method that the Garbage Collector calls shortly before deleting or destroying an object that’s suitable for Garbage Collection in order to do cleanup. Clean-up activity entails de-allocating or closing the resources associated with that object, such as Database Connections and Network Connections. It’s important to remember that it’s not a reserved keyword. Garbage Collector destroys the object as soon as the finalise method completes. The finalise method is found in the Object class and has the following syntax: protected void finalize throws Throwable{}

Since the finalize function is contained in the Object class and Object is the superclass of all Java classes, the finalize method is available to all Java classes. As a result, the garbage collector may invoke the finalise function on any java object. We must override the finalize method present in the Object class to specify our own clean-up activities since the finalize function in the Object class has an empty implementation.

Check out commonly asked Java Problems in Interviews: Click 
2. Java Basics
Let us look at some of the basic concepts frequently used in the Java programming language.

object - An object is an entity with state and behaviour, such as a chair, a bike, a marker, a pen, a table, a car, and so on. It could be either physical or logical (tangible or intangible). The financial system is an example of an intangible object.

There are three characteristics of an object:

