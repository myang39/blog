---
layout: post
title:  "Java Data Structure Review"
date:   2019-01-15
categories: jekyll update
author: "Luke"
---

### LinkedList

```java
// Definition for singly-linked list.
public class ListNode { 
    int val;
    ListNode next;
    ListNode(int x) { val = x; }
}

// The Java LinkedList
LinkedList<Integer> list = new LinkedList<>();
```

### Array

```java
int[] array = new int[5]; // declaration and initialization
int length = array.length; // how to get the length
int a = array[0]; // random access
array[0] = 3; // update operation
```

### String

```java
String a = "hello;bro;let's;go"; // declaration and initialization
int size = a.length(); // how to get the length
char b = a.chatAt(1); // random access
char[] array = a.toCharArray(); // Converts this string to a new character array.

// Just remember they all return a New String or String array
// Because String is immutable !!! 
String c = a.replace('o', 'e'); // Returns a new string resulting from replacing all occurrences of oldChar in this string with newChar.
String d = d.replace("ll", "ooo"); // Replaces each substring of this string that matches the literal target sequence with the specified literal replacement sequence.
String[] parts = a.split(';'); // Splits this string around matches of the given regular expression.
String upper = a.toUpperCase();
String lower = a.toLowerCase();
String trimmed = a.trim(); // Returns a copy of the string, with leading and trailing whitespace omitted.

// static methond: 
// valueOf
String myStringValue = String.valueOf(e);
// e can be 
// boolean, char, char[],
// char[] offset count, double, float, int, long
// Object (if the argument is null, then a string equal to "null"; otherwise, the value of obj.toString() is returned.)
```
### autoboxing and unboxing

Autoboxing is the automatic conversion that the Java compiler makes
between the primitive types and their corresponding object wrapper classes.
For example, converting an int to an Integer, a double to a Double, and so on.

If the conversion goes the other way, this is called unboxing.

### The primitive types and their corresponding wrapper classes
```java
boolean 1-bit(size not precisely defined) Boolean  

byte    8-bit       Byte

short   16-bit      Short
char    16-bit      Character

int     32-bit      Integer
float   32-bit      Float

long    64-bit      Long
double  64-bit      Double
```
### Integer
```java
// constructor
Integer a = new Integer(1);
Integer b = new Integer("1");

Integer input = 1; // autoboxing
String inputString = a.toString(); // Returns a String object representing this Integer's value.

// static method
String c = Integer.toString(2); // Returns a String object representing the specified integer.
String d = Integer.toString(15, 16); // Returns a string representation of the first argument in the radix specified by the second argument.

Integer e = Integer.valueOf(4);
Integer f = Integer.valueOf("4");
Integer g = Integer.valueOf("15", 16);

// useful fields
int min = Integer.MIN_VALUE;
int max = Integer.MAX_VALUE;
```

### StringBuilder
```java
// constructor
StringBuilder sb = new StringBuilder(); //Constructs a string builder with no characters in it and an initial capacity of 16 characters.
StringBuilder sb1 = new StringBuilder(5); // initial capacity as 5
StringBuilder sb2 = new StringBuilder("hello"); // Constructs a string builder initialized to the contents of the specified string.

// append 
sb.append(b);
// b can be
// boolean, char, char[], char[] offset len,
// charSequence, charSequence start end,
// double, float, int, long, Object, String,
// StringBuilder

int capacity = sb.capacity(); // Returns the current capacity.
int length = sb.length(); // Returns the length (character count).

char c = sb2.charAt(3); // Returns the char value in this sequence at the specified index.
int start = 1; int end = 3;
sb.delete(1, 3); // Removes the characters in a substring of this sequence.
// The substring begins at the specified start and extends to the character at index end - 1 or to the end of the sequence if no such character exists.

sb.deleteCharAt(2); // Removes the char at the specified position in this sequence.

int d = sb.indexOf("lo"); // Returns the index within this string of the first occurrence of the specified substring.
int e = sb.indexOf("lo", 3); // Returns the index within this string of the first occurrence of the specified substring, starting at the specified index.

// insert
int offset = 4;
sb.insert(offset, f);
// f can be ...

int index = 3;
sb.setCharAt(index, 'f'); // The character at the specified index is set to ch.

String stringValue = sb.toString(); // a new String Object will be allocated

int start = 1; int end = 4;
char[] array = sb.subSequence(start, end); // Returns a new character sequence that is a subsequence of this sequence.
String g = sb.substring(start); // Returns a new String that contains a subsequence of characters currently contained in this character sequence.
String h = sb.substring(start, end);
```




