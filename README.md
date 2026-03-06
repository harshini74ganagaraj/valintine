<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sathiya</title>

<style>
  body {
    margin: 0;
    height: 100vh;
    background: #ffd6e8;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Segoe UI', sans-serif;
  }

  .card {
    background: #fff;
    padding: 30px;
    border-radius: 25px;
    text-align: center;
    width: 90%;
    max-width: 350px;
    box-shadow: 0 15px 30px rgba(0,0,0,0.15);
  }

  .emoji {
    font-size: 80px;
    margin-bottom: 10px;
  }

  h2 {
    margin: 15px 0;
    color: #333;
  }

  .buttons {
    position: relative;
    height: 110px;
    margin-top: 20px;
  }

  button {
    padding: 12px 25px;
    border: none;
    border-radius: 25px;
    font-size: 16px;
    cursor: pointer;
  }

  #yes {
    background: #ff4f7a;
    color: white;
  }

  #no {
    background: #ddd;
    color: #333;
    position: absolute;
    left: 140px;
    top: 10px;
  }

  #message {
    display: none;
    margin-top: 20px;
    font-size: 18px;
    color: #ff4f7a;
    animation: pop 0.5s ease;
  }

  @keyframes pop {
    0% { transform: scale(0.5); opacity: 0; }
    100% { transform: scale(1); opacity: 1; }
  }
</style>
</head>

<body>

<div class="card">
  <div class="emoji">🐱💗</div>

  <h2>Sathiya,<br>will you be my Valentine? 💌</h2>

  <div class="buttons">
    <button id="yes" onclick="yesClicked()">Yes 💖</button>
    <button id="no" onmouseover="moveNo()">No 😳</button>
  </div>

  <div id="message">
    Yayyy XXXXXX 🥹💞<br>
    You just made my heart so happy!<br>
    I love you 💕
  </div>
</div>

<script>
  function moveNo() {
    const noBtn = document.getElementById("no");
    const x = Math.random() * 220;
    const y = Math.random() * 70;
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
  }

  function yesClicked() {
    document.getElementById("message").style.display = "block";
  }
</script>

</body>
</html>
