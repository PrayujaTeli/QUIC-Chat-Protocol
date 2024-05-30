# QUIC-based Real-Time Chat Service

## Overview

A Python-based real-time chat service leveraging the QUIC protocol to provide seamless, secure, and efficient communication. Features include robust message delivery, connection negotiation, and extensibility for future enhancements.

## Features

- **Real-time Messaging**: Clients connect to the server and send text messages that are broadcast to other clients.
- **Message Exchange**: Clients initiate a connection using QUIC and can send messages to multiple clients simultaneously.
- **Connection Negotiation**: During the initial handshake, connection parameters such as supported features and encryption settings are negotiated.
- **Message History**: Messages persist on the screen during each run, maintaining the conversation flow.

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
   python3 main.py server
   ```
5. Run the client:
   ```bash
   python3 main.py client
   ```

## Usage

1. Start the server by running `server`.
2. Connect a client by running `client` with the appropriate connection parameters.
3. Begin chatting with other connected clients.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## Acknowledgments

This project was developed as part of the CS544 coursework. Special thanks to the course instructors Brian Mitchell.
```
