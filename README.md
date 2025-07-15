# Princess-Ashu-b-day.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Happy Birthday Princess Ashu 👑</title>
  <style>
    body {
      background: linear-gradient(to right, #ffe0f0, #ffe6f7);
      font-family: 'Segoe Script', cursive;
      text-align: center;
      padding: 50px;
      overflow-x: hidden;
    }
    h1 {
      font-size: 3em;
      color: #ff4da6;
    }
    p {
      font-size: 1.5em;
      color: #ff1493;
    }
    #secret {
      display: none;
      margin-top: 20px;
      font-size: 1.3em;
      color: #d63384;
    }
    button {
      padding: 12px 25px;
      font-size: 1.1em;
      background: #ff69b4;
      color: white;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      margin-top: 20px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    .confetti {
      position: fixed;
      width: 10px;
      height: 10px;
      background-color: pink;
      opacity: 0.7;
      z-index: 9999;
    }
  </style>
</head>
<body>
  <h1>🎉 Happy Birthday Princess Ashu 👑</h1>
  <p>Today the world got a little more magical 🌸<br>because someone truly special was born.</p>

  <button onclick="reveal()">Click for a Royal Surprise</button>

  <div id="secret">
    <p>💖 Dearest Princess Ashu,</p>
    <p>May your smile shine brighter than a thousand stars ✨</p>
    <p>May this year bring joy, laughter, and endless cupcakes 🧁</p>
    <p>You're not just a best friend — you're royalty in my life 💫</p>
    <p>👑 Long live the Queen of Hearts — You! 🎂</p>
  </div>

  <script>
    function reveal() {
      document.getElementById('secret').style.display = 'block';
      confettiEffect();
    }

    function confettiEffect() {
      for (let i = 0; i < 120; i++) {
        let confetti = document.createElement('div');
        confetti.classList.add('confetti');
        confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 75%)`;
        confetti.style.left = `${Math.random() * 100}vw`;
        confetti.style.top = `-${Math.random() * 20}px`;
        document.body.appendChild(confetti);

        let fall = confetti.animate([
          { transform: 'translateY(0)' },
          { transform: `translateY(${window.innerHeight}px)` }
        ], {
          duration: 3000 + Math.random() * 2000,
          easing: 'ease-out',
          iterations: 1
        });

        fall.onfinish = () => confetti.remove();
      }
    }
  </script>
</body>
</html>
