---
title: Coding Conventions
excerpt: "Basic coding conventions"
date: 2016-07-06
tags: [oop]
comments: true
---

<h1>Naming Conventions</h1>

<p>
Naming conventions can be tricky and when working on a project with other developers you all need to be on the same page. Most companies adopt some form of coding conventions that developers must follow. There are also some very common industry wide ones as well which I will cover here.
</p>
  <h2>
    Starting with an Underscore before the property names.
  </h2>
    <p>
      If you see a variable that is preceded with an `_`. It’s a naming convention to remind the developer that the variable or property is either `private` or `protected` can cannot be accessed from outside the class.
    </p>

<p>
If you see a file name or html partial with the naming convention it’s to remind you that this page is not intended to be served directly. It says to people "hey, this is a partial view."
</p>

<h2>
  Single Letter Prefixes aka Hungarian Notation.
</h2>
	
<p>
Hungarian notation is a naming convention that lets the developer know what the type of variable they are working with. Be it string, int etc.
</p>
<code>
`iMyAge = 26`
sMyName = “Frank”
var $container = $(‘#container’);
</code>

<h2> 
camelCase
</h2>
<p>
Depending on the company you are working at or the project you are contribuiting to. Some places use `camelCase` where the first word letter is lowercase and the 2nd word is Uppercase. You have seen this in real day to day life with iPhone, eCommerce
</p>

<h2>
Conclusion
</h2>

<p>
  The specific conventions that you use are not paramount, because their are a lot of different ones out there. Even holy wars against using tabs vs spaces. The most important thing is to be consistent with that the group has been using in the project or company.  You can read much more about Coding Conventions at the following link. <a href="https://en.wikipedia.org/wiki/Coding_conventions" target="_blank">https://en.wikipedia.org/wiki/Coding_conventions</a>
</p>
