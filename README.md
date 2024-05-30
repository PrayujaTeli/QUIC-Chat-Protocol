### QUIC-based Real-Time Chat Service

A Python-based real-time chat service leveraging the QUIC protocol to provide seamless, secure, and efficient communication. Features include robust message delivery, connection negotiation, and extensibility for future enhancements.

# QUIC-based Real-Time Chat Service

## Overview

This project is a Python-based real-time chat service designed using the QUIC protocol. It aims to provide users with a seamless messaging experience, supporting both casual conversations and group discussions with reliable and efficient message delivery.

## Features

- **Real-time Messaging**: Clients connect to the server and send text messages that are broadcast to other clients.
- **Message Exchange**: Clients initiate a connection using QUIC and can send messages to multiple clients simultaneously.
- **Connection Negotiation**: During the initial handshake, connection parameters such as supported features and encryption settings are negotiated.
- **Message History**: Messages persist on the screen during each run, maintaining the conversation flow.
- **Security**: Ensures message integrity and user authentication to prevent impersonation and unauthorized access.

## Protocol Details

### QUIC Packet Structure

- **Header**: Contains essential metadata like Packet Number (PN), Packet Type (PT), Connection ID (CID), Packet Number Length (PNL), Version (VER), and Packet Length (PL).
- **Frames**: Different frame types facilitate various aspects of communication, including Chat Message Frames, Ack Frames, Ping Frames, and Connection Close Frames.

### Message Types

- **Control Messages**: `CONNECT`, `ACK`, `DISCONNECT`
- **Data Messages**: Carries chat messages with fields for Sender ID and Recipient IDs.

### State Management

The chat protocol maintains state throughout the communication process using a Deterministic Finite Automaton (DFA) with states like Disconnected, Connecting, Connected, Disconnecting, and Error.

## Extensibility

The protocol is designed with flexibility to accommodate future extensions and updates. It includes mechanisms for version negotiation, backward compatibility, and protocol extensions.

## Security

- **Easy Login**: Users join the chat with a username or localhost.
- **User Identification**: Unique identifiers for users prevent impersonation.
- **Message Integrity**: Ensures messages are not tampered with during transmission.

## Performance

The protocol addresses performance metrics such as latency, throughput, and resource consumption, and includes strategies for handling network issues like congestion, packet loss, and jitter.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/quic-chat-service.git
   ```
2. Navigate to the project directory:
   ```bash
   cd quic-chat-service
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the server:
   ```bash
   python server.py
   ```
5. Run the client:
   ```bash
   python client.py
   ```

## Usage

1. Start the server by running `server.py`.
2. Connect a client by running `client.py` with the appropriate connection parameters.
3. Begin chatting with other connected clients.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## Acknowledgments

This project was developed as part of the CS544 coursework. Special thanks to the course instructors Brian Mitchell.
```
