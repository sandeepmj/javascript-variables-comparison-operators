# JavaScript: Foundation for Logic and Comparisons

We now move away from using coding to simply add interactivity to a website. Instead, we harness JavaScript's ability to calculate and to compare -- all foundations for programming logic.

## Hello JavaScript Console

Visit [this blank page.](http://www.this-page-intentionally-left-blank.org/)

Open the browser's JavaScript console by using **command**-**option**-**J** (⌘ ⌥ J). Use Chrome!

Click on console

Let's do some simple math:

![](/img/basicmath.png)

But using JavaScript as a calculator is not the goal. Instead we want a way to hold numbers and other information that we can manipulate on the fly.

## Variables

Variables are placeholders for values.They can be any of the following:

- **Numbers**.
- **Strings**, that are made up of letter, words, sentences, etc.
- **Placeholders**, that receives its value based on computation or concatenation of other variables.
- **Boolean**, values, which can only be `true` or `false`.
- **Arrays**, that holds a multiple values in one variable.
- **Objects**, which I won't even define here, but [you can look it up](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects) if you are curious.
- **Functions**, that you can call in one or more places in your code.

## Variables at Work.

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

### Exercise One (a few minutes)

Create variables for the following:

- The numeral 5 as a number.
- The number 4 as a string

Add the two variables together. What do you get?

Flip the order of adding them together. What do you get?

![](/img/mag-glass.jpg)What's happening?

## How Might We Use Variables in Journalistic Interactives?

- Compare user input/selection against existing data.
- Store large amounts of organized information and pull out key info based on user interaction.
- Take a user input, run it through a formula and store the result to be used later.
- Compare the information stored in variables.

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
- Make them unique (just like IDs, you should only have ONE variable with a particular name).
- No spaces between words, instead use underscores, hyphens or camelCase (`var myCamelCaseExample`).
- Don't use any JavaScript [reserved words](http://www.w3schools.com/js/js_reserved.asp).
- Think of code as story. Each variable is like a character/actor. Naming each in a relevant way such makes the narrative (the code) easier to follow.
- Keep the variables short but make sure they make sense.
- Don't integrate values into the name of a variable. For example, for drinking age, `var legal21` might work. But what if you expand your piece internationally? Or what if the legal age changes? Making it `var legalDrinkingAge` is more adaptable.

### Declaring a Variable

- For a number, you simply type `var someNumberDog = 123;`

- For a string, you type `var someStringCat = "Some string of letters, words, etc.";`

![](/img/mag-glass.jpg)

What's the difference between naming a variable that holds a number and a string?

- Strings must be contained within either `'Single Quotes'` or `"Double Quotes"`. You can't mix and match.

- You can also declare a variable but assign it a value later based on a computation or some input (age, name, etc.). You simply type `var somePlaceholderDogName;` to declare a variable with no value.

For example:

![](/img/monthly-declaration.png)

- You can also declare a variable and assign a value based on a computation at one time:

![](/img/monthly-after-declaration.png)

You might not remember what x and y variables stand for once you deep into your code, but you will remember what monthlyPaycheck and MonthlyExpenses stand for.

Type:

`var monthlyPaycheck = 1000;` and hit enter.

`var monthlyExpenses = 1100;` and hit enter.

`monthlyPaycheck - monthlyExpenses` and hit enter.

You get the same results but you won't be confused by these variables later as you would be by x and y.

![](/img/monthly.png)

### Exercise Two (10 minutes)

Create three variables that hold _real world numbers_ (cost of groceries, transportation tickets, etc) do a _real world_ mathematical operation on them.

### Global v. Local

More on this later.

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

### Concatenation

The plus sign `+` joins two string variables together.

Remember, if you put a `+` between two variables that hold numbers, it will add the two numbers together.

### Exercise Three (10 minutes)

Create variables for each of the following (Those are quote marks):

- "It's been
- a hard days night
- and I've been working like a dog."

Now create a variable that combines previous variables to create a complete sentence.

HINT: strings can be added together.

<br>

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

At this point you might be wondering, yeah so what?

Here's what:

Imagine an interactive that does different things based on user input. For example, **`if`** someone someone's monthly rent is more than 35 percent of their monthly income, the interactive tells them they are overpaying, **`else`** it tells them they are paying the right amount.

JavaScript actually has powerful **`if`** **`else`** conditional statements for such purposes.

### Homework

Create a Web page on which information is dynamically added from an external JavaScript file. Here's what you need to accomplish:

- Declare two numeric variables.
- Add them together using a JavaScript operator.
- Multiply them together using a JavaScript operator.
- Divide one by the other using a JavaScript operator.
- Subtract one from the other using a JavaScript operator.
- Create separate sentences for each mathematical operation that provides the results. For example, for addition, it should say something like "When I add firstVariable to secondVariable I get thirdVariable."
- You must use Functions and Jquery to make the sentence appear on a web page.
- Remember it has to be dynamic so if you change the value of the variables, the webpage should show updated results automatically.

**Due: Tuesday 5pm in a .js file.
