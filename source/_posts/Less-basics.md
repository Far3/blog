---
title: The basics of .less
excerpt: "The very basics of .less mixin's and &:extend"
date: 2016-04-19
tags: [less, basics, css, preprocessor]
comments: true
---

This week I learned the basics of <a href="http://lesscss.org/features/" target="_blank">less</a>. It’s a preprocessor that is the strongest competitor to <a href="http://sass-lang.com/" target="_blank">Sass</a>. But that may change soon as <a href="http://blog.getbootstrap.com/2015/08/19/bootstrap-4-alpha/" target="_blank">bootstrap is moving towards sass</a>. The two biggest things that I used this week were <a href="http://lesscss.org/features/#mixins-feature" target="_blank">Mixins</a> and using the <a href="http://lesscss.org/features/#extend-feature" target="_blank"> &:Extend</a> pseudo class.
 
A `.mxin()` or `.mixin` is basically a way of including a bunch one or more properties from one rule to another ruleset. Say you have a base button and you want to keep the main styling the same but change one or two things like the color of the button. You can make a `.button` base class and add a modifier to the next class. Button, button cancel example.

<h2>.Less</h2>
<p data-height="266" data-theme-id="0" data-slug-hash="eZLbzR" data-default-tab="css" data-user="franklynroth" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/franklynroth/pen/eZLbzR/">eZLbzR</a> by Franklyn (<a href="http://codepen.io/franklynroth">@franklynroth</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2>Compiled CSS</h2>
{% codeblock css %}
.btn {
  display: inline-block;
  width: 20%;
  max-width: 200px;
  border-raduis: 5px;
  background-color: seagreen;
  color: #fff;
  font-size: 15px;
  margin: 5px;
  padding: 8px;
}
.btn-cancel {
  display: inline-block;
  width: 20%;
  max-width: 200px;
  border-raduis: 5px;
  background-color: seagreen;
  color: #fff;
  font-size: 15px;
  margin: 5px;
  padding: 8px;
  background-color: tomato;
}
{% endcodeblock %}
 
`&:Extend` came up when we had a really long comma separated rule declaration list. At first it was super confusing to me but it is basically a pseudo-class in less which merges the selector that it is put on with the one what matches what it references. I think of it as extending the class or mixin that is passed in.

## .Less
<p data-height="266" data-theme-id="0" data-slug-hash="aNjqaN" data-default-tab="css,result" data-user="franklynroth" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/franklynroth/pen/aNjqaN/">aNjqaN</a> by Franklyn (<a href="http://codepen.io/franklynroth">@franklynroth</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


An example is instead of having a huge list of food, drink, desert etc. We can just use a css selector on what we want and use the &:extend() pseudo-class and pass in what properties that we want to extend to.

## Compiled CSS
{% codeblock css %}
.list,
.food,
.drink,
.desert {
  color: tomato;
}
{% endcodeblock %}



There are many <a href="http://lesscss.org/features/" target="_blank">more features</a> available in less and you can do much more logic like variables, passing values and functions. This was a super simple intro to just two of the features `.less` offers over CSS.
 
 