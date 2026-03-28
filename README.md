# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True:
     msg=input("Client > ") 
     s.send(msg.encode()) 
     print("Server > ",s.recv(1024).decode()) 

```

### Server
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True:
      ClientMessage=c.recv(1024).decode() 
      c.send(ClientMessage.encode()) 
```

## OUPUT

<img width="1917" height="1144" alt="Screenshot 2026-03-17 210417" src="https://github.com/user-attachments/assets/7c0bbdf2-642c-46fe-8583-a4686b3629de" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
