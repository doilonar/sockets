# Socket Connection Flooder


This is a simple C program that initiates multiple TCP socket connections to a specified target IP and port. It uses POSIX threads (`pthread`) to create a user-defined number of concurrent connections for a set duration.

## How It Works

The program prompts the user for four inputs:
1.  **Target IP:** The IP address of the server to connect to.
2.  **Target Port:** The port number on the server.
3.  **Threads:** The number of concurrent sockets to open. Each thread will manage one socket connection.
4.  **Time:** The duration in seconds the program will maintain the connections before exiting.

Each thread creates a socket, connects to the target, and then enters an infinite loop to keep the connection alive until the main program terminates.

## Compilation

To compile the program, you need a C compiler (like a gcc) and the `pthread` library. Use the following command:

```bash
gcc sockets.c -o sockets -lpthread
```

## Usage

1.  Compile the program as shown above.
2.  Run the executable:
    ```bash
    ./sockets
    ```
3.  Enter the requested information at the prompts:

    ```
    ip:127.0.0.1
    port:8080
    threads:100
    time of program(sec):60
    attack...
    ```

The program will then create 100 connections to `127.0.0.1:8080` and hold them for 60 seconds before exiting.
