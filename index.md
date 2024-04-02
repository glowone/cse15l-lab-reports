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
**Code Block** 

`cd`: 

<img width="644" alt="Screenshot 2024-04-02 at 13 16 19" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/f7940407-9f42-4942-bcc9-ad17e57e4b0f">

`ls`: 

![image](https://github.com/glowone/cse15l-lab-reports/assets/146388424/62c229a0-d1b3-41d6-8568-7d7ae6509f88)

`cat`: 

<img width="307" alt="Screenshot 2024-04-02 at 13 45 36" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/816a9b33-a7a6-4d14-b46e-e80f339361d6">

**Absolute path** 
Original path:

`glowone@Manis-Laptop ~ % pwd`

`/Users/glowone`

Absolute path after we used `cd Work`: 

`/Users/glowone/Work`

**Why did I get this output?** 

`cd`: 
Cd did it's job/did what it was asked of. Pwd confirmed it. It didn't return anything because it didn't have to. 

`ls`: 
`ls School` opened up the list of objects within the School directory. 

`cat`: 
The cat command is unable to do anything with a directory. 

**Is the output an error or not?**

`cd`: 
No 

`ls`: 
No 

`cat`: 
Yes, cat is supposed to display the contents of files, we've given it a directory therefore it's unable to work. 

---
3) Share an example of using the command with a path to a file as an argument.
---

**Code Block:**

`cd`: 

`ls`: 

`cat`: 

**Absolute path**

**Why did I get this output?** 

`cd`: 

`ls`: 

`cat`: 

**Is the output an error or not?**

`cd`: 

`ls`: 

`cat`: 
