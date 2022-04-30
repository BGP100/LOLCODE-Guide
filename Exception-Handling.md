<a href="Functions.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Examples.md">Next &gt;</a>
<hr>
Exception handling is one of the powerful mechanisms to handle the runtime errors so that the normal flow of the application can be maintained. LOLCODE does not have a lot of support for exception handling like other programming Languages. Similar to the Try-Catch block in other languages, LOLCODE has the PLZ-block.
<br>
For example, if you want to open a file that may or may not exist, use:
<pre>
PLZ OPEN FILE "filename.TXT"?
   AWSUM THX
      VISIBLE FILE
   O NOES
      INVISIBLE "ERROR!"
KTHX
</pre>
The code that may cause an exception is written in the PLZ block, and the exception is handled in the O NOES block. Here, the INVISIBLE keyword sends an inner message to the debugger.
<br>
Please note that as LOLCODE is not maintained regularly, there are no more updates available for LOLCODE exception handling and many other features.
