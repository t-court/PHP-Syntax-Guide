# PHP Syntax Guide #

## PHP Comments ##
* In PHP your comments can be either single line or multi line:

     `// This is how you do a single line comment`

    `/* This is how you do a multi line comment`
* Comments make it easy to explain your code within the same file without interfering.

## PHP Variables  ##
PHP variables, like other languages, are used to store many different kinds of data.
The equals sign is used as an assignment operator to assign values to variables.
When initializing a PHP variable you must remember that:

| Description                                    |      Example                                   |
|------------------------------------------------|------------------------------------------------|
| The variable name must have a $ at the start   |      `$myVariable = "this is a php variable";` |
| It cannot start with a number                  |      `$1variable = "this is wrong";`    |
| It must start with a letter or an underscore_  |      `$_variable = "this is right";`    |


- It can also only contain alpha-numerical characters and underscores
- The name cannot contain a space 
- Variables are case sensetive, and do not need to be declared before assigning it a value. 
- Constants variables are variable with a value that does not change (once it is initialized, it cannot be changed).

- To define a constant in PHP it looks like this:

    `define('name','value');`

- You could then call it like any other variable using its name.



## PHP Echo / Print ##
- Echo and print are both used to display data to the browser, although similar they have some slight differences.
- Echo can accept multiple parameters and has no return value therefore it is faster.
- Print is slower due to its return value of 1 and it can only accept one parameter.
- They both allow for HTML tags to be used within the statements.


## PHP Data Types ##
These are the data types supported by php:

    ~ Strings

    ~ Numbers

    ~ Floating point numbers

    ~ Booleans

    ~ Arrays

    ~ Objects

    ~ NULL

    ~ Resource

 ## PHP String  ## 
- A string is a collection of characters in single or double quotes, like "this is a string". They can be concatenated together or with other data types using a period.


 ## PHP Numbers ## 
- Also known as integers, they are whole numbers without a decimal point between -2,147,483,648 and 147,483,647.


 ## PHP Float ## 
- A floating point number is a number with a decimal in it or a number in exponential form.


 ## PHP Booleans ## 
- Booleans are simply true and false values, true is represented by 1 and false is represented by 0.


 ## PHP Arrays  ## 
- An array is a variable that is can hold several values. In PHP arrays are defined by using the array() keyword. The parenthesis are where you place your values. All arrays are zero based, so no matter the number of values in a array the index always starts at 0.

- PHP supports 3 types of arrays: 

|   Type        |   Description     |   Example     |
|---------------|-------------------|---------------|
|   Indexed array | A simple array with numeric key | `$skaters = array("Kader", "Horigome", "Silva");` |
|   Associative array | An array where each key has its own specific value. | `$skater_board_deals = array("Kader"=>"Baker", "Horigome"=>"April", "Silva"=>"Real")` |
|   Multidimensional array | An array holding one or more arrays within itself | `array: $skater_shoe_deals = array( array( "Kader"=> "Adidas" ), array( "Horigome"=>"Nike" ), array( "Silva"=>"Nike" ) );` |


`echo "Kader Sylla skates for " . $skater_shoe_deals[0]["Adidas"];`


 ## PHP Objects ## 
- Object-oriented programming consider two main aspects, classes and objects. Classes are a reuseable framework of an object, with properties and funtions, they are essentially templates for objects.
- An object is an instance of a class if you will, with the same properties and funtions as the class but properties contian different values from object to object. 

- A class is declared like so:

```
class myClass {

    public $name;

    function myName($name){
        echo $name;
    }
};
```

- And an object for this class could look like this:

`$newObject = new myClass("Theo");
`



 ## PHP Null  ##
Null is the value assigned to variables that have not been assigned a value. A null variable can only be null untill it is assigned a value. 


 ## PHP Resource ##
- The special resource type is not an actual data type. It is the storing of a reference to functions and resources external to PHP.

- A common example of using the resource data type is a database call.
For example:

```
// Check database connection

if($database = mysqli_connect('localhost','user','password','database')){
    echo "Successfully Connected";
}
```


## PHP Operators ##

 ### Arithmetic operators ### 
- The PHP arithmetic operators are used with numeric values to perform common arithmetical operations, such as addition, subtraction, multiplication etc.

|               |           |         |          |
|---------------|-----------|---------|----------|
| +	| Addition	| $x + $y	| Sum of $x and $y	| 
| -	| Subtraction	| $x - $y	| Difference of $x and $y	| 
| *	| Multiplication	| $x * $y	| Product of $x and $y	| 
| /	| Division	| $x / $y	| Quotient of $x and $y	| 
| %	| Modulus	| $x % $y	| Remainder of $x divided by $y	| 
| ** | Exponentiation	| $x ** $y	| Result of raising $x to the $y'th power| 

 ### Assignment operators ### 
- The PHP assignment operators are used with numeric values to write a value to a variable.

|               |           |                                  |                                     |
|---------------|-----------|----------------------------------|-------------------------------------|
| = | x = y	    | x = y	    | The left operand gets set to the value of the expression on the right	| 
| += | x += y	| x = x + y	| Addition	| 
| -= | x -= y	| x = x - y	| Subtraction	| 
| *= | x *= y	| x = x * y	| Multiplication	| 
| /= | x /= y	| x = x / y	| Division	| 
| %= | x %= y	| x = x % y	| Modulus | 

 ### Comparison operators ### 
- The PHP comparison operators are used to compare two values (number or string):

|               |           |                                  |                                     |
|---------------|-----------|---------------------------------|--------------------------------------|
| `==`	| Equal	| $x == $y	| Returns true if $x is equal to $y	| 
| `===`	| Identical	| $x === $y	| Returns true if $x is equal to $y, and they are of the same type	| 
| `!=`	| Not equal	| $x != $y	| Returns true if $x is not equal to $y	| 
| `<>`	| Not equal	| $x <> $y	| Returns true if $x is not equal to $y	| 
| `!==`	| Not identical	| $x !== $y	| Returns true if $x is not equal to $y, or they are not of the same type	| 
| `>`	| Greater than	| $x > $y	| Returns true if $x is greater than $y	| 
| `<`	| Less than	| $x < $y	| Returns true if $x is less than $y	| 
| `>=`	| Greater than or equal to	| $x >= $y	| Returns true if $x is greater than or equal to $y	| 
| `<=`	| Less than or equal to	| $x <= $y	| Returns true if $x is less than or equal to $y	| 
| `<=>`	| Spaceship	| $x <=> $y	| Returns an integer less than, equal to, or greater than zero, depending on if $x is less than, equal to, or greater than $y. Introduced in PHP 7.| 

 ### Increment/Decrement operators ### 
- The PHP increment operators are used to increment a variable's value.
- The PHP decrement operators are used to decrement a variable's value.

|               |           |                   |
|---------------|-----------|-------------------|
| `++$x`	| Pre-increment	| Increments $x by one, then returns $x	| 
| `$x++`	| Post-increment	| Returns $x, then increments $x by one	| 
| `--$x`	| Pre-decrement	| Decrements $x by one, then returns $x	| 
| `$x--`	| Post-decrement	| Returns $x, then decrements $x by one| 

 ### Logical operators ### 
- The PHP logical operators are used to combine conditional statements.

|               |           |         |          |
|---------------|-----------|---------|----------|
| `and`	| And	| `$x and $y`	| True if both $x and $y are true	
| `or`	| Or	| `$x or $y`	| True if either $x or $y is true	
| `xor`	| Xor	| `$x xor $y`	| True if either $x or $y is true, but not both	
| `&&`	| And	| `$x && $y`	| True if both $x and $y are true		
| `!`	| Not	| `!$x`	        | True if $x is not true

*`||` can also be used instead of or

 ### String operators ### 
- PHP has two operators that are specially designed for strings.

|               |           |         |         
|---------------|-----------|---------|
| `.`	| Concatenation	| `$txt1 . $txt2`	| Concatenation of $txt1 and $txt2	
| `.=`	| Concatenation assignment	| `$txt1 .= $txt2`	| Appends $txt2 to $txt1

 ### Array operators ### 
- The PHP array operators are used to compare arrays.

|               |           |         |          |
|---------------|-----------|---------|----------|
| `+`	    | Union	| `$x + $y`	        | Union of $x and $y	
| `==`	| Equality	| `$x == $y`	| Returns true if $x and $y have the same key/value pairs	
| `===`	| Identity	| `$x === $y`	| Returns true if $x and $y have the same key/value pairs in the same order and of the same types	
| `!=`	| Inequality	| `$x != $y`	| Returns true if $x is not equal to $y	
| `<>`	| Inequality	| `$x <> $y`	| Returns true if $x is not equal to $y	
| `!==`	| Non-identity	| `$x !== $y`	| Returns true if $x is not identical to $y



## PHP Conditional Statements ##
### If ###
- Execute code if condition is met.

```
if (condition){
    run this code;
}
```

### If Else ###
- Executes code if a codition is met and if it is not met it executes the code in the else statement.

```
if (condition){
    run this code;
}else{
    run this code if first condition was not met;
}
```

### If Else if ###
- Executes different code depepnding on which condition is met for more than two conditions.

```
if (condition){
    execute this code
} elseif (condition) {
    execute this code if the condition is met and the first condition is false ;
} else {
    execute this code if neither condition is met;
}
```



## PHP Functions ##

-  PHP has an array of different built in function that can be called from within your script. These function have a variety of different use cases for whatever specific task you have. If there is no function fit for the task you need completed you can create your. Making functions can save you a lot of time as they can be made reuseable to automate your script as much as possible.

- Creating a funtion looks like this:

```
function my_function(){
    code to be executed;
}
```

- You can also pass value into function using parameters.
- That looks like this:

```
function my_function($parameter1,$parameter2){
    echo $parameter1 . $parameter2;     
    other executable code
}
```



## PHP Loops ##
- Loops execute the same code repeatedly until or as long as a specific condition has been met. Loops help users from having to rewrite the same code multiple times.
- There are four types of PHP Loops:

### 1. While Loops ###
- Executes code as long as(while) a specified condition is true.

```
while (condition=true){
    execute this code;
}
```

### 2. Do... While Loop ###
- Executes a block of code once, then repeats the loop as long as the condition is true.

```
do {
    code to be executed;
} while (condition = true);
```

### 3. For Loop ###
- Executes block of code a specified number of times.

```
for (initial counter; Evaluated for each loop iteration. If it evaluates to TRUE, the loop continues. If it evaluates to FALSE, the loop ends; increment the count)[
    execute this code;
]
```

### 4. Foreach Loops ###
- Loops through the block of code for each element there is in an array.

```
foreach($element_in_array){
    complete this code;
}
```
