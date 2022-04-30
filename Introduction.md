<a href="Home.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="Syntax.md">Next &gt;</a>
<hr>
LOLCODE is an esoteric programming language inspired by the funny things on the Internet. It is designed to test the boundaries of programming language design.
<br>
This chapter will make you familiar with setting up the local environment for LOLCODE, and installing it on Windows.
<h1>Setting Up the Local Environment</h1>
The LOLCODE interpreter is written in C Language. It interprets the code written in LOLCODE language on multiple platforms. The LOLCODE interpreter is known as lci, which stands for LOLCODE Interpreter.
<br>
Please note that LOLCODE officially supports direct installation of interpreter for MAC operating Systems only. To install LOLCODE in your operating system, you need to follow the steps given below:
<ol>
  <li>Press CMD+Space, and type Terminal and press enter/return key</li>
  <li>Run in Terminal app</li>
  <li><code>$ git clone https://github.com/justinmeza/lci.git</code></li>
  <li><code>$ cd lci</code></li>
  <li><code>$ cmake.</code></li>
  <li><code>$ make && make install</code></li>
</ol>
<h1>Installation on Windows</h1>
If you need to install LOLCODE on Windows operating system, please take these steps:
<ol>
  <li>First add MinGW and Python to your environment variables path. To do this, right click on My Computer, choose Properties, then select Advanced system settings. Select Environment Variables. In this box, select the PATH variable and then click Edit.</li>
  <li>Now, add "<code>;C:\MinGW\bin;C:\Python32</code>" to the end of that path.</li>
  <li>Next, open the Command Prompt and navigate to the project directory using the "cd" command, for example.</li>
  <li>Run the script install.py.</li>
</ol>
