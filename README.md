## HTTP-Client-Implementation
This project is to develop a client named httpc that provide the HTTP client library implementation. This library provides a command-line interface like cURL with basic functionalities.
The following presents the options of our final command line:

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<code>httpc (get|post) [-v] (-h "k:v")* [-d inline-data] [-f file] URL</code>
   
In the following, the purpose of the expected httpc command options is described:
- Option -v enables a verbose output from the command-line. 
- URL determines the targeted HTTP server. It could contain parameters of the HTTP operation.
- To pass the headers value to your HTTP operation, you could use -h option. The latter means setting the header of the request in the format "key: value."
- -d gives the user the possibility to associate the body of the HTTP Request with the inline data, meaning a set of characters for standard input.
- Similarly to -d, -f associate the body of the HTTP Request with the data from a given file.
- get/post options are used to execute GET/POST requests respectively. post should have either -d or -f but not both. However, get option should not used with the options -d or -f.

[Please click for more information.](https://github.com/DhwaniSondhi/cURL-like-Command-Line-Implementation/blob/master/Assignment%20Description.pdf)

### How to run?
- Install Java 8+.
- Run the command described above.

### OUTPUT
***Get with query parameters***<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;httpc get 'http://httpbin.org/get?course=networking&assignment=1'<br/>
***Output:***<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{ <br/>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"args": { "assignment": "1", "course": "networking" },<br/>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"headers": { "Host": "httpbin.org", "User-Agent": "Concordia-HTTP/1.0" }, <br/>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"url": "http://httpbin.org/get?course=networking&assignment=1" <br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}<br/>

***For more outputs, click the link given in the description***
