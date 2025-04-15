This project provides a basic client-server chat application in Java that features both a console-based interface and a GUI-based interface. The application allows users to connect to a server, join the chat, send and receive messages, and interact with other users in real-time. Here's a breakdown of the key components and features of the application:

Server:
ServerSocket: The server listens for incoming client connections on a specific port (e.g., 8080) and accepts them.

User Management: Each user is represented by a User object, which contains the user's nickname, input/output streams, and connection details.

Message Broadcasting: The server can broadcast messages to all connected users or send private messages to specific users.

User List Management: The server maintains a list of all connected users and can broadcast this list to the clients at any time.

Private Messaging: Users can send private messages to other users by using the "@" symbol followed by the recipient's nickname.

Client:
Console Client: A basic command-line interface that allows users to input their nickname and send messages to the server.

GUI Client: A more advanced graphical user interface (GUI) for the chat application using Java Swing. It allows users to interact with the chat using:

Chat History: Display of the chat history in a scrollable pane.

User List: A pane showing the list of connected users.

Message Input: A text field for inputting messages, with the ability to send messages by pressing the "Enter" key.

Color Customization: Users can change their nickname color using a command like #hexColor.

Emojis: Users can include emojis in their messages by typing common emoticon codes (e.g., :), :D).

Send and Disconnect Buttons: Buttons for sending messages and disconnecting from the server.

Features:
Connection: Users connect to the server by providing their nickname, server address, and port.

Message Exchange: Both the server and client can send and receive messages. The server broadcasts messages to all clients or sends them to specific users.

User Interaction: Users can see who is online in real-time, send messages to all users or privately to specific users.

Emoticons: Users can send emoticons like smiley faces, frowns, and more.

Color Customization: Users can change their display color by entering a valid hexadecimal color code.

Server Logic:
Handling Clients: When a client connects, the server creates a new User object, assigns it a nickname, and starts a new thread to handle the client's messages.

Broadcasting Messages: Messages are broadcasted to all users, and if a user sends a private message, it is sent only to the specified recipient.

User Removal: If a user disconnects, they are removed from the server's list of active users.

Client Logic:
Message Sending: The client can send messages by typing them into a text field or by pressing the "Send" button.

Receiving Messages: The client continuously listens for incoming messages from the server and displays them in the chat window.

Nickname and Server Information: The client asks for a nickname when first connecting and allows the user to specify the server's address and port.

How to Run:
Start the Server: Run the Server class to start the server on the desired port.

Start the Client: Run the ClientGui or Client class to connect to the server. The GUI version offers a more user-friendly interface, while the console version is simpler and more lightweight.

Interact: Once connected, users can chat, see each other's messages, and manage their connections.

Improvements & Enhancements:
File Transfer: Implementing file transfer capabilities between clients.

Private Chats: Enhancing private messaging with more detailed handling.

Persistent Data: Adding a database to store chat history or user information.

This application is a great starting point for building more complex real-time messaging systems, and it demonstrates the basics of socket programming, multithreading, and GUI development in Java.








