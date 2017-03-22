---
title: Namespaces.
excerpt: "What are namespaces about."
date: 2016-06-01
tags: [oop]
comments: true
---
<h1>Namespaces explained</h1>

<p>A namespace is a confusing topic when you first encounter it in OOP. The namespace is the encompassing code block and is usually the company name. You can have multiple levels to the namespace to further differentiate things.</p>
<p>
Next up is the class you are able to have multiple classes with the same name, as long as they are in different namespaces. Much like you can have the same city names in different states. Manhattan, KS and Manhattan, NY are very different places.
</p>

You often may see `System.Console.Write.` 
<ul>
  <li>System is simply the namespace.</li>
  <li>Console is the Class name.</li>
  <li>Write is the method called.</li>
</ul>

<p>This can be shortened by putting a using directive at the top of the program. This is common and makes your code more readable with `using System;` </p>

<p>To think of it in terms of a a mailing address you would need to put the state and country, city and street address for the post office to know what you do with your letter. A namespace works much the same way.</p>
<ol>
  <li>Namespace = State and Country</li>
  <li>ClassName = City</li>
  <li>Method = The street address</li>
</ol>

<p>Hopefully this makes wrapping your head around namepaces a little bit easier.</p>
