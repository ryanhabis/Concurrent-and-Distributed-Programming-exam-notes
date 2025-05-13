## 🚀 Distributed Programming EXAM CRAM – Quiz + Answers + Explanations

---

### 🔹 SECTION 1: BASICS (1 mark each)

**1. What does TCP stand for?**
✅ **Transmission Control Protocol**
➡️ *A reliable, connection-based protocol for sending data over networks.*

**2. Which protocol is faster but less reliable than TCP?**
✅ **UDP (User Datagram Protocol)**
➡️ *It skips handshakes to send data faster — but doesn’t guarantee delivery.*

**3. In which Java layer are remote objects created in RMI?**
✅ **Server layer**
➡️ *Remote objects are instantiated and hosted on the server side.*

**4. What does IPC stand for?**
✅ **Inter-Process Communication**
➡️ *It’s how different programs (processes) talk to each other.*

**5. Name any one fallacy of distributed computing.**
✅ *“The network is secure” or “Latency is zero”*
➡️ *These wrong assumptions cause system design flaws.*

---

### 🔸 SECTION 2: CORE CONCEPTS (3 marks each)

**6. What’s the main difference between connection-based and connection-less communication?**
✅ **Connection-based** (TCP) = Requires a connection, reliable
✅ **Connection-less** (UDP) = No connection needed, fast but unreliable
➡️ *TCP = Phone call, UDP = Sending a flyer by wind.*

---

**7. Define “object serialization” and explain its purpose.**
✅ **Serialization** = Turning an object into bytes for network transfer
➡️ *It lets full Java objects be sent over sockets or stored for reuse.*

---

**8. What are the 3 roles of a connection socket?**
✅

1. Accept connection
2. Send data
3. Receive data
   ➡️ *Think of it like a phone: pick up, speak, listen.*

---

**9. What’s the purpose of the RMI registry?**
✅ **It maps names to remote objects.**
➡️ *Clients find and connect to services using names — like a phonebook.*

---

**10. Explain the difference between stateful and stateless servers.**
✅

* **Stateless**: No memory of client (e.g., Google search)
* **Stateful**: Stores session data (e.g., Amazon shopping cart)
  ➡️ *Stateless forgets you; Stateful remembers your coffee order.*

---

**11. How does Java’s `wait()` and `notify()` work?**
✅

* `wait()` pauses a thread
* `notify()` wakes it up
  ➡️ *Like raising your hand and waiting to be called on.*

---

**12. What is a race condition and how do you prevent it?**
✅ *Two threads access the same data at once → unpredictable results*
🛠️ Fix: Use `synchronized` blocks to lock the code.
➡️ *Like two chefs trying to chop onions with one knife.*

---

**13. Method-level vs Block-level synchronisation in Java?**
✅

* **Method-level**: Locks the whole method
* **Block-level**: Locks just part of code
  ➡️ *Block-level = more control, better performance*

---

**14. What does the JVM do?**
✅ **Java Virtual Machine** = Runs Java bytecode on any machine
➡️ *Acts as the translator between your Java program and the hardware.*

---

**15. What is a stub in RMI and why is it important?**
✅ *A stub is a local proxy that represents the remote object.*
➡️ *It hides the network from the client and forwards method calls.*

---

### 🔺 SECTION 3: CHALLENGERS (5 marks each)

**16. Compare RMI and socket-based communication.**

| Feature     | RMI                    | Sockets               |
| ----------- | ---------------------- | --------------------- |
| Abstraction | High (objects/methods) | Low (raw data)        |
| Ease of Use | Easier for Java devs   | Manual I/O            |
| Use Case    | Call remote methods    | General data transfer |

➡️ *RMI feels like calling a method. Sockets feel like mailing a package.*

---

**17. List 4 challenges in distributed computing and how to fix them.**

| Challenge   | Fix                             |
| ----------- | ------------------------------- |
| Latency     | Caching, shorter routes         |
| Failures    | Redundancy, backups, monitoring |
| Concurrency | Thread synchronisation, locks   |
| Security    | Encryption, authentication      |

➡️ *Distributed = more power, more problems.*

---

**18. Describe the Java Thread Lifecycle.**
✅ States:

* **New** → Created
* **Runnable** → Ready to run
* **Running** → Actively executing
* **Waiting/Blocked** → Paused
* **Terminated** → Finished

➡️ *Like a race: Get ready → Go → Wait → Done.*

---

**19. Show pseudocode to register a remote object in RMI.**

```java
MyService obj = new MyServiceImpl();
Naming.rebind("MyService", obj);
```

➡️ *Create → Bind → Wait for client*

---

**20. How does a browser retrieve a web page?**

1. User types URL
2. DNS converts URL to IP
3. Browser sends **HTTP request** using **TCP**
4. **Internet Layer** routes packets
5. Server responds → page rendered

➡️ *It’s a handshake through the layers: App → Transport → Internet → Link.*

---

### 💡 BONUS LIGHTNING ROUND (1 mark each)

**21. What port does HTTP use?**
✅ **Port 80**

**22. What is marshalling?**
✅ *Turning objects/data into a form that can be transferred*

**23. What are the 4 Internet Architecture layers?**
✅ *Network Access, Internet, Transport, Application*

**24. Thread vs Process?**
✅ *Thread = small, shares memory; Process = bigger, separate memory*

**25. What’s a surrogate server?**
✅ *A middleman server that handles requests on behalf of another*

---

## ✅ TOTAL MARKS: 65

🟢 Great Score: 55–65
🟡 Solid Pass: 45–54
🔴 Danger Zone: < 44 → Let me know and we’ll drill your weak points.
