# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name: KISHORE NARAYANAN S R
## Reg.No: 212223110023
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### client.py
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server.py
```python
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
## OUTPUT
### client.py
![image](https://github.com/user-attachments/assets/25c1672a-610e-4c05-8c3d-529746c86dbb)

### server.py
![image](https://github.com/user-attachments/assets/a519dc13-3d0c-40d4-801c-2a10e2a12f5e)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
