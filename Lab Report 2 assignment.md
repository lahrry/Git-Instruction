# Servers and Bugs <br>
## Part 1 : Building web server called ```StringServer```

The code of StringServer.java 

```java
import java.io.IOException;
import java.net.URI;


class Handler implements URLHandler{

  String str = " ";
  //initializing to an empty string
  public String handleRequest(URI url){
    System.out.println("Path: " + url.getPath());
    if(url.getPath().contains("/add-message")){
      //after the domain, "/add-message" should be contained
      String[] parameters = url.getQuery().split("=");
      //in this query, key-value is separated by "=". 
      //So the key parameter will be "s" and the string that we will type will be the value parameter. 
      if(parameters[0].equals("s")){ //&& (parameters.length == 2)
      //if the first parameter(key) equals to "s" and the parameter length is two
      //parameter length has to be 2 because in "s"="How%20are%20you" there are two strings
        String type = parameters[1].replace("%20", " ");
        //Talking about the second parameter which is value parameter
        //where we are going to type after "="
 
        //replace() method: first parameter in replace(first parameter, second parameter) is replaced by 
        //the second parameter. So here %20 is replaced by space because URL encode space as %20 or +. 
        //I used %20 which is URL space character. 
        str += "\n" + type;
        //str = str + type"\n" means it will concatenate a new line after we type a string(type)
        return str;

      }
    }
    return "404 Not Found!";
  }
}

class StringServer {
  public static void main(String[] args) throws IOException {
      if(args.length == 0){
          System.out.println("Missing port number! Try any number between 1024 to 49151");
          return;
      }

      int port = Integer.parseInt(args[0]);

      Server.start(port, new Handler());
  }
}
```
Let's build and run! 
In the terminal write :
``` 
    => javac Server.java StringServer.java
    => java StringServer 2800
    Server Started! Visit http://localhost:2800
```
Then it will look like :
<br> <img width="448" alt="Screen Shot 2023-04-22 at 1 57 06 AM" src="https://user-images.githubusercontent.com/62029893/233774290-22aa1af5-93cc-4f6c-83fe-446b9b83ae11.png">
<br>Now visit to the link "http://localhost:2800"
<br>
<br>
<br>Type ```/add-message?s=Hello``` after the domain
<br>Then you will see this page:
<br><img width="718" alt="Screen Shot 2023-04-22 at 2 00 45 AM" src="https://user-images.githubusercontent.com/62029893/233774480-a4edf0b0-67dc-41c2-8803-780d5abc8c63.png">
<br>
<br>**Methods that is used**
<br>*I have put comments in the code for most annotation, so let's find which methods were used in this code*
<br><sub>Method: it is a code that take an action on a specific task</sub>
<br>(1) handleRequest()
<br>(2) getPath()
<br>(3) contains()
<br>(4) getQuery()
<br>(5) split()
<br>(6) equals()
<br>(7) replace()
<br>(8) parseInt()
<br>(9) start()
<br>
<br>*Let's dive in more deeply!*
<br>First, we have initialized an empty string as 'str' in order to concatenate a new string when it's added which will be a Handler class's field. **handlerRequest** method who has 'URI'object as an argument will print the URL path. Then, it will check if there is "/add-message" included in the URL path. In this case, yes there is, so it will split the query by "=" character. Then "s" and "Hello" is divided! If the first parameter which is the key parameter equals to "s", it will replace "%20" character in the second parameter(value parameter) into space. However,"Hello" value has no space so the "type" value will assign "Hello\n" to be concatenate into 'str'.
<br>
<br>Type ```/add-message?s=How are you``` now
<br>Let's see what we have!:
<br><img width="758" alt="Screen Shot 2023-04-22 at 2 04 42 AM" src="https://user-images.githubusercontent.com/62029893/233774621-16e6358b-c71e-4a3e-b4d9-bdcb85e5ae0b.png">
<br>
<br>**Methods that is used**
<br>(1) handleRequest()
<br>(2) getPath()
<br>(3) contains()
<br>(4) getQuery()
<br>(5) split()
<br>(6) equals()
<br>(7) replace()
<br>(8) parseInt()
<br>(9) start()
<br>*Let's dive in more deeply!*
<br>Now we have typed 'Hello', the value of 'str' is 'Hello\n'. When we type 'How are you' in the query, in the **handlerRequest**, method URI argument will call 'add-message/?s=How%20are%20you. If statement will determine it is true because it's URL contains '/add-message'. Then, it will split the query by "=" character. Then "s" and "How%20are%20you" is divided! Like we did above, because the key parameter is equal to "s", it will replace "%20" character in the value parameter into space. Then the type variable will be 'How are you' replacing %20 into space. Finally, 'str' will be 'str = 'Hello\n' + 'How are you\n'' with **handleRequest** method returning 'Hello\nHow are you\n'. 
<br>
<br>
## Part 2: Bugs
<br>In part 2, we are going to look at a code that has a bug. Knowing the 'failure-inducing input' for the buggy program, the symptom and fixing the bug is very important! Let's figure these out by following below.
<br>
<br>The code will be the method ```reverseInPlace``` in ```ArrayExamples.java```. 
<br><sub>See the picture below</sub>
<br><img width="553" alt="Screen Shot 2023-04-24 at 8 00 14 PM" src="https://user-images.githubusercontent.com/62029893/234163869-a06c5465-2957-4f8f-910c-5d0dc50bc9ce.png">
<br>
<br>
### 2-1) A failure-inducing input 
<br>
**"Failure-inducing input** is 'how you set things up to run the program to get that bad result'. For example, run the program with some specific method arguments, run the program with some specific command line arguments, or run the program at all from the command line. 

<br>As we can see the results applying several failure-inducing inputs, we can see that while this method aims to reverse the original array in place, it actually overwrites the first array with the value from the last array.<br>
<br>**First failure-inducing input = {1,2,3}** <br>
```java
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = {1,2,3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3,2,1}, input1);
	}
}
```
<br><img width="714" alt="Screen Shot 2023-04-24 at 8 26 16 PM" src="https://user-images.githubusercontent.com/62029893/234167961-a804e90b-037d-4483-bd6f-c5154ca8bd51.png"><br>
<br>
<br>**Second failure-inducing input = {50,60,70}** <br>
```java
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = {50,60,70};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{70,60,50}, input1);
	}
}
```
<br><img width="714" alt="Screen Shot 2023-04-24 at 8 26 47 PM" src="https://user-images.githubusercontent.com/62029893/234168039-ca315ae0-d25c-4ef3-8663-cd1a33e60e0d.png"><br>
<br>
<br>**Third failure-inducing input = {11,12,14}** <br>
```java
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = {11,12,14};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{14,12,11}, input1);
	}
}
```
<br><img width="714" alt="Screen Shot 2023-04-24 at 8 27 32 PM" src="https://user-images.githubusercontent.com/62029893/234168085-17685217-985c-4ba6-9653-72efebe89d92.png">
### 2-2) An input that **doesn't** induce a failure
The inputs that doesn't induce a failure will be a pair of same number. It will be the same even the first value replaces the last value.
<br>For example, "input1 = {1,1};" 
```java
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = {1,1};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{1,1}, input1);
	}
} 
```
<br><sub>If we run the JUnit test it will show this result</sub>
<br><img width="709" alt="Screen Shot 2023-04-24 at 7 58 29 PM" src="https://user-images.githubusercontent.com/62029893/234165050-ca007ca0-bd8d-4b19-b7df-fedee8698f80.png"> 

### 2-3) The symptom 
<br>Let's see the output of running the tests with the input that we want them to be reversed in the output. I'll give 2 examples below. 
<br>(1)
<br><img width="717" alt="Screen Shot 2023-04-24 at 8 58 03 PM" src="https://user-images.githubusercontent.com/62029893/234171132-54107cbd-6b33-478c-8abc-7c3dc4ba4b27.png"><br>
<br>
<br>
<br>(2)
<br><img width="717" alt="Screen Shot 2023-04-24 at 8 56 42 PM" src="https://user-images.githubusercontent.com/62029893/234170968-58874fdc-0465-4b6a-80d8-be5a55bd2945.png">
<br>
<br>=>So the symptom is if each array is index [0],[1],[2],[3], index [3],[2],[1],[0] should be changed in order, but index[0] is changed to index[3], index[1] to index[2], index[2] to index[1], and index[3] to index[0], so it is overwritten.


### 2-4) The bug, as the before-and-after code change

