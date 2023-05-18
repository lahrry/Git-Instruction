# Grep command in Unix/Linux
Today we are going to learn about a specific command with examples. 
We learned about three basic things to count text files(.txt) 
1.find 2.less 3.grep 
Let's dive into "grep" command!
<br>
<br>
###### Citation : the context of ChatGpt & GeeksforGeeks pages was partially referenced.
###### GeeksforGeeks:
######  "GeeksforGeeks." GeeksforGeeks grep command, https://www.geeksforgeeks.org/grep-command-in-unixlinux/.

###### ChatGPT (OpenAI):
###### OpenAI. "ChatGPT." OpenAI, OpenAI, openai.com/models/gpt-3.5, https://chat.openai.com/. 
                  
## Step 1: What is "grep" ?
According to "geeksforgeeks", grep command searches a file for a particular pattern of characters, and displays all lines that contain that pattern.

## Step 2: Clone docsearch repository
Let's first clone this specific repository : https://github.com/ucsd-cse15l-s23/docsearch.git.
<br>You can follow how to clone looking at the terminal that I attached below. 
<img width="650" alt="Screen Shot 2023-05-10 at 2 22 29 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/d9dd1947-4975-4868-9904-eaa9453b784f">

<br>You can see the technical folder inside and we are going to use this for this task!
<br><img width="370" alt="Screen Shot 2023-05-10 at 2 29 30 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/6040271b-a6f0-4f86-a24d-7c0788d2e3e6">
<br>We can see that there are 4 folders(report, biomed, government, plos) inside the technical directory, each containing variety of text files. 

## Step 3: First grep command option 
### grep [-i] pattern [files]
###### According to GeeksforGeeks,
`grep -i` : Ignores, case for matching 
We are going to compare `grep` and `grep -i` command using water_fees.txt file in the technical/government/Media directory. I'll post the absolute path to this.  /Users/bella/Desktop/git:github/cse15l/src/cse15l/docsearch/technical/government/Media/water_fees.txt 
### Example One
Let's say we want to find sentences that includes **'water'**. 
If we run `grep water water_fees.txt`, it will search for lines that has 'water'. 
<br><img width="479" alt="Screen Shot 2023-05-10 at 10 27 19 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/996a54f0-ecef-4b25-bbea-3efad036b18a">
<br>But I also want to see sentences that includes 'Water' too. 
<br>`grep water water_fees.txt` only search for the word 'water', it doesn't ignores case. 
<br>Try `grep -i water water_fees.txt`and see the result below. 
<br><img width="481" alt="Screen Shot 2023-05-10 at 10 30 57 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/3a490245-14fe-483c-a340-574f090a9b9d">
 <br><img width="105" alt="Screen Shot 2023-05-10 at 10 31 19 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/a1ac94c1-260d-41bf-a554-ca2e47084034">
<br>There we go! We found 'water' with capital case too. `grep -i` enables to search for a string case insensitively in the given file. In this case, it matches the words like "Water", "WAter", "WaTER".  

### Example Two
<br>Let's try one more command using `grep -i`. 
<br><img width="439" alt="Screen Shot 2023-05-10 at 10 38 51 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/0049b157-23f4-4a37-a474-ad277875fb6d">
<br>In the government folder, I searched 'local' through "Law_Schools.txt" and it searched a sentence that includes "Local" which ignored the case for matching. 

## Step 4: Second grep command option 
### grep [-c] pattern [files]
###### According to GeeksforGeeks,
`grep -c` : This prints only a count of the lines that match a pattern
Let's dive in! Use `grep -c` command through water_fees.txt file in the technical/government/Media directory. I'll post the absolute path to this.  /Users/bella/Desktop/git:github/cse15l/src/cse15l/docsearch/technical/government/Media/water_fees.txt 

### Example One
If we run `grep -c water water_fees.txt`, it will find the number of lines that matches 'water'. 
<br><img width="439" alt="Screen Shot 2023-05-10 at 10 54 18 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/cd9dfa1b-fc7b-401b-9309-c8039d28da0e">
<br>You can find the command outputed '9' because there is 9 lines that matches the pattern 'water'. 

### Example Two
<br>Let's find one more example of `grep -c`!
<br>Try a command `grep -c Chris water_fees.txt`. 
<br><img width="439" alt="Screen Shot 2023-05-10 at 10 54 32 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/1ed3052f-4956-4d7a-8590-58ae2ecedc1c">
<br>You can find the command outputed '1' because there is only one line that matches the pattern 'Chris'. 
###### According to ChatGPT, 
<br>We can conclude that `grep -c`command is very useful to quickly count the number of lines in a file that match a specific pattern and can be a valuable tool in analyzing and processing large datasets. 


## Step 5: Third grep command option 
### grep [-l] pattern [files]
###### According to GeeksforGeeks,
`grep -l` : Output matching files only. 
Let's dive in! Use `grep -l` command through all files in Media folder. 

### Example One
If we run `grep -l water *`, it will search for files in this directory that contain the word "water". 
<br><img width="439" alt="Screen Shot 2023-05-10 at 11 12 01 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/c4750b71-d51d-4abb-8d61-f33d39627159">

<br>You can find the command outputed all the files in the Media directory that contains "water" string. 

### Example Two
<br>Let's find one more example of `grep -l`!
<br>Try a command `grep -l Chris *`. 
<br><img width="345" alt="Screen Shot 2023-05-10 at 11 14 35 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/d27652a6-d784-4307-a04b-5b70f58b1f9a">

<br>You found all the files that contains "Chris"! Congrats!!
###### According to ChatGPT, 
In summary, the `grep -l` command is a powerful tool that can be used to quickly identify files that match a specific pattern or regular expression, and can be beneficial in a variety of scenarios, including data analysis, automation, filtering, and debugging.


## Step 6: Fourth grep command option 
### grep [-v] pattern [files]
###### According to GeeksforGeeks,
`grep -v` : Invert match
Let's dive in! Use `grep -v` command through water_fees.txt file in the technical/government/Media directory. I'll post the absolute path to this.  /Users/bella/Desktop/git:github/cse15l/src/cse15l/docsearch/technical/government/Media/water_fees.txt 

### Example One
If we run `grep -v water water_fees.txt`, it will output all the text that excludes "water". 
###### Don't be confused! It won't exclude "Water" it will only exclude lines with the same string. 
<br><img width="473" alt="Screen Shot 2023-05-10 at 11 20 30 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/0bf20346-e3d0-455a-87ef-37aef3cb27ec">

<br>I excluded 'water' because this text was about water but I guess there are more sentences that didn't use 'water' to their sentences :) 

### Example Two
<br>Let's find one more example of `grep -v`!
<br>Try a command `grep -v a water_fees.txt`. 
<img width="473" alt="Screen Shot 2023-05-10 at 11 24 52 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/b52ed940-dc9f-49a8-bed5-40a07c54e5ed">

<br>Most of the sentences will include 'a' in their words so I excluded all the lines that has 'a' in their sentences. We only have 5 lines total! WOW!
###### According to ChatGPT, 
In summary, the `grep -v` command can be useful in situations where you want to exclude lines that match a specific pattern from the output of a command or a file, and can be combined with other grep options to perform complex searches.

