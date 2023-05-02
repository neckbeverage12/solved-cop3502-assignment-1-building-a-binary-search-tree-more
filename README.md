Download Link: https://assignmentchef.com/product/solved-cop3502-assignment-1-building-a-binary-search-tree-more
<br>
Build a Java program that will support the creation of a <em>Binary Search Tree</em>, hereinafter referred to as a <em>BST</em>. This program will support reading a command file that supports insertion, deletion, searching, printing, and subtree children and depth counts. All output will be to either STDOUT or STDERR. 2             Requirements

<ol>

 <li>Read the input file formatted as follows. The input file will contain at least one command per line, either insert, delete, search, print, or quit. These are defined in detail below. For example, one of the input files, named <strong>txt </strong>contains the following:</li>

</ol>

i 9 i 24 i 3 i 4 i 11

p q

<ol start="2">

 <li>The specific commands are <strong>i </strong>for insert, <strong>d </strong>for delete, <strong>s </strong>for search, <strong>p </strong>for print, and <strong>q </strong>for quit.

  <ul>

   <li>Insert</li>

  </ul></li>

</ol>

The insert command uses the single character <strong>i </strong>as the command token. The command token will be followed by a single space then an integer.

(This command’s success can be verified by using the <em>print </em>command.)

<ul>

 <li>Delete</li>

</ul>

The delete command uses the single character <strong>d </strong>as the command token. The command token will be followed by a single space, then an integer.

In the event that the <em>integer </em>cannot be found, the program will issue an error message to <strong>STDOUT </strong>and recover gracefully to continue to accept commands from the input file.

command-&gt; d 100: integer 100 NOT found

(This command’s success can be verified by using the <em>print </em>command.)

<ul>

 <li>Search</li>

</ul>

The search command uses the single character <strong>s </strong>as the command token. The command token will be followed by a single space, then an integer.

In the event that the <em>integer </em>cannot be located, the program will issue an error message to <strong>STDOUT </strong>and recover gracefully to continue to accept commands from the input file.

command-&gt; s 101: integer 101 NOT found

<ul>

 <li>Print</li>

</ul>

The print command uses the single character <strong>p </strong>as the command token. This command will invoke the <em>print </em>function which will output the data in the tree <em>inorder</em>.

This command is critical for verification of all the commands specified above.

<ul>

 <li>Quit</li>

</ul>

The quit command uses the single character <strong>q </strong>as the command token. In the event the quit command is invoked, the program exits. There is no requirement for data persistence.

<h2>2.1           Functions</h2>

While there are no specific design requirements (with one exception), it might be a meaningful suggestion to consider breaking this problem into several small classes. For example, a <em>BST </em>class and a <em>Node </em>class would seem to be the minimal set of classes.

<strong>2.1.1       Required Function(s)</strong>

<ul>

 <li><strong>complexityIndicator</strong></li>

</ul>

Prints to <strong>STDERR </strong>the following:

<ul>

 <li>NID</li>

 <li>A difficulty rating of how difficult this assignment was on a scale of 1.0 (easypeasy) through 5.0 (knuckle busting degree of difficulty).</li>

 <li>Duration, in hours, of the time you spent on this assignment.</li>

 <li>Delimit each field with a <strong>semicolon </strong>as shown below.</li>

 <li>Sample output:</li>

</ul>

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="82e4e4b0b3b2b1b5b5c2e7f7f1f6ebf1">[email protected]</a>:~/COP3503$ ff210377;3.5;18.5

<ul>

 <li><strong>countChildren </strong>which will count <em>all </em>nodes on the left branch of the BST, and then the right branch.</li>

 <li><strong>getDepth </strong>which will provide the depth of the right and left branches of the BST.</li>

</ul>

<h1>3             Testing</h1>

Make sure to test your code on Eustis <strong><u>even if it works perfectly on your machine </u></strong>. If your code does not compile on Eustis you will receive a 0 for the assignment. There will be eight (8) input files and seven (7) output files provided for testing your code, they are respectively shown in Table 1 and in Table 2.

<table width="445">

 <tbody>

  <tr>

   <td width="127">Filename</td>

   <td width="318">Description</td>

  </tr>

  <tr>

   <td width="127">input01.txt</td>

   <td width="318">Insert 7 integers with 2 searches and a delete the prints the tree.</td>

  </tr>

  <tr>

   <td width="127">in5.txt</td>

   <td width="318">Five integers inserted with no duplicates. Prints the tree.</td>

  </tr>

  <tr>

   <td width="127">in5del2.txt</td>

   <td width="318">Five integers added followed by two deletes. One will be a delete of a non-existent integer.Prints the tree.</td>

  </tr>

  <tr>

   <td width="127">in5del1srch1.txt</td>

   <td width="318">Five names added, one valid delete, followed by a valid search, then an invalid search.Prints the tree.</td>

  </tr>

  <tr>

   <td width="127">in10.txt</td>

   <td width="318">10 integers inserted with no duplicates. Prints the tree.</td>

  </tr>

  <tr>

   <td width="127">in100.txt</td>

   <td width="318">100 integers inserted. Prints the tree</td>

  </tr>

  <tr>

   <td width="127">in100m5000.txt</td>

   <td width="318">100 random integers (all modulo 5,000) inserted with random deletes.</td>

  </tr>

  <tr>

   <td width="127">in10k-m5000.txt</td>

   <td width="318">10,000 integers (all modulo 5,000) inserted with random deletes.</td>

  </tr>

  <tr>

   <td width="127">in1m-m5000.txt</td>

   <td width="318">1,000,000 integers (all modulo 5,000) inserted with random deletes.</td>

  </tr>

  <tr>

   <td width="127">mega5.txt</td>

   <td width="318">5,000,000 random integers with random deletes. (<em>For entertainment value, as it takes a <u>long </u>time to complete</em>.)</td>

  </tr>

 </tbody>

</table>

Table 1: Input files

The expected output for these test cases will also be provided as defined in Table 2. To compare your output to the expected output you will first need to redirect <em>STDOUT </em>to a text file. Run your code with the following command (substitute the actual names of the input and output file appropriately):

java Hw01 <em>inputFileName </em>&gt; <em>inputFileName</em>St.txt

The run the following command (substitute the actual name of the expected <em>input file name </em>concatenated with either <strong>St </strong>for the student generated code or with <strong>Valid </strong>for the validation file:

diff output.txt <em>inputFileName</em>St.txt <em>inputFileName</em><strong>Valid</strong>.txt

If there are any differences the relevant lines will be displayed (note that even a single extra space will cause a difference to be detected). If nothing is displayed, then congratulations the outputs match!

If your code crashes for a particular test case, you will not get credit for that case.

<h1>4             Submission – via WebCourses</h1>

The Java source file(s). Make sure that the <em>main </em>program is in Hw01.java.

Use reasonable and customary naming conventions for any classes you may create for this assignment.

<h1>5                  Sample output</h1>

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="bcdada8e8d8c8f8b8bfcd9c9cfc8d5cf">[email protected]</a>:~/COP3503$ java Hw01 in10.txt in10.txt contains:

i 888 i 77 i 90 i 990 i 120 i 450 i 7900 i 7000 i 500 i 65

p q

65 77 90 120 450 500 888 990 7000 7900

left children:                                  6

left depth:                                       5

right children:                                3

right depth:                                    3

ff210377;3.5;18.5

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="1c7a7a2e2d2c2f2b2b5c79696f68756f">[email protected]</a>:~/COP3503$ java Hw01 &gt;5in-myOutput.txt ff210377;3.5;18.5

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="23454511121310141463465650574a50">[email protected]</a>:~/COP3503$ diff 5in-myOutput.txt 5in-expectedOutput.txt <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="3e53570f0f0d0d0a0b7e5b4b4d4a574d">[email protected]</a>:~/COP3503$

<strong>Note </strong>The <strong>ff210377;3.5;18.5 </strong>output shown above is the output from the <em>complexityIndicator </em>function to <strong>STDERR</strong>.

<table width="446">

 <tbody>

  <tr>

   <td width="203">Command</td>

   <td width="243">Output filenames</td>

  </tr>

  <tr>

   <td width="203">java Hw01 in5.txt</td>

   <td width="243">in5Valid.txt</td>

  </tr>

  <tr>

   <td width="203">java Hw01 in5del1srch1.txt</td>

   <td width="243">in5del1srch1Valid.txt</td>

  </tr>

  <tr>

   <td width="203">java Hw01 in5del2.txt</td>

   <td width="243">in5del2Valid.txt</td>

  </tr>

  <tr>

   <td width="203">java Hw01 in100.txt</td>

   <td width="243">in100Valid.txt</td>

  </tr>

  <tr>

   <td width="203">java Hw01 in100m5000.txt</td>

   <td width="243">in100m5000Valid.txt</td>

  </tr>

  <tr>

   <td width="203">java Hw01 in10.txt</td>

   <td width="243">in10Valid.txt</td>

  </tr>

  <tr>

   <td width="203">java Hw01 in10k-m5000.txt</td>

   <td width="243">in10k-m5000Valid.txt</td>

  </tr>

  <tr>

   <td width="203">java Hw01 in1m-m1000.txt</td>

   <td width="243">in1m-m1000Valid.txt</td>

  </tr>

 </tbody>

</table>

Table 2: Commands with input file