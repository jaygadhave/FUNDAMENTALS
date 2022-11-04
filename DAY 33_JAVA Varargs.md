Variable Arguments (Varargs) in Java

Variable Arguments (Varargs) in Java is a method that takes a variable number of arguments. Variable Arguments in Java simplifies the creation of methods that need to take a variable number of arguments.

Need of Java Varargs
Until JDK 4, we cant declare a method with variable no. of arguments. If there is any change in the number of arguments, we have to declare a new method. This approach increases the length of the code and reduces readability.
Before JDK 5, variable-length arguments could be handled in two ways. One uses an overloaded method(one for each), and another puts the arguments into an array and then passes this array to the method. Both of them are potentially error-prone and require more code. 
To resolve these problems, Variable Arguments (Varargs) were introduced in JDK 5. From JDK 5 onwards, we can declare a method with a variable number of arguments. Such types of methods are called Varargs methods. The varargs feature offers a simpler, better option.
Syntax of Varargs

Internally, the Varargs method is implemented by using the single dimensions arrays concept. Hence, in the Varargs method, we can differentiate arguments by using Index. A variable-length argument is specified by three periods or dots(…). 

For Example, 

public static void fun(int ... a) 
{
   // method body
} 
This syntax tells the compiler that fun( ) can be called with zero or more arguments. As a result, here, a is implicitly declared as an array of type int[].


Below is a code snippet for illustrating the above concept :


// Java program to demonstrate varargs
 
class Test1 {
    // A method that takes variable
    // number of integer arguments.
    static void fun(int... a)
    {
        System.out.println("Number of arguments: "
                           + a.length);
 
        // using for each loop to display contents of a
        for (int i : a)
            System.out.print(i + " ");
        System.out.println();
    }
 
    // Driver code
    public static void main(String args[])
    {
        // Calling the varargs method with
        // different number of parameters
       
        // one parameter
        fun(100);
           
          // four parameters
        fun(1, 2, 3, 4);
         
          // no parameter
          fun();
    }
}
Output
Number of arguments: 1
100 
Number of arguments: 4
1 2 3 4 
Number of arguments: 0
Explanation of the above program

The … syntax tells the compiler that varargs have been used, and these arguments should be stored in the array referred to by a.
The variable a is operated on as an array. In this case, we have defined the data type of an array ‘a’ as int. So it can take only integer values. The number of arguments can be found out using a.length, the way we find the length of an array in Java.
Note: A method can have variable length parameters with other parameters too, but one should ensure that there exists only one varargs parameter that should be written last in the parameter list of the method declaration. For example:

int nums(int a, float b, double … c)
