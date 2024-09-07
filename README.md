# Decentralized Distributed File Storage System
This project implements a decentralized distributed file storage system using Go, leveraging cryptography and peer-to-peer (P2P) libraries. It allows users to store files securely and distribute them across a network of nodes. The decentralized nature ensures no central authority controls the data, while the cryptographic functionality ensures data integrity, confidentiality, and security.

## Features
### Distributed Storage: 
Files are divided into chunks and stored across multiple nodes.
### Peer-to-Peer Network:
Uses a P2P network for file sharing and retrieval, ensuring scalability and decentralization.
### File Encryption: 
Files are encrypted before being distributed to ensure data security.
### Redundancy: 
Replicates file chunks across nodes to provide fault tolerance.
### Data Integrity: 
Cryptographic hashing is used to verify file integrity.
### File Retrieval: 
Users can retrieve files from the decentralized network by reassembling chunks.
### Node Participation:
Any user can join the network as a storage node and contribute resources.
## Technology Stack
### Go (Golang): 
The primary language used for development.
### Cryptography (crypto): 
Provides encryption and hashing for secure file storage.
### Peer-to-Peer (P2P) Library: 
Implements decentralized communication and file sharing among nodes.
## Requirements
Go version 1.16 or later
Network of nodes (local or remote) to participate in the decentralized system
Basic understanding of Go, P2P, and cryptography
## Installation
### Clone the repository:

git clone https://github.com/yourusername/decentralized-storage-system.git
cd decentralized-storage-system
### Install dependencies:

go mod tidy
### Build the project:

go build -o decentralized-storage
### Run the application:

./decentralized-storage
Usage
File Upload
### Start the P2P node by running:

./decentralized-storage node --start
### Upload a file to the network:

./decentralized-storage upload --file <path-to-your-file>
The system will encrypt the file, divide it into chunks, and distribute it across the connected nodes.

## File Retrieval
### To retrieve a file from the network:

./decentralized-storage download --file <file-id>
The system will fetch the distributed chunks from the network, verify their integrity using cryptographic hashes, decrypt the data, and reassemble the file.

## Node Management
### Join the network as a storage node:

./decentralized-storage node --join
### List active nodes in the network:

./decentralized-storage node --list
### Monitor node activity:

./decentralized-storage node --status
## Configuration
### You can configure parameters such as:

Node address
File chunk size
Encryption algorithm
Maximum replication factor
These settings can be adjusted in the config.yaml file.

## Security Features
### File Encryption:
All files are encrypted using AES-256 before being distributed.
### Hashing:
Files and chunks are hashed using SHA-256 to verify integrity and prevent tampering.
### P2P Authentication: 
Nodes in the P2P network are authenticated using public-private key pairs.
## Contributing
Fork the repository.
Create a new branch for your feature or bug fix.
Commit your changes and create a pull request.
### License
This project is licensed under the MIT License.
