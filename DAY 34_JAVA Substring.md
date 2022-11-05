There are two variants of the substring() method. This article depicts all of them, as follows : 

1. String substring(): This method has two variants and returns a new string that is a substring of this string. The substring begins with the character at the specified index and extends to the end of this string. Endindex of substring starts from 1 and not from 0.

Syntax : 
public String substring(int begIndex)
Parameters : 
begIndex : the begin index, inclusive.
Return Value : 
The specified substring.

// Java code to demonstrate the
// working of substring(int begIndex)
public class Substr1 {
    public static void main(String args[])
    {
 
        // Initializing String
        String Str = new String("Welcome to DAY 34");
 
        // using substring() to extract substring
        // returns (whiteSpace)
       
        System.out.print("The extracted substring is : ");
        System.out.println(Str.substring(10));
    }
}
Output: 


The extracted substring is :  geeksforgeeks
2. String substring(begIndex, endIndex): This method has two variants and returns a new string that is a substring of this string. The substring begins with the character at the specified index and extends to the end of this string or up to endIndex – 1 if the second argument is given. 

Syntax : 
public String substring(int begIndex, int endIndex)
Parameters : 
beginIndex :  the begin index, inclusive.
endIndex :  the end index, exclusive.
Return Value : 
The specified substring.

// Java code to demonstrate the
// working of substring(int begIndex, int endIndex)
public class Substr2 {
    public static void main(String args[])
    {
 
        // Initializing String
        String Str = new String("Welcome to DAY 34");
 
        // using substring() to extract substring
        
        System.out.print("The extracted substring  is : ");
        System.out.println(Str.substring(10, 16));
    }
}
Output: 

The extracted substring  is :  geeks
Possible application: The substring extraction finds its use in many applications including prefix and suffix extraction. For example to extract a Lastname from the name or extract only denomination from a string containing both amount and currency symbol. The latter one is explained below.  


// Java code to demonstrate the
// application of substring()
public class Appli {
    public static void main(String args[])
    {
 
        // Initializing String
        String Str = new String("Rs 1000");
 
        // Printing original string
        System.out.print("The original string  is : ");
        System.out.println(Str);
 
        // using substring() to extract substring
        // returns 1000
        System.out.print("The extracted substring  is : ");
        System.out.println(Str.substring(3));
    }
}
Output : 

The original string  is : Rs 1000
The extracted substring  is : 1000
