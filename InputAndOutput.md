<a href="Operators.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Statements.md">Next &gt;</a>
<hr>
This chapter will explain you how to input a value through LOLCODE terminal and how to output it onto the terminal.
<h1>I/O from Terminal</h1>
You can use the keyword VISIBLE to print something in LOLCODE. VISIBLE is a function which can take an infinite number of characters as input, and prints them all at once by internally concatenating them, and converting them to strings or YARN.
<br>
The VISIBLE function ends or terminates by a delimiter, which is either a line end or a comma.
<br>
The output is automatically terminated by the compiler with a carriage return. If the final token is terminated with an exclamation symbol (!), then the carriage returned is over-ridden by this symbol.
<pre>VISIBLE &lt;any_expression&gt; [&lt;any_expression&gt; ...][!]</pre>
Please note that in LOLCODE, currently there is no defined standard for printing some data to a file.
<br>
To take some input from the user, the keyword used is GIMMEH. It is a function which can take any number of variables as input. It takes YARN as the input and stores the value in any given variable.
<pre>GIMMEH &lt;any_variable&gt;</pre>
<pre>
HAI 1.2
   I HAS A VAR ITZ A YARN BTW DECLARE A VARIABLE FOR LATER USE
   VISIBLE "TYPE SOMETHING AND ENTER"
   GIMMEH VAR BTW GET INPUT (STRING) INTO VARIABLE
   VISIBLE VAR
KTHXBYE
</pre>
When this code is run, it will ask you to enter a number and then prints the number back in the next line automatically. When you run this code, it will print the following output:
<pre>
sh-
4.3$ lci main.lo
TYPE SOMETHING AND ENTER
67<br>
67
</pre>
