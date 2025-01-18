# CS2600 Project 2: Chat App

This project is a basic chat application written in C for the CS2600 Systems Programming course. It includes a client-server model where clients can send messages to a server, which relays them to all connected clients and logs the conversation to a file.

## Project Description

The goal of this project was to create a prototype chat application demonstrating scalability and efficiency. The application consists of two main components:
- **Server:** Handles connections from multiple clients, broadcasts messages, and logs chat history.
- **Client:** Sends messages to the server and displays broadcasted messages from other users.

The scenario and requirements were fictional and intended for educational purposes.

## Features

1. **Server Functionality:**
   - Listens for incoming client connections on a specified port.
   - Broadcasts received messages to all connected clients.
   - Logs all messages to a file named `chat_history` in real-time.

2. **Client Functionality:**
   - Prompts users for a username upon startup.
   - Allows users to send messages to the server.
   - Displays messages broadcasted by the server, including those from other clients.

3. **Chat History:**
   - Maintains a persistent log of all messages in a session.
   - Can be closed gracefully using `$ kill <pid>` with real-time logging to avoid data loss.

## How to Use

### Setting Up

1. Clone the repository:
   ```bash
   git clone https://github.com/KhaledKorfali2/cs2600_Project2_C_Chat_App.git
   cd cs2600_Project2_C_Chat_App
   ```

2. Compile the client and server using the provided Makefile:
   ```bash
   make
   ```

   This generates two executables: `chat_client` and `chat_server`.

### Running the Server

1. Start the server with a specified port:
   ```bash
   ./chat_server <port_number>
   ```

### Running the Client

1. Start the client, connecting to the server on the same port:
   ```bash
   ./chat_client <server_ip> <port_number>
   ```

2. Enter a username when prompted and start chatting!

### Multi-User Chat

To test the chat app with multiple users:
1. Open multiple terminal sessions.
2. Start the server in one session.
3. Run the client in other sessions, passing the server's IP and port.
4. Chat messages will be broadcasted to all connected clients.

### Stopping the Server
- Use `Ctrl+C` or `$ kill <pid>` to terminate the server.
- Check the `chat_history` file for a log of the session.

## Testing and Verification

To test the application:
1. Start the server on one terminal.
2. Run the client on multiple terminals or devices.
3. Exchange messages and verify:
   - Messages are broadcasted correctly.
   - The `chat_history` file is updated in real-time.
4. Switch roles with a partner, letting them host the server and connecting your client.
