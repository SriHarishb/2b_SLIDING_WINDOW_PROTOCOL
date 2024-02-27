# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL

### Name: Sri Harish B
### Reg No: 212223220110
### Dept: Btech-IT


## AIM
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM

### CLIENT-
 import socket
 s=socket.socket()
 s.bind(('localhost',8000))
 s.listen(5)
 c,addr=s.accept()
 size=int(input("Enter number of frames to send: "))
 l=list(range(size))
 s=int(input("Enter Window size:"))
 st=0
 i=0

### SERVER-
 while True:
Thus, python program to perform stop and wait protocol was successfully executed
 while(i<len(l)):
    st+=s
    
    c.send(str(l[i:st]).encode())
    
    ack=c.recv(1024).decode()
    
    if ack:
    
        print(ack)
        
        i+=s

## OUPUT

### CLIENT-
![Screenshot 2024-02-27 220601](https://github.com/SriHarishb/2b_SLIDING_WINDOW_PROTOCOL/assets/150308442/99d9a068-5f81-48ac-825f-56cd49a041a1)

### SERVER-
 ![Screenshot 2024-02-27 220608](https://github.com/SriHarishb/2b_SLIDING_WINDOW_PROTOCOL/assets/150308442/e3175d2d-bd5c-4f9e-b3c7-046f5d1b1a6b)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed
