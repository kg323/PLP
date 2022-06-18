# **ARIZONA STATE UNIVERTSITY**

Author: Kenneth Galindo

Instructor: Christopher Mar

![image](https://user-images.githubusercontent.com/98668234/174452285-821f7e76-d440-4081-992c-758325ce9bfa.png)

# **PLP Project 3: UART Palindrome Checker** 

**Learning Objectives:** 

● Create modular code and interface with unfamiliar modularized code 

**The Task:**

In  this  project,  you  will  be  writing  a  program  that  receives  a  string  of  characters  via  the  UART,  checks  if  this 
string is a palindrome, and then uses a print function to print either “Yes” or “No”. A palindrome is a sequence 
of characters (typically a word or phrase) that is the same both forwards and backwards. For this project, strings 
will be terminated using a period (‘.’). You may assume that a string will contain at least one letter in addition to 
a period (e.g., the input, “b.”, should be considered a palindrome). You will not need to handle empty strings, 
strings  containing  only  a  period,  or  stings  containing  characters  other  than  letters,  spaces,  and  periods.  Your 
program  should  be  able  to  handle  multiple  strings  sent  one  after  another  or  concatenated  together.  For 
example, the string: “abba. data.” should print “Yes” followed by “No” on the  next  line.  Spaces  should  be 
ignored when checking for a palindrome and the palindrome should not be case sensitive. For example, “A nut 
for a jar of Tuna.” would be considered a palindrome. 

**Print Function:**

A template PLP project file is available to download on Canvas. The PLP project includes a second ASM file titled, 
project3_lib.asm.  This  ASM  file  contains  the  print  function  used  in  this  project.  PLPTool  concatenates  all  ASM 
files within a PLP project into a single location in memory (unless additional .org statements have been added to 
specify different location for code). No changes to project3_lib.asm should be made. 

<br>

When  called,  depending  on  the  value  in  register  $a0,  the  following  string  will  be  displayed  on  the  simulated 
UART device’s output.  If  $a0  contains  a  zero  then  “No”  will  be  displayed  and  if  $a0  contains  a  non-zero  value 
(e.g. one) then “Yes” will be displayed. The print function is called using the following instruction: 

![image](https://user-images.githubusercontent.com/98668234/174452065-dade4491-f721-4a1d-8180-210705d5c187.png)


To  use  the  print  function,  your  PLP  program  needs  to  initialize  the  stack  pointer  ($sp)  before  performing  the 
function  call  (or  any  other  operations  involving  the  stack  pointer).  For  this  reason,  the  template  project  file 
includes an initialization that sets the stack pointer to 0x10fffffc (the last address of RAM).  


**Template Structure:**

The template project file contains six function stubs that need to be implemented. Five are called from the main 
loop and the sixth is called from “period_check”. The template file contains comments with descriptions of what 
each function needs to do and how it should be  implemented.  The table  below provides a brief description of 
the functions. 

![image](https://user-images.githubusercontent.com/98668234/174452091-86cd13ae-0c76-444f-9bac-42d985ef37a5.png)


**Debugging Tools:**

To  show  that  you  properly  tested  your  program,  please  save  your  program  while  it  is  in  simulation  mode  (the 
blue simulation mode button has been toggled on) such that a **CPU Memory Visualization window** is open and 
shows  **at  least  the  first  6 words  of  memory  in  the  array.**  Please keep  in mind  that  the  starting  address  of  the 
array  is  relative  to  the  number  of  initializations  placed  before  the  assembler  directive  allocating  space  for  the 
array.  If  you  change  your  initializations  you  may  need  to  adjust  your  CPU  Memory  Visualization  base  address. 
The  Array  Example  video in this project’s module demonstrates how to set up a CPU Memory Visualization window. It is acceptable to also see program contents in memory (these cells will be colored blue). For example, it would be acceptable to see the following in the visualizer after the string, “abcd.”, has been sent by the user.

![image](https://user-images.githubusercontent.com/98668234/174452122-73249daa-8efc-46fe-ace7-2d90b6d9ba91.png)

Additionally, the **watcher window** should contain, at minimum, registers $v0, $s1, and $s2. You may also include 
any other registers in the watcher window that you find useful for debugging. 

