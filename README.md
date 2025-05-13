# Concurrent-and-Distributed-Programming-exam-notes

## 🔥 SUPER-COMPRESSED EXAM CRAM NOTES – Distributed Programming

---

### 🧠 SECTION 1: HIGH-YIELD QUESTIONS & ANSWERS

#### ✅ 1. **How does a web browser talk to a server?**

* Uses **HTTP** (Application Layer)
* TCP/IP handles the data transport
* **NIC** (Network Interface Card) connects hardware
* Data travels via **4 layers**:

  1. **Application** – HTTP turns URLs into requests
  2. **Transport** – TCP segments data, ensures delivery
  3. **Internet** – IP addresses and routes packets
  4. **Network Access** – Deals with physical transmission (e.g., MAC address)

#### ✅ 2. **Distributed Computing Types**

* **Single Machine**: Monolithic, Parallel (no network)
* **Multi Machine**: Grid (different locations), Cluster (same location, 1 master many slaves)
* Example: Netflix uses distributed computing to stream

#### ✅ 3. **Stateful vs Stateless**

* **Stateless**: Server doesn’t remember you (e.g., HTTP)
* **Stateful**: Server keeps your info (e.g., login sessions)

#### ✅ 4. **Object Server**

* Hosts remote objects for use by other machines
* Often seen in **RMI** systems

#### ✅ 5. **RMI Registry**

* A directory service
* Lets clients find remote objects by name

#### ✅ 6. **Purpose of Logs in Multithreaded Apps**

* Help track **thread activities**, bugs, and deadlocks
* 💡 Use `synchronized` logs to avoid race conditions

```java
synchronized(log) {
  log.write("Thread X completed.");
}
```

#### ✅ 7. **4 Challenges in Distributed Computing**

| Challenge   | Fix                             |
| ----------- | ------------------------------- |
| Latency     | Use caching, faster connections |
| Failure     | Redundancy, failover systems    |
| Security    | Encryption, authentication      |
| Concurrency | Locks, thread management        |

#### ✅ 8. **Transparency in Distributed Systems**

* **Access Transparency**: Hide server location
* **Replication Transparency**: User doesn’t know it's redundant
* **Scaling Transparency**: Handles more users
* **Performance Transparency**: Optimised behind-the-scenes

#### ✅ 9. **IPC Key Components**

* **Sockets**, **Shared Memory**, **Pipes**, **Message Queues**

#### ✅ 10. **Thread Synchronisation (2 types)**

1. **Method-Level**

```java
public synchronized void myMethod() {}
```

2. **Block-Level**

```java
synchronized(this) {
   // critical code
}
```

#### ✅ 11. **Connection Socket Roles**

1. Accept connections
2. Send data
3. Receive data

#### ✅ 12. **Registering Remote Object (RMI)**

```java
MyObject obj = new MyObject();
Naming.rebind("myService", obj);
```

* Start RMI registry → Create object → Bind

#### ✅ 13. **Connection-less vs Connection-based**

| Type             | Example | Features            |
| ---------------- | ------- | ------------------- |
| Connection-less  | UDP     | Fast but unreliable |
| Connection-based | TCP     | Reliable, slower    |

#### ✅ 14. **Multicast Communication**

* Send one message to **multiple receivers**
* Used in streaming, conferences

#### ✅ 15. **Software Layering**

* Each layer only talks to the **one above/below**
* Layers can be updated independently

#### ✅ 16. **Java Thread States**

Diagram: New → Ready → Running → Waiting → Terminated

#### ✅ 17. **RMI Architecture Diagram**

* Client → Stub → Remote Reference Layer → Transport Layer → Server Skeleton

#### ✅ 18. **Remote Interface in RMI**

* Interface that defines methods accessible remotely

```java
public interface MyService extends Remote {
  void sayHi() throws RemoteException;
}
```

#### ✅ 19. **Iterative vs Concurrent Server**

| Type       | Handles    | Example         |
| ---------- | ---------- | --------------- |
| Iterative  | One client | Simple Telnet   |
| Concurrent | Multiple   | Modern websites |

#### ✅ 20. **Fallacies of Distributed Computing (Any 2)**

* **“Latency is zero”** – Can cause UI lag in apps
* **“Network is secure”** – Leads to no encryption

#### ✅ 21. **Wait and Notify (Java)**

* Used to pause/resume threads

```java
synchronized(obj) {
  obj.wait();   // pause
  obj.notify(); // resume
}
```

#### ✅ 22. **Java Socket API Event Sync**

* Uses input/output streams and blocking calls to manage data flow

#### ✅ 23. **Thread vs Process**

* **Process** = Independent, own memory
* **Thread** = Lightweight, shares memory

```java
Thread t = new Thread(); // thread
ProcessBuilder pb = new ProcessBuilder(); // process
```

#### ✅ 24. **Race Condition**

* Two threads access shared data at the same time → unpredictable results

#### ✅ 25. **Improve Scalability (with Code)**

* Use **Thread Pools**

```java
ExecutorService pool = Executors.newFixedThreadPool(10);
pool.execute(new MyRunnable());
```

#### ✅ 26. **RMI vs Sockets**

| Feature     | RMI                      | Sockets               |
| ----------- | ------------------------ | --------------------- |
| Abstraction | High (objects & methods) | Low (raw data)        |
| Use Case    | Method calling remotely  | General communication |

---

### 🧠 SECTION 2: DEFINITIONS CRAM

| Term                 | Quick Explanation                            |
| -------------------- | -------------------------------------------- |
| NIC                  | Hardware for network access                  |
| TCP                  | Reliable, connection-based protocol          |
| UDP                  | Fast, no guarantee (used in games/streaming) |
| Flow Control         | Stops too much data being sent               |
| Sockets              | Endpoint for communication                   |
| Port Number          | Identifies process on a machine              |
| OS                   | Software that manages hardware               |
| RMI                  | Lets Java call methods on remote objects     |
| Object Serialization | Converts object to byte stream               |
| Surrogate Server     | Intermediary server                          |
| Stub                 | Local representative of a remote object      |
| Deadlock             | Threads locking each other indefinitely      |
| Context Switch       | CPU switches between processes               |
| Thread Pool          | Manages reusable threads                     |
| RMID                 | Activates RMI objects when needed            |
| Datagram             | Basic transfer unit in UDP                   |

---

### 🧠 SECTION 3: EASY MEMORY HOOKS

| Concept               | Hook                                                       |
| --------------------- | ---------------------------------------------------------- |
| TCP vs UDP            | **TCP = Telephone**, **UDP = Shouting across the room**    |
| Stateful vs Stateless | **Stateless = Snapchat**, **Stateful = WhatsApp**          |
| RMI                   | **RMI = Remote Java WhatsApp**                             |
| Threads vs Processes  | **Threads = Roommates**, **Processes = Neighbours**        |
| Iterative Server      | **One-in, One-out queue**                                  |
| Concurrent Server     | **Open all tills**                                         |
| Race Condition        | **Two chefs using same knife**                             |
| Deadlock              | **Two cars stuck in narrow road both refusing to reverse** |
