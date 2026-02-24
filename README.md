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
Client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True: 
    s.send(input("Client > ").encode())
    print("Server >",s.recv(1024).decode())
```
Server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(1)
c,_=s.accept()
while True: 
    c.send(c.recv(1024))
```
## OUPUT
<img width="1918" height="1141" alt="image" src="https://github.com/user-attachments/assets/f71e6345-e93a-4358-a92d-3479b111dbc8" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
