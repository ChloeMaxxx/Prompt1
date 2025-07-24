<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Prompt Copy Tool</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 600px;
      margin: 50px auto;
      padding: 20px;
      background-color: #f9f9f9;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
    }
    textarea {
      width: 100%;
      height: 250px;
      font-size: 16px;
      padding: 10px;
      border-radius: 8px;
    }
    button {
      margin-top: 10px;
      padding: 10px 20px;
      font-size: 16px;
      border-radius: 8px;
      background-color: #4CAF50;
      color: white;
      border: none;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    #status {
      margin-top: 10px;
      font-size: 14px;
      color: green;
    }
  </style>
</head>
<body>
  <h2>🎮 Word Association Prompt</h2>
  <p>Click the button below to copy the prompt for ChatGPT:</p>
  <textarea id="promptText">Hey, let’s play a word association game about my favorite star. You say one word, and I’ll say a related word. Let’s take turns. Please make sure each word is clearly connected to the topic of a favorite star — like their talent, fans, awards, shows, or personality. Please speak slowly and clearly and use words within CEFR B1 level. We will take 10 turns each, for a total of 20 words. Please count and let me know which turn we are on each time. You give me the first word. Let’s begin!</textarea>
  <br />
  <button onclick="copyText()">📋 Copy Prompt</button>
  <p id="status"></p>

  <script>
    function copyText() {
      const textArea = document.getElementById("promptText");
      textArea.select();
      document.execCommand("copy");
      document.getElementById("status").innerText = "✅ Prompt copied!";
    }
  </script>
</body>
</html>
