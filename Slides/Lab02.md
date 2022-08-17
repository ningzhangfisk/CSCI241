# CSCI241L
# Dr. Ning Zhang
# Introduction to Java Class
# 1. Java OOP
+ OOP stands for Object-Oriented Programming.
+ Procedural programming is about writing procedures or methods that perform operations on the data, while object-oriented programming is about creating objects that contain both data and methods.
+ Object-oriented programming has several advantages over procedural programming:
  - OOP is faster and easier to execute
  - OOP provides a clear structure for the programs
  - OOP helps to keep the Java code DRY "Don't Repeat Yourself", and makes the code easier to maintain, modify and debug
  - OOP makes it possible to create full reusable applications with less code and shorter development time
+ **Tip**: The "Don't Repeat Yourself" (DRY) principle is about reducing the repetition of code. You should extract out the codes that are common for the application, and place them at a single place and reuse them instead of repeating it.

# 2. Java Classes and Objects
+ Java is an object-oriented programming language.
+ Classes and objects are the two main aspects of object-oriented programming.
+ Everything in Java is associated with classes and objects, along with its `attributes` and `methods`. For example: in real life, a car is an object. The car has attributes, such as weight and color, and methods, such as drive and brake.
+ A Class is like an object constructor, or a "blueprint" for creating objects.
+ Look at the following illustration to see the difference between class and objects:

![classes and objects 1](https://miro.medium.com/max/1400/1*PwmN5iM2NMkDhGpXvMyK1A.png)

+ For the following sections, we use the code [here](https://replit.com/@ZhangNing1/CSCI241NingZhang#CSCI241L/Car.java)
## 2.1 Create a class and objects
+ Create the `Car` class with no attributes or methods.
+ Create `Car` objects
~~~~
// create Car class
class Car {
  // attributes
  // constructors
  // methods
  // main method contains all the test code
  public static void main(String[] args) {
    // create a Car object
    Car myCar = new Car();
  }
}
~~~~

+ Using Multiple Classes
  - You can also create an object of a class and access it in another class. This is often used for better organization of classes (one class has all the attributes and methods, while the other class holds the main() method (code to be executed)).
  - Remember that the name of the java file should match the class name. In this example, we can create two files in the same directory/folder:
    + Car.java
    + Test.java
~~~~
// filename Car.java
class Car {
  // attributes
  // constructors
  // methods
}
~~~~

~~~~
// create Car class
class Test {
  // main method contains all the test code
  public static void main(String[] args) {
    // create a Car object
    Car myCar = new Car();
  }
}
~~~~

  - In this class, we will put the class and the test code in one single java file.

## 2.2 Java Class Attributes
+ Class `attributes` are variables within a class.
+ Another term for class attributes is `fields`.
### 2.2.1 Define attributes
+ You can define attributes as variables in a class.

~~~~
// attributes
String Company;
String Color;
Double Speed;
~~~~
### 2.2.2 Accessing Attributes
+ You can access attributes by creating an object of the class, and by using the dot (`.`) syntax.
+ Note that we have not initialized the attributes, so the default values will be printed.
~~~~
Car myCar = new Car();
System.out.println(myCar.Company);
System.out.println(myCar.Color);
System.out.println(myCar.Speed);
~~~~
### 2.2.3 Modify Attributes
+ You can also modify attribute values by using the dot (`.`) syntax.

~~~~
    Car myCar = new Car();
    myCar.Company = "Honda";
    myCar.Color = "Black";
    myCar.Speed = 80;
    System.out.println(myCar.Company);
    System.out.println(myCar.Color);
    System.out.println(myCar.Speed);
~~~~


## 2.3 Java Class Methods
+ Methods are declared within a class
+ They are used to perform certain actions.
+ [Understand this keyword in Java](https://www.w3schools.com/java/ref_keyword_this.asp)
~~~~
// create Car class
class Car {
  // attributes
  String Company;
  String Color;
  double Speed;
  // constructors
  // methods
  public double getSpeed(){
    return Speed;
    // you can also use return this.Speed;
  }
  public void setSpeed(double Speed){
    this.Speed = Speed;
  }
  // main method contains all the test code
  public static void main(String[] args) {
    // create a Car object
    Car myCar = new Car();
    System.out.println(myCar.getSpeed());
    myCar.setSpeed(80);
    System.out.println(myCar.getSpeed());
  }
}
~~~~

## 2.4 Java Constructors
+ A constructor in Java is a special method that is used to initialize objects.
+ The constructor is called when an object of a class is created. 
+ It can be used to set initial values for object attributes.
+ It has the same name with the Class.
+ It has no return value.

~~~~
// create Car class
class Car {
  // attributes
  String Company;
  String Color;
  double Speed;
  // constructors
  public Car(){
    this.Company = "Honda";
    this.Color = "Black";
    this.Speed = 0;
  }
  public Car(String Company, String Color){
    this.Company = Company;
    this.Color = Color;
    this.Speed = 0;
  }
  public Car(String Company, String Color, double Speed){
    this.Company = Company;
    this.Color = Color;
    this.Speed = Speed;
  }
  // methods
  public double getSpeed(){
    return Speed;
    // you can also use return this.Speed;
  }
  public void setSpeed(double Speed){
    this.Speed = Speed;
  }
  // main method contains all the test code
  public static void main(String[] args) {
    // create a Car object
    Car myCar1 = new Car();
    Car myCar2 = new Car("Nissan", "Blue");
    Car myCar3 = new Car("Toyota", "Red", 80);
    
  }
}
~~~~
## 2.5 Java Modifiers
### 2.5.1 Access Modifiers
+ For `classes`, you can use either `public` or `default`:

|Modifier|Description|
|~~~|~~~|
|public|The class is accessible by any other class|
|default|The class is only accessible by classes in the same [package](https://www.w3schools.com/java/java_packages.asp). This is used when you don't specify a modifier.|

+ For `attributes`, `methods` and `constructors`, you can use the one of the following

|Modifier|Description|
|~~~|~~~|
|public|The code is accessible for all classes|
|private|The code is only accessible within the declared class|
|default|The code is only accessible in the same package. This is used when you don't specify a modifier.|
|protected|The code is accessible in the same package and [subclasses](https://www.w3schools.com/java/java_inheritance.asp).|

### 2.5.2 Non-Access Modifiers
+ We will not use non-access modifiers a lot in our class(maybe we will use the `final` modifier in later topics/labs). If you need to learn it, please googole it or use this [link](https://www.w3schools.com/java/java_modifiers.asp)

## 2.6 Java Encapsulation
+ The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users. To achieve this, you must:
  - declare class variables/attributes as private
  - provide public `get` and `set` methods to access and update the value of a private variable

~~~~
// attributes
  private String Company;
  private String Color;
  private double Speed;
~~~~

+ Why Encapsulation?
  - Better control of class attributes and methods
  - Class attributes can be made read-only (if you only use the get method), or write-only (if you only use the set method)
  - Flexible: the programmer can change one part of the code without affecting other parts
  - Increased security of data
