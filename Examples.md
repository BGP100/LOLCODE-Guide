<a href="Exception-Handling.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/Resources/Main.md">Next &gt;</a>
<hr>
The previous chapters explained you the programming in LOLCODE. In this chapter, you will learn some examples that lets you code at an advanced level in LOLCODE.
<h1>Program to Calculate the Power of a Number</h1>
In this example, you will find the code to calculate the power of an input number. For example, 2 raised to power 4 is equal to 16.
<pre>
HAI 1.2
HOW IZ I POWERTWO YR NUM
   BTW RETURN 1 IF 2 TO POWER OF 0
   BOTH SAEM NUM AN 0, O RLY?
      YA RLY, FOUND YR 1
   OIC
   BTW CALCULATE 2 TO POWER OF NUM
   I HAS A INDEX ITZ 0
   I HAS A TOTAL ITZ 1
   IM IN YR LOOP UPPIN YR INDEX TIL BOTH SAEM INDEX AN NUM
      TOTAL R PRODUKT OF TOTAL AN 2
   IM OUTTA YR LOOP
   FOUND YR TOTAL
   IF U SAY SO
   BTW OUTPUT: 8
   VISIBLE I IZ POWERTWO YR 4 MKAY
KTHXBYE
</pre>
The above code will print the following output once it runs succesfully:
<pre>
sh-
4.3$ lci main.lo
16
</pre>
<h1>Program to Make an Array</h1>
This example shows the code for making an array with five elements and each element with value 10.
<pre>
HAI 1.3
   OBTW
      CREATES A ONE DIMENSIONAL ARRAY WITH N ELEMENTS, EACH IS A 0
   TLDR
	HOW IZ I MAKEMATRIX YR N
      I HAS A MATRIX ITZ A BUKKIT
      IM IN YR LOOP UPPIN YR INDEX TIL BOTH SAEM INDEX N
         MATRIX HAS A SRS INDEX ITZ 10
      IM OUTTA YR LOOP
      FOUND YR MATRIX
   IF U SAY SO
      I HAS A N ITZ 5
      I HAS A MATRIX ITZ A BUKKIT
      MATRIX R I IZ MAKEMATRIX YR N MKAY
	   BTW PRINTS THE CONTENTS OF THE ARRAY
      IM IN YR LOOP UPPIN YR INDEX TIL BOTH SAEM INDEX N
         VISIBLE MATRIX'Z SRS INDEX
   IM OUTTA YR LOOP
KTHXBYE
</pre>
You can see the following output when you execute the above code
<pre>
sh-4.3$ lci main.lo
10<br>
10<br>
10<br>
10<br>
10
</pre>
<h1>Program to Calculate the Factorial of a Number</h1>
This program shows the code to calculate the factorial of an input number.
<pre>
HAI 1.3
   HOW IZ I FACTORIAL YR N
   BOTH SAEM N AN 0
   O RLY?
	   YA RLY, FOUND YR 1
   NO WAI
      FOUND YR PRODUKT OF N AN I IZ FACTORIAL YR DIFF OF N AN 1 
      MKAY
   OIC
   IF U SAY SO
   VISIBLE I IZ FACTORIAL YR 6 MKAY
KTHXBYE
</pre>
The above program prints the factorial of the number 6 and you can see the output as shown below:
<pre>
sh-
4.3$ lci main.lo<br>
720
</pre>
<h1>Program to Design a Calculator</h1>
You can design a calculator to perform basic math operations using LOLCODE programming. Observe the code given below:
<pre>
HAI 1.2
   I HAS A V1
   I HAS A V2
   I HAS A CHOICE
   VISIBLE "VALUE1"
   GIMMEH V1
   VISIBLE "VALUE2"
   GIMMEH V2VISIBLE "Choose Operation? + - * /"
   GIMMEH CHOICE CHOICE, WTF?
      OMG "+"
      VISIBLE SUM OF V1 AN V2
		GTFO
	OMG "-"
   VISIBLE DIFF OF V1 AN V2
		GTFO
   OMG "*"
   VISIBLE PRODUKT OF V1 AN V2
		GTFO
   OMG "/"
   VISIBLE QUOSHUNT OF V1 AN V2
      GTFO
   OMGWTF
      VISIBLE "CHOOSE SOME OPERATION"
   OIC
KTHXBYE
</pre>
When we execute the above program with following input:
<pre>
3
4
+
</pre>
Upon execution, the above program will generate the following output:
<pre>
VALUE1
VALUE2
Choose Operation? + - * /
7
</pre>
