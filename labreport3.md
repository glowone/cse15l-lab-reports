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
