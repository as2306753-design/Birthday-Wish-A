<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday My Most Lovable Senior 💖</title>

<style>
body {
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #ff758c, #ff7eb3);
  font-family: 'Segoe UI', sans-serif;
  overflow: hidden;
}

.card {
  background: rgba(255,255,255,0.15);
  backdrop-filter: blur(10px);
  padding: 25px;
  border-radius: 25px;
  text-align: center;
  width: 90%;
  max-width: 350px;
  box-shadow: 0 20px 40px rgba(0,0,0,0.25);
}

h1 {
  color: white;
  margin-bottom: 10px;
}

p {
  color: white;
  font-size: 16px;
}

.slider {
  width: 100%;
  height: 280px;
  margin: 15px 0;
  position: relative;
  overflow: hidden;
  border-radius: 20px;
}

.slider img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  opacity: 0;
  transition: opacity 1s ease;
}

.slider img.active {
  opacity: 1;
}

.buttons {
  position: relative;
  height: 120px;
  margin-top: 20px;
}

button {
  padding: 12px 28px;
  border: none;
  border-radius: 30px;
  font-size: 16px;
  position: absolute;
  cursor: pointer;
}

#yes {
  left: 20px;
  background: #2ecc71;
  color: white;
}

#no {
  right: 20px;
  background: #e74c3c;
  color: white;
}
</style>
</head>

<body>

<div class="card">
  <h1>🎂 Happy Birthday 💖</h1>
  <p>
    Do you accept my wish?<br>
    <strong>My Most Lovable Senior 💕</strong>
  </p>

  <div class="slider">
    <img src="photo1.jpg" class="active">
    <img src="photo2.jpg">
    <img src="photo3.jpg">
    <img src="photo4.jpg">
    <img src="photo5.jpg">
    <img src="photo6.jpg">
    <img src="photo7.jpg">
    <img src="photo8.jpg">
  </div>

  <div class="buttons">
    <button id="yes">Yes 💖</button>
    <button id="no">No 😜</button>
  </div>
</div>

<script>
const images = document.querySelectorAll(".slider img");
let index = 0;

setInterval(() => {
  images[index].classList.remove("active");
  index = (index + 1) % images.length;
  images[index].classList.add("active");
}, 2500);

const noBtn = document.getElementById("no");
noBtn.addEventListener("mouseover", moveNo);
noBtn.addEventListener("touchstart", moveNo);

function moveNo() {
  noBtn.style.left = Math.random() * 180 + "px";
  noBtn.style.top = Math.random() * 80 + "px";
}

document.getElementById("yes").onclick = () => {
  document.body.innerHTML = `
    <h1 style="color:white;font-size:38px;">🥰💖 She Said YES 💖🥰</h1>
    <p style="color:white;font-size:20px;text-align:center;">
      Thank you for accepting my wish 💕<br><br>
      You truly make my day brighter ✨<br><br>
      <strong>Happy Birthday 🎂🎉</strong>
    </p>
  `;
};
</script>

</body>
</html>
