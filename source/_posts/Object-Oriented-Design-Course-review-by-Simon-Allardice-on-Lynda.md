---
title: Object-Oriented Design Course review by Simon Allardice on Lynda
date: 2018-05-14 11:22:21
tags:
---

Course notes from Object-Oriented Design by Simon Alladice

This was an exceptional course that I followed along with on Lynda.com. It was language agnostic, but Simon put in great examples of how different things would be implemented in differing languages.

It was broken down into very easy to understand concepts that I will 100% take to work with me. He touched on UML design and how to structure your programs in an Object Oriented fashion.

Below are my rough notes that I took while following along. If you want to really get to know OOP principles I would probably reccommend learning a strong static typed language like C# or Java.


[https://www.lynda.com/Java-tutorials/Foundations-Programming-Object-Oriented-Design/96949-2.html](https://www.lynda.com/Java-tutorials/Foundations-Programming-Object-Oriented-Design/96949-2.html)

Abstraction: Abstract out a new object. Only focus on the essentials.

Encapsulation: Hide code, show only what you need.

Inheritance: Write a new class but base it on an existing class.

Person > Customer. Customer inherits from the person. THen we say, what do we add to it.

customer number

Person is the superclass or parent class and customer is child class or subclass.

More common to inherit from one class. C#/Java/Ruby/Obj C all enforce this.

Polymorthpism: Many forms. Automatically do the correct behavior?

+ sign will automatically do the correct behavior. We can do the same idea. concat vs adding

ovverriding a behavior. Is to re-write it.

Example of investment account, add penality to the withdraw method.

What classes do you need and what do you want?

1. Gather requirements

	Always write it down.

2. Describe app

	In plain conversational language, what does the app do. use cases, user stories.

3. ID most important objects

	Pick out the most important ideas and things and discard what is irrelevent.

4. Describe the interactions

	what needs to happen and what order do they need to happen in

5. create a class diagram.

	Be really specific about inheritence and polymorphism. The output is on paper for now or a whiteboard. The class diagram is the most common method.

Creating requirements

Functional Requirements. What does it do.

non-functional requirements

help, legal, performance, support, security.

FURPS

Functional, usability, reliability, performance, supportability requirements

design, implementation, interface and physical requirements.

Creating a use case for you app.

Title:

Actor:

Scenario:

1.

2.

3.

Workout use cases as good as you can, but finish it and move to the next step.

Use active voice and focus on intention. Keep exxtra words and pseudocode out of it.

Identifying objects: Identify all of the nouns.

Customer confirms items in shopping car. customer provides payment and address to process sale. system validates payment and responds by confirming order, and provides order number that customer can use to check on order status. System will send customer a copy of order details by email.

Customer, item, shopping card, payment, address, order, order number, email

Create a basic UML Diagram and then assign responsibilities.

Always multiple successful ways to incorporate different ideas.

CRC: Class responsibility collaboration.

Class Name, Responsibility, collaborators(other classes).

Use nouns in the description.

Payment

Store payment detaisl, validate payment.

Product

Attributes

name

isActive

launchDate

itemNumber

Operations

getName

setActive

getProductDetails

verbNoun

instantiation: Create a new object.

Customer fred = new Customer();

Constructor: Special method that exists to construct the object.

Spaceship

name

shieldStrength

fire();

reduceShields();

Spaceship turny = new Spaceship();

//Object exists, but has a meaningless state.

name: null

shieldStrength: 0

Constructors allow you to populate meaningful values when a new object is instantiated.

public Spaceship() {

 name = "theTurny"

shieldStrength = 100;

}

overloaded, allow you to set the values to different values. Allows flexibiliy.

static: one object shared accross all levels. One copy along all objects.

Inheritance describes an "Is A" relationship.

An employee is a person a customer is a person

Abstract classes are never instantiated.

Interface: <ust provide the methods the interface calls out. Many differnt classes can use the same interace.

Well tested best practices to write code. design pattern

design patterns, gang of 4

DRY: Dont repeat yourself.

YAGNI: You ain't gonna need it. 

Don't write speculative code, keep it simple and write for today.

Code smell, unecessary code. Code smell.

long method

short identifiers

pointless comments

god object

feature envy

SOLID

uncle bob

single resp

One reason to exist.

open close

open to extension but closed to modification

GRASP