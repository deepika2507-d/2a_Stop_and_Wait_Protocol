# 2a_Stop_and_Wait_Protocol
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
 CLIENT:
 
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

 SERVER:
 
 import socket
 
 s=socket.socket()
 
 s.connect(('localhost',8000)
## OUTPUT
CLIENT:
![Screenshot (56)](https://github.com/user-attachments/assets/96dbe12e-79dd-46a3-9767-ab703d3f76bc)
SERVER:
![Screenshot (57)](https://github.com/user-attachments/assets/22f5c62b-a9f3-4275-a397-b1b0802c2c25)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
