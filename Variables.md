<a href="Syntax.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Types.md">Next &gt;</a>
<hr>
As in any other programming language, LOLCODE allows you to define variables of various types. This chapter will make you familiar with working with variables in LOLCODE.
<h1>Scope of Variables</h1>
The scope of a variable is local to the function or to the program block, i.e. a variable defined in one scope cannot be called in any other scope of the same program. Variables are accessible only after they are declared.
<br>
Please note that there is no global scope of variables in LOLCODE.
<h1>Naming Conventions</h1>
Variable names are usually called identifiers. Here are some of the conventions for naming variables in LOLCODE:
<ul>
  <li>Variable identifiers may be in all CAPITAL or lowercase letters (or a mixture of the two).</li>
  <li>They can only begin with a letter and then may be followed by other letters, numbers, and underscores.</li>
  <li>LOLCODE does not allow use of spaces, dashes, or other symbols while naming a variable.</li>
  <li>Variable identifiers are case sensitive.</li>
</ul>
Here are some of the rules for valid and invalid names for variables in LOLCODE:
<ul>
  <li>The name should always begin with an alphabet. For example, name, Name are valid.</li>
  <li>The name of a variable cannot begin with a digit. For example, 2var is invalid.</li>
  <li>The name of a variable cannot begin with a special character.</li>
  <li>A variable can contain <code>_</code> or a digit anywhere inside its name, except at the starting index. For example, name2_m is a valid name.</li>
</ul>
Some examples of valid names in LOLCODE are shown below:
<pre>
HAI 1.2
I HAS A food ITZ "111.00033"
I HAS A food2 ITZ "111"
I HAS A fo_od ITZ "1"
VISIBLE food
VISIBLE food2
VISIBLE fo_od
KTHXBYE
</pre>
All the declaration statements in the above code are valid and will produce the following output when executed:
<pre>
sh-4.3$ lci main.lo
111.00033
111
1
</pre>
Some examples of invalid statements and their output are given below:
<br>
<b>Example 1:</b>
<pre>
HAI 1.2
I HAS A 2food ITZ "111.00033"
KTHXBYE
</pre>
The above code will give the following output when you execute it −
<pre>
sh-4.3$ lci main.lo
Line 2: Expected: identifier; Got: int(2).
</pre>
<b>Example 2:</b>
<pre>
HAI 1.2
I HAS A _food ITZ "111.00033"
KTHXBYE
</pre>
The above code will give the following output when you execute it −
<pre>
sh-4.3$ lci main.lo
Line 2: Unrecognized sequence at: _food ITZ "111.00033".
</pre>
<b>Example 3:</b>
<pre>
HAI 1.2
I HAS A f$ood ITZ "111.00033"
KTHXBYE
</pre>
The above code will give the following output when you execute it −
<pre>
sh-4.3$ lci main.lo
Line 2: Unrecognized sequence at: $ood ITZ "111.00033".
</pre>
<h1>Declaration and Assignment of Variables</h1>
To declare a variable, LOLCODE provides a keyword “I HAS A” which is followed by the variable name. You can find below the syntax for declaring a variable.
<pre>I HAS A VAR BTW VAR is empty now, You can use any name instead of var</pre>
To assign the variable a value in the same statement, you can then follow the variable name with “ITZ” and then give the value you want to assign. Use the following syntax to assign a value to a variable:
<pre>&lt;variable&gt; R &lt;expression&gt;</pre>
<hr>
<pre>
VAR R "Green" BTW VAR is now a YARN and equals "Green"
VAR R 30 BTW VAR is now a NUMBR and equals 30
</pre>
You can also declare and assign variables at the same time using the following syntax:
<pre>I HAS A VAR ITZ VALUE</pre>
<hr>
<pre>I HAS A NAME ITS “BLEDYGUIDES”</pre>
<hr>
<pre>
HAI 1.2
BTW this is how we declare variables
I HAS A food
I HAS A bird
BTW this is how we assign variables
food R 1
bird R 5
BTW this is how initialize variables
I HAS A biz ITZ "OMG!"
VISIBLE food
VISIBLE biz
VISIBLE bird
KTHXBYE
</pre>
The above program shows the declaration of variables and prints them. The output is −
<pre>
sh-
4.3$ lci main.lo
1
OMG!
5
</pre>
<h1>Type Casting</h1>
To convert a value of one type to another type, we use type casting. Casting a NUMBAR to a NUMBR truncates the decimal portion of the floating point number. Casting a NUMBAR to a YARN (by printing it, for example), truncates the output to a default 2 decimal places.
<pre>
HAI 1.2
I HAS A food ITZ "111.00033"
VISIBLE food
BTW this is how we do type casting
MAEK food A NUMBAR
VISIBLE food
KTHXBYE
</pre>
The above line of code will produce the following output −
<pre>
sh-4.3$ lci main.lo
111.00033
111.00033
</pre>
All the variables declared in a LOLCODE program are local variables and there is no global scope in this language for any variable.
