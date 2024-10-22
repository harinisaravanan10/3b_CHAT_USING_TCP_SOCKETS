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
SERVER
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
CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())


```
## OUPUT
SERVER
![Screenshot 2024-10-22 084430](https://github.com/user-attachments/assets/50bb8fe2-2503-4c43-ad36-d8a7acf9f932)
CLIENT
![Screenshot 2024-10-22 084421](https://github.com/user-attachments/assets/fdaa1c62-e12e-4116-9920-a446fc22bfd1)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
