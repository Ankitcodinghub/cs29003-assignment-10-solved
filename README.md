# cs29003-assignment-10-solved
**TO GET THIS SOLUTION VISIT:** [CS29003 Assignment 10 Solved](https://www.ankitcodinghub.com/product/cs29003-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;114551&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS29003 Assignment 10  Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
CS29003 ALGORITHMS LABORATORY

ASSIGNMENT 10

Important Instructions

1. List of Input Files: input.txt

2. Output Files to be submitted: ROLLNO A10 P1.c/.cpp, ROLLNO A10 P2.c/.cpp

3. Files must be read using file handling APIs of C/C++. Reading through input redirection isn’t allowed.

4. You are to stick to the file input output formats strictly as per the instructions.

5. Submission through .zip files are not allowed.

6. Write your name and roll number at the beginning of your program.

7. Do not use any global variable unless you are explicitly instructed so.

8. Use proper indentation in your code.

10. There will be part marking.

Hashing

Problem Statement

By the end of each day, the company X needs to determine the set of distinct portfolios associated to trades that are still active by then, that is, the portfolios of trades that have not been canceled during the day. You are required to find an efficient solution to this using Hashing and print the hashtables.

NOTE:

1. The hashing function is a simple mod function (K%size), where K is the input key and size is the size of hash table (aka hash map).

+ 101 26

+ 2 25

– 101

+ 3005 26

– 2

Table 1: Sample log file.

2. Collisions will be handled by separate chaining.

3. Use the following definition to define the hash:

typedef struct _hashing { int key; struct _hashing *next;

} hash;

Part 1: Two mirroring hash maps

The file is traversed top-down. Each line with a “+” sign, be it “+ Y P”, triggers two updates in our data structure: the first is the inclusion of Y in the list of counterparties associated with portfolio P in the counterparties-by-portfolio hash map (the key P will be inserted for the first time if it is not already there); the second change is the inclusion of P in the list of portfolios associated with counterparty Y in the portfolios-by-counterparty hash map (the key Y will be first inserted for the first time if it is not already there).

(a) counterparties-by-portfolio map (b) portfolios-by-counterparty map

Figure 1: Two mirroring hash maps. Collision handling is done using seperate chaining.

(a) counterparties-by-portfolio map (b) portfolios-by-counterparty map

Figure 2: Hash map multi level example

Part 2 : Multi Level Hashing

To implement the hash set, you can re-use the hash map data structure. Here, you will only need to maintain the key values.

Sample Input File

FILE: input-part1.txt

7

9

+ 55 23

+ 45 56

+ 78 67

+ 55 78

– 45

+ 56 23

+ 45 67

+ 78 679

– 78

The first line contains the size of the hash map. The second line contains the number of test cases T.

Each of the next T lines contains ‘+’ sign with two integers Y and P, or a ‘-’ sign with single integer Y.

Sample Output File

FILE: output-part1.txt

p 0 -1 -1 p 1 78 55 p 2 23 56 p 2 23 55 p 3 -1 -1 p 4 67 45 p 5 -1 -1 p 6 -1 -1 c 0 56 23 c 1 -1 -1 c 2 -1 -1 c 3 45 67 c 4 -1 -1 c 5 -1 -1

c 6 55 78 c 6 55 23

Each of the lines in output file should contain the four parts. First, ‘p/c’ to denote if the hash map being printed is counterparties-by-portfolio (p) or portfolios-by-counter-party (c). Second will be the index position in the hash map. Third will be the key. If the key is empty, print ‘-1’. Fourth will be the values present in that key (list/ hash set). If multiple values are present for a key, print them in the order present. If no value is present, print ‘-1’.

Make sure to read from a file named “input.txt”. Create a sample input file like the one shown above to test your code. At the time of evaluation, the input data might be different from the one given here.

You need not to submit “output.txt”, but your code should write the output in the given format in a file named “output.txt”
