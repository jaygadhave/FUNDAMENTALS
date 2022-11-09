Before that, let’s go over what a prime number is.

All numbers that are greater than one and have only two divisors, i.e., one and the number itself, are identified as prime numbers. We can also understand a prime number as a number that has exactly two divisors.

For example, let’s take the numbers two through seven:

Divisors of 2 are 1 and 2

Divisors of 3 are 1 and 3

Divisors of 4 are 1, 2, and 4

Divisors of 5 are 1 and 5

Divisors of 6 are 1, 2, 3, and 6

Divisors of 7 are 1 and 7

Two, three, five, and seven are numbers that have exactly two divisors, i.e., one and the respective number itself, so they are prime numbers. Four and six are non-prime numbers/composite numbers.

The isPrime() function
We can use the isPrime() function, which takes the number as input and returns true if the number is prime and false if it is not.

How to find a prime number in Java
Take a number as input.
Check if there is a divisor of the number in the range of [two, number/2] because two is the smallest prime number.
There is no number that can be completely divided by more than half of the number itself. We need to loop through two to the number itself divided by two (number/2).
If any divisor is found, then the number is not prime; otherwise, the given number is prime.