Download Link: https://assignmentchef.com/product/solved-cs1027-lab3
<br>
<ul>

 <li>Hand-trace a program to anticipate the flow of execution</li>

 <li>Analyze the effects of try-catch statements on the overall program execution</li>

 <li>Locate the source of errors using the messages displayed in the console</li>

 <li>Use the Debugger Tool in Eclipse to step through code and track variable values to understand the reason for such errors</li>

 <li>Fix the errors that have been found in the code to make it run as expected</li>

</ul>

<h1>Pre-Lab</h1>

<ul>

 <li>Create a new Java project called Lab3</li>

 <li>Download the files: <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/Exceptions.java">java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/Exceptions.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/DebuggingExercise1.java">DebuggingExercise1.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/DebuggingExercise1.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/DebuggingExercise2.java">DebuggingExercise2.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/DebuggingExercise2.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/DebuggingExercise3.java">DebuggingExercise3.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/DebuggingExercise3.java">,</a> and <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/MyObject.java">MyObject.java</a>  Save these downloaded files into the Lab3 src folder</li>

</ul>




<h1>Exercise 1 – Follow the exception handling execution</h1>




<ol>

 <li>Open the Exceptions.java file in Eclipse. Do not run it yet.</li>

 <li>Examine the code to think about the flow of execution.</li>

 <li>Jot down what you think the program would output to the console from each of the 3 cases (the calls to method1() from the main method).</li>

 <li>Once you have finished hand-tracing the program, run it to see the actual output.</li>

 <li>Were you correct? If not, read through the code again to understand why it executed this way.</li>

 <li>Now comment out Line 10 (P[x] = 5) and un-comment Line 11 (method2(P, x)).</li>

 <li>Read the code within method2() and hand-trace the execution on paper with this small change in the code.</li>

 <li>Once you have thought about the expected output, run the program to see the actual output.</li>

 <li>Were you correct? If not, read through the code again to understand why it executed this way.</li>

</ol>




<h1>Exercise 2 – Using the Debugging Tool</h1>




<ol>

 <li>Open DebuggingExercise1.java and run it. You will see that it compiles but it crashes when you run it. Read the error message and try to understand it. It will give you some information that may help you find the source of the error.</li>

 <li>Check that you have a Debug button in the top right corner of your Eclipse window (a button with a little green bug in it), beside the Java button. If you don’t, select Window &gt; Perspective &gt; Open Perspective &gt; Debug.</li>

 <li>Click on the Debug button to change to the Debug view. You can, at any time, switch back to the Java view by clicking on the Java button in the top right corner (the button with the blue letter J located to the left of the debug button).</li>

 <li>In the window displaying your code, add a breakpoint to the line for (int j=1; j&lt;=6; j++). You do this by right-clicking in this line at the very left, and then clicking Toggle Breakpoint. You can remove a breakpoint at any time in the exact same way. 5. When executing your program, the debugger will stop every time this line is reached. Run your program in the debug mode by selecting on Run &gt; Debug (alternatively, press the key F11).</li>

 <li>You will see that the line for (int j=1; j&lt;=6; j++) is highlighted in green. The execution of the program has stopped at this point. In the Variables window (upper right corner) you will see the variables of the program: args, testArray, and i and their values. Since testArray is a variable referencing a 2-dimensional array, or an array in which every entry is an array of integers, when you click on the “&gt;” symbol to its left, the debugger shows 5 new variables ([0], [1], [2], [3], and [4]), each one of them references an array of length 6; these are the rows of the 2-dimensional array. If you click on the “&gt;” symbol to the left of [0], six new variables will be shown; these are the columns of the first row of the two dimensional matrix.</li>

 <li>Now you can use F5 to execute your program one instruction at a time (this is called single-stepping). Press F5 once. Note how the variables i and j, and the values stored in the 2-dimensional array are changing in the Variables window. Why did testArray[0][0] not change?</li>

 <li>Keep pressing F5 and stop when the value of testArray[0][5] changes value from 0 to 5 and the statement for (int j=1; j&lt;=6; j++) is highlighted in green. Push key F5 one more time. What are the values of i and j? Is it correct that the program tries to store the value (i+1)*j in testArray[i][j]?</li>

 <li>After answering the previous questions, you should know what is wrong with the program. Fix the error. Run the program and make it sure that it does not crash; it should print 30 values.</li>

 <li>Modify the code so all entries of testArray are properly initialized. The first row of testArray should store the values: 1, 2, 3, 4, 5, 6; the second row should store the values: 2, 4, 6, 8, 10, 12; the third row: 3, 6, 9, 12, 15, 18; the fourth row: 4, 8, 12, 16, 20, 24, and the last row: 5, 10, 15, 20, 25, 30.</li>

</ol>




<h1>Exercise 3 – Using the Debugging Tool</h1>




<ol>

 <li>For this and the following exercises you CANNOT add any print or println statements to the code that you are testing.</li>

 <li>Open DebuggingExercise2.java and run it. It will also crash.</li>

 <li>Add a breakpoint to the line i = process(2);</li>

 <li>Run the program in Debug mode.</li>

 <li>Keep pressing F5 until you reach the statement return result; (do not execute this statement yet).</li>

 <li>Using the debugger, find out the values of the variables: i, step, result, and load.</li>

 <li>Since load is a static variable, to see its value in the Variables window you need to click on the little inverted triangle in the upper right corner of the Variables window; this will bring two options: “Layout” and “Java”. Click on Java and then select “Show static variables” (see a <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/debugger_static.jpg">screenshot of this option</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab03/debugger_static.jpg">)</a>.</li>

 <li>Terminate the program by selecting Run &gt; Terminate.</li>

 <li>Run this program again and stop execution at statement i = process(2).</li>

 <li>This time press the key F6 instead of the key F5. You will see that the debugger now does not go inside method process(), but it goes directly to statement total = (i * 100) / load (key F5 tells the debugger to “step into” a method, while key F6 makes the debugger “step over” a method). What is the value of load? Why does the program crash if you keep pressing F6? (Do not press F5 or the debugger will try to step into the code of the Java’s virtual machine).</li>

 <li>Fix the program so that it does not crash and it prints the message “The value of total is infinity”. Change the statement i = process(2) to i = process(1) and run the program again; this time it must print “The value of total is 5”. (hint: check if load is 0 before computing total = (i * 100) / load).</li>

</ol>




<h1>Exercise 4 – Using the Debugging Tool</h1>




<ol>

 <li>Open DebuggingExercise3.java and run it. It will not compile.</li>

 <li>Which line causes the compilation error? Why does the compiler complain about this line even though i has been declared in the statement: for (int i = 1; i &lt; 2; ++i) (hint: what is the scope of i?)</li>

 <li>Fix the code by commenting out the line with the compilation error.</li>

 <li>Run the program; it should not produce any output.</li>

 <li>Study the code for this class and try to determine without running the program what the values for the variables var1 and obj1 are immediately after method2(obj1) is executed. Write down your answers. Now try to determine the values of the variables immediately after method1(var1) is executed. Write down your answers again.</li>

 <li>Now use the debugger to determine the actual values of the above variables. To see the string stored in obj1, in the Variables window click on the “&gt;” symbol to the left of obj1; you will see now the value of name.</li>

 <li>Were you correct? If not, study the code and try to understand why the variables have the values shown by the debugger.</li>

 <li>Add a breakpoint at the line if (obj1 == obj2). Press F11 to run the program in debugging mode and stop at this statement.</li>

 <li>Press F5. Why is the result of the comparison false even though both obj1 and obj2 contain the same information, namely “joe”?</li>

 <li>Look at the value of obj1 in the Variables window of the debugger. Since obj1 is a nonprimitive variable its value is the address of an object of the class MyObject. Note that the debugger does not show the actual address of the object referenced by obj1; instead it displays the address in a user-friendly format: MyObject (id = 19) —you might get a different value for id. This means that the address stored in obj1 is the address of an object of class MyObject and the debugger assigns it a unique internal identifier (in the above example the identifier is 19). If you were to print the value of obj1 with</li>

</ol>

System.out.println(obj1) you would get a similar output, not the actual address of the object but a string of the form <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="75380c3a171f101601354016161141461647">[email protected]</a>; the Java virtual machine will assign a different identifier to the object (5ccd43c2) than the debugger.


