<a href="Syntax.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Operators.md">Next &gt;</a>
<hr>
LOLCODE is designed to test the boundaries of the programming language design. It is an esoteric programming language inspired by the funny things on the Internet. This chapter gives you an understanding of LOLCODE types.
<hr>
Currently, the variable types in LOLCODE are:
<ul>
  <li>strings (YARN)</li>
  <li>integers (NUMBR)</li>
  <li>floats (NUMBAR)</li>
  <li>and booleans (TROOF)</li>
  <li>Arrays (BUKKIT)</li>
</ul>
In LOLCODE the variable type is handled dynamically by the compiler. If a variable does not have an initial value, it is called untyped (known as NOOB in LOLCODE).
<br>
The syntax for declaring and using different types in LOLCODE is shown below:
<br>
<b>To create a variable of any data type:</b>
<pre>I HAS A &lt;VARIABLE&gt; ITZ A &lt;DATA TYPE&gt;</pre>
<b>To create a variable and assign a value to it:</b>
<pre>I HAS A &lt;VARIABLE&gt; ITZ &lt;EXPRESSION&gt;</pre>
<b>To assign a value to an already created data type:</b>
<pre>&lt;VARIABLE&gt; R &lt;EXPRESSION&gt;</pre>
<h1>Untyped (NOOB)</h1>
The untyped data type (known as NOOB), cannot be converted into any other type except into a TROOF data type. The implicit casting of a NOOB into TROOF makes the variable FAIL. After that any operation on a NOOB results in an error.
<br>
Explicit casts of a NOOB data type (i.e. the types that are uninitialized and do not have any initial value) variable results to zero values for all other types.
<br>
To define an untyped variable, just declare a variable and assign a value as shown in this example:
<pre>
HAI 1.2
I HAS A VAR3
VAR3 R "ANYVALUE"
VISIBLE VAR3
BTW Or declare in same line
I HAS A VAR4 ITZ 44
VISIBLE VAR4
KTHXBYE
</pre>
When you run the above program, you will find the following result:
<pre>
sh-
4.3$ lci main.lo 
ANYVALUE
44
</pre>
<h1>Booleans (TROOFS)</h1>
In LOLCODE, the Boolean values are of two types. BOOLEAN generally have two values- true and false. But, in LOLCODE, the Boolean is known as TROOF, and the true/ false values are known as WIN/FAIL respectively. All the uninitialized values like an empty string (""), or an empty array will all cast to FAIL. All other initialized values evaluate to WIN.
<pre>
HAI 1.2
I HAS A VAR3 ITZ A TROOF
VAR3 R "FAIL"
   VISIBLE VAR3
KTHXBYE
</pre>
You can see the following output when you execute the above code −
<pre>
sh-4.3$ lci main.lo
FAIL
</pre>
<h1>Numerical Types (NUMBR)</h1>
In LOLCODE, a NUMBR stands for an integer. Any sequence of digits is considered as a NUMBR, unless it has a decimal appearing anywhere in between the sequence. To make any number negative, it may be preceded by a hyphen (-) which signifies a negative number.
<pre>
HAI 1.2
I HAS A VAR3 ITZ A NUMBR
   VISIBLE VAR3
KTHXBYE
</pre>
The above code shows you the following result when you run it−
<pre>
sh- 
4.3$ lci main.lo
0
</pre>
Similar to NUMBR, LOLCODE has another data type, which represents a decimal or a float in many programming languages. In LOLCODE, a NUMBAR is a float containing one decimal point. Casting a NUMBAR to a NUMBR truncates the decimal portion of the floating point number and returns it as a NUMBR, without any decimal.
<h1>Strings (YARN)</h1>
In LOLCODE, value containing strings, i.e. string literals (YARN) should start and end with double quotation marks ("”).
<br>
Anything may be written inside the string, like space, comma, full stop, exclamation or any other symbol. A string where any single quote is missing may cause an error. Colons are used as escape characters in LOLCODE, and any value following a colon gets a special meaning.
<ul>
  <li><code>:)</code> − A closing bracket following a colon represents a newline (\n)</li>
  <li><code>:&gt;</code> − A closing angle bracket following a colon represents a tab (\t)</li>
  <li><code>:o</code> − A ‘o’ character following a colon represents a bell (beep) (\g)</li>
  <li><code>:"</code> − A “ following a colon represents a literal double quote (")</li>
  <li><code>::</code> − A colon following a colon represents a single literal colon (:)</li>
</ul>
<pre>
HAI 1.2
I HAS A VAR3 ITZ A YARN
VAR3 R "XYZ"
   VISIBLE VAR3
KTHXBYE
</pre>
The code given above produces the following output upon execution:
<pre>
sh-
4.3$ lci main.lo 
XYZ
</pre>
<h1>BUKKIT</h1>
This type represents an array. It has named slots, which can contain either variables or functions. A BUKKIT can be declared in the following way −
<pre>
BTW declaration of the BUKKIT
I HAS A [object] ITZ A BUKKIT BTW creating a variable in a slots
[object] HAS A [var] ITZ [value] BTW creating a function inside the BUKKIT
HOW IZ [object] [function name] (YR [argument1] (AN YR [argument2] (AN YR [argument3] ...)))
[function code]
IF U SAY SO
</pre>
A function inside a BUKKIT may also access variables and other functions of the BUKKIT by using ME'Z [var] or ME IZ [function name] (YR [argument1] (AN YR [argument2] (AN YR [argument3] ...))) MKAY.
<pre>
HAI 1.2
   I HAS A VAR6 ITZ A BUKKIT
   BTW DECLARING AN ARRAY
   VAR6 HAS A VAR7 ITZ "DOGE"
   BTW VAR7 IS A STRING VARIABLE THAT IS INSERTED  INTO ARRAY VAR6
   VISIBLE VAR6'Z VAR7
   BTW GET THE ELEMENT OF ARRAY
KTHXBYE
</pre>
This is the output you will find when you run the code given above −
<pre>
sh-
4.3$ lci main.lo 
DOGE
</pre>
