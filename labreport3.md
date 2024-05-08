## Part 1 

For part 1 of this section, I am testing the following code and giving it one JUNIT test with a failure inducing input, and one that'll work:

Code: 

```
  static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for(String s: list) {
      if(sc.checkString(s)) {
        result.add(0, s);
      }
    }
     return result;
  }
  ```

  One failure inducing test: 


    @Test
    public void testFilter() {
        ListExamples listExamples = new ListExamples();
        List<String> original = Arrays.asList("apple", "banana", "cherry", "date");
        List<String> expected = Arrays.asList("banana", "cherry", "date");
        // StringChecker that checks if a string has an even number of letters
        StringChecker sc = new StringChecker() {
            @Override
            public boolean checkString(String s) {
                return s.length() % 2 == 0;
            }
        };
        List<String> actual = listExamples.filter(original, sc);
        assertEquals(expected, actual);
    }
    ```


One test that passes in a faulty manner:


```
   @Test
    public void testFilterNoMatch() {
        ListExamples listExamples = new ListExamples();
        List<String> original = Arrays.asList("apple", "banana", "cherry", "date");
        List<String> expected = Arrays.asList();
        // StringChecker that checks if a string starts with 'z', which none do
        StringChecker sc = new StringChecker() {
            @Override
            public boolean checkString(String s) {
                return s.startsWith("z");
            }
        };
        List<String> actual = listExamples.filter(original, sc);
        assertEquals(expected, expected);
    }
```

Symptom of code that did not pass: 

<img width="875" alt="Screenshot 2024-05-07 at 15 04 11" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/846342a9-a55a-4833-864f-9ba384720397">


Output of the faulty running test: 

<img width="651" alt="Screenshot 2024-05-07 at 14 44 49" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/a3251d32-5575-4ac1-b85b-67fc61748f79">


FIXED code that passes the first test: 

```
  static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for(String s: list) {
      if(sc.checkString(s)) {
        result.add(s);
      }
    }
     return result;
  }
  ```

FIXED test, that still passes because the code works: 

```
   @Test
    public void testFilterNoMatch() {
        ListExamples listExamples = new ListExamples();
        List<String> original = Arrays.asList("apple", "banana", "cherry", "date");
        List<String> expected = Arrays.asList();
        // StringChecker that checks if a string starts with 'z', which none do
        StringChecker sc = new StringChecker() {
            @Override
            public boolean checkString(String s) {
                return s.startsWith("z");
            }
        };
        List<String> actual = listExamples.filter(original, sc);
        assertEquals(expected, actual);
    }
```

What happened? 

Code: 
As for the faulty code, when we provided the insertions with an index at 0, we would get the reversed order of what we were actually supposed to get. Hence why removing index 0 fixed the issue. 


Test: 
The test just had a faulty expected and actual, the actual was equal to the expected which made the code pass, regardless of whether the method was faulty or not. It is important to make sure your tests check methods correctly. 


## Part 2 

For this section of the lab, I chose `grep`. 

Here are four interesting options:

-`i`: makes a case-insensitive search.

-`r`: makes search recursive and searches within all subdirectories (case sensitive).

-`v`: invert search, returning lines that do not match what we're searching for.

-`l`: returns the names of files that contain what we're searching for.

Two examples for each command are: 

1. `i`

   input 1: 

we use r in combination with i to search through all subdirectories! 

In the case of using these commands with `i`, it's useful if we're not caring about the lower or upper case and just want to make a search. In this example we're looking for sentences that use the word school. 

<img width="828" alt="Screenshot 2024-05-07 at 16 52 57" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/0ee31c0f-f3c8-48bd-9b08-2ed1f975035c">

  output 1: 

  <img width="1056" alt="Screenshot 2024-05-07 at 16 55 37" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/26615e4d-8472-4ccf-865e-c7485d7858b3">

Now we're looking for texts that use the word cool. 

 input and output 2:

   <img width="1055" alt="Screenshot 2024-05-07 at 16 57 17" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/f57e07b3-9745-4df4-bd46-7bf2227f9d8d">

2. In the case that we do care about case-sensitivity, we can use `r` as followed:

input 1 `r` with the word SCHOOL: 
<img width="789" alt="Screenshot 2024-05-07 at 17 02 44" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/644392ee-7677-446e-a4fa-668d840990b0">

output 1: 

no output! hence SCHOOL doesn't exist within any of these texts. 

input and output 2 `r` with the word School: 

<img width="1055" alt="Screenshot 2024-05-07 at 17 03 55" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/045428d8-af7a-4c70-82f8-d5fa4854a4d0">

This time around we got a case sensitive output. 


3. `v` looks for all lines within a file that do not contain a what our search defined, it's useful when trying to filter something out.

   input 1 - for the sake of making it interesting I used the following input:

   <img width="783" alt="Screenshot 2024-05-07 at 17 10 21" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/5d3cded3-dea6-4c71-b483-efb261d62e5b">

   output 1:

   <img width="1062" alt="Screenshot 2024-05-07 at 17 11 03" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/8d635b15-5ff9-414b-9d91-ad5827888538">


  input 2, as we can see in this example, very few lines do not have the vowel a: 
  
<img width="776" alt="Screenshot 2024-05-07 at 17 12 40" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/dc4ea3cd-a98f-42cc-b4bf-90de33fe5ac3">

  ouput 2: 

  <img width="1063" alt="Screenshot 2024-05-07 at 17 13 00" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/e28d144f-b02d-470a-bad5-61bc9a699c4d">


4. `l` will give us the names of the files that have what we're searching for, so let's what files contain school and cool:

   input and output 1:

   <img width="873" alt="Screenshot 2024-05-07 at 17 15 33" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/ac8c925a-1ba0-4162-b089-b63a973f4255">

   input and output 2:

   <img width="872" alt="Screenshot 2024-05-07 at 17 16 33" src="https://github.com/glowone/cse15l-lab-reports/assets/146388424/87d02f73-9099-45bb-8450-a40bf4677ca9">


Source: 

https://www.gnu.org/software/grep/manual/grep.html

