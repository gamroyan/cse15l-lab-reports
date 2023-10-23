# Lab Report 2 - Servers and SSH Keys (Week 3)
## Part 1:
### Code for StringServer:
![Image](lab2-code.png)

### examples:
![Image](lab2-ex1.png)
The main method is initially called, which calls the Handler class, containing the handleRequest and addMessage methods. The relevant arguments in these methods are the url in handleRequest and message in addMessage. The index is a relevant field of the class that incremented the number of the list by 1. In this example, the value of the index was not modified and remained at 1. The String message is also a relevant field of the class, which holds the value of parts[1], where parts is a list that organizes information within the query. Specific to this request, parts[1] equaled "how are you."

![Image](lab2-ex2.png)
In this request, the main method, handleRequest, and addMessage methods were all called. The relevant arguments were the url in handleRequest and message in addMessage. The index is a relevant field of the class, which was modified in this example and was incremented by 1. Since this was not the first request, the next number in sequence was index = 2. Additionally, message had a different value, which was "hello." Since this string contained no spaces, it didn't need to be further modified in the addMessage method.

## Part 2:
![Image](labreport2-2.1.png)

The private key for my SSH key for logging into ieng6 is /Users/gayaneamroyan/.ssh/id_rsa and the path to the public key is /Users/gayaneamroyan/.ssh/id_rsa.pub

![Image](labreport2-2.2.png)

## Part 3:
In the past few weeks of lab, I've learned how to use and work with many new commands in the terminal. One topic that really stood out to me was writing and running the servers since doing that was completely new to me. Running the website on the ieng6 server was very interesting. Also, before these few weeks, I had no idea what was stored in URLs or how they were formatted. 
