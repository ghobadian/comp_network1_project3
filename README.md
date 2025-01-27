# Go-Back-N and CRC Implementation in Socket Programming

## Project Overview

This project is an implementation of the Go-Back-N protocol and Cyclic Redundancy Check (CRC) method for error detection and correction in computer networks. The project utilizes socket programming to simulate network communication between a client and a server.

### Key Features

1. **Error Detection with CRC**: The project uses CRC to detect errors in transmitted data.
2. **Error Correction with Go-Back-N**: The Go-Back-N protocol is implemented to handle error correction by retransmitting lost or corrupted packets.
3. **Socket Programming**: The communication between the client and server is handled using socket programming.
4. **Acknowledgements (ACKs) and Timeouts**: ACKs are used for packet delivery confirmation, and timeouts are set to handle lost packets.

### Implementation Details

1. **Cyclic Redundancy Check (CRC)**:
   - Generates a codeword by appending the Frame Check Sequence (FCS) to the data.
   - Used at both the sender and receiver ends to ensure data integrity.

2. **Go-Back-N Protocol**:
   - Maintains a window of packets that are sent but not yet acknowledged.
   - Retransmits packets starting from the first unacknowledged packet upon detecting an error or timeout.

3. **Socket Programming**:
   - The project is implemented using socket programming to establish communication between a client and a server.
   - Both TCP and UDP protocols are supported, but TCP is used for its reliability features.
   - The user interface (UI) is designed for easy interaction and visualization of the data transmission process.

4. **Using Hamming Code**: 
   - Implement Hamming code on both sender and receiver sides to enable error detection and correction.

5. **Adding Other Error Detection Methods**: 
   - Add methods such as 2D parity, parity check, checksum for error detection.

6. **Implementing Two-Way Socket Programming**: 
   - Implement Socket programming on both sending and receiving ends and cover all mentioned cases.

8. **User Interface (UI)**:
   - Implement a user-friendly interface to display the data transmission process.


### Project Components

- **CRC Implementation**: Handles error detection by calculating and verifying CRC codes.
- **Go-Back-N Protocol**: Manages error correction through selective retransmission of packets.
- **transmitter and receiver**: Two separate programs simulating the transmitter and receiver roles in a network.
- **Error Handling**: Includes mechanisms for handling lost packets, timeouts, and retransmissions.

### How to Run

1. **receiver**: Start the receiver program which will wait for connections from transmitters.
2. **transmitter**: Run the transmitter program to connect to the receiver and begin data transmission.
3. **Data Transmission**: The transmitter sends packets to the receiver, which acknowledges receipt. The CRC and Go-Back-N protocols handle error detection and correction.



### References

- [Socket Programming in Python](https://realpython.com/python-sockets/)
- [Hamming Code in Computer Networks](https://www.geeksforgeeks.org/hamming-code-in-computer-network/)

