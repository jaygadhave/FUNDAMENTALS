Reflection is an API that is used to examine or modify the behavior of methods, classes, and interfaces at runtime. The required classes for reflection are provided under java.lang.reflect package which is essential in order to understand reflection. So we are illustrating the package with visual aids to have a better understanding as follows: 

java.lang.reflect

Reflection gives us information about the class to which an object belongs and also the methods of that class that can be executed by using the object.
Through reflection, we can invoke methods at runtime irrespective of the access specifier used with them.
reflection

 Reflection can be used to get information about class, constructors, and methods as depicted below in tabular format as shown:


Class	 The getClass() method is used to get the name of the class to which an object belongs.
Constructors	The getConstructors() method is used to get the public constructors of the class to which an object belongs.
Methods	The getMethods() method is used to get the public methods of the class to which an object belongs.
We can invoke a method through reflection if we know its name and parameter types. We use two methods for this purpose as described below before moving ahead as follows:

getDeclaredMethod()
invoke()
Method 1: getDeclaredMethod(): It creates an object of the method to be invoked. 

Syntax: The syntax for this method

Class.getDeclaredMethod(name, parametertype)
Parameters:

Name of a method whose object is to be created
An array of Class objects
Method 2: invoke(): It invokes a method of the class at runtime we use the following method.

Syntax: 

Method.invoke(Object, parameter)
Tip: If the method of the class doesn’t accept any parameter then null is passed as an argument.

Note: Through reflection, we can access the private variables and methods of a class with the help of its class object and invoke the method by using the object as discussed above. We use below two methods for this purpose.

Method 3: Class.getDeclaredField(FieldName): Used to get the private field. Returns an object of type Field for the specified field name. 


Method 4: Field.setAccessible(true): Allows to access the field irrespective of the access modifier used with the field.

Important observations Drawn From Reflection API
Extensibility Features: An application may make use of external, user-defined classes by creating instances of extensibility objects using their fully-qualified names.
Debugging and testing tools: Debuggers use the property of reflection to examine private members of classes.
Performance Overhead: Reflective operations have slower performance than their non-reflective counterparts, and should be avoided in sections of code that are called frequently in performance-sensitive applications.
Exposure of Internals: Reflective code breaks abstractions and therefore may change behavior with upgrades of the platform.
