# 3b.CREATION FOR CHAT USING TCP SOCKETS
# NAME:SANJITH R
# REG NO:212223230191
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## Server
``` 

import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
## Server
![image](https://github.com/user-attachments/assets/1cc5bd3f-3532-48d9-9817-d0db66ebc3e3)
## Client
![image](https://github.com/user-attachments/assets/3b1a0c10-a155-4e08-a57e-2ca6c9fd9b6e)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
