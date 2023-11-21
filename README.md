# CSPB-3753 Lab: Unbounded Data Structures
<figure width=100%>
  <IMG SRC="https://www.colorado.edu/cs/profiles/express/themes/cuspirit/logo.png" WIDTH=100 ALIGN="right">
</figure>
<br>
Often our implementations need to handle a unspecified amount of data.  We can always try to create a buffer that is large enough to handle any data, but it is a waste of space in most instances and will not handle all quantities of data.

A better solution is to use the heap to dynamically allocate space as needed.  In this lab you will dynamically create two data structures to handle space efficiency and unknown amount of data.
	
<hr>

You will implement two functions for this lab:  `get_unbounded_line()` and `get_value_table()`.   These functions will allocate the data structure needed from the heap using `malloc`, `realloc`, and `free` function calls to manage the allocated space.   Make sure that at the end of your program you have released any memory that has been allocated (no memory leaks should be detected).
	

    
<img src="images/construction-set-icon.jpg" alt="Under Construction" WIDTH=120 ALIGN="left" />

### This lab is still under construction.  
 
 Please report all speeling and grammered issues.<br>
 Also let us know about any unclear descriptions of work to be performed. 
 <br><br><br>
<hr>    

**Objectives**
	
* use C to create simple application(s) 
* use C to read unbounded amount of characters from user.
* use `malloc` and `realloc` to manage data structure sizes.
* use memory checking to validate that all allocated memory is explicitly released.
* use debugger (GDB or VSCode) to aid program development.
* use return value checking on all system and library calls.
	
<hr>
	
Presumably you have completed a computer systems course such as CSPB-2400 that covered the internal subsystems in a Computer.  You were also introduced to debugging, machine language, code optimization, processes, and memory management.  You also learned about the different sections of memory allocated to a program or process.  The code, data, stack, and heap are different areas of memory that are used within a program.
	
In this lab you will use memory allocated from the HEAP for collecting an unknown quantity of data from the user.  The HEAP is used to dynamically allocate variables that are managed by the program itself.  You will only allocate a small amount of memory to begin with, and extend that memory in small amounts to use only as much memory as needed.
	
<hr>
	
### Part 1 - Implement the `main()` function
The program should print a prompt and then collect the data from the user into a command line.  
Once the user terminates the input, parse the data into a set of values to be placed into a dynamically allocated list of integer values. 
Take the value table and print a summary of the data (# values, min, max, avg).
Release the data structures and exit the program.
	
<hr>
	
### Part 2 - Implement the `get_unbounded_line()` function
Here is a basic algorithm for the function:

	
```
allocate a minimum amount of buffer space
while not EOF or EOL
	get next character
	if (no space left in buffer)
		extend the buffer
	append the character to the buffer
return buffer
```

<hr>
	
### Part 3 - Implement the `get_value table(command_line)` function

Here is a basic algorithm for the function:
```
allocate a minimum amount of table space
while more data in command line
	get next token
	convert token into integer value
	if (no space left in table)
		extend the table
	append the value to the table
return table
```
<hr>
    
### When you have completed the Lab tutorial 

<img src="images/deliverable.png" alt="Deliverable Item" WIDTH=40 ALIGN="left" />
Although the grading will be done by accessing your Public Domain Website, <br>
you must submit the following to Moodle Assignment:

* Your name:
* CU ID: (4 letters - 4 digits)
* GitHub Username:
* hours to complete lab:

<hr><hr><hr>