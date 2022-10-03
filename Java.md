Boilerplate
class HelloWorld{ 
public static void main(String args[]){ 
System.out.println("Hello World"); 
} 
}
Showing Output
It will print something to the output console.

System.out.println([text])
Taking Input
It will take string input from the user

import java.util.Scanner; //import scanner class

// create an object of Scanner class
Scanner input = new Scanner(System.in);

// take input from the user
String varName = input.nextLine();
Primitive Type Variables
The eight primitives defined in Java are int, byte, short, long, float, double, boolean, and char those aren't considered objects and represent raw values.

byte
byte is a primitive data type it only takes up 8 bits of memory.

age = 18;
