#

# JavaScript Lesson 1: Introduction

## Why Use JavaScript?

- Widespread language that is built into modern browsers, including mobile browsers.
- Add interactivity to your websites by changing the HTML/CSS based on user action, an event or input.
- Tap data, images and other content from remote sources to populate your site.

## Hello JavaScript Console

Visit [this blank page.](http://www.this-page-intentionally-left-blank.org/)

Open the browser's JavaScript console by using **command**-**option**-**J** (⌘ ⌥ J). Ideally you are using Chrome or Firefox.

Type: document.write("hello world!");

![](/img/console.png)

If you see "Hello World!" appear in your browser, congrats! Your just wrote your first bit of JavaScript.

![](/img/mag-glass.jpg)Why the semi-colon? Because semi-colons end JavaScript statements. Your code is likely to work without it, but as your code gets more complex, the semi-colon will play an valuable role. Basically, if unsure, just use a colon.

![](/img/mag-glass.jpg) If it didn't work, make sure all quote marks are straight quotes rather than curly quotes.

### Really, type it out

I don't know why it happens at a cognitive level, but unless you type out the code, you won't reall understand out it works. So even though I provide each line of code we'll use, please do type it out.

 <

## The DOM

We've typed `document.write();` a few times now. In English, we're simply telling JavaScript to write something on the document, or our web page. However, we're not harnessing the power of JavaScript. We're simply writing into a default location on the document.

Here's where the **DOM**, or **Document Object Model**, comes into play. Think of a Webpage as a document. The HTML gives structure to the content on the page. The document owns all the HTML on the page -- creating an "object" that represents the page and all its content. We use JavaScript to access and manipulate, or change, various elements in this document object. Later, you'll begin to create new elements where they didn't exist on the page.

Doesn't quite make sense?

The best thing is to try it out.

Create a page with the same budget info, but use HTML in the Body.

Give the H1 tag the id of "budget". It should look like:

![](/img/budget-id.png)

### Make JavaScript Easier to Read

- Commenting - You're going to forget what various parts of your code are supposed to do. Leave a comment as a reminder or as a quick clarification for anyone you might collaborate with. You comment in JavaScript with two slashes `// Comment here` usually at the end of the line of code.
- White Space - JavaScript doesn't care about white space. Use it to make it easier to read your code.
- Line Length - The longer the line of code gets, the harder it is to read and evaluate. Try to keep a line less than 80 characters long.
- Line Break - If the line of code must be longer than 80 characters, break it onto a new line after an operator (+ , - , * , / , etc.)

For example, reformated code with proper line breaks is now easier to read compared to the earlier code:

![](/img/easily-read.png)

### Exercise One (15 minutes)

In Sublime, create a list of classes you are taking.

- Create an HTML page.
- Use CSS IDs for each course.
- The title: "My Spring 2016 Courses"
- An unordered list of your course titles.
- The title and each course should have separate IDs.
- Style each ID in a different color in an external stylesheet.
- View the page.
- Now change the color of each course using JavaScript to manipulate the DOM.

What happens when you reload the page?

### InnerHTML

Another great feature of being able to manipulate the DOM is that you can change the actual text that any tag contains using the `innerHTML` `document.getElementById("IdName").innerHTML = "New Text Here";`

Let's try it:

- Create an index.html file through the Command Line, and open it via subl.
- Create a basic html document and add `<div id="test">Something here?</div>` in the body.

![](/img/innerhtml-0.png)

Here's what you should see in the browser:

![](/img/innerhtml-1.png)



- Now, just before the closing tag add `<script> document.getElementById("test").innerHTML = "Like magic, it appears!"; </script>`

- Reload your browser window. What do you see?

<br>

Hopefully you see:

![](/img/innerhtml-2.png)

But when you use view the source, you see that the content in the div has NOT changed at all, but rather the JavaScript and `.innerHTML`has dynamically changed the text in the div.

![](/img/innerhtml-3.png)

<br>

Soon we'll learn how to trigger the change based on user action/input.

## Variables

Variables are placeholders for values.They can be any of the following:

- Numbers.
- Strings, that are made up of letter, words, sentences, etc.
- A placeholder that receives its value based on computation or concatenation of other variables.
- A Boolean value, which can only be `true` or `false`.

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
- **Reuseable** - you can use the same variable in different places in your code.
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

For a number, you simply type `**var** myInfo = someNumber;`

For a string, you type `**var** myInfo = "Some string of letters, words, etc.";`

![](/img/mag-glass.jpg)What's the difference between naming a variable that holds a number and a string?

Strings must be contained within either `'Single Quotes'` or `"Double Quotes"`. You can't mix and match.

You can also declare a variable but assign it a value later based on a computation or some input (age, name, etc.). You simply type `**var** myPlaceholder;` to declare a variable with no value.

For example:

![](/img/monthly-declaration.png)

You can also declare a variable and assign a value based on a computation at one time:

![](/img/monthly-after-declaration.png)

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

### External JavaScript File

As your JavaScript code gets more involved and longer, it will clutter up your HTML file (and slow its response time).

Or you have several HTML files that require the same JavaScript. You don't want to same JavaScript repeated across many files. It's a pain to fix one error (let alone many errors) across numberous files.

It's good practice to place your JavaScript into an external file -- just like you've been placing your CSS into an external stylesheet for several reasons.

- All HTML pages across a website can call the same JavaScript located in one external page.
- Keeps your HTML free of code, making it reasier to read.
- Keeps your JavaScript free of HTML, making it easier to read.
- A browser will cache that JavaScript file, speeding up load time on each HTML page.

<br>

**[Social J students - ignore Command Line instructions]** Let's use Command Line to create a JavaScript file.

1. Make a new directory call my-first-js using `mkdir`.
2. Navigate into your directory (or folder) using `cd`.
3. Create three different files at one time using `touch index.html page2.html myjavascript.js mystylesheet.css`.
4. Open all the files at one time using `subl .` and all should appear.
5. In the `index.html` file, add the basic HTML that all HTML files require.
6. In `index.html` add `<p>Content I typed into page 1.</p>` with the opening and closing `body` tags.
7. In `page2.html` add `<p>Content I typed into page 2.</p>` with the opening and closing `body` tags.
8. In both the HTML files, add the following into the `head`: `<script type="text/javascript" src="myjavascript.js"></script>`
9. In the `myjavascript.js` file, type `document.write("Content created using JavaScript");`
10. After saving all files, open them in your browser.

What do you see?

Here's what you should see:

![](/img/external-js.png)

Move the `<script type="text/javascript" src="myjavascript.js"></script>` out of the `head` and place right before the `</body>` tag.

What happens?

Going forward, ALWAYS place the link to your `.js` file right before the `</body>` tag. This allows the page to be rendered first before the JavaScript is applied to it. Another reason to do this is that the more JavaScript you have in the `head`, the slower the page will load.

### Exercise Three (15 minutes)

Recreate the webpage you produced in Exercise One but this time using an external JavaScript file. There should be NO content in `index.html` file beyond the barebones required HTML and link to the external JavaScript file.

Do NOT use `document.write` instead use `document.getElementById().innerHTML = "something here";`.

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
