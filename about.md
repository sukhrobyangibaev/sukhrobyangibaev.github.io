---
layout: page
title: About
permalink: /about/
---

Hi, I'm Sukhrob! 👋

<div id="chat-container">
  <div id="chat-messages"></div>
  <input type="text" id="user-input" placeholder="Type your message...">
  <button id="send-button">Send</button>
</div>

<script>
  const chatMessages = document.getElementById('chat-messages');
  const userInput = document.getElementById('user-input');
  const sendButton = document.getElementById('send-button');

  let messages = [{role: "system", content: "You are a helpful assistant."}];

  function addMessage(role, content) {
    const messageElement = document.createElement('div');
    messageElement.classList.add(role);
    messageElement.textContent = content;
    chatMessages.appendChild(messageElement);
  }

  async function sendMessage() {
    const userMessage = userInput.value;
    addMessage('user', userMessage);
    userInput.value = '';

    messages.push({role: "user", content: userMessage});

    const response = await fetch('https://ubiquitous-platypus-096596.netlify.app/.netlify/functions/langbase-proxy', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify({ messages: messages })
    });

    const data = await response.json();
    const assistantMessage = data.completion;

    messages.push({role: "assistant", content: assistantMessage});
    addMessage('assistant', assistantMessage);
  }

  sendButton.addEventListener('click', sendMessage);
  userInput.addEventListener('keydown', (event) => {
    if (event.key === 'Enter') {
      sendMessage();
    }
  });
</script>

<style>
  #chat-container {
    border: 1px solid #ccc;
    padding: 10px;
    width: 500px;
    margin: 20px auto;
  }

  #chat-messages {
    min-height: 100px;
    margin-bottom: 10px;
  }

  .user {
    text-align: right;
    color: blue;
  }

  .assistant {
    text-align: left;
    color: green;
  }
</style>