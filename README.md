# FileWare

**A Multithreaded Distributed File Sharing System using Java**

FileWare is a scalable, distributed file-sharing application built in Java that leverages multithreading and ServerSockets to enable seamless registration, lookup, and transfer of files across a decentralized network. Inspired by real-world peer-to-peer systems, FileWare allows efficient communication between nodes through a centralized server, significantly boosting file access performance and network reliability.

---

## 🚀 Features

- ⚙️ **Distributed Architecture**: Supports file sharing across multiple nodes in a distributed environment.
- 🧵 **Multithreading**: Handles concurrent requests efficiently using Java’s multithreaded capabilities.
- 🌐 **Centralized Directory Server**: Maintains file indices and handles up to 100 simultaneous node connections.
- 📁 **File Registration & Retrieval**: Nodes can register files and search/download files shared by others.
- 🚄 **Performance Boost**: Increases file access speed by ~30% through optimized communication protocols.
- 🔌 **Socket Programming**: Utilizes TCP ServerSockets for reliable inter-node communication.

---

## 🛠️ Tech Stack

- **Language**: Java  
- **Concurrency**: Java Threads, Synchronization  
- **Networking**: ServerSocket, Socket, I/O Streams  
- **Architecture**: Centralized Server with Multiple Clients (Peer Nodes)

---

## 🗂️ Project Structure

```
FileWare/
│
├── Server/
│   ├── CentralServer.java        # Manages file registry and client connections
│
├── Client/
│   ├── PeerNode.java             # Registers, searches, and downloads files
│
├── Common/
│   ├── FileUtils.java            # Handles file metadata and utilities
│
└── README.md
```

---

## 🧪 How It Works

1. **Start the Central Server**  
   The server listens for incoming peer connections and maintains a registry of all shared files.

2. **Start Peer Nodes**  
   Each peer registers its local files with the server and can query the registry to find files from other peers.

3. **File Lookup and Download**  
   When a file is requested, the server returns the peer’s address hosting it. The requesting peer then initiates a direct socket connection for download.

---

## 📦 Setup & Usage

### Prerequisites

- Java 8 or above
- Terminal or IDE (e.g., IntelliJ, Eclipse)

### Compile

```bash
javac Server/CentralServer.java Client/PeerNode.java
```

### Run Central Server

```bash
java Server.CentralServer
```

### Run a Peer Node

```bash
java Client.PeerNode
```

You can run multiple peers in different terminals to simulate a distributed environment.

---

## 🔒 Security Note

This project is for educational and experimental use only. No built-in encryption or authentication is included.

---

## 📈 Performance

- Tested with up to 100 concurrent client connections
- Achieved ~30% faster access time compared to basic sequential file-sharing setups

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository and submit a pull request.

---

## 📄 License

This project is licensed under - see the [LICENSE](LICENSE) file for details.

---



