# <h1>JavaScript Lesson 1: Introduction</h1>

<h3>Hello JavaScript Console </h3>

<p>Visit <a href="http://www.this-page-intentionally-left-blank.org/">this blank page.</a></p>

<p>Open the browser's JavaScript console by using <strong>command</strong>-<strong>option</strong>-<strong>J</strong> (&#8984; &#8997; J). Ideally you are using Chrome or Firefox.</p>

<p>Type: document.write("hello world!");</p>

<img src="/img/console.png">
<p>If you see "Hello World!" appear in your browser, congrats! Your just wrote your first bit of JavaScript.</p>

<p><img src="/img/mag-glass.jpg">Why the semi-colon? Because semi-colons separate JavaScript statements. If unsure, just use it.</p>

<p><img src="/img/mag-glass.jpg"> If it didn't work, make sure all quote marks are straight quotes rather than curly quotes</p>

<h3>Adding HTML using JavaScript:</h3>

<p>Type: 

	<code>document.write("You make $1000 per month but your expenses are $1100 per month.");</code></p>

<p>You can copy and paste part of this, but type: document.write("Your Budget Anlysis. You make $1000 per month but your expenses are $1100 per month. You need to earn more or spend less!");</p>

<p>But it just comes out as one paragraph. Let's add some HTML:</p>

<p>Type: 
	<pre>
	<code>document.write("<h2>Your Budget Analysis</h2><p>You make $1000 per month but your expenses are $1100 per month. You need to earn more or spend less!</p>");</code>
	</pre>


	document.write("&lt;h2&gt;Your Budget Analysis&lt;/h2&gt;&lt;p&gt;You make $1000 per month but your expenses are $1100 per month. You need to earn more or spend less!&lt;/p&gt;");</p>

<h3>Sublime Time</h3>

<p>When you hit reload on your browser, you lose all the work in the console. You have to keep retyping the JavaScript. Instead, let's start adding code to a Sublime file.</p>

<p>Use Command Line to create a directory call learning-js, and an index.html file inside the newly created folder.</p>

<p>Launch the index.html file using subl in Command Line.</p>

<p>Set up basic html document with doctype, html, head and body with closing tags too. It should look like this:</p>

<p><img src="/img/basic-html.png"></p>

<p>Add the following script tags into the head: &lt;script type=&quot;text/javascript&quot;&gt;
&lt;/script&gt;</p>

<p>Type the following in between the opening and closing script tags: document.write("&lt;h2&gt;Your Budget Analysis&lt;/h2&gt;&lt;p&gt;You make $1000 per month but your expenses are $1100 per month. You need to earn more or spend less!&lt;/p&gt;&lt;p&gt;Here are some ways to save money:&lt;/p&gt;&lt;li&gt;Bring your lunch to work.&lt;/li&gt;&lt;li&gt;Stop taking cabs.&lt;/li&gt;&lt;li&gt;Stop shopping at Whole Foods.&lt;/li&gt;&quot;");</p>

<p>Open your index.html file in chrome. You should see a formatted html page.</p>

<p><img src="/img/budget-js.png"></p>

<p>View Source the browser page and you'll see that you created an HTML page without any HTML in the body. It's all JavaScript:</p>

<p><img src="/img/html-normally-here.png"></p>

