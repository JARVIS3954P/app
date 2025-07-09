# 🗨️ Real-Time Chat Application

A simple real-time chat application built using **Java Spring Boot**, **WebSockets (STOMP over SockJS)**, **Bootstrap**, and a clean HTML frontend. Users can send and receive messages in real time, with sender name locked after the first message for consistency.

---

## 🚀 Features

- Real-time bidirectional communication using STOMP over WebSocket
- Fallback support with SockJS for unsupported browsers
- Clean and responsive UI with Bootstrap 5
- Prevents sender name modification after the first message
- Lightweight to extend

---

## 🛠️ Tech Stack

- **Backend:** Java 17+, Spring Boot, Spring WebSocket, STOMP, SockJS
- **Frontend:** HTML5, JavaScript, Bootstrap 5
- **Build Tool:** Maven

---


## 📡 WebSocket Flow

- **Client sends message to:** `/app/sendMessage`
- **Server receives via:** `@MessageMapping("/sendMessage")`
- **Server broadcasts to:** `/topic/messages`
- **Client subscribes to:** `/topic/messages`
- **WebSocket endpoint:** `/chat`
---
## 🧪 Running Locally

### Prerequisites
- Java 17 or higher
- Maven 3.8 or higher

### Steps
```bash
git clone https://github.com/your-username/chat-app.git
cd chat-app
mvn spring-boot:run
```

Visit: [http://localhost:8080/chat](http://localhost:8080/chat)

---
## 🖥️ UI Behavior

- Enter your name and message  
- After the first message is sent, the name field becomes disabled  
- Messages from all clients are broadcast instantly  
- Scroll automatically to the newest message  

---

## 📌 Future Enhancements

- Chat persistence using a database (MySQL, PostgresSQL)  
- Private chats or chat rooms  
- Authentication and user session tracking  
- Timestamps and message history  
- Emoji and file sharing support  
- Dockerization for deployment  
