---
title: Fields
excerpt: "Adding fields to a class."
date: 2016-06-08
tags: [oop]
comments: true
---
<p>When assind fields or properties to a class you need to think about what attributes that a class has. Ideally you want to set the minimal amount of attributes. A super simple example would be a map. It can be divided into X for the width and Y for the height. You start adding fields by listing the protection level, the type and then finally the name.</p>
<p>
Every field in a class has an accessibility level, meanind how protected they make the declared properties. Their are private, protected and public.
</p>
<ul>
  <li>Public: The field can be accessed by any method in any class.</li>
  <li>Private: The field can be accessed by only the same class they were declared in. This is the default value.</li>
  <li>Protected: The field can be accessed by only the current class and subclasses</li>
</ul>

`private int Width`
`private int Height`

<p>Next up we will cover how to use these fields with constructors.</p>
