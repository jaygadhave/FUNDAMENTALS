Check whether two Strings are anagram of each other
Difficulty Level : Easy

Given two strings. The task is to check whether given strings are anagrams of each other or not. 

An anagram of a string is another string that contains the same characters, only the order of characters can be different. For example, “abcd” and “dabc” are an anagram of each other.

Examples:

Input: str1 = “listen”  str2 = “silent”
Output: “Anagram”
Explanation: All characters of “listen” and “silent” are the same.


Input: str1 = “gram”  str2 = “arm”
Output: “Not Anagram”

We strongly recommend that you click here and practice it, before moving on to the solution.
Check whether two strings are anagram of each other using sorting
Sort the two given strings and compare, if they are equal then they are anagram of each other.

Sort both strings.
Compare the sorted strings: 
If they are equal return True.
Else return False.
