BigInteger class is used for the mathematical operation which involves very big integer calculations that are outside the limit of all available primitive data types.

In this way, BigInteger class is very handy to use because of its large method library and it is also used a lot in competitive programming. 
Now below is given a list of simple statements in primitive arithmetic and its analogous statement in terms of BigInteger objects.

Example:
int a, b;                
BigInteger A, B; 
Initialization is as follows:


a = 54;
b = 23;
A  = BigInteger.valueOf(54);
B  = BigInteger.valueOf(37); 
And for Integers available as strings you can initialize them as follows:

A  = new BigInteger(“54”);
B  = new BigInteger(“123456789123456789”); 
Some constants are also defined in BigInteger class for ease of initialization as follows:

A = BigInteger.ONE;
// Other than this, available constant are BigInteger.ZERO 
// and BigInteger.TEN 
Mathematical operations are as follows:  

int c = a + b;
BigInteger C = A.add(B); 
Other similar functions are subtract(), multiply(), divide(), remainder(), but all these functions take BigInteger as their argument so if we want this operation with integers or string convert them to BigInteger before passing them to functions as shown below: 

String str = “123456789”;
BigInteger C = A.add(new BigInteger(str));
int val  = 123456789;
BigInteger C = A.add(BigInteger.valueOf(val)); 
Extraction of value from BigInteger is as follows:

int x   =  A.intValue();   // value should be in limit of int x
long y   = A.longValue();  // value should be in limit of long y
String z = A.toString();  
Comparison 

if (a < b) {}         // For primitive int
if (A.compareTo(B) < 0)  {} // For BigInteger 
Actually compareTo returns -1(less than), 0(Equal), 1(greater than) according to values. For equality we can also use: 

if (A.equals(B)) {}  // A is equal to B 
