# Grep command in Unix/Linux
Today we are going to learn about a specific command with examples. 
We learned about three basic things to count text files(.txt) 
1.find 2.less 3.grep 
Let's dive into "grep" command!
## Step 1: What is "grep" ?
According to "geeksforgeeks", grep command searches a file for a particular pattern of characters, and displays all lines that contain that pattern.<br>

## Step 2: Clone docsearch repository
Let's first clone this specific repository : https://github.com/ucsd-cse15l-s23/docsearch.git.
<br>You can follow how to clone looking at the terminal that I attached below. 
<img width="650" alt="Screen Shot 2023-05-10 at 2 22 29 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/d9dd1947-4975-4868-9904-eaa9453b784f">

<br>You can see the technical folder inside and we are going to use this for this task!
<img width="370" alt="Screen Shot 2023-05-10 at 2 29 30 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/6040271b-a6f0-4f86-a24d-7c0788d2e3e6">
<br>We can see that there are 4 folders(report, biomed, government, plos) inside the technical directory, each containing variety of text files. 

## Step 3: First grep command option 
### grep [-i] pattern [files]
`grep -i` : Ignores, case for matching 
We are going to compare `grep` and `grep -i` command using water_fees.txt file in the technical/government/Media directory. I'll post the absolute path to this.  /Users/bella/Desktop/git:github/cse15l/src/cse15l/docsearch/technical/government/Media/water_fees.txt 
Let's say we want to find sentences that includes **'water'**. 
If we run `grep water water_fees.txt`, it will search for lines that has 'water'. 

<br><img width="479" alt="Screen Shot 2023-05-10 at 10 27 19 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/996a54f0-ecef-4b25-bbea-3efad036b18a">
<br>But I also want to see sentences that includes 'Water' too. 
<br>`grep water water_fees.txt` only search for the word 'water', it doesn't ignores case. 
<br>Try `grep -i water water_fees.txt`and see the result below. 
<img width="481" alt="Screen Shot 2023-05-10 at 10 30 57 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/3a490245-14fe-483c-a340-574f090a9
                                                                  <img width="105" alt="Screen Shot 2023-05-10 at 10 31 19 AM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/a1ac94c1-260d-41bf-a554-ca2e47084034">
b9d">
<br>There we go! We found 'water' with capital case too. `grep -i` enables to search for a string case insensitively in the given file. In this case, it matches the words like "Water", "WAter", "WaTER".  
