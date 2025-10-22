<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>I Love You Aswathy Amma</title>
  <style>
    body {
      background: linear-gradient(to bottom right, #ffe4ec, #fceeff);
      text-align: center;
      font-family: 'Poppins', sans-serif;
      color: #333;
      margin: 0;
      overflow: hidden;
    }

    h1 {
      font-size: 3em;
      color: #ff2d55;
      margin-top: 80px;
    }

    h2 {
      font-size: 2.5em;
      color: #8a2be2;
    }

    h3 {
      font-size: 1.5em;
      color: #444;
    }

    .hearts {
      font-size: 2em;
      color: #ff7aa2;
    }

    /* Floating hearts animation */
    .heart {
      position: absolute;
      color: #ff7aa2;
      animation: float 6s infinite ease-in-out;
      opacity: 0.8;
    }

    @keyframes float {
      0% { transform: translateY(100vh) scale(0.8); opacity: 0.5; }
      50% { opacity: 1; }
      100% { transform: translateY(-10vh) scale(1.2); opacity: 0; }
    }

    audio {
      display: none;
    }
  </style>
</head>
<body>
  <h1>I Love You</h1>
  <h2>Aswathy Amma</h2>
  <div class="hearts">💖💗💞</div>
  <h3>Love from,<br><b>Anirudh</b></h3>

  <!-- Background music -->
  <audio autoplay loop>
    <source src="LoveStory.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <script>
    // Create floating hearts
    const colors = ['#ff7aa2', '#ff4d6d', '#f78fb3', '#f5a9b8'];
    for (let i = 0; i < 15; i++) {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.innerHTML = '💖';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = 5 + Math.random() * 5 + 's';
      heart.style.fontSize = 20 + Math.random() * 40 + 'px';
      heart.style.color = colors[Math.floor(Math.random() * colors.length)];
      document.body.appendChild(heart);
    }
  </script>
</body>
</html>
