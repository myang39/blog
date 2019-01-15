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
// valueOf group
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





