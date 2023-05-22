# Vim Control with Timing Tasks
## We are going to edit some code in java file to fix the failing test using vim in the terminal!

### Step 1
```Log into ieng6```
First open your terminal as we did in report 1 and log into your ieng6 account.<br> 
<br><img width="422" alt="Screen Shot 2023-05-21 at 6 33 57 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/ac68f613-d303-4914-a662-19e87654fad9">
###### Your should enter your password like before. I made a ssh keys for ieng6 account so that's why I can get logged in automatically :)


### Step 2
```Clone your fork of the repository from your Github account```
Make a fork of the lab7 : https://github.com/ucsd-cse15l-s23/lab7 on your Github account. 
<br><img width="983" alt="Screen Shot 2023-05-21 at 6 41 40 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/ae1019ff-7c20-4a97-8c61-a9b2620692bd">
Click the green button "code" and make a copy of HTTPS.
<br><img width="424" alt="Screen Shot 2023-05-21 at 6 42 25 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/acaea929-6ed7-46f3-ad8e-5bc40fc81d9b"><br>
Next, go back to your terminal that you logged in and type the HTTPS (https://github.com/ucsd-cse110-sp23/lab7.git) after git clone command. So it will be like ```git clone https://github.com/ucsd-cse110-sp23/lab7.git```
<br><img width="563" alt="Screen Shot 2023-05-21 at 6 50 44 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/f6997bd9-3c15-4234-a8d7-77e9f5d9d5fe"><br>

**Keys Pressed**
: From typing ```mkdir LABREPORT4``` I made a new folder to clone the repository and ```<enter>```. I typed ```git clone``` in the next command statement and ```<Command-V>``` to paste the HTTPS link. ```ls``` ```<enter>``` to check the folder made. ```cd``` ```<enter>``` to go into the 'lab7' folder. ```<up>``` ```<enter>```command was 1 up in the search history, so I used up arrow to access it. 


### Step 3
```Run the tests, demonstrating that they fail```

**Keys Pressed**
: ```<up>``` ```<up>``` ```<up>``` ```<up>``` ```<up>``` ```<enter>```, ```<up>``` ```<up>``` ```<up>``` ```<up>``` ```<up>``` ```<enter>``` The ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` command was 5 up in the search history from my previous lab history. Then ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests``` command was 5 up in the history, so I accessed and ran it in the same way. 

<br><img width="563" alt="Screen Shot 2023-05-21 at 7 09 49 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/a1445128-f2a5-4e3b-8003-a211a3d9fd9d"><br>
<br>We can see that we have a 1 failure. So we need to change a code for test to run successfully!


### Step 4
```Edit the code file ListExamples.java to fix the failing test (as a reminder, the error in the code is just that index1 is used instead of index2 in the final loop in merge)```

To edit the code, type ```vim ListExamples.java``` and you will see the following page. 
<br><img width="563" alt="Screen Shot 2023-05-21 at 7 15 11 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/8a0f5d01-794b-4c95-b398-f5edc7241ac5"><br>

**Keys Pressed**
: ```<j>``` ```<j>``` ```<j>``` ```<j>``` ```<j>``` ```<j>``` by clicking ```<j>``` key 6 times, it went down through the pages. However, I was thinking I want to look at the end of the line. So by clicking ```Ctrl-E```, I could see the end of the line which moved the cursor to the last. 
<br><img width="563" alt="Screen Shot 2023-05-21 at 7 19 53 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/45d78a22-8e1f-4d30-92c8-8d6064f5ae61"><br>

<br>
The error was here! to move up, I clicked ```<k>``` 6 times to move to line 44 from the end line. Then I clicked ```<l>``` 10 times to move to the right to delete '1' in 'index1'. To do that, I pressed ```<dw>``` to delete one word '1'. 
<br><img width="563" alt="Screen Shot 2023-05-21 at 7 26 02 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/6a4a41b5-0c60-4ed6-8606-50a8ed6487d9">
<br>```<i>```command was made to get access to edit in vim. Then ```< -> >```(shift-right key),```<spacebar>```, ```< <- >```(shift-left key) was made to make space to insert '2' in the original '1' place. 2 was typed and we need to get out of this --insert-- page. In order to do that, ```<esc>``` command was clicked. Also, to save the files ```<:wq!>```,```<enter>```command was clicked. 




### Step 5
```Run the tests, demonstrating that they now succeed```


### Step 6
```Commit and push the resulting change to your Github account```












