Download Link: https://assignmentchef.com/product/solved-cmsc204-assignment-4
<br>
A <strong>concordance</strong> is an alphabetical list of the principal words used in a book or body of work, listing every instance of each word with its immediate context. Only works of special importance have had concordances prepared for them, such as the Bible, Qur’an, the works of Shakespeare, or classical Latin and Greek authors, because of the time, difficulty, and expense involved in creating a concordance in the pre-computer era.




The first Bible concordance was compiled for the Vulgate Bible by Hugh of St Cher (d.1262), who employed 500 monks to assist him.




The reconstruction of the text of some of the Dead Sea Scrolls involved a concordance.







<strong> </strong>

<strong> </strong>




Write a program that creates a concordance from some text. It will list all the words in alphabetic order followed by a list of line numbers where the word can be found in the text.

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>




Hash Table,

Link List,

hash code, buckets/chaining,

exception handling,

<table>

 <tbody>

  <tr>

   <td width="749">

    <table width="100%">

     <tbody>

      <tr>

       <td><strong>Classes</strong></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

read/write files using FileChooser













<strong>Data Element – </strong>ConcordanceDataElement,

ConcordanceDataElement implements Comparable&lt;ConcordanceDataElement&gt; and consists of a String (the word) and a reference to a LinkedList&lt;Integer&gt; (list of line numbers where word occurs).  Follow the Javadoc provided for you.




<strong>Data Structure – </strong>ConcordanceDataStructure,

Implements the ConcordanceDataStructureInterface Interface that is provided.

You will be implementing a hash table with buckets.  It will be an array of linked list of ConcordanceDataElements.  The add method will take a word and a line number to be added to the data structure. If the word already exists, the line number will be added to the linked list for this word.  If the line number for the word already exists, don’t add it again to the linked list. (i.e. if Sarah was on line 5 twice, the first line 5 would be added to the linked list for Sarah, the second one would not). If the word doesn’t exist, create a ConcordanceDataElement and add it to the HashTable. Two constructors will be required, one that takes in an integer that is the estimated number of words in the text, the other is used for testing purposes.  Look at the provided Javadoc.




<strong>Data Manager – </strong>ConcordanceDataManager

Implements the ConcordanceDataManagerInterface interface that is provided.

The data manager allows the user to create a concordance file or a concordance list (ArrayList of strings). The input is read (from a file or string) and is added to the data structure through the add method.  The add method requires a word and a line number. The line number is incremented every time a newline appears in the file or the string.  Change all words to lowercase so that Now and now are considered the same word.




<strong>Exception Classes</strong>

IOException – created and thrown when user selects an input file that cannot be read (check out the methods of File).




<strong>GUI Driver</strong>

<ul>

 <li>Do not allow the user to create a concordance file until they have entered an input file and an output file</li>

 <li>Show the text area only when the option to create from text is chosen.</li>

 <li>Use a FileChooser for the user to select the input and output files. Use a filter so that user can only select .txt files.</li>

 <li>Inform the user if there is an error with the input file or the output file</li>

 <li>Use exception handling for the validity of the files.</li>

 <li>If creating a concordance from text, make sure the user has entered some text in the text area. Inform user if text area is empty.</li>

 <li>Display the concordance from the text in the text area.</li>

 <li>Provide a way for the user to “clear” the text area.</li>

</ul>




<strong>Testing</strong>

<ol>

 <li>Create a JUnit Test – ConcordanceDataManagerTest_STUDENT. Test all the methods of the ConcordanceDataManager with a different set of data than the ConcordanceDataManagerTest provided for you.</li>

 <li>Create a JUnit Test – ConcordanceDataStructureTest_STUDENT. Test all the methods of the ConcordanceDataStructure with a different set of data than the ConcordanceDataStructureTest provided for you.</li>

</ol>



















There will be two ways to create a concordance.  The first requires a document to be read from an input file, and the concordance data is written to an output file.  The second reads the input from a string and returns an ArrayList of strings that represent the concordance of the string.

Because they are so common, <strong>don’t include the words “the” or “and” </strong>in your concordance. Also, <strong>do not include words that have length less than 3</strong>.  <strong>Strip out all punctuation, except apostrophes that occur in the middle of a word, i.e. let’s, we’d, etc.</strong>

























Example of creating a Concordance from an input file













Select an input file and an output file.  PrideAndPrejudice.txt was used.

Sample of output file:




Example of Creating a Concordance from text:













Using “Create Concordance” button displays Concordance in text area



















<strong><u>Deliverables / Submissions</u></strong><strong>: </strong>

Design: UML class diagram with algorithm (pseudo-code) for methods

Implementation: Submit a compressed file containing the follow (see below):  The Java application (it must compile and run correctly); Javadoc files in a directory; a write-up as specified below.  Be sure to review the provided project rubric to understand project expectations.  The write-up will include:

<ul>

 <li>UML diagram</li>

 <li>In three or more paragraphs, highlights of your learning experience</li>

</ul>




<strong><u>Deliverable format</u>:</strong> The above deliverables will be packaged as follows. Two compressed files in the following formats:

<ul>

 <li>zip, a compressed file in the zip format, with the following:

  <ul>

   <li>Write up (Word document) – reflection paragraphs</li>

   <li>UML Diagram – latest version (Word or jpg document)</li>

   <li>doc (directory) – Javadoc</li>

  </ul></li>

</ul>

<ul>

 <li style="list-style-type: none;">

  <ul>

   <li style="list-style-type: none;">

    <ul>

     <li style="list-style-type: none;">

      <ul>

       <li>File1.html (example)</li>

       <li>File2.html (example)</li>

      </ul></li>

    </ul></li>

  </ul></li>

</ul>

<ul>

 <li>src (directory)</li>

</ul>

<ul>

 <li style="list-style-type: none;">

  <ul>

   <li style="list-style-type: none;">

    <ul>

     <li style="list-style-type: none;">

      <ul>

       <li>File1.java (example)</li>

       <li>File2.java (example)</li>

      </ul></li>

    </ul></li>

  </ul></li>

</ul>




<ul>

 <li>zip, a compressed file containing one or more Java files:

  <ul>

   <li>java (example)</li>

   <li>java (example)</li>

  </ul></li>

</ul>

This folder should contain Java source files only











