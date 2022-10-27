Definition and Usage
The instanceof keyword checks whether an object is an instance of a specific class or an interface.

The instanceof keyword compares the instance with type. The return value is either true or false.

Example
Check whether an object is an instance of a specific class:

public class Main {
  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj instanceof Main); // returns true
  }
}
