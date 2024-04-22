# Lab Report 1 
1) Share an example of using the command with no arguments

--- 
**Code Block** 

`cd`: 
```
glowone@Manis-Laptop lecture1 % cd
glowone@Manis-Laptop ~ %`
```
`ls`: 
```
glowone@Manis-Laptop ~ % ls
`Applications    Documents       Library         Music           Public          lecture1
Desktop         Downloads       Movies          Pictures        Work`
```

`cat`: 
```
glowone@Manis-Laptop ~ % cat

hi

hi
```

**Absolute path** 
```
glowone@Manis-Laptop ~ % pwd
/Users/glowone
```

**Why did I get this output?** 

`cd`: 
stands for change directory, we didn't give it a directory to change to so it defaults to the home directory. 

`ls`: Gives us a list of the files and directories within a path. In this case our absolute path is `/Users/glowone`, therefore we're able to see all the objects within `/Users/glowone`.

`cat`: 
The cat command without any given arguments simply waits for input which it then echoes. 


**Is the output an error or not?**

`cd`: 
No.

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
```
glowone@Manis-Laptop ~ % pwd
/Users/glowone
```

Absolute path after we used `cd Work`: 

`/Users/glowone/Work`

**Why did I get this output?** 

`cd`: 
`cd` did it's job/did what it was asked of. `pwd` confirmed it. It didn't return anything because it didn't have to. 

`ls`: 
`ls School` opened up the list of objects within the School directory. 

`cat`: 
The cat command is unable to do anything with a directory. 

**Is the output an error or not?**

`cd`: 
No. 

`ls`: 
No.

`cat`: 
Yes, cat is supposed to display the contents of files, we've given it a directory therefore it's unable to work. 

---
3) Share an example of using the command with a path to a file as an argument.
---

**Code Block:**

`cd`: 

<img width="370" alt="Screenshot 2024-04-02 at 14 10 51" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/04c7787f-e78b-4d83-813d-d1b4731c5b3c">

`ls`: 

![image](https://github.com/glowone/cse15l-lab-reports/assets/146388424/f63e6b6d-e995-44ab-bcb6-cf7d2368a719)


`cat`: 

![image](https://github.com/glowone/cse15l-lab-reports/assets/146388424/a3eaf80a-1385-4475-8a99-fa03d4b45987)



**Absolute path**

```
glowone@Manis-Laptop Work % pwd
/Users/glowone
```

**Why did I get this output?** 

`cd`: 
I think it's because you're not able to change your directory to a file, it has to be a folder which has contents inside of it. 

`ls`: 
`ls` still makes an attempt at displaying a list of contents, since we're working with a file the only content it's able to display is the filename, which it does. 

`cat`: 
`cat`'s function is to display contents of a file. Since we're working with a file now it does what it's supposed to. 

**Is the output an error or not?**

`cd`: 
It's definitely an error, `cd` is not made for working with files. 

`ls`: 
No.

`cat`:
No.

