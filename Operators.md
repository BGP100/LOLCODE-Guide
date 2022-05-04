<a href="Types.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="InputAndOutput.md">Next &gt;</a>
<hr>
Operators play an important role to perform various operations on variables. This chapter brings you various operators in LOLCODE and their usage.
<hr>
Mathematical operators depend on a prefix notation i.e. the notation that comes before the operand. When all the operators have known number of arguments or operands, then no grouping markers are necessary. In cases where operators don’t have fixed arguments or operands, the operation is closed with MKAY.
<br>
An MKAY may not be used if it coincides with the end of the statement. In such cases, the EOL keyword should be used. To use unary mathematical operators , use the following syntax:
<pre>&lt;operator&gt; &lt;expression&gt;</pre>
The AN keyword can optionally be used to separate arguments, and apply a single operation on more than one operand, so a binary operator expression has the following syntax:
<pre>&lt;operator&gt; &lt;expression1&gt; AN &lt;expression2&gt;</pre>
Any expression containing an operator with infinite number of arguments can be expressed with the following syntax:
<pre>&lt;operator&gt; &lt;expression1&gt; [[AN &lt;expression2&gt;] AN &lt;expression3&gt; ...] MKAY</pre>
<h1>Math</h1>
Following are the basic mathematical operations in LOLCODE:
<pre>
SUM OF &lt;a&gt; AN &lt;b&gt;      BTW This is a plus + operator
DIFF OF &lt;a&gt; AN &lt;n&gt;     BTW This is a minus - operator
PRODUKT OF &lt;a&gt; AN &lt;n&gt;  BTW This is a multiply operator *
QUOSHUNT OF &lt;a&gt; AN &lt;n&gt; BTW This is a divide operator
MOD OF &lt;a&gt; AN &lt;n&gt;      BTW This is a modulo operator
BIGGR OF &lt;a&gt; AN &lt;n&gt;    BTW This is a max operator
SMALLR OF &lt;a&gt; AN &lt;n&gt;   BTW This is a min operator
</pre>
<b>&ly;a&gt;</b> and <b>&ly;b&gt;</b> can each be unique expressions in the above, so mathematical operators can be nested and grouped indefinitely.
<br>
Math is performed considering arguments as integer math in the presence of two NUMBRs, but if either of the expressions is NUMBAR, then operations are considered as floating point operations.
<pre>
HAI 1.2
   I HAS A m ITZ 4
   I HAS A n ITZ 2
VISIBLE SUM OF m AN n      BTW +
VISIBLE DIFF OF m AN n     BTW -
VISIBLE PRODUKT OF m AN n  BTW *
VISIBLE QUOSHUNT OF m AN n BTW /
VISIBLE MOD OF m AN n      BTW modulo
VISIBLE BIGGR OF m AN n    BTW max
VISIBLE SMALLR OF m AN n   BTW min
KTHXBYE
</pre>
The above code will produce the following output when you run it:
<pre>
sh-
4.3$ lci main.lo<br>
6<br>
2<br>
8<br>
2<br>
0<br>
4<br>
2
</pre>
<h1>Important Points</h1>
Consider the following important points related to working with mathematical operators in LOLCODE:
<br>
If one or both arguments in an expression are YARN, they are treated as NUMBARs.
<br>
If any of the arguments cannot be safely casted internally to a numerical type, then it fails with an error
<h1>Boolean</h1>
Boolean operators are applied on those values that may be true or false. Boolean operators working on TROOFs are as following:
<pre>
BOTH OF &lt;m&gt; AN &lt;n&gt;             BTW its and operation: WIN if m = WIN and n = WIN
EITHER OF &lt;m&gt; AN &lt;n&gt;           BTW its or operation: FAIL iff m = FAIL, n = FAIL
WON OF &lt;m&gt; AN &lt;n&gt;              BTW its xor operation: FAIL if m = n
NOT &lt;m&gt;                        BTW its an unary negation: WIN if m = FAIL
ALL OF &lt;m&gt; AN &lt;n&gt; ... MKAY     BTW it will take infinite arguments and apply AND
ANY OF &lt;m&gt; AN &lt;n&gt; ... MKAY     BTW it will take infinite arguments and apply OR.
</pre>
Please note that <b>&lt;m&gt;</b> and <b>&lt;n&gt;</b> in the expression syntax above are automatically cast as TROOF values if they are not already TROOF Values.
<h1>Comparison</h1>
When you want to compare two or more operands in LOLCODE, you can do so in any of the following methods:
<br>
<b>Method 1:</b>
<br>
You can compare two binary operands using equality operators. The syntax is shown below:
<pre>
BOTH SAEM &lt;m&gt; AN &lt;n&gt;   BTW this will return WIN if m is equal to n
DIFFRINT &lt;m&gt; AN &lt;n&gt;    BTW this will return WIN if m is not equal to n
</pre>
<b>Method 2:</b>
<br>
You can compare if both the values are of NUMBRs type. Remember that if either of the values are NUMBARs, then they are compared as floating point values.
<br>
<b>Method 3:</b>
<br>
You can also perform comparison using the minimum and maximum operators. The syntax is shown below:
<pre>
BOTH SAEM &lt;m&gt;   AN BIGGR OF &lt;m&gt; AN &lt;n&gt;
BOTH SAEM &lt;m&gt;  AN SMALLR OF &lt;m&gt; AN &lt;n&gt;
DIFFRINT &lt;m&gt;  AN SMALLR OF &lt;m&gt; AN &lt;n&gt;
DIFFRINT &lt;m&gt; AN BIGGR OF &lt;m&gt; AN &lt;n&gt;
</pre>
<pre>
HAI 1.2
   I HAS A VAR11 ITZ 7
   BOTH SAEM VAR11 SMALLR OF VAR11 AN 8, O RLY?
      YA RLY
         VISIBLE "TRUE"
      NO WAI
         VISIBLE "FALSE"
   OIC
KTHXBY
</pre>
You can see the following output when you execute the given code:
<pre>
sh-
4.3$ lci main.lo
TRUE
</pre>
<h1>Concatenation of Values</h1>
LOLCODE allows you to explicitly concatenate infinite number of YARNs using the SMOOSH…MKAY operator. For concatenation, multiple arguments can be separated with the AN operator.
<pre>
HAI 1.2
I HAS A VAR1 ITZ A YARN
VAR1 R "TRUE"
I HAS A VAR2 ITZ A YARN
VAR2 R "ANOTHER TRUE"
I HAS A VAR3 ITZ A YARN
VAR3 R "ONE MORE TRUE"
VISIBLE SMOOSH VAR1 " " VAR3 " " VAR2 MKAY
KTHXBYE
</pre>
The above given code will produce the following result upon execution:
<pre>
sh-
4.3$ lci main.lo
TRUE ONE MORE TRUE ANOTHER TRUE
</pre>
<h1>Type Casting</h1>
Operators that work on specific types implicitly cast or convert the values of one type to other type safely. If the value cannot be safely converted to other type, then it results in an error.
<br>
An expression's value may be explicitly casted or converted to some other type with the binary MAEK operator. The syntax of MAEK Operator is:
<pre>MAEK &lt;expression&gt; A &lt;type&gt;</pre>
where, <type> can be one of TROOF, YARN, NUMBR, NUMBAR, or NOOB.
<br>
To explicitly cast a variable to some other type, a normal assignment statement with the MAEK operator can be used, or a casting assignment statement may be used as follows:
<pre>
&lt;Any_variable&gt; IS NOW A &lt;type&gt;  BTW this code will be equal to
&lt;Any_variable&gt; R MAEK &lt;variable&gt; A &lt;type&gt;
</pre>
<pre>
HAI 1.2
I HAS A food ITZ "111.00033"
VISIBLE food
BTW this is how we do type casting
MAEK food A NUMBAR
VISIBLE food
KTHXBYE
</pre>
The above code will produce the following output:
<pre>
sh-4.3$ lci main.lo
111.00033
</pre>
