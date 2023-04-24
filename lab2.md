# Lab Report 2
## Part 1
<br/>
This part is to create a web server that "keeps track of a single string that gets added to by incoming requests" (week3 lab report 2). <br/>
<br/>
__Code for StringServer:__ <br/>
![Image](lab2_1.1.png)<br/>
<br/>
__Screen Shot for__  ```/add-message?s=Hello``` <br/>
![Image](lab2_1.2.png) <br/>
* In this example, methods ```public String handleRequest(URI url)``` and ```start()``` of Server Class as well as the main method are called.
* In the handleRequest method, an argument ```URI url``` is passed in for the method to modify the request and query. The variable ```String str``` in the Handler class stored the string value from the query and keeps track of it as more queries are passed in.
__Screen Shot for__  ```/add-message?s=Hello``` __&__ ```/add-message?s=How are you```<br/>
![Image](lab2_1.3.png) <br/>
