# Lab Report 1 
1) Share an example of using the command with no arguments
--- 
**Code Block** 

`cd`: 

`glowone@Manis-Laptop lecture1 % cd`

`glowone@Manis-Laptop ~ %`

`ls`: 

`glowone@Manis-Laptop ~ % ls`

`Applications    Documents       Library         Music           Public          lecture1
Desktop         Downloads       Movies          Pictures        Work`


`cat`: 

`glowone@Manis-Laptop ~ % cat`

`hi`

`hi`

**Absolute path** 

`glowone@Manis-Laptop ~ % pwd`

`/Users/glowone`

**Why did I get this output?** 

`cd`: 
stands for change directory, we didn't give it a directory to change for therefore nothing happens.

`ls`: Gives us a list of the files and directories within a path. In this case our absolute path is /Users/glowone, therefore we're able to see all the objects within /Users/glowone.

`cat`: 
The cat command without any given arguments simply waits for input which it then echoes. 


**Is the output an error or not?**

`cd`: 
I think on a technical basis there is an error since we're using a change directory command but not actually changing it to anything, but we're throwing a null pointer expection which handles this case. 

`ls`: No.

`cat`: No. 

--- 

2. Share an example of using the command with a path to a directory as an argument.
---

