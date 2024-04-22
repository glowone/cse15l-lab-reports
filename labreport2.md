# Part 1

Here is the code: 
<img width="777" alt="Screenshot 2024-04-22 at 12 37 08" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/6078a614-5ff8-424b-9731-445f77557945">


Default window when first opening up the page: 
<img width="749" alt="Screenshot 2024-04-22 at 12 34 46" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/ec55ca25-db12-4b8e-94de-0c994b76fbf2">


Adding the first message: 
<img width="748" alt="Screenshot 2024-04-22 at 12 35 37" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/a2c1c4ae-8539-4134-9446-251c57feb5a0">
<img width="747" alt="Screenshot 2024-04-22 at 12 35 12" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/9b80b7a8-df0b-40b3-93e2-137b9e0944fc">


Adding the second message: 
<img width="748" alt="Screenshot 2024-04-22 at 12 35 37" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/a2c1c4ae-8539-4134-9446-251c57feb5a0">
<img width="751" alt="Screenshot 2024-04-22 at 12 35 43" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/2dddde3b-a6d8-4fbe-805a-62e9ec82a2fe">


**Which methods in your code are called?**

The query sequentially runs through the whole code. First it checks for `/add-message`, after confirming that it checks if the query is null through `.getQuery` which in this case is false so we continue. We split the input at `&` and `=` to get user inputs for the string and the username. 


**What are the relevant arguments to those methods, and the values of any relevant fields of the class?**

In my opinion it is important to mention that all this data is taken in through an ArrayList as our datastructure, where stuff gets concatenated to. And throughout our code we initialize `params` `messages and `user`, because we need to be able to update those values as we get user string input and usernames. 

**How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.**

If `add-message` is true with its following inputs `s=` and `user`, we update all those said variables. The message gets added to the arraylist initalized up top, and `message` and `user` get updated throughout the code. Although it's worth mentioning that obviously, stuff like where we take our `keyValue` from will not change, as it determines where our arguments are that we need to extract. 

# Part 2

Private key absolute path: 

<img width="405" alt="Screenshot 2024-04-22 at 14 40 22" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/904c3304-a1de-4cd5-afff-46518a48212d">

Public key absolute path: 

<img width="567" alt="Screenshot 2024-04-22 at 14 41 48" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/395b414d-6493-4c6d-8a42-2b33d00fe36d">

Terminal interaction without being asked for a password: 

<img width="818" alt="Screenshot 2024-04-22 at 14 42 12" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/d05a3a4e-0b11-4d4b-a8ec-86fb7105d2ae">




# Part 3

So far, week 2 and 3 have shown me that although simple, I am able to create my own websites already and modify them. It's cool to be able to access remote servers, and use the code I wrote to for example interact with others on that website, like a chat room, or make a custom search engine in which I store words and am able to search them up upon request. In my opinion, this class has finally made me passionate about CS and made me wanna learn more as I think the art of creation is fun. 
