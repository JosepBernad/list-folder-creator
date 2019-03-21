# FIB's courses folder creator

## Usage
1. Visit [the api site](https://api.fib.upc.edu/v2/assignatures/) of the FIB, login with your Raco-FIB account and copy the whole JSON.
2. Visit [this JSON Query Tester](http://www.jsonquerytool.com) and paste the JSON in the *JSON* spot.
3. Paste the next code in the *Extraction Query* spot and click **Run**.
```bash
$.results[*].id
```
4. Copy the *Resoult*, paste it in the *Entry to test against* spot from [this online regex tester](https://www.freeformatter.com/regex-tester.html) and paste the next RegEx in the *Regular Expression* spot:
```regex
[^a-zA-Z0-9-(\r\n|\r|\n)]
```
5. Leave the *Replace with (Optional)* empty and click **Replace**.
6. Create a new folder and create a file called *names.txt*.
6. Paste in this new file the *Result* of the RegEx replacement.
7. In this folder, copy the file named *program* from this repo.
8. Using the bash terminal run:
```bash
# chmod u+x program
```
9. Run the program using
```bash
# ./program 
```
