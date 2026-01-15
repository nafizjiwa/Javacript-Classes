# Javacript-Classes

## CLASSES
- A blueprint used to create objects.
- The objects do an action.
- The class creates:
  1. What an object will have --> each Instance has properties - Data
      eg. Person (properties): name, height, age.
  2. What an object will do --> each Instance has methods.
      Instance methods use instances properties to get results. 
      eg. Person (mehtods): run, walk, jump. talk [their actions and behariors.]
       
 ### How to create a class?</br>
    1. Use class keyword.</br>
    2. Use the class Name (first letter capped)</br>
    3. Use curly braces `{}` containing the class definition.</br>
    4. Has a constructor. A method run when object is created.</br> 
 #### Result ==>
  
        class Name {
          definition
          constructor 
          `remainder of class body`
          - A METHOD AND IS USED TO SET UP THE OBJECT-
          }
        }
    
### **ONCE THE CLASS IS CREATED AN OBJECT FOR THAT CLASS CAN BE CREATED. 
  1. Create a variable
    let variable name
  2. Set variable equal to the new class created using the 'new' keyword and objects name
    let variable name = new ojbect name
  3. Add parenthese to call the constructor method and set object up.
    let variable name = new object name();
    
NOW THE INSTANCE PROPERTIES CAN BE DEFINED IN THE CONSTRUCTOR

#### HOW TO DEFINE INSTANCE PROPERTIES? 
1.Use the 'this' keyword
  'this' refers to the current object being created by the class. 
2.Use 'this' keyword with property name
  Result --> this.property name


## Side‑by‑Side Comparison
|Feature  |Class Declaration  | CLass Expression | 
|----|----|----|
|Name required | Yes | No(can be anonymous) | 
|Hoisted |Yes(but uninitialzed) | No | 
|Can be anonymous | No | Yes | 
|Can be used inline  |No | Yes  | 
|Typical use |Defining main classes  | Dynamic or conditional class creation | 



## Class Declaration Vs Class Expression
#### Classes allow creation of multiple objects

### Declaration
- Syntax of class declaration
- Has `class` keyword and the class Name
- A body (contains methods and a constructor)

        class Dog {
          constructor(name) {
          this.name = name;
           }
             bark() {
               console.log(`${this.name} says woof!`);
             }
         }
  
- Can't be used before being defined
  
        const p = new Dog(); // ReferenceError
        class Dog { body }

#### Create an Instance of a class:

- Instances is created using 'new' keyword
- Constructor called when object created
- Example: Create a new instance of Dog class

        const dog = new Dog("Gino");
- To access the property us dot notation

        dog.name
- Call methods

                dog.bark();
  
### Expression
- Class defined as an expression and assigned to variable

        const Dog = class {
          constructor(name) {
            this.name = name;
          }
        
          bark() {
            console.log(`${this.name} says woof!`);
          }
        };
- Dynamic, so can be used before declaration

    const Dynamic = Dog();
    new Dynamic().speak();
  
#### Purpose of a constructor 
- Initialize an objects properties when created
#### How to create an instance of a class 
- new keyword, class's Name, arguments 
#### Difference between class and object 
- class is a blueprint to create an ojbect
- Object is an instance of a class


`this` keyword accesses and manipulates objects
1. Primary Purpose:
To access properties and methods of current object
2. What does `this` refer to
`this` refers to different objects depending on the context which it is used
3. When do we use `this`
To access properties and methods of an object

## INHERITANCE
- Parent is the blueprint for other classes
- It defines properties and methods inherited by other classes
- Child class inherits the properties
- Children can also extend functionality of the parent by adding new props and methods.
- The keyword `extends` is used to implement inheritance
- extnds indicates its a child class of another class
#### Purpose of inheritance
- To reuse code and create hierarchical relationships between classes
#### What is the keyword use to inherit from a parent class
- extends
#### How are parent and child class different
- A child class is a specialized version of a parent class
- As in below example a chld that adds a property actually extends the parent

          class Vehicle {                  ---> Parent or superclass
            constructor(brand, year) {
              this.brand = brand;
              this.year = year;
            }
          }
  
          class Tire extends Vehicle {            ---> Tire extend Vehicle but not with new properties
                Flat() {                          ---> It only extends with a method
                  console.log("I have a Flate tire!");    ---> constructor not requred to extend
                }
            }
          
          class Car extends Vehicle {            ---> Child class or subclass
            constructor(brand, year, numDoors) { ---> has a constructor because it adds a propery numDoors
              super(brand, year);                ---> super invokes constructor of the parent
              this.numDoors = numDoors;          ---> This property is exclusive to the Car class
            }                                    ---> If Child class did not contain a property constructor is not required
          }
          
          let myCar = new Car("bmw", 2016, 4);          ----> create an instance of Car class and store it in myCar
          console.log(myCar.brand);
          console.log(myCar.year);
          console.log(myCar.numDoors);

          let myTire = new Tire("honda", 2019);
          console.log(myTire.brand); // honda
          console.log(myTire.year);  //2019
          myTire.honk();   //"I have a flat tire" 

  - 
