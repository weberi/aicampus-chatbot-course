# AI Campus Chatbot Course

This repository provides a GitHub Codespace for the hands-on [AI Campus](https://www.ai-campus.org/) course on conversational AI: **[Step by Step zu deinem Chatbot - KI praktisch anwenden!](https://ki-campus.org/courses/conversational-ai)**.



The goal is to build a transactional chatbot using **[Rasa Open Source](https://rasa.com/docs/rasa/)** for conversations and **[Node-RED](https://nodered.org)** for custom actions.

## Setup Overview

The repository includes the setup for:

- A [GitHub Codespace](https://github.com/features/codespaces) environment
- A chatbot powered by [Rasa Open Source](https://rasa.com/docs/rasa/)
- An action server for the chatbot running on  [Node-RED](https://nodered.org), utilizing [node-red-contrib-rasa-actionserver](https://github.com/weberi/node-red-contrib-rasa-actionserver) nodes for integration

### Notes

#### Start Rasa:

   ```rasa run --port 5005 --cors "*"```

#### Chatroom.html:

```
<!DOCTYPE html>
<html lang="en">

<head>
    <link rel="stylesheet" href="https://cdn.statically.io/gh/weberi/chatroom/master/dist/Chatroom.css" />
    <link rel="stylesheet" type="text/css" href="https://cdn.statically.io/gh/weberi/chatroom/master/index.css">
    <link rel="stylesheet" type="text/css" href="https://cdn.statically.io/gh/weberi/chatroom/master/themes/theme2.css" />
</head>
<body>
    <div class="chat-container"></div>
    <script src="https://cdn.statically.io/gh/weberi/chatroom/master/dist/Chatroom.js"></script>
    <script type="text/javascript">
    var chatroom = new window.Chatroom({
        host: "https://your-codespace-url-5005.preview.app.github.dev",   
        title: "Chat with a bot",
        container: document.querySelector(".chat-container"),
        welcomeMessage: "Nice to meet you.",
        speechRecognition: "en-US",
        voiceLang: "en-US"
    });
    chatroom.openChat();
    </script>
</body>
</html>
```