---
title: Constructors.
excerpt: "Why we need constructors."
date: 2016-06-22
tags: [oop]
comments: true
---

<p>Constructors confused me for a while, but once you understand the basics of OOP, fields, objects etc it becomes easier to grasp the concepts of them and why they are necessary in OOP. It deals with object initalization. When we gave the properties of the map to Width and Height we weren't doing anything with them. This is where a constructor comes in to construct new instances of a class.</p>

<p>
Conventions tell us that we need to name the constructor the same name as the class and make sure you put public in front of it or else it will be private by default and useless! A quick tip if you are using visual studio is to type out "ctor" and then hit tab tab. Their are so many more useful snippets at <a href="http://www.dotnetperls.com/snippet" target="_blank">this web address.</a> This constructor is called when the object is created. Make sure to put the parameters in the signature. 
</p>

```
Public Map(int width, int height)
{
  Width = width;
  height = height;
}

```

<p>
Lowercase letters are convention and are method level variables. That means they only exist in the constructor method and local to the scope of the constructor. The instance variables are accessible thought the class and possible other classes as well. We may need other objects to know about the Map width and height.
</p>
<p>When we initalize the objects field with values, sometimes we want to be able to change the values. Should the map values be allowed to change? Probably not. So making the fields `readonly` will help ensure that the Map size and coordinates doesn't change. If this were to happen their would be a lot of wierd errors going on down the line.
</p>
