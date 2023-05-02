Download Link: https://assignmentchef.com/product/solved-comp-206-software-systems-mini-assignment-4
<br>
<span style="font-size: 2em;">Files and Pointers</span>

A CSV file, Comma Separated Vector, is a file format normally used to implement log files or simple database applications. It is a text file that uses the .csv file extension. Every row of the file is a series of fields separated by commas and terminating with a carrage return.  For example, we have a phone book of friends: Bob is 19 his number is 514-123-4567, and Mary is 20 her number is 450-345-7890.  This would be stored in the CSV file as:

Bob, 19, 514-123-4567

Mary, 20, 450-345-7890

The comma and the carrage return are reserved words and cannot be used in the file to mean anything else.  In CSV2, escape characters are used to overcome this limitation, but for this assignment we are not implmenting CSV2. It is optional to include a space after the comma.

A CSV record is one row of information. For example: Bob, 19, 514-123-4567 is a record. In this case, it is populated by three fields, deliniated by the comma and carrage return: field #1 is Bob, field #2 is 19, and field #3 is 514-123-4567.  It is standard to refer to the contents of a CSV file as records and fields.

Create a program that does the following:

<ul>

 <li>Ask for a name</li>

 <li>Ask for a replacement name</li>

 <li>Search for the record in the CSV file that belongs to name 1</li>

 <li>Load that record into an array of size 1000 characters</li>

 <li>Using pointers and no library functions and no array indexes, properly replace the name in the record with the replacement name</li>

 <li>Then write this updated record back into the CSV file replacing the old record 7) Program terminates</li>

</ul>

In the above, steps 1 – 2 are in the main function.

Steps 3 – 4 are in a function called void FindRecord(char *filename, char *name, char record[]), it is invoked from the main function. FindRecord opens the file and reads each record looking for the matching record name. It then returns the matching record in the array record[] and closes the file.

Step 5 is in a function called void Replace(char *name, char *newname, char record[]), it is invoked from the main function. It replaces the name in the array record[] with newname. The updated information is returned through the array record[].  You must use pointers.

Step 6 is in a function called void SaveRecord(char *filename, char *name, char record[]) and it is invoked from the main function. SaveRecord replaces the record in CSV that matches name

Vybihal           Assignment #4            Page 1 of 2 McGill University            COMP 206      School of Computer Science

with the array record[]. It then closes the file.  The entire CSV file must be preserved as in its original form escept the one record that is replaced.

Do not use global variables.

Using vim, create a csv file called phonebook.csv and populate it with 5 records.  Each record will be formatted as: name, age, phone_number.

Your C program is called Replace.c.

<h2><strong>WHAT TO HAND IN</strong></h2>

Submit your .c file and your .csv file to myCourses.

<h3>HOW IT WILL BE GRADED</h3>

Points removed for bad practices:

<ul>

 <li>-1 for not following instructions</li>

 <li>-1 for not indenting, spacing, and/or commenting</li>

 <li>-1 for not using good variable names</li>

</ul>

This assignment is worth 20 points:

<ul>

 <li>+2 main()</li>

 <li>+4 FindRecord()</li>

 <li>+4 Replace()</li>

 <li>+4 SaveRecord()</li>

 <li>+3 Good use of pointers</li>

 <li>+3 Good file manipulation techniques</li>

</ul>


