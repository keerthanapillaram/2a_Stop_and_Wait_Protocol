# 2a_Stop_and_Wait_Protocol
## Name : Keerthana P 
## Register number : 212223240069
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
```
DEVELOPED BY: P Keerthana
REG : 212223240069
```
## ClIENT:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
i=input("Enter a data: ")
c.send(i.encode())
ack=c.recv(1024).decode()
if ack:
print(ack)
continue
else:
c.close()
break
```
## SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```

## OUTPUT

## ClIENT:
![image](https://github.com/user-attachments/assets/3441b197-7542-4a86-b873-841deef2a48c)


## SERVER:
![image](https://github.com/user-attachments/assets/3dc977c5-8a3c-4519-a5b4-ef3815f4d63c)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
