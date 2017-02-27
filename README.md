#

# JavaScript Lesson 1: Introduction

## Why Use JavaScript?

- Widespread language that is built into modern browsers, including mobile browsers.
- Add interactivity to your websites by changing the HTML/CSS based on user action, an event or input.
- Tap data, images and other content from remote sources to populate your site.

## Hello JavaScript Console

Visit [this blank page.](http://www.this-page-intentionally-left-blank.org/)

Open the browser's JavaScript console by using **command**-**option**-**J** (⌘ ⌥ J). Ideally you are using Chrome.

### Make JavaScript Easier to Read

- Commenting - You're going to forget what various parts of your code are supposed to do. Leave a comment as a reminder or as a quick clarification for anyone you might collaborate with. You comment in JavaScript with two slashes `// Comment here` usually at the end of the line of code.
- White Space - JavaScript doesn't care about white space. Use it to make it easier to read your code.
- Line Length - The longer the line of code gets, the harder it is to read and evaluate. Try to keep a line less than 80 characters long.
- Line Break - If the line of code must be longer than 80 characters, break it onto a new line after an operator (+ , - , * , / , etc.)

For example, reformatted code with proper line breaks is now easier to read compared to the earlier code:

![](/img/easily-read.png)

### Exercise One (15 minutes)

????????

## Variables

Variables are placeholders for values.They can be any of the following:

- **Numbers**.
- **Strings**, that are made up of letter, words, sentences, etc.
- A **placeholder** that receives its value based on computation or concatenation of other variables.
- A **Boolean** value, which can only be `true` or `false`.
- An **Array** that holds a multiple values in one variable.
- An **Object**...which I won't even define here, but [you can look it up](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects) if you are curious.

<br>

Let's try some out.

Back in the console, type `var x = 1000;` and hit enter.

In the next line, type x

You should see "1000".

Now type, `var y = 1100;` and hit enter.

Now type y

You should see "1100".

Now for something that neither HTML or CSS can do: Math.

Type `x - y` into the console.

You should get -100.

![](/img/variables.png)

### Why use Variables?

- **Clarity** - you can assign meaningful names to variables.
- **Reusability** - you can use the same variable in different places in your code.
- **Time saver** - you can change its value in one place and the new value is called on throughout your code
- **Placeholder** - a variable can be empty until some event or user action or input gives it a value.

<br>

### Naming Variables

The idea is to give meaningful names so you aren't confused by what they stand for. Apart from that, here are some basic rules:

- They ARE case sensitive.
- Cannot begin with numbers.
- No spaces between words, instead use underscores, hypens or camelCase.
- Don't use any JavaScript [reserved words](http://www.w3schools.com/js/js_reserved.asp).

<br>

You might not remember what x and y variables stand for once you deep into your code, but you will remember what monthlyPaycheck and MonthlyExpenses stand for.

Type:

`var monthlyPaycheck = 1000;` and hit enter.

`var monthlyExpenses = 1100;` and hit enter.

`monthlyPaycheck - monthlyExpenses` and hit enter.

You get the same results but you won't be confused by these variables later as you would be by x and y.

![](/img/monthly.png)

### Declaring a Variable

For a number, you simply type `var someNumberDog = 123;`

For a string, you type `var someStringCat = "Some string of letters, words, etc.";`

![](/img/mag-glass.jpg)What's the difference between naming a variable that holds a number and a string?

Strings must be contained within either `'Single Quotes'` or `"Double Quotes"`. You can't mix and match.

You can also declare a variable but assign it a value later based on a computation or some input (age, name, etc.). You simply type `**var** myPlaceholder;` to declare a variable with no value.

For example:

![](/img/monthly-declaration.png)

You can also declare a variable and assign a value based on a computation at one time:

![](/img/monthly-after-declaration.png)

### Naming Variables

EXPLAIN GLOBAL SCOPE V. LOCAL SCOPE

### Escaping Special Characters

Type the following into your console:

`var testString = ""He could not find his keys," the inspector said.";`

`var testString = 'It's time to sleep.';`

![](/img/string-quotes-error.png)

You get an error. Why?

You'll recall that strings in a variable have to be contained within either `'Single Quotes'` or `"Double Quotes"`. The problem occurs when a `"Double Quotes"` string itself contains a quotation. Or a `'Single Quotes'` string has a contraction that uses an apostrophe.

We get around this situation by using the `\ escape character.`

Try it. Type the following into your console:

`var testString = "\"He could not find his keys,\" the inspector said."`

`var testString = 'It\'s time to sleep.';`

Now the strings work and you see either the quotation or the apostrophe.

![](/img/escaping.png)

### Exercise Two (10 minutes)

Create variables for each of the following (Those are quote marks):

- "It's been
- a hard days night
- and I've been working like a dog."

Now create a variable that combines previous variables to create a complete sentence.

HINT: strings can be added together.

Create variables for the following:

- The numeral 5 as a number.
- The number 4 as a string

Add the two variables together. What do you get?

Flip the order of adding them together. What do you get?

![](/img/mag-glass.jpg)What's happening?

<br>

### Homework

Create a Web page on which information is dynamically added from an external JavaScript file. Here's what you need to accomplish:

- Declare two numberic variables.
- Add them together using a JavaScript operator.
- Multiply them together using a JavaScript operator.
- Divide one by the other using a JavaScript operator.
- Subtract one from the other using a JavaScript operator.
- Create separate sentences for each mathematical operation that provides the results. For example, for addition, it should say something like "When I add firstVariable to secondVariable I get thirdVariable."
- You must use `document.getElementById().innerHTML`
- Do NOT use `document.write`.
- Remember it has to be dynamic so if you change the value of the variables, the webpage should show updated results automatically.

**Due: Monday, Feb. 15 by Noon on your github account**. Share the URL on Slack (your instructor will tell you which channel.

# Review Homework

Create a Web page on which information is dynamically added from an external JavaScript file. Here's what you need to accomplish:

- Declare two numberic variables.
- Add them together using a JavaScript operator.
- Multiply them together using a JavaScript operator.
- Divide one by the other using a JavaScript operator.
- Subtract one from the other using a JavaScript operator.
- Create separate sentences for each mathematical operation that provides the results. For example, for addition, it should say something like "When I add firstVariable to secondVariable I get thirdVariable."
- You must use `document.getElementById().innerHTML`
- Do NOT use `document.write`.
- Remember it has to be dynamic so if you change the value of the variables, the webpage should show updated results automatically.

# JavaScript Lesson 2: Interactivity

A web page can react or change according to user inputs and clicks. Let's explore one of the most common forms of interactivity--the button.

In order to create interacvity with a button, we need to know three things:

- Creating a button with the HTML button tag.
- Making JavaScript recognize an event, with with the "`onclick`" event handler .
- Telling that button what to do with a JavaScript function.

## The Button

You can create a simple HTML button by typing: `<button type="button">Do Something!</button>`

You can [style this button](http://www.sitepoint.com/build-a-better-button-in-css3/) using CSS or use a [button generator](http://css3buttongenerator.com/). We're not covering that today.

You might give the button a class or an Id so you can control them later using JavaScript. It should look like: `<button type="button" "class="someClass" id="someId">Do Something Else!</button>`

So now you have two buttons but they don't do anything

## onclick

`onclick` is an HTML event that JavaScript recognizes. Adding the following into your button tag is the first step in making it interactive: `onclick="someCommand()"` where someCommand will be a series of instructions we provide using JavaScript. The word someCommand is a placeholder I just created. It could have been someDog() or even someCat().

### alert()

We'll use the window `alert()` method to see if a command we are giving is actually coming through. You'll quickly realize how useful these alerts are to debugging your code.

In your first button tag, add: `onclick="alert('Hello, my button works!')"`

![](/img/mag-glass.jpg)

Note that if you start with a double quote, you must have a single quote inside the alert() and vice versa.

Add an alert with a different message into your second button.

## Functions

Now we come to one of the real strengths of just about any programming language - the **Function**. Let's actually just put a function to work before I even define it. Inside your button tag, add `onclick='myAlert()'`. In an external JavaScript file, add the following:

![](/img/js1.png)

What happens when you click on button 1?

Let's go one step further before explaining functions. Make a copy of your current html file and save it as `button3.html`.

Create a placeholder div with the `id="test"` in your new html file.

In your button tag, remove the alert and replace with `onclick='fillText()'`. Again, I could have named it almost anything from `runDog()` to `sleepCat()`.

It should look like this:

![](/img/button3.png)

Then type the following into your js file:

![](/img/function1.png)

What happens when you click on the button....you get some intactivity!

### Defining Functions

A functions is:

- a little block of script (one line or many) that performs specific task or a series of tasks.
- reusable.
- performed when something "invokes" or "calls" it.
- ideally modular--that is, it performs a narrow task so you can run several functions to perform more complex tasks.

![](/img/define-function.png)

### Naming Functions

All the same rules as naming variables apply.

Again the idea is to give meaningful names to functions-- name them for what they do. Apart from that, here are some basic rules:

- They ARE case sensitive.
- Cannot begin with numbers.
- No spaces between words, instead use underscores, hypens or camelCase.
- Don't use any JavaScript [reserved words](http://www.w3schools.com/js/js_reserved.asp).

### Calling or Invoking a Function

When you call or invoke a function, you trigger it to run and complete its task. You've already called a function in your button. You call a function by typing `myFunctionName();`.

## Exercise 1 (20 minutes)

In Sublime, take your work from last week's [Exercise One](https://github.com/sandeepmj/JavaScript-lesson-1#exercise-one-15-minutes) and trigger the change in style at the click of a button.

## User Inputs

You can integrate information your audience provides into your interactive. Use HTML form inputs to ask for information. Then use JavaScript to capture and process it before returning altering your page.

Let's first build the form:

![](/img/form.png)

Then we need to create a function to capture and process that information.

We'll use the `.value` method to grab the value of a variable.

![](/img/rentFunction.png)

### Exercise Two (25 minutes)

Take your homework exercise and update it by asking your audience to provide the two numbers that are then calculated for addition, subtraction, division and multiplication. Display the results only after someone clicks a submit button.

## Comparison Operators

JavaScript allows us to make comparison which then allows us to take an action. For example, if a user is paying more than 35 percent of his or her income on rent, we can tell them they are overpaying.

You've seen some of these operators before:

- `5 > 3` or 5 is greater than 3.
- `4 < 8` or 4 is less than 8.

Where it gets a little stanger is for **equal** and **not equal**. Because we use `=` to assign value to a variable, we have to use `==` to denote equality and `!=` for inequality

Here's a [complete list of comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Comparison_operators)

### Logical Operators

Logical Operators simply allow you to compare relationships or logic between various variables-- like **and** and **or**. The logic for "and" is written as `&&` and the logic for "or" is written as `||`. Here's a [full list of logical operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Logical_operators).

![](/img/comparison.png)

### So What?

At this point you might be wondering, so what?

Here's what:

Imagine writing a function that does different things based on user input. For example, **`if`** someone someone's rent to income is greater than 35 percent your function can tell them they are overpaying, **`else` your function tells them they are paying the right amount.**

I created a `form2.html` that is exactly the same except I'm pointing it to `main2.js`

`main2.js` should look like this:

![](/img/compjs.png)

## Homework

Using JavaScript learned over the past two weeks, create a simple calculator to inform your audience whether they should buy a monthly MetroCard or a per ride MetroCard based on how many times they ride the subway per month.

**Due: Monday, Feb. 22 by Noon on your github account**. Share the URL on Slack (your instructor will tell you which channel.
