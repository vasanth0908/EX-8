# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER
EXP: 8
DATE:26-04-2023
AIM:
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

ALGORITHM:
Import the necessary modules in python
Create a socket connection to using the socket module.
Send message to the client and receive the message from the client using the Socket module in server.
Send and receive the message using the send function in socket.
PROGRAM:
CLIENT:
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
SERVER:
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   c.send(ClientMessage.encode())
OUTPUT :
![1](https://github.com/vasanth0908/EX-8/assets/122000018/c43e625b-6ca0-4a60-bf5c-d30b58b8e724)

![2](https://github.com/vasanth0908/EX-8/assets/122000018/916c0872-a4b6-4fba-8afa-95cf384e467f)




RESULT :
APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER EXECUTED SUCCESSFULLY
