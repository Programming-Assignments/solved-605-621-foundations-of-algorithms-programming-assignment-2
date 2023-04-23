Download Link: https://assignmentchef.com/product/solved-605-621-foundations-of-algorithms-programming-assignment-2
<br>
These programming problems are not collaborative assignments. You are required to follow the Programming Assignment Guidelines and the Pseudocode Restrictions (Blackboard page <a href="https://blackboard.jhu.edu/webapps/blackboard/content/listContentEditable.jsp?content_id=_7216507_1&amp;course_id=_197167_1&amp;mode=reset"><em>Syllabus &amp; Course Information</em></a> ) when

preparing your solutions to these problems.

For small input instances, <em>n</em>≤30, you may output your results to the command window. Larger input instances must be written to a file. In either case, you may need to produce an output file for trace runs or asymptotic performance analysis.

<ol>

 <li><strong><em>Programming (non-collaborative)</em></strong>: You are consulting for a group of people (who would prefer not to be mentioned here by name) whose job consists of monitoring and analyzing electronic signals coming from ships in the Atlantic ocean. They want a fast algorithm for a basic primitive that arises frequently: “untangling” a superposition of two <strong>known signals</strong>.</li>

</ol>

Specifically, they are picturing a situation in which each of two ships is emitting a short sequence of 0s and 1s over and over, and they want to make sure that the signal they are receiving is simply an <em>interweaving </em>of these two emissions, with nothing extra added in. The short sequence emitted by each ship is known to the ship and to you, the receiver.

Given a string <em>x </em>consisting of 0s and 1s, we write <em>x<sup>k </sup></em>to denote <em>k </em>copies of <em>x </em>concatenated together. We say that string <em>x</em><sup>0 </sup>is a <em>repetition </em>of <em>x </em>if it is a prefix of <em>x<sup>k </sup></em>for some number <em>k</em>. So, <em>x</em><sup>0 </sup>=101101101 is a repetition of <em>x</em>=101.

We say that a string <em>s </em>is an <em>interweaving </em>of <em>x </em>and <em>y </em>if its symbols can be partitioned into two (not necessarily contiguous) subsequence <em>s</em><sup>0 </sup>and <em>s</em><sup>00 </sup>so that <em>s</em><sup>0 </sup>is a repetition of <em>x </em>and <em>s</em><sup>00 </sup>is a repetition of <em>y</em>. Each symbol in <em>s </em>must belong to exactly one of <em>s</em><sup>0 </sup>of <em>s</em><sup>00</sup>. For example, if <em>x </em>= 101 and <em>y </em>= 0, then <em>s </em>= 100010101 is an <em>interweaving </em>of <em>x </em>and <em>y </em>since characters 1,2,5,7,8, and 9 form 101101 – a repetition of <em>x </em>– and the remaining characters 3,4,6 form 000 – a repetition of <em>y</em>. In terms of our application, <em>x </em>and <em>y </em>are the repeating sequences from the two ships, and <em>s </em>is the signal we are receiving. We want to make sure <em>s </em>“unravels” into simple repetitions of <em>x </em>and <em>y</em>.

You want a ”fast algorithm for …’untangling’ a superposition of two known signals”, <em>x </em>and <em>y</em>. You receive some set of symbols <em>s</em>. You do not know if the signal you receive has its first symbol in <em>x</em>, <em>y</em>, or a symbol that is extra and added in. You need to use your knowledge of <em>x </em>and <em>y </em>and the received signal <em>s </em>to determine if <em>s </em>consists only of valid <em>interwoven </em>symbols from <em>x </em>and <em>y</em>. That may require your solution to discard some symbols at the beginning or end of <em>s </em>to get to at least a full match of <em>x </em>and a full match of <em>y</em>. The received signal could be too short to do this. <strong>If you can’t determine that the signal is an <em>interweaving </em>of </strong><em>x </em><strong>and </strong><em>y</em><strong>, either because </strong><em>s </em><strong>is not long enough to do so or because </strong><em>s </em><strong>contains symbols not in </strong><em>x </em><strong>or </strong><em>y </em><strong>then you cannot decide that </strong><em>s </em><strong>is an <em>interweaving </em>of </strong><em>x </em><strong>and </strong><em>y</em><strong>.</strong>

<ul>

 <li>[50 points] Give an efficient algorithm that takes strings <em>s</em>, <em>x</em>, and <em>y </em>and decides if <em>s </em>is an <em>interweaving </em>of <em>x </em>and <em>y</em>. Derive the computational complexity of your algorithm.</li>

 <li>[50 points] Implement your algorithm and test its run time to verify your complexity analysis. Remember that CPU time is not a valid measure for testing run time. You must use something such as the number of comparisons.</li>

</ul>

1