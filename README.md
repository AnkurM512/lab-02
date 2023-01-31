# Lab 2
[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repo and clone it to your machine to get started!

## Team Members
Ankur Mathur
Worked with: Jerry and Munir

## Lab Question Answers

Answer for Question 1: 
The reliability of UDP decreased when 50% loss was added. This happened because half of the messages that were sent by the client were lost in
transmission, making it less reliable.

Answer for Question 2:
The reliability for TCP remained the same after 50% loss was added. TCP was just as reliable because no messages were lost during transmission. No messages were lost because TCP can detect when messages were lost and resends them. 

Answer for Question 3:
Some of the messages took longer to arrive. This is because TCP can detect when a message is lost and it tries to correct the mistake by resending the message. Because TCP has to spend more time resending messages that were lost, this causes a delay since it resends the lost message first, then sends the other messages in the queue. 

Questions in tcp_server.c:
1. argc stores the number of arguments entered on the command line as an integer. *argv[] is a char array that contains pointers to strings. The first index stores the program name and the ones after that store the argument entered in the command line.
2. A file descriptor is where the operating system creates an entry to represent each file that is opened. A file descriptor table is the collection of indeces of each file that is in the file descriptor.
3. A struct is a precursor to a class in C++. It allows the user to store many variables of different types. sockaddr_in has variables short sin_family, unsigned short sin_port, struct in_addr sin_addr, and char sin_zero[8]. 
4. The input parameters of socket are int family, int type, and int protocol. The return value of socket is a positive integer if successful and -1 if there was an error.
5. The input parameter of listen is a socket object. The input parameters of bind is a socket object, sockaddr struct which is a pointer, and the length of the sockaddr struct.
6. while(1) is used to keep the server open to receive messages from the client. This could be a problem for multiple connections because the server would only connect to the client that connects first and will be unable to connect to any others after because it is an infinite loop connected to that client.
7. The fork() command creates a child process that is an exact copy of the calling process. This can be used within the while(1) loop to make a copy of the server process and accept a connection from another client, allowing the server to handle multiple clients.
8. A system call is the way in which a program requestes a service from the operating system. 
...
