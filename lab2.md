# Lab Report 2
## Part 1
This part is to create a web server that "keeps track of a single string that gets added to by incoming requests" (week3 lab report 2). <br/>
<br/>
__Code for StringServer:__ <br/>
![Image](lab2_1.1.png)<br/>
<br/>
__Screen Shot for__  ```/add-message?s=Hello``` <br/>
<br/>
![Image](lab2_1.3.png)
* In this example, methods ```public String handleRequest(URI url)``` and ```start()``` of Server Class as well as the main method are called.
* In the handleRequest method, an argument ```URI url``` is passed in for the method to modify the request and query. The variable ```String str``` in the Handler class stored the string value from the query and keeps track of it as more queries are passed in.
* ```url.getPath()``` gets the request from the url and determines the following action.
* ```url.getQuery()``` gets the query from the url and determines the value to stroe in the string field.
* There are also minor methods like ```parseInt()``` and ```equals()``` but they are mainly for modifying Strings, not handling the requests.
* In this request, the value of field "str" is changed as the string value "Hello" from the query is added to it and gets displayed.
<br/>
<br/>
__Screen Shot for__  ```/add-message?s=Hello``` __&__ ```/add-message?s=How are you```<br/>
![Image](lab2_1.4.png)
<br/>
* In this example, methods ```public String handleRequest(URI url)``` and ```start()``` of Server Class as well as the main method are called.
* In the handleRequest method, an argument ```URI url``` is passed in for the method to modify the request and query. The variable ```String str``` in the Handler class stored the string value from the query and keeps track of it as more queries are passed in.
* ```url.getPath()``` gets the request from the url and determines the following action.
* ```url.getQuery()``` gets the query from the url and determines the value to stroe in the string field.
* There are also minor methods like ```parseInt()``` and ```equals()``` but they are mainly for modifying Strings, not handling the requests.
* In this request, the value of ```str``` is changed twice as not only "Hello" but also later "How are you" is added one by one to ```str```.
<br/>
<br/>
__Screen Shot for__ no request given: <br/>
![Image](lab2_1.2.png)
<br/>
When either no request nor no correct query is given, the method ```handleRequest``` returns 404 and displayed it.
<br/>
<br/>
## Part 2
This part demonstrates one of the bugs from lab 3 and its fix. <br/>
The origninal code with bug is: <br/>
```static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }``` <br/>
  which attempts to return an array of the elements in input array in reverse order.<br/>
