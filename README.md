# Javacript-Classes

## CLASSES
- Used to create objects.
- The objects do things in progams.
You can define 2 main areas of a class which are created:
  1. What an object will have --> Called an Instance property.
      Instance properties describes the property - Data about property
      eg. Person (properties): name, height, age.
  2. What an object will do --> Called an Instance method.
      Instance methods use instances properties to get their results. 
      eg. Person (mehtods): run, walk, jump. talk [their actions and behariors.]
      
      
 ### How to create a class?</br>
    1. Use class keyword.</br>
    2. Use the class Name (first letter capped)</br>
    3. Use curly braces `{}` containing the class definition.</br>
    4. Has a constructor. A method run when object is created.</br> 
 #### Result ==>
  
        class Name {
          definition
          constructor {
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
2.Use 'keyword' with property name
Result --> this.property name

## Class Declaration Vs Class Expression

### Declaration
`class` keyword and the class Name

      class Person {
        constructor(name) {
          this.name = name;
            `remainder of class body`
          }
        }

### Expression
Class defined by expression assigned to variable

    const Person = class {
        constructor(name) {
          this.name = name;
        }
     };

## Side‑by‑Side Comparison
|Feature  |Class Declaration  | CLass Expression | 
|----|----|----|
|Name required | Yes | No(can be anonymous) | 
|Hoisted |Yes(but uninitialzed) | No | 
|Can be anonymous | No | Yes | 
|Can be used inline  |No | Yes  | 
|Typical use |Defining main classes  | Dynamic or conditional class creation | 


#### Classes create multiple objects
- Define as a class declaration

        class Dog {
          constructor(name) {
          this.name = name;
           }
             bark() {
               console.log(`${this.name} says woof!`);
             }
         }

#### Contains:
- class keyword,
- A Name,
- A body (contains methods and a constructor)
- Constructor called when object created
- Instances of the classs can be created using 'new' keyword
- Example: Create a new instance of Dog class

        const dog = new Dog("Gino");
- To access the property us dot notation

        dog.name
- Call methods

                dog.bark();
- Or Defined as a class Expression

        const Dog = class {
          constructor(name) {
            this.name = name;
          }
        
          bark() {
            console.log(`${this.name} says woof!`);
          }
        };
#### Purpose of a constructor 
- Initialize an objects properties when created
#### How to create an instance of a class 
- new keyword, class's Name, arguments 
#### Difference between class and object 
- class is a blueprint to create an ojbect
- Object is an instance of a class


