# Marc jQuery Intro

##Agenda
- Libraries v Frameworks
- Why use jQuery?
- Element Selectors
- DOM Manipulation
- $(document).ready


<br>

## Libraries v Frameworks

- Define: Library in this context.
- Individual search excercise on Libraries v Frameworks 2mins. Group discussion 2 mins.   
- Look at libraries in both CSS (animate.css and bootstrap) and JS (jQuery and Angular).


**Library** 

- A library performs specific, well-defined operations.
- You call library, framework calls you
- When you call a library, you are in control

**Framework** 

- A framework is a skeleton where the application defines the "meat" of the operation by filling out the skeleton. The skeleton still has code to link up the parts but the most important work is done by the application.
- You call library, framework calls you
- Hollywood Principle: Don't call Us, We'll call You.)


Walk through the LA FWED slides [jquery intro](http://jrosebud.github.io/lesson09/#/1) and [jquery advanced/review](http://jrosebud.github.io/lesson11/#/1)

[jQuery API](http://api.jquery.com/)

<br>

## Why use jQuery?

- simple selectors
	- uses CSS selectors which are specific and most folks are already familiar with them 
- common tasks in less code & method chaining
- cross-browser compatability
	- Under the hood it uses 'feature detection' - or many conditional statements to check if a browser uses a certain method. If not, it moves on to the next best option. 
- 1.9x or 2.0x
	- If you read the documentation you'll notice that there are 2 main versions. The older version contains support for older browsers while the newer version is more lightweight (it omits that support). 	


<br>

## Element selectors for DOM traversal

Thus far, you have been used to using ```document.getElementBy...``` to select DOM elements. jQuery does this slightly differently. 

> The **$** sign **doesn't** mean that you're rich (just yet)

Element, Descendant, Child, Multiple & First(pseudo) Selectors:

* $("element, #id or .class") 
* $("#id **descendant**")
* $(".class > **child**")
* $("#id1**,** #id2**,** #id3")
* $("li :first")

A few useful jQuery methods that will also help with selection:

* $("").first()
* $("").last()
* $("").prev()

(More on these when we look at traversing the DOM)

<br>

## DOM Manipulation
For a complete list please refer to the jQuery documentation [jQuery API](http://api.jquery.com/)

### Mouse Events

1. .click()
2. .dblclick()
3. .hover()
4. .mouseover()
5. .mouseout()

### DOM Insertions

1. .append()
2. .appendTo()
3. .text()
3. .prepend()
4. .prependTo()

### DOM Removal

1. .empty()
2. .remove()
3. .unwrap()



### Class Attribute

1. .addClass()
2. .removeClass()
3. .toggleClass()


<br>

## $(document).ready
When the window is loading it will take a while before it is ready for you to start adding events to the page.


```
$(document).ready(function() {
 // executes when HTML-Document is loaded and DOM is ready
 alert("document is ready");
});


$(function(){})
//jQuery shorthand

```

<br>

##LAB
Have the students convert the Jedi Javascript lab to jQuery.

- If they did the JS lab in the console then make sure they convert to a Sublime folder structure.
- Create a `scripts` folder and a `css` folder.
- Add the jQuery link in the head
- Wrap the code in a `$(function(){})`