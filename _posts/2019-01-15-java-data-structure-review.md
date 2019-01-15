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

// static valueOf group (9 of them ...)
String myStringValue = String.valueOf(e);
// e can be boolean, char, char[],
// char[] offset count, double, float, int, long
// and even Object (if the argument is null, then a string equal to "null"; otherwise, the value of obj.toString() is returned.)
```







