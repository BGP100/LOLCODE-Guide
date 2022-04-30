<a href="Statements.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Functions.md">Next &gt;</a>
<hr>
Loops are used in programming languages to execute a set of statements multiple times. For example, if you want to print the digit 5 for five times, then instead of writing the VISIBLE “5” statement five times, you can run a loop with single VISIBLE “5” statement for five times.
<br>
Simple loops are represented with IM IN YR <b>&lt;label&gt;</b> and IM OUTTA YR <b>&lt;label&gt;</b>. Loops defined in this way are infinite loops and they should be terminated with a GTFO break statement.
<br>
Iteration loops have the following structure:
<pre>
IM IN YR &lt;label&gt; &lt;any_operation&gt; YR &lt;any_variable&gt; [TIL|WILE &lt;expression&gt;]
   &lt;code block to execute inside the loop multiple times&gt;
IM OUTTA YR &lt;label&gt;
</pre>
Please note that inside the function body, UPPIN (increment by one), NERFIN (decrement by one), or any unary function can be used.
<br>
The TIL keyword calculates the expression as a TROOF: if it evaluates as FAIL, the loop continues once more, if it evaluates as WIN, then the loop execution stops, and continues after the matching IM OUTTA YR statement.
<br>
The WILE keyword is the opposite of TIL keyword, if the expression is WIN, execution continues, otherwise the loop exits.
<pre>
HAI 1.2
I HAS A VAR ITZ 0
IM IN YR LOOPY UPPIN YR VAR TIL BOTH SAEM VAR AN 10
   VISIBLE SUM OF VAR AN 1
IM OUTTA YR LOOPY
KTHXBYE
</pre>
When the above code is compiled on any LOLCODE compiler, or on our online codingground, this will produce the following output.
<pre>
sh-
4.3$ lci main.lo
1<br>
2<br>
3<br>
4<br>
5<br>
6<br>
7<br>
8<br>
9<br>
10
</pre>
