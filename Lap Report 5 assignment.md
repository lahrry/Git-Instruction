# Debugging Scenario
###### Student's Question 
<img width="998" alt="Screen Shot 2023-06-04 at 9 10 27 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/c4cba57f-abb9-4a47-ab11-aa7e74f90eda">

###### TA Response

Re: Solving issue with reversed() method in ArrayExamples.java debugging

Hi John, this is Bella Jeong who is your tutor and thank you for reaching me out. 
I will be helping you out with this problem today! 
As I can see, I don't think there are any problems in your ArrayTests.java file however, I think there could be an error in your ArrayExamples.java code, specifically in reversed() method. Can you please share your whole ArrayExamplese.java code? 

Also, try to run these two following commands in your terminal : <br>
```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar ArrayExamples.java``` <br>
```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ArrayTests```

Or if it's cumbersome to run these two commands every time you test, try creating a bash script.
I'll give you an example of the bash script "arraytest.sh":
```java
set -e
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar ArrayExamples.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ArrayTests
```
After running the bash script in your terminal, try: 
```java
bash-3.2$ echo $?
```
This will tell you have an error it will show 1 if not 0. You can use this in order to check quickly if you have an error or not.  

Please share the result after running these commands so that I can figure out what exact problem you have. 

Best Regards, <br>
<br>Bella Jeong. <br><br>



###### Student's Response

Re: Issue with reversed() method in ArrayExamples.java 

Hi, Bella this is John again and thank you for helping me out. I will share what I have in my ArrayExamples.java code:

<img width="581" alt="Screen Shot 2023-06-04 at 9 17 48 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/44f8411c-6f02-456a-bb5f-d66f565a303b">

 I think I had a minor mistake in my reversed() method implementation. In the original code that I wrote, the reversed value should have assign to "newArray" however, it was assigning to "arr" instead. So I fixed my code: 
 
 <img width="582" alt="Screen Shot 2023-06-04 at 9 34 00 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/21965e36-c7df-46c7-b27b-cf27bc7b089a">


Also, the commands that you told me to run: 
<img width="895" alt="Screen Shot 2023-06-04 at 9 19 28 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/cca5ec7a-e6f3-4b5e-9795-8344890fb0aa">

But I made a bash script which was very convinient to use everytime I test my codes. I will attach how I made a bash script:<br><img width="744" alt="Screen Shot 2023-06-04 at 9 51 27 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/03455482-80ab-4a89-9d32-c4c3e040ebbc">

This is the result of running the bash script:
<img width="209" alt="Screen Shot 2023-06-04 at 9 35 22 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/4a7ebca0-0a6e-451b-b82e-d6c7e18ff4bd">

After running 
```java
bash-3.2$ echo $?
```
this command, 
```
[With Bug]
```
<img width="701" alt="Screen Shot 2023-06-04 at 10 04 29 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/aacb3bb2-78b1-4068-89d9-926830e5f60e">

```
[With Fixed Code]
```
<img width="697" alt="Screen Shot 2023-06-04 at 10 02 19 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/489378ee-97dc-49e0-bc9d-895d8e0384df">


# Reflection
<br>
The most interesting thing that I learned from my lab experience is when we learned about server.java and local host. That time I didn't know how to handle code in java that much so I asked to TAs a lot for help. Once I knew that I can control URL and local host server with java code in VSCode, it was amazing experience. I think that was the turning point of this course that I got more interest in coding/computer science. It thrilled be to learn many new things like making autograder, bash script, learning about vim and all of them. This class and lab is the most useful course that I have taken before. Thank you for teaching us useful sources:)





