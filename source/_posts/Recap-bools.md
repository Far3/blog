---
title: Recap and booleans.
excerpt: "Quick review and intro to booleans."
date: 2016-06-29
tags: [oop]
comments: true
---

<h1>A quick recap</h1>
<ul>
  <li>You don't have to capitalize class names for the program to compile, but is a good idea/coding convention to do so.</li>
  <li>`readonly` fields can be set only during object construction</li>
  <li>Constructors cannot return anything, they are void methods.</li>
  <li>Public fields are directly accessible from outside the class</li>
  <li>Private fields can only be accessed from within the class they are defined in</li>
</ul>

<h2>Boolean Values</h2>
<p>
 Boolean values are essential to know. We want to create a Method (behavior) of the map that will let us know if a particular point is in bounds or not. an `OnMap` method is an example. We would have a boolean (True/False) variable where if the width or height are greater than the map values passed in then the `OnMap` method would return false. Letting you know the point is not on the map.
 </p>
 <p>
 C# uses a practice called short-circuiting. This means that it will try and do as little work as possible when evaluating a Boolean expression. Some operators include `||`, `&&`, and the `!`.
 </p>
 <p>
 More info can be found at the following links about <a href="https://msdn.microsoft.com/en-us/library/2a723cdk.aspx" target=_"blank">&&</a>, <a href="https://msdn.microsoft.com/en-us/library/6373h346.aspx" target=_"blank">||</a> and  <a href="https://msdn.microsoft.com/en-us/library/f2kd6eb2.aspx" target=_"blank"></a>
 </p>
 
 <p>Knowing how these operators work in your sleep will definately help you along in all aspects of development. It also sometimes comed in handy in life when making choices between one thing or another.</p>
