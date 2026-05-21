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
##SERVER
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
##CLIENT
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
~~~


## OUTPUT
##SERVER

<img width="947" height="151" alt="Screenshot 2026-05-21 122352" src="https://github.com/user-attachments/assets/d73d12bd-7c98-404d-9442-9fe21af2c8bb" />


##CLIENT


<img width="810" height="212" alt="Screenshot 2026-05-21 122334" src="https://github.com/user-attachments/assets/3d6a3cd7-0f29-4efd-bd67-927d6d1548d8" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
