Download Link: https://assignmentchef.com/product/solved-comp201-assignment-2-movie-review-sentiment-analysis
<br>
5/5 - (1 vote)

Movie Review Sentiment Analysis

Sentiment Analysis is a Big Data problem which seeks to determine the general attitude of a writer given some text they have written. For instance, we would like to have a program that could look at the text “The film was a breath of fresh air” and realize that it was a positive statement while “It made me want to poke out my eye balls” is negative.

The problem that we’ll solve in this assignment is about calculating or analyzing sentiments of the critics by their reviews about the movie. You are going to search through a file containing movie reviews from the Rotten Tomatoes website which have both a numeric score as well as text. You’ll use this to learn which words are positive and which are negative. The data file looks like this:

Note that each review starts with a number 0 through 4 with the following meaning:

<ul>

 <li>  0 : negative</li>

 <li>  1 : somewhat negative</li>

 <li>  2 : neutral</li>

 <li>  3 : somewhat positive</li>

 <li>  4 : positive</li>

</ul>

Please read the following sections from your textbook in order to do this assignment easily:

<ul>

 <li>  Chapter 7: Input and Output from The C Programming Language by Kernighan andRitchie</li>

 <li>  C Strings from Essential CTask 0: Setting up the environment</li>

</ul>

<ol>

 <li>Accept the assignment from the following link https://classroom.github.com/a/qEj84RHr</li>

 <li>Create a file main.c using “touch” command.</li>

 <li>Import libraries such as  </li>

 <li>Use editor to edit this file and make a main() function.</li>

 <li>Write a program to read a text file.</li>

</ol>

Task 1: Average review based on a word (40 points)

You will ask the user to enter a word, and then you will search every movie review for that word. If you find it, add the score for that review to the word’s running score total (i.e., an accumulator variable). You also will need to keep track of how many appearances the word made so that you can report the average score of reviews containing that word back to the user.

Some sample runs of the program might look like this:

(Hint: you can use strstr() functions to find the substring in a given string.)

if (strstr(string, substring) != NULL) checks if the substring is present in the string or not. However, if the word is “impractical” and you search for “practical”, this function strstr() will return the index of “(im)practical”.

 So it will be a good idea to first split the strings into smaller strings using “ ” (space) as the delimiter. Then you can look for the entire word. You can also use any other approach to solve this issue.

<pre>#include &lt;stdio.h&gt;</pre>

<pre>#include &lt;string.h&gt;</pre>

<pre>#include &lt;math.h&gt;</pre>

<ul>

 <li>  Use int datatype to count the frequency as well as score of the given word.</li>

 <li>  Display the average score up to 4 decimal places. i.e. display 1.9502156450 as 1.9502Task 2: Max occurring word in positive and negative reviews (55 points)</li>

</ul>

<ol>

 <li>For this part of the assignment, you need to open wordList.txt. This file contains some words that are frequently found in the movie reviews. You can open two files simultaneous just create two distinct instances.</li>

 <li>For each word in wordList file count the number of instances it occurred in Positive reviews and number of instances in occurred in negative reviews. Save these values in 2 arrays (one for positive reviews and negative reviews each).</li>

 <li>Find maximum of these two arrays to find the most occurring word in positive reviews and most occurring word in negative reviews.</li>

 <li>Print these two numbers.</li>

</ol>

Note: Consider 2 – neutral as a negative review.

Oral Assessment

Important Note: We use automated plagiarism detection to compare your assignment submission with others and also the code repositories on GitHub and similar sites. Moreover, we plan to ask randomly selected 10% of students to explain their code verbally after the assignments are graded. And one may lose full credit if he or she fails from this oral part.

How to Read a file

You should follow the following steps to successfully read the file:

<ol>

 <li>First, open the text file using the fopen() function.</li>

 <li>Then, use the function fgets() to read text from the stream and store it as a string. Thenewline or EOF character makes the fgets() function stop reading so you can check thenewline or EOF file character to read the whole line.</li>

 <li>When you are done reading all the contents of the file, close the text file usingthe fclose() function.</li>

</ol>

<ul>

 <li> </li>

</ul>