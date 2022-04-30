<a href="Introduction.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Variables.md">Next &gt;</a>
<hr>
The LOLCODE constructs are slang words. The following table shows the alphabetical list of constructs implemented so far:
<table class="ws-table-all notranslate">
  <tr>
    <th>Numbr</th>
    <th>Syntax</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>1</td>
    <td>BTW</td>
    <td>It starts a single line comment.</td>
  </tr>
  <tr>
    <td>2</td>
    <td>DOWN &lt;variable&gt;!!&lt;times&gt;</td>
    <td>This corresponds to variable = variable - times. Note that "times" is a wut-only language extension.</td>
  </tr>
  <tr>
    <td>3</td>
    <td>GIMMEH &lt;variable&gt;</td>
    <td>This represents the input statement.</td>
  </tr>
  <tr>
    <td>4</td>
    <td>GTFO</td>
    <td>This is similar to break in other languages and provides a way to break out of a loop.</td>
  </tr>
  <tr>
    <td>5</td>
    <td>HAI</td>
    <td>This corresponds to <b>main()</b> function in other languages. It is the program entry point in LOLCODE.</td>
  </tr>
  <tr>
    <td>6</td>
    <td>HEREZ &lt;label&gt;</td>
    <td>This is another wut-only language extension and declares a label for use with SHOO</td>
  </tr>
  <tr>
    <td>7</td>
    <td>I HAS A &lt;type&gt; &lt;variable&gt;</td>
    <td>This declares a variable of said type.<br>There are three built-in types in LOLCODE:<ul><li>NUMBAH (int)</li><li>DECINUMBAH (double)</li><li>WORDZ (std::string)</li></ul>Note that types are a wut-only language extension.</td>
  </tr>
  <tr>
    <td>8</td>
    <td>IM IN YR LOOP</td>
    <td>This starts an infinite loop. The only way to exit the loop is using GTFO. Corresponds to <b>for(;;)</b> in other languages</td>
  </tr>
  <tr>
    <td>9</td>
    <td>IZ &lt;expr1&gt; &lt;operator&gt; &lt;expr2&gt;?: Conditional structure</td>
    <td>This is similar to if operator in other languages. Operator is one of: BIGGER THAN, SMALLER THAN, SAEM AS. Note that the ? at the end is optional.</td>
  </tr>
  <tr>
    <td>10</td>
    <td>KTHX</td>
    <td>It ends a block. Corresponds to a <code>}</code></td>
  </tr>
  <tr>
    <td>11</td>
    <td>KTHXBAI</td>
    <td>This ends a program</td>
  </tr>
  <tr>
    <td>12</td>
    <td>NOWAI</td>
    <td>This corresponds to <b>else</b></td>
  </tr>
  <tr>
    <td>13</td>
    <td>PURR &lt;expr&gt;</td>
    <td>This prints argument on screen, followed by a newline. It is a wut-only language extension.</td>
  </tr>
  <tr>
    <td>14</td>
    <td>RELSE</td>
    <td>This corresponds to <b>if else</b></td>
  </tr>
  <tr>
    <td>15</td>
    <td>SHOO</td>
    <td>This is another wut-only language extension, that corresponds to goto (the horror!)</td>
  </tr>
  <tr>
    <td>16</td>
    <td>UP &lt;variable&gt;!!&lt;times&gt;</td>
    <td>This corresponds to variables = variable + times. Here "times" is a wut-only language extension.</td>
  </tr>
  <tr>
    <td>17</td>
    <td>VISIBLE &lt;expr&gt;</td>
    <td>This prints the argument on screen. Note that this does not print a newline.</td>
  </tr>
  <tr>
    <td>18</td>
    <td>YARLY</td>
    <td>This denotes the start of the "true" conditional block</td>
  </tr>
</table>
<h1>Whitespace</h1>
In most programming languages, keywords or tokens may not have spaces between them. However, in some languages, spaces are used in tokens to differentiate them.
<h2>Comma</h2>
The comma behaves like a newline keyword in most languages, for example, \n in Java and C. You can write many commands in a single line in LOLCODE, provided that you separate them using a comma (,).
<h2>Three Periods</h2>
The three periods (…) enables you to combine multiple lines of code into a single line or a single command by including (...) at the end of the line. This makes the compiler to treat the content of the next line as the content of previous line only. Infinite lines of code can be written together as a single command, as long as each line is ended with three periods.
<br>
A comment is terminated by a newline. Please note that the line continuation (...) and (,) after the comment (BTW) are ignored by the lci.
<h1>Comments</h1>
Single line comments are written followed by the BTW keyword. They may occur anywhere inside a program body: it can be at the first line of program, in between the program, in between some line, or at the end of a program.
<br>
All of these are valid single line comments:
<pre>
I HAS A VAL ITZ 19      BTW VAL = 19
I HAS A VAL ITZ 19,   BTW VAL = 19
I HAS A VAL ITZ 14
BTW VAR = 14
</pre>
In LOLCODE, multiple line comments are written followed by OBTW and they are ended with TLDR.
<br>
This is a valid multi−line comment:
<pre>
I HAS A VAL ITZ 51
   OBTW this is a comment
      No it’s a two line comment
      Oops no.. it has many lines here
   TLDR
</pre>
<h1>File Creation</h1>
A LOLCODE program begins with HAI keyword and it should end with KTHXBYE. As LOLCODE uses shorthand language HAI basically stands for Hi and KTHXBYE can be remembered as “Ok, thanks, bye ”.
<pre>
HAI 1.2
I HAS A NAME
VISIBLE "NAME::"!
GIMMEH NAME
VISIBLE "BledyGuides " NAME "!"
KTHXBYE
</pre>
