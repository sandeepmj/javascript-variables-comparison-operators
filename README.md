# <h1>JavaScript Lesson 1: Introduction</h1>

<h3>Why Use JavaScript?</h3>
<ul>
<li>Widespread language that is built into modern browsers, including mobile browsers.</li>
<li>Add interactivity to your websites by changing the HTML/CSS based on user action, an event or input.</li>
<li>Tap data, images and other content from remote sources to populate your site.</li>
</ul>


<h3>Hello JavaScript Console </h3>

<p>Visit <a href="http://www.this-page-intentionally-left-blank.org/">this blank page.</a></p>

<p>Open the browser's JavaScript console by using <strong>command</strong>-<strong>option</strong>-<strong>J</strong> (&#8984; &#8997; J). Ideally you are using Chrome or Firefox.</p>

<p>Type: document.write("hello world!");</p>

<img src="/img/console.png">
<p>If you see "Hello World!" appear in your browser, congrats! Your just wrote your first bit of JavaScript.</p>

<p><img src="/img/mag-glass.jpg">Why the semi-colon? Because semi-colons end JavaScript statements. Your code is likely to work without it, but as your code gets more complex, the semi-colon will play an valuable role. Basically, if unsure, just use a colon.</p>

<p><img src="/img/mag-glass.jpg"> If it didn't work, make sure all quote marks are straight quotes rather than curly quotes.</p>

<h3>Adding HTML using JavaScript:</h3>

<p>Type: 

	<code>document.write("You make $1000 per month but your expenses are $1100 per month.");</code></p>

<p>You can copy and paste part of this, but type: </p>
<p>
<code>document.write("Your Budget Anlysis. You make $1000 per month but your expenses are $1100 per month. You need to earn more or spend less!");</code>
</p>

<p>It appears as one long paragraph. Let's add some HTML to provide more structure:</p>

<p>Type: </p>
<p>
	<pre>
	<code>
	document.write(&quot;&lt;h2&gt;Your Budget Analysis&lt;/h2&gt;&lt;p&gt;You make $1000 per month but your expenses are $1100 per month. You need to earn more or spend less!&lt;/p&gt;&quot;);
	</code>
	</pre>
</p>
	


<h3>Sublime Time</h3>

<p>When you hit reload on your browser, you lose all the work in the console. You have to keep retyping the JavaScript. Instead, let's start adding code to a Sublime file where we can test, edit and retest.</p>

<p>Use Command Line to create a directory call learning-js, and an index.html file inside the newly created folder.</p>

<p>Launch the index.html file using subl in Command Line.</p>

<p>Set up basic html document with doctype, html, head and body with closing tags too. It should look like this:</p>

<p><img src="/img/basic-html.png"></p>

<p>Add the following script tags into the head:</p>
<p>
<code>&lt;script type=&quot;text/javascript&quot;&gt;
&lt;/script&gt;</code> </p>

<p>Type the following in between the opening and closing script tags: </p>

<p>
	<pre>
<code>document.write(&quot;&lt;h2&gt;Your Budget Analysis&lt;/h2&gt;&lt;p&gt;You make $1000 per month but your expenses are $1100 per month. You need to earn more or spend less!&lt;/p&gt;&lt;p&gt;Here are some ways to save money:&lt;/p&gt;&lt;li&gt;Bring your lunch to work.&lt;/li&gt;&lt;li&gt;Stop taking cabs.&lt;/li&gt;&lt;li&gt;Stop shopping at Whole Foods.&lt;/li&gt;&quot;);</code>
	</p>
</pre>
<p>Open your index.html file in chrome. You should see a formatted HTML page.</p>

<p><img src="/img/budget-js.png"></p>

<p>View Source the browser page and you'll see that you created an HTML page without any HTML in the body. It's all JavaScript:</p>

<p><img src="/img/html-normally-here.png"></p>



<h3>The DOM</h3>
<p>We've typed <code>document.write()</code> a few times now. In English, we're simply telling JavaScript to write something on the document. We're not harnessing the power of JavaScript, we're simply writing into a default location on the document.</p>

<p>Here's where the <strong>DOM</strong>, or <strong>Document Object Model</strong>, comes into play. Think of a Webpage as a document. The HTML gives structure to the content on the page. The document owns all the HTML on the page -- creating an "object" that represents the page and all its content. We use JavaScript to access and manipulate, or change, various elements in this document object. Later, you'll begin to create new elements where they didn't exist on the page.</p>
<p>Doesn't quite make sense?</p>

<p>The best thing is to try it out.</p>

<p>
Create a page with the same budget info, but use HTML in the Body.
</p>

<p>
Give the H1 tag the id of "budget".
</p>

<p><img src="/img/budget-id.png"></p>

<h3>ID Power</h3>
<p>
Imagine a webpage full of IDs. We can use JavaScript and the DOM to target a particular ID and do something to it using the <code>document.getElementbyId()</code> method.
</p>
<p>
In English, it says, "In this current document, get the element with a particular ID and do something to it."
</p>
<p>
You'll be using <code>document.getElementByID();</code> often.
</p>

<p>
Let's try it. At the bottom of the page (but before the closing Body tag), add following:
</p>

<p>
	<code>
	&lt;script type=&quot;text/javascript&quot;&gt;
	document.getElementById(&quot;budget&quot;).style.color = &quot;red&quot;;
&lt;/script&gt;
	</code>
</p>

<p>
<img scr="/img/style-color.png">
</p>

<p>
Your page should look like this:
</p>
<p>
<img src = "/img/page-red.png">
</p>

<h3>
The Style Object
</h3>
<p>
	Color is just one of about 100 styling objects. Find the <a href="http://www.w3schools.com/jsref/dom_obj_style.asp">full list here</a>. I use just a fraction of these, but feel free to experiment.
</p>
<p>
Add the following between the script tags:
</p>
<p>
<code>
document.getElementById("budget").style.fontFamily = "Arial";
document.getElementById("budget").style.textTransform = "uppercase";
</code>
</p>
<p>
	<img src ="/img/more-style.png">
</p>

<p>
It should look like this:
</p>

<p>
<img src="/img/styled.png">
</p>


<h3>JavaScript Good Habits</h3>

<ul>

<li>White Space - JavaScript doesn't care about white space. Use it to make it easier to read your code.</li>

<li>Line Length - The longer the line of code gets, the harder it is to read and evaluate. Try to keep a line less than 80 characters long.</li>

<li>Line Break - If the line of code must be longer than 80 characters, break it onto a new line after an operator (+ , - , * , / , etc.)</li>
</ul>

<p>For example, reformated code with proper line breaks is now easier to read compared to the earlier code:</p>
<p>
<img src = "/img/easily-read.png"> 
</p>

<h3>Exercise One (15 minutes)</h3>

<p>In Sublime, create a list of classes you are taking.</p>
<ul>
<li>Use JavaScript and HTML tags in the Head. </li>
<li>There should be NO HTML in the Body.</li>
<li>The title: "My Spring Courses"</li>
<li>An unordered list of your course titles.</li>


<h3>Manipulating the Style</h3>
<p>
You don't necessarily want to build an entire webpage in JavaScript. Rather you want to be able to manipulate existing pages when there is user input, an event or an input.
</p>
<p>But we aren’t there yet.
</p>
<p>We need more foundational knowledge that will help us build up to controlling interactivity with button clicks or some user action and/or input. 
</p> 





<h3>Exercise Two (15 minutes)</h3>
<p>Rebuild your course list for the spring, but this time:</p>
<p>
	<li>
		Place the HTMl in the body.
	</li>
	<li>
		Add IDs for various content.
	</li>
	<li>
		Style it JavaScript.
	</li>


</p>

<h3>Variables</h3>
<p>Variables are placeholders for values.They can be any of the following:</p>
<ul>
<li>
	Numbers.
</li>
<li>
	Strings, that are made up of letter, words, sentences, etc. 
</li>
<li>
	A placeholder that receives its value based on computation or concatenation of other variables.
</li>
<li>
	A Boolean value, which can only be <code>true</code> or <code>false</code>.
</li>


</ul>
<br>
<p>
	Let's try some out.
</p>
<p>Back in the console, type <code>var x = 1000;</code> and hit enter.</p>
<p>In the next line, type x</p>
<p>You should see "1000".</p>
<p>Now type, <code>var y = 1100;</code> and hit enter.</p>
<p>Now type y</p>
<p>You should see "1100".</p>
<p>Now for something that neither HTML or CSS can do: Math.</p>
<p>Type <code>x - y </code>into the console.</p>
<p>You should get -100.</p>
<p><img src="/img/variables.png"></p>
<h3>Why use Variables? </h3>
<ul>
	<li><strong>Clarity</strong> - you can assign meaningful names to variables. </li>
	<li><strong>Reuseable</strong> - you can use the same variable in different places in your code.</li>
	<li><strong>Time saver</strong> - you can change its value in one place and the new value is called on throughout your code</li>
	<li><strong>Placeholder</strong> - a varible can be empty until some event or user action or input gives it a value.</li>
</ul>
<br>
<h3>Naming Variables</h3>
<p>The idea is to give meaningful names so you aren't confused by what they stand for. Apart from that, here are some basic rules: </p>

<ul>
	<li>
		They ARE case sensitive.
	</li>
	<li>
		Cannot begin with numbers.
	</li>
	<li>
		No spaces between words, instead use underscores, hypens or camelCase.
	</li>
	<li>
		Don't use any JavaScript <a href="http://www.w3schools.com/js/js_reserved.asp">reserved words</a>.
	</li>



</ul>
<br>
<p>You might not remember what x and y variables stand for once you deep into your code, but you will remember what monthlyPaycheck and MonthlyExpenses stand for.</p>
<p>Type:</p>
<p><code>var monthlyPaycheck = 1000;</code> and hit enter.</p>
<p><code>var monthlyExpenses = 1100;</code> and hit enter.</p>
<p><code>monthlyPaycheck - monthlyExpenses</code> and hit enter.</p>
<p>You get the same results but you won't be confused by these variables later as you would be by x and y.</p>
<p><img src="/img/monthly.png"></p>

<h3>Declaring a Variable</h3>


<p>For a number, you simply type <code><strong>var</strong> myInfo = someNumber;</code></p>
<p>For a string, you type <code><strong>var</strong> myInfo = "Some string of letters, words, etc.";</code></p>

<p><img src="/img/mag-glass.jpg">What's the difference between naming a variable that holds a number and a string?</p>

<p>Strings must be contained within either <code>'Single Quotes'</code> or <code>"Double Quotes"</code>. You can't mix and match.</p>

<p>You can also declare a variable but assign it a value later based on a computation or some input (age, name, etc.). You simply type <code><strong>var</strong> myPlaceholder;</code> to declare a variable with no value.</p>
<p>For example:</p>
<p><img src="/img/monthly-declaration.png"></p>
<p>You can also declare a variable and assign a value based on a computation at one time:</p>
<p> 
	<img src="/img/monthly-after-declaration.png">
</p>

<h3>Escaping Special Characters</h3>
<p>
Type the following into your console:
</p>
<p><code>var testString = ""He could not find his keys," the inspector said.";</code></p>

<p>
<code>
var testString = 'It's time to sleep.';
</code>
</p>
<p>
	<img src="/img/string-quotes-error.png">
</p>
<p>You get an error. Why?</p>

<p>You'll recall that strings in a variable have to be contained within either <code>'Single Quotes'</code> or <code>"Double Quotes"</code>. The problem occurs when a <code>"Double Quotes"</code> string itself contains a quotation. Or a <code>'Single Quotes'</code> string has a contraction that uses an apostrophe.  </p>

<p>
We get around this situation by using the <code>\ escape character.</code>
</p>

<p>Try it. Type the following into your console:</p>

<p>
<code>var testString = "\"He could not find his keys,\"; the inspector said."</code>
</p>

<p>
<code>
var testString = 'It\'s time to sleep.';
</code>
</p>
<p>Now the strings work and you see either the quotation or the apostrophe.</p>
<p>
<img src="/img/escaping.png">
</p>

<h3>Exercise Three (10 minutes)</h3>
<p>Create variables for each of the following:</p>
<ul>
<li>"It's been</li>
<li>a hard days night</li>
<li>and I've been working like a dog."</li>
</ul>
<p>
Now create a varible that combines previous variables to create a complete sentence. 
</p>
<p span="font-size: 5px;">HINT: strings can be added together.</p>
<p>Create variables for the following:</p>
<ul>
<li>The numeral 5 as a number.
</li>
<li>The number 4 as a string</li>
</ul>
<p>Add the two variables together. What do you get?</p>
<p>Flip the order of adding them together. What do you get?</p>
<p><img src="/img/mag-glass.jpg">What's happening?</p>

<h3>External JavaScript File</h3>

<p>As your JavaScript code gets more involved and longer, it will clutter up your HTML file (and slow its response time).</p>
<p>Or you have several HTML files that require the same JavaScript. You don't want to same JavaScript repeated across many files. It's a pain to fix one error (let alone many errors) across numberous files. </p>

<p>It's good practice to place your JavaScript into an external file -- just like you've been placing your CSS into an external stylesheet for several reasons. </p>

<ul>
	<li>
		All HTML pages across a website can call the same JavaScript located in one external page.
	</li>
	<li>
		Keeps your HTML free of code, making it reasier to read.
	</li>
	<li>
		Keeps your JavaScript free of HTML, making it easier to read.
	</li>
	<li>
		A browser will cache that JavaScript file, speeding up load time on each HTML page.
	</li>


</ul>
<br>
<p>Let's use Command Line to create a JavaScript file.</p>
<ol type="1">
	<li>
		Make a new directory call my-first-js using <code>mkdir</code>.
	</li>
	<li>
		Navigate into your directory (or folder) using <code>cd</code>.

	</li>
	<li>
		Create three different files at one time using <code>touch index.html page2.html myjavascript.js mystylesheet.css</code>. 
	</li>
	<li>
		Open all the files at one time using <code>subl .</code> and all should appear.
	</li>
	<li>
		In the <code>index.html</code> file, add the basic HTML that all HTML files require.
	</li>
	<li>
		In <code>index.html</code> add <code>&lt;p&gt;Content I typed into page 1.&lt;/p&gt;</code> with the opening and closing <code>body</code> tags.
	</li>

	<li>
		In <code>page2.html</code> add <code>&lt;p&gt;Content I typed into page 2.&lt;/p&gt;</code> with the opening and closing <code>body</code> tags.
	</li>
	<li>In both the HTML files, add the following into the <code>head</code>: <code>&lt;script type=&quot;text/javascript&quot; src=&quot;myjavascript.js&quot;&gt;&lt;/script&gt;</code></li>
	<li>
		In the <code>myjavascript.js</code> file, type <code>document.write("Content created using JavaScript");</code>
	</li>
	<li>After saving all files, open them in your browser.</li>

</ol>

<p>What do you see?</p>
<p>Here's what you should see:</p>
<p>
	<img src="/img/external-js.png">
</p>
<p>
Move the <code>&lt;script type=&quot;text/javascript&quot; src=&quot;myjavascript.js&quot;&gt;&lt;/script&gt;</script></code> out of the <code>head</code> and place right before the  <code>&lt;/body&gt;</code> tag.
</p>

<p>What happens?</p>

<p>Going forward, ALWAYS place the link to your <code>.js</code> file right before the <code>&lt;/body&gt;</code> tag. This allows the page to be rendered first before the JavaScript is applied to it. Another reason to do this is that the more JavaScript you have in the <code>head</code>, the slower the page will load.</p>

<h3>Exercise 4 (15 minutes)</h3>

<p>Recreate the webpage you produced in Exercise One but this time using an external JavaScript file. There should be NO content in <code>index.html</code> file beyond the barebones required HTML and link to the external JavaScript file.</p>

<h3>Homework</h3>

<p>TK</p>



