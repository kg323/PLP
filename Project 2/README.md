# **ARIZONA STATE UNIVERTSITY**

Author: Kenneth Galindo

Instructor: Christopher Mar

![image](https://user-images.githubusercontent.com/98668234/174452285-821f7e76-d440-4081-992c-758325ce9bfa.png)

# **PLP Project 2: LED Pattern Generator** 

**Learning Objectives:** 

● Use PLP branch instructions 

● Read from a memory mapped I/O device 
 
The Task: 

Write a program in PLP assembly that repeatedly reads the value of the switches (address: 0xf0100000) and 
displays a pattern on the LED array based on what switches. Each time the switch value is read, the pattern 
should be displayed (regardless of whether the switch value has changed or not since the last time it was read). 
The table below indicates the pattern that should be displayed for each possible switch setting: 

![image](https://user-images.githubusercontent.com/98668234/174451978-b09d3001-df94-495f-9870-0aa9ebe941ce.png)


**Note:** Logical shifts are not required to complete this project, but they can be used to make your program shorter 
and more readable than hard coding every value to be written to the LEDs. Shifts can also be useful to generate 
the value that you compare with the value of the switches. 
