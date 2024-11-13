# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT:
```PYTHON
DEVELOPED BY : Kanagavel A K
REGISTER NO : 212223230096
```
```PYTHON
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER:
```PYTHON
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
![image](https://github.com/user-attachments/assets/af918fa7-b2af-41d3-b004-e276da72fee5)
![image](https://github.com/user-attachments/assets/5d5b7091-ee29-454b-9536-a192945e1bc2)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
