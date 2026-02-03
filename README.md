index.htmlj
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: repeating-linear-gradient(
        45deg,
        #ff6b6b,
        #ff6b6b 20px,
        #ff8787 20px,
        #ff8787 40px
      );
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
    }
    .card {
      background: #fff;
      padding: 25px;
      border-radius: 20px;
      text-align: center;
      width: 300px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }
    h1 { color: #ff4d6d; }
    img {
      width: 150px;
      border-radius: 15px;
      margin: 15px 0;
    }
    button {
      padding: 10px 20px;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      margin: 10px;
    }
    #yes { background: #4caf50; color: white; }
    #no {
      background: #f44336;
      color: white;
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Will you be my Valentine? 💘</h1>
    <img src="https://i.imgur.com/2yaf2wb.jpg">
    <br>
    <button id="yes" onclick="yesClick()">Yes 💖</button>
    <button id="no" onmouseover="moveNo()">No 😢</button>
  </div>

  <script>
    function moveNo() {
      const noBtn = document.getElementById("no");
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 50);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    function yesClick() {
      document.body.innerHTML = `
        <h1 style="color:white; text-align:center;">
          Yay!!! 💕😍<br>
          Best Valentine ever 💖
        </h1>
      `;
    }
  </script>

</body>
</html>
