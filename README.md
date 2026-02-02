 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Special Question 💖</title>
  <style>
    body {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: 'Arial', sans-serif;
      text-align: center;
    }

    h1 {
      color: #fff;
      margin-bottom: 10px;
    }

    p {
      color: #fff;
      font-size: 18px;
      margin-bottom: 30px;
    }

    .buttons {
      position: relative;
      width: 300px;
      height: 150px;
    }

    button {
      padding: 12px 25px;
      font-size: 16px;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      position: absolute;
    }

    #yes {
      left: 30px;
      background-color: #28a745;
      color: white;
    }

    #no {
      right: 30px;
      background-color: #dc3545;
      color: white;
    }
  </style>
</head>
<body>

  <h1>Happy Birthday 🎂💖</h1>
  <p>
    Do you accept my wish? <br>
    <strong>Happy Birthday to You, <br>
    My Most Lovable Senior 💕</strong>
  </p>

  <div class="buttons">
    <button id="yes" onclick="yesClicked()">Yes</button>
    <button id="no">No</button>
  </div>

  <script>
    const noBtn = document.getElementById("no");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * 200;
      const y = Math.random() * 100;
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    });

    function yesClicked() {
      document.body.innerHTML = `
        <h1 style="color:white;">🥰💖 Yayyyy! 💖🥰</h1>
        <p style="color:white;font-size:20px;">
          Thank you for accepting my wish 💕<br>
          Once again,<br>
          <strong>Happy Birthday 🎉🎂</strong>
        </p>
      `;
    }
  </script>

</body>
</html>
