<a href="Loops.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Exception-Handling.md">Next &gt;</a>
<hr>
Functions are useful in programming because they reduce time and effort for writing the code again and again. A well written function code offers high reusability. This chapter explains you how to write and work with functions in LOLCODE.
<h1>Definition of a Function</h1>
A function is a set of statements that are executed all at once by calling that function. In LOLCODE, a function’s definition starts with the keyword “HOW IZ I” and the closing keyword is “IF U SAY SO”.
<br>
The syntax for writing a function in LOLCODE is:
<pre>
HOW IZ I &lt;function name&gt; [YR &lt;parameter/argument&gt; [AN YR &lt;other_arguments..&gt; ...]]
   &lt;code block to execute / Set of statements to execute&gt;
IF U SAY SO
</pre>
<h2>Important Points</h2>
Consider the following important points when you are defining a LOLCODE function −
<ul>
  <li>In LOLCODE, the function can accept only a certain fixed number of arguments as an input.</li>
  <li>The arguments or parameters, are the identifiers that become a variable to the function.</li>
  <li>Functions in LOLCODE can’t access any other values other than the values passed to them as arguments.</li>
</ul>
<h1>Returning Value from a Function</h1>
Return in coding means something that is given back. In programming, a function can return some value to the program when its execution is completed. In LOLCODE, functions return varying values as explained below −
<ul>
  <li><b>FOUND YR &lt;any_expression&gt;</b> returns the value of the expression when function block is executed completely.</li>
  <li><b>GTFO</b> returns no value (NOOB), which is similar to <b>return 0</b> in other programming languages like C and Java.</li>
  <li>If no other return statement is found, then <b>IF U SAY SO</b> is executed and the value in the IT variable is returned.</li>
</ul>
<h1>Calling Functions</h1>
A function is defined in the body of program and is later called for execution. A function which accepts a given number of arguments is called as shown below:
<pre>I IZ &lt;function_name&gt; [YR &lt;expression_One&gt; [AN YR &lt;expression_Two&gt; [AN YR &lt;expression_Three&gt; ...]]] MKAY</pre>
While calling a function, the expression is formed by the function name, followed by the number of arguments that the function will accept. These arguments can be simple variables or any expressions. If a function accepts any expression instead of a simple value, then the expressions' values are calculated before the function is called.
<br>
Please remember that the number of arguments a function will accept, should be defined in the definition of the function.
<pre>
HAI
HOW DUZ I MAINUMBA
  I HAS A NUMBA
  GIMMEH NUMBA
  FOUND YR NUMBA
IF U SAY SO
VISIBLE MAINUMBA
KTHXBYE
</pre>
When you run the above code, it will ask for an input, and then when you submit the input, you’ll see the same as the result. For example, if we enter 55, it will print 55.
<pre>
HAI 1.2
HOW IZ I MULTIPLY YR FIRSTOPERANT AN YR SECONDOPERANT
  FOUND YR PRODUKT OF FIRSTOPERANT AN SECONDOPERANT
  IF U SAY SO
  VISIBLE I IZ MULTIPLY YR 2 AN YR 3
KTHXBYE
</pre>
The above function that performs multiplication of input operands will print the following output when you run it:
<pre>
sh-
4.3$ lci main.lo<br>
6
</pre>
<pre>
HAI 1.2
I HAS A STRINGARRAY ITZ A BUKKIT
  STRINGARRAY HAS A VAR17 ITZ "OBJECT1"
  STRINGARRAY HAS A VAR18 ITZ "OBJECT2"
  HOW IZ STRINGARRAY ACCESS YR VARIABLE
    FOUND YR STRINGARRAY'Z SRS VARIABLE
  IF U SAY SO
  I HAS A STRING ITZ "VAR17"
  VISIBLE STRINGARRAY IZ ACCESS YR STRING MKAY
KTHXBYE
</pre>
The output that the above code will produce is:
<pre>
sh-
4.3$ lci main.lo 
OBJECT1
</pre>
