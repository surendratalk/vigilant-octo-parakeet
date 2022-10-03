Php Cheatsheet
Basics
Hello World
echo function is used to display or print output

<?php echo "Hello World!"; ?>
Comments
Commets are used to make the code more understandable for programmer, they are not executed by compiler or interpreter.

One Liner
This is a singleline comment

// Twinkle Twinkle Little Star
Another One Liner
This is a single-line comment

# Chocolate dedo mujhe yaar
Multiline
This is a multiline comment

/* Code With 
Harry */
Vardump
This function dumps information about one or more variables.

<?php var_dump(var1, var2, ...); ?>
Variables
Variables are "containers" for storing information.

Defining Variables
<?php
$Title = "PHP Cheat Sheet By CodeWithHarry";
?>
Datatypes
Datatype is a type of data

String
A string is a sequence of characters, like "Hello world!".

<?php 
$x = "Harry"; 
echo $x; 
?>
Integer
An integer is a number without any decimal part.

<?php
$x = 1234;
var_dump($x);
?>
Float
A float is a number with a decimal point or a number in exponential form.

<?php 
$x = 1.2345; 
var_dump($x); 
?>
Array
An array stores multiple values in one single variable

<?php
$names = array("Harry","Rohan","Shubham");
var_dump($names);
?>
Class
A class is a template for objects

<?php 
class Harry{ 
// code goes here... 
} 
?>
Object
An object is an instance of the class.

<?php 
class Bike { 
public $color; 
public $model; 
public function __construct($color, $model) { 
$this->color = $color; 
$this->model = $model; 
} 
public function message() { 
return "My bike is a " . $this->color . " " . $this->model . "!"; 
} 
} 

$myBike = new Bike("red", "Honda"); 
echo $myBike -> message(); 
?>
Escape Characters
Escape sequences are used for escaping a character during string parsing. It is also used for giving special meaning to represent line breaks, tabs, alerts and more.

Line feed
It adds a newline

\n
Carriage return
It inserts a carriage return in the text at this point.

\r
Horizontal tab
It gives a horizontal tab space

\t
Vertical tab
It gives a vertical tab space

\v
Escape
It is used for escape characters

\e
Form feed
It is commonly used as page separators but now is also used as section separators.

\f
Backslash
It adds a backslash

\\
Dollar sign
Print the next character as a dollar, not as part of a variable

\$
Single quote
Print the next character as a single quote, not a string closer

\'
Double quote
Print the next character as a double quote, not a string closer

\"
Operators
Operators are symbols that tell the compiler or interpreter to perform specific mathematical or logical manipulations. These are of several types.

Arithmetic Operators
Addition
Sum of $x and $y

$x + $y
 
Subtraction
Difference of $x and $y

$x - $y
Multiplication
Product of $x and $y

$x * $y
Division
Quotient of $x and $y

$x / $y
Modulus
The remainder of $x divided by $y

$x % $y
Exponentiation
Result of raising $x to the $y'th power

$x ** $y
PHP Assignment Operators
The PHP assignment operators are used with numeric values to write a value to a variable.

x = y
The left operand gets set to the value of the expression on the right

x = y
x += y
Addition

x = x + y
x -= y
Subtraction

x = x - y
x *= y
Multiplication

x = x * y
x /= y
Division

x = x / y
x %= y
Modulus

x = x % y
PHP Comparison Operators
Equal
Returns true if $x is equal to $y

$x == $y
Identical
Returns true if $x is equal to $y, and they are of the same type

$x === $y
