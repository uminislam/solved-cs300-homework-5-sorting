Download Link: https://assignmentchef.com/product/solved-cs300-homework-5-sorting
<br>
In this homework, you have a PhoneBook that you kept updating without caring about sorting it <strong>alphabetically</strong>,​ and since you are a CS student, you care about the time taken to sort the PhoneBook so you want the <strong>fastest</strong>​<strong> algorithm</strong> to perform this operation and the<strong> fastest search structure</strong>.​ Therefore, you must compare <strong>4</strong>​ Sorting​ algorithms and conclude which one is faster then perform search operation as you did in HW2.

You will be implementing the PhoneBook as you did already in the 2<sup>nd</sup>​ homework, in addition to using <strong>vectors</strong>​ to​ store the list of contacts in it loaded from the input file. You should load the PhoneBook in 4 different vectors then perform <strong>comparison</strong>​ between them (in terms of running times).

The sorting algorithms:

<ul>

 <li>Insertion Sort</li>

 <li>Quick Sort (pivot = [median])</li>

 <li>Merge Sort (in place; without using auxiliary memory storage) ● Heap Sort</li>

</ul>




Please note that after sorting the vectors, you should conduct a <strong>binary</strong>​<strong> search</strong> about a contact or list of contacts on the sorted vector and compare the running times with those of the BST and AVL tree.




<h1><strong>Program Flow </strong></h1>




First, you have to read the input file and load the PhoneBook into vectors where you are going to apply a sorting algorithm on each one. In order to insert a contact, you need to insert its information into a data structure of your definition. There are 2 types of search that should be valid in your implementation, Partial and Full name search (similar to HW2).




After loading the PhoneBook into each vector copy, your program should ask for a search query (Partial or Full), then all 4 vectors should be sorted according to the sorting algorithms listed above.

Concerning the search operation, it should be performed on each PhoneBook copy (BST, AVL tree and sorted vector) so we can make comparisons between the search running times on each data structure.




For the comparisons, you should measure the running time without printing anything to the screen then display it for each structure.

You are also required to calculate the speedups between algorithms, the equation for calculating the speedup is given below.




<h1>Speedup<sub>i </sub>= <u>S</u>F<u>l</u>a<u>o</u>s<u>w</u>te<u>e</u>r<u>r</u> <u> </u>S<u>S</u>A<u>A</u> <u> </u>e<u>e</u>x<u>x</u>e<u>e</u>c<u>c</u> <u> </u>t<u>t</u>i<u>i</u>m<u>m</u>e<u>e</u></h1>

<strong><em>SA: Sorting Algorithm</em></strong>




The same formula applies when comparing between AVL tree, BST and the vector search times:




<h1> Speedup<sub>i </sub>= <u>S</u>F<u>l</u>a<u>o</u>s<u>w</u>te<u>e</u>r<u>r</u> <u> </u>S<u>S</u>e<u>e</u>a<u>a</u>r<u>r</u>c<u>c</u>h<u>h</u> <u> </u>e<u>e</u>x<u>x</u>e<u>e</u>c<u>c</u> <u> </u>t<u>t</u>i<u>i</u>m<u>m</u>e<u>e</u> <sub> </sub></h1>




<h2>Input</h2>

First, your program should ask for an input file (PhoneBook file) then it asks for a query entry where you should enter a full/partial contact name in one line.




<h2>Output</h2>

After inserting the inputs, you should first display the sorting times, second, the search times for AVL, BST and the vector, and last, the speedups list (check the sample runs to have a more clear image).

After getting the execution times, you will be able to compute the speedups and also display them.

<strong> </strong>

<h3>Important notes</h3>




<ul>

 <li>Even though you are not asked to print out the results to the screen, your search functions should return correct results, this will be tested during the grading process.</li>

 <li>Your classes should be <strong>template-based</strong>​ .​</li>

 <li><strong>Note:</strong> The previous sample runs were taken from a machine with the following specifications:

  <ul>

   <li>CPU: Intel(R) Core(TM) i5-8250U CPU @ 1.60GHz (4 cores – 8 threads) ● RAM: 4GiB</li>

  </ul></li>

</ul>

Therefore, we understand that you have different machines, it can be powerful or weak in terms of specifications, so, we don’t expect the speedup ratios to be exactly the same as in the sample runs, however, the results should be reasonable and conform with the results correctness, for example:

<ul>

 <li>In <strong>sample</strong>​<strong> run 6</strong>,​ the speedup ratio (Insertion Sort / Quick Sort) is so high (119.058) so we will accept lower ratios like 30 or 20 or even 10. However, ratios beneath 5 would be suspicious and ratios like 0.9 or less (less than 1) are not acceptable and it shows that the code is problematic somehow.</li>

</ul>

<strong> </strong>

<h2>Sample runs</h2>

<strong> </strong>

<h3>Sample Run 1</h3>

<strong> </strong>

Please enter the contact file name:

PhoneBook-sample2.txt Please enter the word to be queried :

Shane




Sorting the vector copies

======================================

Quick Sort Time: 267392 Nanoseconds

Insertion Sort Time: 1485445 Nanoseconds

Merge Sort Time: 1375031 Nanoseconds

Heap Sort Time: 518291 Nanoseconds




Searching for Shane

======================================

The search in BST took 20098 Nanoseconds

The search in AVL took 9647 Nanoseconds

Binary Search Time: 16210 Nanoseconds




SpeedUps in search

======================================

(BST / AVL) SpeedUp  = 2.08334

(Binary Search / AVL) SpeedUp  = 1.68032

(Binary Search / BST) SpeedUp  = 0.806548




SpeedUps between Sorting Algorithms

======================================

(Insertion Sort/ Quick Sort) SpeedUp = 5.55531

(Merge Sort / Quick Sort) SpeedUp = 5.14238

(Heap Sort / Quick Sort) SpeedUp = 1.93832

<h3>Sample Run 2</h3>

<strong> </strong>




Char




Sorting the vector copies

======================================

Quick Sort Time: 26376 Nanoseconds

Insertion Sort Time: 44829 Nanoseconds

Merge Sort Time: 42555 Nanoseconds

Heap Sort Time: 41510 Nanoseconds




Searching for Char

====================

The search in BST took 4635 Nanoseconds

The search in AVL took 5161 Nanoseconds

Binary Search Time: 10613 Nanoseconds




SpeedUps in search

======================================

(BST / AVL) SpeedUp  = 0.898082

(Binary Search / AVL) SpeedUp  = 2.05638

(Binary Search / BST) SpeedUp  = 2.28975




SpeedUps between Sorting Algorithms

======================================

(Insertion Sort/ Quick Sort) SpeedUp = 1.69961

(Merge Sort / Quick Sort) SpeedUp = 1.6134

(Heap Sort / Quick Sort) SpeedUp = 1.57378




























<h3>Sample Run 3</h3>

Tina Gulko




Sorting the vector copies

======================================

Quick Sort Time: 93656 Nanoseconds

Insertion Sort Time: 512859 Nanoseconds

Merge Sort Time: 489748 Nanoseconds

Heap Sort Time: 202962 Nanoseconds




Searching for Tina

====================

The search in BST took 1260 Nanoseconds

The search in AVL took 1193 Nanoseconds

Binary Search Time: 3889 Nanoseconds




SpeedUps in search

======================================

(BST / AVL) SpeedUp  = 1.05616

(Binary Search / AVL) SpeedUp  = 3.25985

(Binary Search / BST) SpeedUp  = 3.08651




SpeedUps between Sorting Algorithms

======================================

(Insertion Sort/ Quick Sort) SpeedUp = 5.47599

(Merge Sort / Quick Sort) SpeedUp = 5.22922

(Heap Sort / Quick Sort) SpeedUp = 2.1671




























<h3>Sample Run 4</h3>

Gulsen Demiroz




Sorting the vector copies

======================================

Quick Sort Time: 135189 Nano secs

Insertion Sort Time: 435134 Nano secs

Merge Sort Time: 449873 Nano secs

Heap Sort Time: 235754 Nano secs




Searching for Gulsen

====================

The search in BST took 2665 Nanoseconds

The search in AVL took 2730 Nanoseconds

Binary Search Time: 9550 Nanoseconds




SpeedUps in search

======================================

(BST / AVL) SpeedUp  = 0.97619

(Binary Search / AVL) SpeedUp  = 3.49817

(Binary Search / BST) SpeedUp  = 3.58349




SpeedUps between Sorting Algorithms

======================================

(Insertion Sort/ Quick Sort) SpeedUp = 3.21871

(Merge Sort / Quick Sort) SpeedUp = 3.32773

(Heap Sort / Quick Sort) SpeedUp = 1.74388

























<h3>Sample Run 5</h3>




PhoneBook-shuffled.txt Please enter the word to be queried :

Virg




Sorting the vector copies

======================================

Quick Sort Time: 10056248 Nanoseconds

Insertion Sort Time: 1186275960 Nanoseconds

Merge Sort Time: 981504897 Nanoseconds

Heap Sort Time: 18064775 Nanoseconds




Searching for Virg

======================================

The search in BST took 26106 Nanoseconds

The search in AVL took 7118 Nanoseconds

Binary Search Time: 8562 Nanoseconds




SpeedUps in search

======================================

(BST / AVL) SpeedUp  = 3.6676

(Binary Search / AVL) SpeedUp  = 1.20287

(Binary Search / BST) SpeedUp  = 0.327971




SpeedUps between Sorting Algorithms

======================================

(Insertion Sort/ Quick Sort) SpeedUp = 117.964

(Merge Sort / Quick Sort) SpeedUp = 97.6015

(Heap Sort / Quick Sort) SpeedUp = 1.79637




<strong> </strong>

<strong> </strong>

<strong> </strong>
















<h3>Sample run 6</h3>

PhoneBook-shuffled.txt Please enter the word to be queried :

James




Sorting the vector copies

======================================

Quick Sort Time: 9994504 Nanoseconds

Insertion Sort Time: 1189930420 Nanoseconds

Merge Sort Time: 983665907 Nanosecond

Heap Sort Time: 17199362 Nanoseconds




Searching for James

======================================

The search in BST took 132991 Nanoseconds

The search in AVL took 38027 Nanoseconds

Binary Search Time: 10237 Nanoseconds




SpeedUps in search

======================================

(BST / AVL) SpeedUp  = 3.49728

(Binary Search / AVL) SpeedUp  = 0.269203

(Binary Search / BST) SpeedUp  = 0.0769751




SpeedUps between Sorting Algorithms

======================================

(Insertion Sort/ Quick Sort) SpeedUp = 119.058

(Merge Sort / Quick Sort) SpeedUp = 98.4207

(Heap Sort / Quick Sort) SpeedUp = 1.72088


























