Download Link: https://assignmentchef.com/product/solved-cse100-lab-6-hash-table-with-chaining
<br>
<h1>Hash Table with Chaining</h1>

<strong>Description </strong>In this assignment you are requested to implement a hash table that handles collisions by chaining. You have to use linked lists, either from the Standard Template Library (STL) (recommended) or by implementing your own. For usage of STL, refer – for instance – to http://www.cppreference.com/wiki.

You need to implement the insert, search and delete operations. The keys are integers (C++ int type) and you can assume that all keys are non-negative. The first number in the input will be the size <em>m </em>of the chained hash table. You will use the simple hash function <em>h</em>(<em>k</em>) = <em>k </em>mod <em>m</em>. Then lines will follow starting with ‘i’, ‘s’, ‘d’,‘o’, or ‘e’. The details are as follows:

<ul>

 <li>Use the hash function <em>h</em>(<em>k</em>) = <em>k </em>mod <em>m</em>.</li>

 <li>i(key): Insert (key) into the table. For example, “i2” implies “Insert key 2 into the table.” For collisions, insert the colliding key at the <em>beginning </em>of the linked list. You just need to insert the key and don’t have to output anything in this case.</li>

 <li>d(key): delete (key) from the table. For example, d2 implies “Delete key 2 from the table.” If there are multiple elements of the same key value, delete the element of the key value that appears the earliest in the list. If the delete was successful, you have to output</li>

</ul>

(key):DELETED;

If not (since there was no element with the key value), output

(key):DELETE_FAILED;

<ul>

 <li>s(key): search (key) in the table. If there is an element with the key value, then you have to output</li>

</ul>

(key):FOUND_ATi,j;

where <em>i </em>is the hash table index and <em>j </em>is the linked list index. If there are multiple elements with the same key value, choose the first one appearing in the linked list. If you couldn’t find the key, then output

(key):NOT_FOUND;

<ul>

 <li>o: output the table. Output the entire hash table. Each line should begin with the slot/hash table index followed by key values in the linked list. For example, if <em>m </em>= 3 and we inserted 3, 6, and 1 into an empty table in this order, then you should output</li>

</ul>

0:6-&gt;3-&gt;;

1:1-&gt;;

2:;

<ul>

 <li>e: finish your program.</li>

</ul>

<strong>Example of input and output</strong>

The following example shows an execution of the program in interactive mode. See the input files and output files under the testfiles folder for examples where input and output are separated.

2 i4 i2 i6 i3 o

0:6-&gt;2-&gt;4-&gt;; 1:3-&gt;; s2

2:FOUND_AT0,1; s4

4:FOUND_AT0,2; d5

5:DELETE_FAILED; d2 2:DELETED; o 0:6-&gt;4-&gt;; 1:3-&gt;; e

See the lab guidelines for submission/grading, etc., which can be found in Files/Labs.