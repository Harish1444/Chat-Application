# Real-Time Chat Application

A real-time chat application built with Spring Boot, WebSocket (STOMP), and Thymeleaf. This project demonstrates how to create a modern, interactive chat room with live messaging and a simple in-chat game (Tic-Tac-Toe).

## Features
- Real-time messaging using WebSocket and STOMP
- Typing indicators
- User-friendly, modern UI (Bootstrap, custom CSS)
- In-chat emoji reactions
- Play Tic-Tac-Toe with other users in the chat
- Built with Spring Boot 3, Java 17, and Thymeleaf

## Screenshots
![Chat UI Screenshot](#) <!-- Add your screenshot here -->

## Getting Started

### Prerequisites
- Java 17 or higher
- Maven 3.6+

### Running Locally
1. **Clone the repository:**
   ```bash
   git clone <your-repo-url>
   cd app
   ```
2. **Build and run the application:**
   ```bash
   ./mvnw spring-boot:run
   # or on Windows
   mvnw.cmd spring-boot:run
   ```
3. **Access the chat app:**
   Open your browser and go to [http://localhost:8080/chat](http://localhost:8080/chat)

### Project Structure
- `src/main/java/com/chat/app/` - Main application source code
  - `controller/ChatController.java` - Handles chat endpoints and WebSocket messaging
  - `config/WebSocketConfig.java` - WebSocket/STOMP configuration
  - `model/ChatMessage.java` - Message model
- `src/main/resources/templates/chat.html` - Frontend UI (Thymeleaf template)
- `src/main/resources/application.properties` - App configuration

### WebSocket Endpoints
- **STOMP endpoint:** `/chat` (SockJS enabled)
- **Message topic:** `/topic/messages`
- **Typing topic:** `/topic/typing`
- **Send message mapping:** `/app/sendMessage`
- **Typing mapping:** `/app/typing`, `/app/stopTyping`

### Message Model
```json
{
  "id": 1,
  "sender": "Alice",
  "content": "Hello, world!"
}
```

## Running Tests
Run all tests with:
```bash
./mvnw test
```

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

.

## References
- [Spring Boot WebSocket Guide](https://spring.io/guides/gs/messaging-stomp-websocket/)
- See `HELP.md` for more Spring Boot and Maven resources.
