<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>For My Love ❤️</title>

  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      overflow: hidden;
    }

    .container {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 400px;
      width: 90%;
      z-index: 2;
    }

    h1 {
      color: #ff4d6d;
    }

    p {
      color: #555;
      margin-bottom: 20px;
    }

    .buttons {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
    }

    button {
      padding: 12px;
      border: none;
      border-radius: 25px;
      font-size: 14px;
      cursor: pointer;
      background: #ff4d6d;
      color: white;
      transition: transform 0.2s, box-shadow 0.2s;
    }

    button:hover {
      transform: scale(1.08);
      box-shadow: 0 10px 20px rgba(255,77,109,0.4);
    }

    .message {
      margin-top: 20px;
      font-size: 16px;
      color: #ff4d6d;
      min-height: 40px;
      font-weight: 500;
    }

    /* Floating hearts */
    .heart {
      position: absolute;
      font-size: 20px;
      animation: floatUp 2s ease-out forwards;
      pointer-events: none;
    }

    @keyframes floatUp {
      0% {
        transform: scale(0) translateY(0);
        opacity: 1;
      }
      100% {
        transform: scale(1.5) translateY(-120px);
        opacity: 0;
      }
    }
  </style>
</head>

<body onclick="startMusic(event)">

  <!-- Background Music -->
  <audio id="bgMusic" loop>
    <!-- You can replace this with any romantic MP3 -->
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
  </audio>

  <div class="container">
    <h1>Hey My Love 💕</h1>
    <p>Click the buttons for sweet surprises</p>

    <div class="buttons">
      <button onclick="showMessage(0, event)">💖 Click Me</button>
      <button onclick="showMessage(1, event)">🌸 This One</button>
      <button onclick="showMessage(2, event)">🥰 Love Button</button>
      <button onclick="showMessage(3, event)">✨ Magic</button>
      <button onclick="showMessage(4, event)">💌 Secret</button>
      <button onclick="showMessage(5, event)">❤️ Always</button>
    </div>

    <div class="message" id="message">💗</div>
  </div>

  <script>
    const messages = [
      "I smile every time I think of you ❤️",
      "You are my favorite notification 🥰",
      "My heart chose you, every single time 💖",
      "You make my world softer and brighter ✨",
      "If love had a face, it would look like you 💌",
      "No matter what happens, it’s always you ❤️"
    ];

    let musicStarted = false;

    function startMusic(e) {
      if (!musicStarted) {
        document.getElementById("bgMusic").play();
        musicStarted = true;
      }
      createHeart(e.clientX, e.clientY);
    }

    function showMessage(index, e) {
      document.getElementById("message").innerText = messages[index];
      createHeart(e.clientX, e.clientY);
    }

    function createHeart(x, y) {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerText = ["💖","💕","💘","❤️","💗"][Math.floor(Math.random()*5)];
      heart.style.left = x + "px";
      heart.style.top = y + "px";
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 2000);
    }
  </script>

</body>
</html>

# project-for-client
# 💕 Love Buttons Webpage

A cute and romantic single-page website made with ❤️ for your girlfriend.  
It features adorable buttons, sweet love messages, floating hearts on click, and soft background music to create a magical vibe.

---

## ✨ Features

- 💖 Multiple cute buttons with romantic messages  
- 💕 Floating heart animations on every click  
- 🎶 Background music (starts automatically on first interaction)  
- 📱 Fully responsive – works on mobile and desktop  
- 🌸 Simple, clean, and aesthetic design  

---

## 📁 Project Structure


> No external libraries required. Everything works in a single HTML file.

---

## 🚀 How to Use

1. Download or copy the `love.html` file  
2. Place it in any folder on your computer  
3. Double-click the file OR right-click → open with browser  
4. Click anywhere to start the music 🎶  
5. Click the buttons and enjoy the love 💘  

---

## 🎵 Changing the Background Music

Inside `love.html`, find this section:

```html
<audio id="bgMusic" loop>
  <source src="YOUR_MUSIC_LINK.mp3" type="audio/mpeg">
</audio>


---

If you want, I can also:
- Add **your names in the README**
- Write a **cute dedication note**
- Make a **GitHub-ready version**
- Create a **ZIP package**

Just say the word 😄💖
