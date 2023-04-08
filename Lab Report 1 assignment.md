# Hi! So today we are going to learn about *remote access* that you will learn in CS15l. You'll be following steps that I provide below to log-in to a specific account on ieng6 .

## 1st Step : Creating CSE15L Account 

Go into this link -> [Link](https://sdacs.ucsd.edu/~icc/index.php)
<br> You will see a page like this 
<br> <img width="672" alt="Screen Shot 2023-04-05 at 5 39 27 PM" src="https://user-images.githubusercontent.com/62029893/230244041-bf2412d3-bccf-4136-88df-5611a539447c.png">
<br>Type your username and PID there to find your account that you use in UCSD.
<br>After you *submit*, you will see this page 
<br>![Screen Shot 2023-04-05 at 5 42 05 PM](https://user-images.githubusercontent.com/62029893/230244755-af37a4d8-1edd-46e2-8a45-cade18c7730f.jpg)
The 11 letters inside a red circle is your additional account and you will be using this account name!
<br>Next step is to reset your password. **REMAIN IN THE PAGE THAT YOUR ARE IN!** 
<br>This time click the "*change your password*" link shown as below.
<br>![Screen Shot 2023-04-05 at 5 42 05 PM 3](https://user-images.githubusercontent.com/62029893/230245705-708cd13b-deb1-4cb7-aff8-06353ffae0fe.jpg)
<br>Enter your username which is your 11 digit additional account name. *It's not your UCSD username so keep that in mind*
<br><img width="643" alt="Screen Shot 2023-04-05 at 6 03 07 PM" src="https://user-images.githubusercontent.com/62029893/230246958-8422b26e-33d6-422d-9422-c97bee0ff088.png">
<br> 
Your 1st step is **almost** done!
<br>*Remain on this process if you are Mac if you are a Window user, go to step 2*. 
<br>Open your terminal(if you are using Window you have to download Visual Studio Code). *I will tell you how to download VS Code later on* 
<br>Try ssh 11DIGIT OF ADDITIONAL ACCOUNT_NAME @ ieng6.ucsd.edu in your terminal. Then enter your new password.  
<br>*"you can't see the password when you are typing in. You are doing it right, so no worries :)"*<br>
![Image 4-5-23 at 6 06 PM](https://user-images.githubusercontent.com/62029893/230247403-6d6c0c7d-7560-4e62-b64e-b57dd56e1833.jpg)
<br>If you are seeing this page in your terminal you are all set! **CONGRATULATION!**

## 2nd Step : Using Visual Studio Code (Window and also Mac)

This step is easy to clear!
<br>Go to this link -> [Link](https://code.visualstudio.com/)
If you are using Mac, download macOS Universial version. If you are using Windows, click Windows x64 User Installer. **EASY RIGHT?** 
<br>After you install open it and you will see this system page. 
<br> <img width="899" alt="Screen Shot 2023-04-05 at 6 23 49 PM" src="https://user-images.githubusercontent.com/62029893/230249178-4936d769-40dd-4092-97ab-6b179224f5c2.png">
<br>Click "New File" 
<br>You can just open any files you have in your computer OR open a text file as below
<br><img width="604" alt="Screen Shot 2023-04-08 at 12 02 04 PM" src="https://user-images.githubusercontent.com/62029893/230739945-adbedb7f-8594-4be3-a8dd-85edff8dc1f6.png">
<br>
<br>Then click "New Terminal" to open the terminal page in VSCode. See the picture below as well
<br> <img width="604" alt="Screen Shot 2023-04-08 at 12 02 04 PM" src="https://user-images.githubusercontent.com/62029893/230739976-a19b0fff-785e-4797-8bef-a872c9624c4f.png">
<br>Type "ssh cs15lsp23xx @ ieng6.uscd.edu" the 11 digit of your additional account name @ ieng6.ucsd.edu in the terminal to switch to another computer. That's what **"ssh"** does! 
<br><img width="655" alt="Screen Shot 2023-04-08 at 11 59 13 AM" src="https://user-images.githubusercontent.com/62029893/230740033-465bf0f7-92ea-4306-a6be-8a15b4f90852.png">
<br>Put your password below the ssh command. *YOU CAN'T SEE THE PASSWORD THAT YOU ARE TYPING* **IT'S A SECRET MODE SO JUST GO ON :)** 
<br> Now you finshed making a terminal signing into your additional account. 
<br>

## Last Step : Trying Some Commands 

Now this is the real part! Let's write some commands in the terminal. 
<br>I'll give you some commands that you can type and follow. 
<br>*Keep in mind you have to write after a dollar sign*
<br>1.pwd
<br>2.ls
<br>3.ls -lat
<br> Windows and Mac Version using VSCode 
<br><img width="655" alt="Screen Shot 2023-04-08 at 12 00 39 PM" src="https://user-images.githubusercontent.com/62029893/230740148-9487742a-6088-47db-aefd-1ae550ccc5c8.png">
<br>
<br>
<br> Only Mac Version
<br><img width="563" alt="Screen Shot 2023-04-05 at 7 01 35 PM" src="https://user-images.githubusercontent.com/62029893/230253660-1d1281e8-449b-4f93-afda-6edad694fa54.png">
<br>Each of the command you type you can see the results like above. 
<br>I will tell you guys the definition of each commands and give you some examples to work on 
<br>**pwd**: print working directory 
<br>It shows you the whole pathname of your current working directory.
<br>EX)/home/linux/ieng6/cs15lsp23/cs15lsp23an 
<br>
<br>**ls**: list files or directories 
<br>It shows you the list of files of your current working directory. 
<br>EX)per15
<br>
<br>**ls -lat**: list 
<br>“ls -lat” is a command that shows all the files that I have even the hidden ones. When I just type “ls”, ‘per15’ only appears on my terminal however, when I type “ls -lat” I can see the hidden ones including ‘per15'.
<br>
<br>
<br>Now try it on your own! I'll give you some lists
<br>* cd
<br>* cd~
<br>* ls -a
<br>* cp /home/linux/ieng6/cs15lsp23/public/hello.txt~/
<br>
<br>**CONGRATS!!** Your are ready to go:)





















