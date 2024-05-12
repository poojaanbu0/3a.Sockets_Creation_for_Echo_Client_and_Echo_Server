# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

### Name: POOJA A
### Register No: 212222240072
### Date: 12-05-2024

# AIM
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server .
4. Send and receive the message using the send function in socket.
   
## PROGRAM
### Client: 
```python
import socket
s=socket.socket()
s.connect(('localhost',9000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

### Server:
```python
import socket
s=socket.socket()
s.bind(('localhost',9000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
 ```

## OUTPUT
![image](https://github.com/poojaanbu0/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/119390329/63b7cad2-e1e1-4f8c-a279-87acfda8f5e5)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
