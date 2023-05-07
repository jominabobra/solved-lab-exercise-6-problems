Download Link: https://assignmentchef.com/product/solved-lab-exercise-6-problems
<br>
<ol>

 <li>Write C++ programs</li>

 <li>Compile C++ programs</li>

 <li>Implement programs that use functions</li>

</ol>

<h1><a id="user-content-additional-reading" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06#additional-reading" aria-hidden="true"></a>Additional Reading</h1>

This lab exercise will require you to store function prototypes and implementations in separate files. Kindly go through <a href="https://github.com/ILXL-guides/function-file-organization">this tutorial</a> before starting the lab exercise.

<h1><a id="user-content-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06#instructions" aria-hidden="true"></a>Instructions</h1>

Answer the programming problems sequentially (i.e., answer prob01 before prob02). If you have questions let your instructor or the lab assistant know. You can also consult your classmates.

When you answer two programming problems correctly, let your instructor know and wait for further instruction.

<h1><a id="user-content-lab-exercise-guide" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06#lab-exercise-guide" aria-hidden="true"></a>Lab exercise guide</h1>

Here’s a link to the <a href="https://docs.google.com/document/d/1EX01EtrO-pkHNLVPxiq7HNh1f5KnJZnr_dlJcO4T7t0/edit?usp=sharing" rel="nofollow">Lab exercise guide</a> in case you need to review the lab exercise objectives, grading scheme, or evaluation process.




<h1>Military to Regular time</h1>

Create a function called <code>mil_to_reg</code> that converts time in the military time format into the regular format. For example, convert <code>2249</code> to <code>10:49 pm</code>.

The function should receive a single <code>unsigned short int</code> parameter that represents the military time. It should return a <code>std::string</code> that contains the regular time counterpart of the given military time.

Please see the sample output below to guide the design of your program.

<em>Note: Consider possible edge cases in user input to ensure your program works correctly.</em>

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob01#sample-output" aria-hidden="true"></a>Sample output:</h2>

<pre>Please enter the time in military time: <b>1433</b>The equivalent regular time is: 2:33 pm</pre>

Make sure that you write the <code>mil_to_reg</code> function prototype in <code>time.hpp</code> and its implementation in <code>time.cpp</code>, and call it from inside of <code>main.cpp</code>. You’ll find that skeleton code has already been provided and you simply need to call the function and include the necessary header files.

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob01#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob01#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code save in <code>time.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp time.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Header maker</h1>

Create a function called <code>display_header</code> that displays text surrounded by a rectangle composed of asterisks. The function receives a <code>std::string</code> text as input and does not return anything as an output, but displays the header. For example, given the text <code>Hello World</code>, the function should display this on screen:

<pre><code>***************** Hello World! *****************</code></pre>

Create another function called <code>within_width</code> that helps make sure that the header does not exceed the width of the screen. The function accepts two parameters: a <code>std::string</code> text that is the text input used for displaying the header, and an <code>unsigned short int</code> which is the maximum width of the screen. Typically, this is 80 characters, but this parameter makes it more flexible for the user. The function returns a <code>bool</code> value indicating whether the text will fit on the screen or not.

<em>Note: Make sure you account for the added <code>*</code> and <code></code>when the header is created. The function should return true if the length of the text together with the <code>*</code> and <code></code>fit within the width.</em>

A very important member function you will need to use is the <code>std::string</code> object’s <code>length</code> function. This will allow you to get the length of the string that you need for your function implementations. This is a good <a href="http://www.cplusplus.com/reference/string/string/length/" rel="nofollow">reference</a> for the member function. Don’t forget to include the <code>string</code> header.

Make sure that you write the <code>display_header</code> and <code>within_width</code> function prototypes in <code>header.hpp</code> and their implementations in <code>header.cpp</code>, and call them from inside of <code>main.cpp</code>. You’ll find that skeleton code has already been provided and you simply need to call the function and include the necessary header files.

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob02#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob02#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile codes saved in <code>header.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp header.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>




<h1>Power</h1>

Create the <code>power</code> function that computes the value of a base value raised to a power. The function should accept a <code>double</code> and an <code>int</code> parameter to represent the <code>base</code> and the <code>power</code> values, respectively. The function should return a <code>double</code> value after performing the operation.

<em>Hint: Be careful with your parameter names. If you use the same name for the function and parameters, the compiler won’t be able to distinguish between them. Your function’s name should be <code>power</code>, but you can use something else for the parameter names.</em>

<h2><a id="user-content-sample-inputoutput" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob03#sample-inputoutput" aria-hidden="true"></a>Sample input/output:</h2>

<pre>Please enter the base number: <b>5</b>Please enter the power: <b>3</b>5 ^ 3 = 125</pre>

<pre>Please enter the base number: <b>2.5</b>Please enter the power: <b>3</b>2.5 ^ 3 = 15.625</pre>

<pre>Please enter the base number: <b>4</b>Please enter the power: <b>-4</b>4 ^ -2 = 0.06</pre>

Make sure that you write the <code>power</code> function prototype in <code>power.hpp</code> and its implementation in <code>power.cpp</code>, and call them from inside of <code>main.cpp</code>. You’ll find that skeleton code has already been provided and you simply need to call the function and include the necessary header files.

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob03#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob03#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile codes saved in <code>power.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp power.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Draw Rectangle Function</h1>

Create the <code>draw_rectangle</code> function that draws a rectangle on the screen given the user-defined length and width. The function should accept two <code>unsigned short int</code> parameters. The first refers to the length, and the second refers to the width. The function should not return any value, but display the rectangle on the screen.

In cases when the user provides invalid length or width values (i.e., zero or negative values), your function should display an error message.

Take a look at the sample input/output below.

<h2><a id="user-content-sample-inputoutput" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob04#sample-inputoutput" aria-hidden="true"></a>Sample input/output:</h2>

<pre>Please enter the length: <b>2</b>Please enter the width: <b>2</b>****</pre>

<pre>Please enter the length: <b>3</b>Please enter the width: <b>5</b>***************</pre>

<pre>Please enter the length: <b>2</b>Please enter the width: <b>7</b>**************</pre>

<pre>Please enter the length: <b>-2</b>Please enter the width: <b>3</b>Invalid length and/or width values.</pre>

Make sure that you write the <code>draw_rectangle</code> function prototype in <code>rectangle.hpp</code> and its implementation in <code>rectangle.cpp</code>, and call them from inside of <code>main.cpp</code>. You’ll find that skeleton code has already been provided and you simply need to call the function and include the necessary header files.

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob04#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob04#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>main.cpp</code> and <code>rectangle.cpp</code> and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp rectangle.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Most significant digit</h1>

Make a program that utilizes functions and loops to determine the most significant digit of a given number

The function you make should be named: <code>most_significant_digit</code>

The parameters should be an <code>int</code> for the number you want to find the most significant digit of.

This function should return an <code>int</code>, the most significant digit.

Make sure that you write the <code>most_significant_digit</code> function prototype in <code>most_sig_digit.hpp</code> and its implementation in <code>most_sig_digit.cpp</code>, then and call it from inside of <code>main.cpp</code>. You’ll find that skeleton code has already been provided and you simply need to call the function.

<h2><a id="user-content-sample-inputoutput" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob05#sample-inputoutput" aria-hidden="true"></a>Sample input/output:</h2>

<pre>Please enter an integer, this program will produce it's more significant digit: <b>4582</b>The most significant digit is 4</pre>

<pre>Please enter an integer, this program will produce it's more significant digit: <b>0</b>The most significant digit is 0</pre>

<pre>Please enter an integer, this program will produce it's more significant digit: <b>-8382</b>The most significant digit is -8</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob05#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_06/prob05#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>main.cpp</code> and <code>most_sig_digit.cpp</code> and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp most_sig_digit.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<pre><code>make all</code></pre>