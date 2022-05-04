<a href="InputAndOutput.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Loops.md">Next &gt;</a>
<hr>
LOLCODE allows you to control the flow of program through various statements. This chapter explains different types of statements available in LOLCODE.
<h1>Expression Statements</h1>
An expression without any assignment, i.e. simply calling a mathematical operation or any function, is a legal statement in LOLCODE. Once the expression is evaluated, its final value is placed in the temporary variable IT. The value of IT remains in the local scope, and exists until the next time it is replaced with an expression.
<h1>Assignment Statements</h1>
Assignment statements are used to assign the output of any expression to a given variable. They are generally of the form:
<pre>&lt;any_variable&gt; &lt;assignment operator&gt; &lt;any expression&gt;</pre>
Please note that, you can use a variable in the expression, even before it is being assigned.
<h1>Conditional Statements</h1>
<h2>If-Then Statements</h2>
The if−then statement is a very simple operation working on the IT variable. It is similar to if−else statements in other programming languages like C and Java.
<br>
There are four keywords to apply the if–then statements.
<ul>
  <li>O RLY?</li>
  <li>YA RLY</li>
  <li>NO WAI</li>
  <li>OIC</li>
</ul>
The general form is:
<pre>
&lt;any_expression&gt;
O RLY?
   YA RLY
      &lt;code to execute if above condition is true&gt;
   NO WAI
      &lt;code to execute in this block&gt;
OIC
</pre>
All of the above statements can be written in the same line separated by commas like:
<pre>
 BOTH SAEM NAMES AN "Name", O RLY?
   YA RLY, VISIBLE "My name is ABCD"
   NO WAI, VISIBLE "Your name is ABCD"
 OIC
</pre>
While using the if-then statements, an optional MEBBE <b>&lt;any expression&gt;</b> may be used between the YA RLY and NO WAI blocks.
If the <b>&lt;any expression&gt;</b> following MEBBE is True (WIN), then that block is executed. Otherwise, if that expression is false, the block is skipped until the next MEBBE, NO WAI, or OIC statements.
<pre>
&lt;any expression&gt;
O RLY?
   YA RLY
      &lt;code to be executed if true&gt;
   MEBBE &lt;expression&gt;
      &lt;code to be executed mebbe is true&gt;
   MEBBE &lt;expression&gt;
      &lt;code to be executed mebbe is true&gt;
   NO WAI
      &lt;code to be executed if above are false&gt;
OIC
</pre>
<pre>
BOTH SAEM NAMES AN "NAME"
O RLY?
   YA RLY, VISIBLE "YOUR NAME IS ABCD"
   MEBBE BOTH SAEM ANIMAL AN "OUR NAME IS ABCD"
   VISIBLE "NO ABCD"
OIC
</pre>
<h1>Case Statements</h1>
In LOLCODE, the keyword ‘WTF?’ is similar to switch in many other languages. The keyword WTF? takes IT as the expression value for comparison. To use WTF, a comparison block is opened by OMG which should be a literal, and not an expression.
<br>
Please remember that each literal must be unique, similar to the case in other languages.
<br>
The OMG block must be terminated by a GTFO statement. If an OMG block is not terminated by a GTFO, then the next OMG block is executed till GTFO is reached.
<br>
If none of the literals evaluate as true, then default case is signified by OMGWTF.
<pre>
WTF?
   OMG &lt;any value to compare&gt;
      &lt;code block to execute if expression is satisfied&gt;
   OMG &lt;any value to compare&gt;
      &lt;code block to execute if expression is satisfied&gt;
   OMGWTF
      &lt;code block to execute as a default case&gt;
OIC
NAME, WTF?
   OMG "A"
      VISIBLE "ABCD"
      GTFO
   OMG "E"
      VISIBLE "EFGH"
      GTFO
   OMGWTF
      VISIBLE "ZYXW"
OIC
</pre>
The output results of the above code will be:
<pre>
"E":
EFGH
</pre>
