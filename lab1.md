This is a tutorial for incoming cse15L students as well as future me on how to login to the course-specific account on ieng6. <br/>
<br/>
The tutorial is conducted on windows and screenshots are taken accordingly. For commands on macOS, go to https://ucsd-cse15l-s23.github.io/week/week1/ for more information. <br/>
<br/>
__Step 1: Install VSCode__<br/>
Go to https://code.visualstudio.com/ and download VSCode according to your operating system.<br/>
After installation, you should get something like this: <br/>
![Image](vscode1.png) <br/>
<br/>
__Step 2: Install git and make git bash your terminal for login server__<br/>
Go to https://gitforwindows.org/ and download git for windows.<br/>
Go to https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994 and change the terminal in vscode to bash terminal.<br/>
<br/>
__Step 3: login to server__<br/>
Find your course specific account at https://sdacs.ucsd.edu/~icc/index.php <br/>
You might need to reset your password if you are logging in for the first time. <br/>
A tutorial for resetting password could be found here https://drive.google.com/file/d/17IDZn8Qq7Q0RkYMxdiIR0o6HJ3B5YqSW/view?usp=share_link <br/>
Once you're set, go to bash terminal in vscode and type in "ssh" followed by your course specific username + "@ieng6.ucsd.edu" <br/>
If it shows "connection denied by host" or something like that, try adding "-202" which appoints to a specific server following "@ieng6" <br/>
For the first time login, it may ask to whether to continue connecting or not; type yes in command <br/>
You will get something like this: <br/>
