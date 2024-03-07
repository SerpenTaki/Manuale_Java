Java is a popular programming language, created in 1995. Owned by Oracle.
It is used for:
- mobile application
- Desktop application
- Web application
- Web server and application servers
- Games
- Database connection
- ...
# Why use Java?
- Work on different platforms
- Is very popular
- It has a large demand on current job markert
- It's easy and simple to use
- opensource and free
- It is secure, fast and powerful
...
`java -version` for check if you havve installed Java on your pc.

# QuickStart
In Java every application begins with a class name, and that class must match the filename.
Let's create our first Java file, called Main.java. which can be done in any text editor.
```Java
public class Main {  
    public static void main(String[] args) {  
        System.out.println("Hello world");  
    }  
}
```
To execute navigate to your directory where the file is saved and type
`javac Main.java` this is for compiling
`java Main` this is for executing

--

Every line of code that runs in Java must be inside a `class`. In our example, we named the class **Main**. A class should always start with an uppercase first letter.

**Note:** Java is case-sensitive: "MyClass" and "myclass" has different meaning.

The name of the java file **must match** the class name. When saving the file, save it using the class name and add ".java" to the end of the filename.

## The main Method
The `main()` method is required and you will see it in every Java program:
`public static void main(String[] args)`
Any code inside the `main()` method will be executed. Just remember that every Java program has a `class` name which must match the filename, and that every program must contain the `main()` method.
### Print text
For printing we use the method `println()`
```Java
public class Main {  
    public static void main(String[] args) {  
        System.out.println("Hello world");  
        System.out.println("Second line");
        System.out.println(3); //print 3  
        System.out.println(4+4); //print 8
    }  
}

//single line comment
/*Multi 
Line
Comment Like C and C++ */ 
```
## Variables
| types     | desc                                                                                      |
| --------- | ----------------------------------------------------------------------------------------- |
| `String`  | stores text, sting values are surrounded by double quotes `"Hello"`                       |
| `int`     | stores integers, without decimal such as 123 or -123                                      |
| `float`   | stores floating point number with decimal such as 19.99 or -19.99                         |
| `char`    | stores a single char such as 'a' or 'b'. Char are sourrounded by single quotes ` 'a' 'b'` |
| `boolean` | stores values with 2 states: true or false                                                |
`type variableName = value; //to declare a variable`
```Java
public class Main {  
    public static void main(String[] args) {  
        String name = "John";  
        int num = 69;  
        System.out.println(name); //print John  
        System.out.println(num);//print 69  
    }  
}
```
#### Final keyword
If you don't want others to overwrite existing values, use `final` keyword (this will declare the variable as final or constant, witch means unchangeable)
```Java
final int myNum = 15;
myNum = 20; //will generate an error
```
#### Display variables
The `println()` method is often used to display variables, to combine both text and a variable, use the `+` character:
```Java
public class Main {  
    public static void main(String[] args) {  
        String name = "John";  
        System.out.println("Hello " + name);//print Hello John
        String surname = "Galt";  
        String fullname = name + surname;  
        System.out.println(fullname); // print John Galt 
        int x = 5;
        int y = 6;
        System.out.println(x + y); //print 11 
    }  
}
```
#### Declare many variables
Instead of:
```Java
int x = 5;
int y = 6;
int z = 50;
System.out.println(x+y+z);
```
We can simply write:
```Java
int x = 5, y = 6, z = 50;
System.out.println(x+y+z);

// if we want to asign the same value to multiple variables
int x, y, z;
x = y = z = 50;
System.out.println(x + y + z);
```
# Java identifiers
All java **variables** must be **identified** with an **unique names**. These unique names are called **identifiers**.
Identifiers can be short names (`x, y`) or more descriptive names `(age, sum, totalVolume)`
```Java
//good
int minutesPerHour = 60;

//OK, but not so easy to understand what m actually is
int m = 60;
```
## Primitive Data Types
A primitive data types specifies the size and type of variable values, and it has no additional methods. There are 8 primitive types in Java:

| **Data Type** | **Size** | **Description**                                                                   |
| ------------- | -------- | --------------------------------------------------------------------------------- |
| `byte`        | 1 byte   | stores whole numbers from -128 to 127                                             |
| `short`       | 2 bytes  | Stores whole numbers from -32,768 to 32,767                                       |
| `int`         | 4 bytes  | Stores whole numbers from -2,147,483,648 to 2,147,483,647                         |
| `long`        | 8 bytes  | Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| `float`       | 4 bytes  | Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits           |
| `double`      | 8 bytes  | Stores fractional numbers. Sufficient for storing 15 decimal digits               |
| `boolean`     | 1 bit    | Stores true or false values                                                       |
| `char`        | 2 bytes  | Stores a single char/letter or ASCII values                                       |
## Non-Primitive Data Types
Non-primitive data types are called **reference types** because they refer to objects.
The main difference between **primitive** and **non-primitive** data types are:
- Primitive types are predefined (already defined) in Java. Non-primitive types are created by the programmer and is not defined by Java (except for `String`).
- Non-primitive types can be used to call methods to perform certain operations, while primitive types cannot.
- A primitive type has always a value, while non-primitive types can be `null`.
- A primitive type starts with a lowercase letter, while non-primitive types starts with an uppercase letter.
## Java Type Casting
Type casting is when you assign a value of one primitive data type to another type.
2 type of Casting in Java:
- **Widening Casting** (*automatically*)->converting a smaller type to a larger type size
	`byte->short->char->int->long->float->double`
- **Narrowing Casting** (*manually*) -> converting a larger type to a smaller size type
	`double->float->long->int->char->short->byte`
```Java
public class Main {  
    public static void main(String[] args) {  
        int myInt = 9;  
        double myDouble = myInt; // Automatic casting: int to double  
		  //Widening Casting
        System.out.println(myInt);      // Outputs 9  
        System.out.println(myDouble);   // Outputs 9.0  
    }  
}
```
```java
public class Main {
  public static void main(String[] args) {
    double myDouble = 9.78d;
    int myInt = (int) myDouble; // Manual casting: double to int
		//Narrowing casting
    System.out.println(myDouble);   // Outputs 9.78
    System.out.println(myInt);      // Outputs 9
  }
}
```
# Operators
- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Bitwise operators
##### Arithmetic Operators
| Operator | Name           | Description                            | Example |
| -------- | -------------- | -------------------------------------- | ------- |
| `+`      | Addition       | Adds 2 values                          | `x+y`   |
| `-`      | Subtraction    | Subtracts one value from another       | `x-y`   |
| `*`      | Multiplication | Multiplies 2 values                    | `x*y`   |
| `/`      | Division       | Divides one value by another           | `x/y`   |
| `%`      | Modulus        | Returns the division remainder         | `x%y`   |
| `++`     | Increment      | Increases the value of a variable by 1 | `++x`   |
| --       | Decrement      | Decreases the value of a variable by 1 | `--x`   |
##### Assignment Operator
| Operator | Example | Same as     |
| -------- | ------- | ----------- |
| `=`      | `x=5`   | `x=5`       |
| `+=`     | `x+=3`  | `x = x + 3` |
| `-=`     | `x-=3`  | `x = x - 3` |
| `*=`     | `x*=3`  | `x = x * 3` |
| `/=`     | `x/=3`  | `x = x / 3` |
| `%=`     | `x%=3`  | `x = x % 3` |
| `&=`     | `x&=3`  | `x = x & 3` |
| `\|=`    | `x\|=3` | `x = x\|3`  |
| `^=`     | `x^=3`  | `x = x^3`   |
| `>>=`    | `x>>=`  | `x= x>>3`   |
| `<<=`    | `x<<=`  | `x<<=3`     |
##### Comparison Operators
```Java
int x=3, y=5;
System.out.println(x > y); //returns false
```

| Operator | Name                     | Example  |
| -------- | ------------------------ | -------- |
| `==`     | Equal to                 | `x==y`   |
| `!=`     | Not Equal                | `x!=y`   |
| `>`      | Greater than             | `x>y`    |
| `<`      | Less than                | `x>=y`   |
| `>=`     | Greater than or equal to | `x >= y` |
| `<=`     | Less than or equal to    | `x <= y` |
##### Logical operators

| Operator | Name        | Description                                             | Example          |
| -------- | ----------- | ------------------------------------------------------- | ---------------- |
| `&&`     | Logical and | Returns true if both statements are true                | `x < 5 && x<10`  |
| `\|\|`   | Logical or  | Returns true if one of the statement is true            | `x<5 \|\| x<4`   |
| `!`      | Logical NOT | reverse the result. returns false if the result is true | `!(x<5 && x<10)` |
# Java Strings
