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

<p><img src="/img/mag-glass.jpg"> If it didn't work, make sure all quote marks are straight quotes rather than curly quotes</p>

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
<p>Open your index.html file in chrome. You should see a formatted html page.</p>

<p><img src="/img/budget-js.png"></p>

<p>View Source the browser page and you'll see that you created an HTML page without any HTML in the body. It's all JavaScript:</p>

<p><img src="/img/html-normally-here.png"></p>

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

<h3>Exercise (15 minutes)</h3>

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
<p>
Create a page with the same budget info, but use HTML in the Body.
</p>

<p>
Give the H1 tag the id of "budget".
</p>
<p><img src="/img/budget-id.png"></p>

<h3>ID Power</h3>
<p>
Imagine a webpage full of IDs. We can use JavaScript to target a particular ID and do something to it using the <code>document.getElementbyId()</code> method.
</p>
<p>
In English, it says, "In this current document, get the thing with a particular ID and do something to it."
</p>
<p>
Let's try it. At the bottom of the page (but before the closing Body tag), add following:
</p>

<p>
	<code>
	&lt;script type=&quot;text/javascript&quot;&gt;
	document.getElementById(&quot;less&quot;).style.color = &quot;red&quot;;
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
	Color is just one of about 100 styling objects. Find the <a href="http://www.w3schools.com/jsref/dom_obj_style.asp">full list here</a>.
</p>
<p>
Add the following between the script tags:
</p>
<p>
<code>
document.getElementById("less").style.fontFamily = "Arial";
document.getElementById("less").style.textTransform = "uppercase";
</code>
</p>
<p>
	<img src ="/img/more-style.png">
</p>

<p>
It should look like this:
</p>

<p>
<img src="/img/stlyed.png">
</p>