<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Valentine 💖</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      font-family: "Segoe UI", sans-serif;
    }

    .card {
      background: white;
      padding: 30px 40px;
      border-radius: 18px;
      text-align: center;
      box-shadow: 0 15px 40px rgba(0,0,0,0.25);
      width: 320px;
    }

    h1 {
      color: #e91e63;
      margin-bottom: 10px;
    }

    h2 {
      margin-top: 0;
    }

    .buttons {
      margin-top: 25px;
      position: relative;
      height: 60px;
    }

    button {
      font-size: 18px;
      padding: 10px 24px;
      border-radius: 8px;
      border: none;
      cursor: pointer;
    }

    #yes {
      background: #4caf50;
      color: white;
    }

    #no {
      background: #f44336;
      color: white;
      position: absolute;
      left: 140px;
    }

    #result {
      display: none;
      margin-top: 20px;
      font-size: 22px;
      color: #4caf50;
    }
  </style>
</head>

<body>

  <div class="card">
    <!-- CHANGE NAME HERE -->
    <h1>Hey ❤️</h1>

    <h2>Chutiya, Will you be my Valentine?</h2>

    <div class="buttons">
      <button id="yes" onclick="yesClicked()">Yes 😍</button>
      <button id="no" onmouseover="moveNo()">No 😏</button>
    </div>

    <div id="result">
      Yayyy 💖 I knew it!
    </div>
  </div>

  <script>
    function moveNo() {
      const noBtn = document.getElementById("no");
      const maxX = 200;
      const maxY = 40;

      const x = Math.random() * maxX;
      const y = Math.random() * maxY;

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    function yesClicked() {
      document.getElementById("result").style.display = "block";
    }
  </script>

</body>
</html>
