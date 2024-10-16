# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
 ### Name : VIJEY K S
### Register No : 212223040239
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT.PY:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER.PY:
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
## CLIENT.PY:

![Screenshot 2024-10-16 110909](https://github.com/user-attachments/assets/17cac651-f207-473b-9869-b26eea75e8e2)


## SERVER.PY:
![Screenshot 2024-10-16 110923](https://github.com/user-attachments/assets/556241d5-b05d-4ba4-a57d-d64167c6f506)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
