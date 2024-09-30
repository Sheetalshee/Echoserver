# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
### Server code:
```
import socket
HOST = "127.0.0.1" 
PORT = 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
### Client code:
```
import socket
HOST = "127.0.0.1"
PORT = 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT)) 
    s.sendall(b"Sheetal.R,")
    s.sendall(b"212223230206")
    data = s.recv(1024)
print(f"\nRecived {data!r}") 
```

## OUTPUT:
### Server side:
![Screenshot 2024-09-30 100524](https://github.com/user-attachments/assets/3845d080-509a-4e2f-b996-f43557c9e6b9)


### Client side:
![Screenshot 2024-09-30 100445](https://github.com/user-attachments/assets/d98869e9-c329-4526-88c7-9751f5233661)




## RESULT:
The program is executed successfully.
