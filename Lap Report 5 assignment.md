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
I'll give you an example of the bash script:
```java
test.sh
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar ArrayExamples.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ArrayTests
```
Everytime you test your code, run the bash file and tell me how you did it!

Please share the result after running these commands so that I can figure out what exact problem you have. 

Best Regards, <br>
<br>Bella Jeong. <br><br>



###### Student's Response

Re: Issue with reversed() method in ArrayExamples.java 

Hi, Bella this is John again and thank you for helping me out. I will share what I have in my ArrayExamples.java code:
<img width="581" alt="Screen Shot 2023-06-04 at 9 17 48 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/44f8411c-6f02-456a-bb5f-d66f565a303b">

 I think I had a minor mistake in my reversed() method implementation. 

Also, the commands that you told me to run: 
<img width="895" alt="Screen Shot 2023-06-04 at 9 19 28 PM" src="https://github.com/lahrry/cse15l-lab-reports/assets/62029893/cca5ec7a-e6f3-4b5e-9795-8344890fb0aa">




