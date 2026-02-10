<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Teddy Day</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&family=Pacifico&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  padding: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #ff9ecb, #ffc1dd);
  color: white;
  text-align: center;
  overflow: hidden;
}

.container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

h1 {
  font-family: 'Pacifico', cursive;
  font-size: 34px;
  margin-bottom: 10px;
}

p {
  font-size: 16px;
  max-width: 320px;
  line-height: 1.5;
}

button {
  margin-top: 20px;
  padding: 12px 25px;
  border: none;
  border-radius: 30px;
  background: white;
  color: deeppink;
  font-size: 16px;
  font-weight: bold;
}

button:active {
  transform: scale(0.95);
}

.hidden {
  display: none;
}

video {
  width: 85%;
  max-width: 320px;
  border-radius: 20px;
  margin-top: 15px;
  box-shadow: 0 0 15px rgba(255,255,255,0.6);
}

/* floating hearts */
.heart {
  position: absolute;
  bottom: -20px;
  font-size: 20px;
  animation: floatUp 6s linear infinite;
}

@keyframes floatUp {
  0% { transform: translateY(0); opacity: 1; }
  100% { transform: translateY(-110vh); opacity: 0; }
}
</style>
</head>

<body>

<div class="container" id="home">
  <h1>Happy Teddy Day 🧸💖</h1>
  <p>
    Tum meri life ka sabse soft, cutest aur warm hug ho 🤗💗  
    Jab bhi tum yaad aati ho, dil ko bilkul teddy jaisa sukoon milta hai 🧸✨
  </p>
  <p>🧸 Teddy aapka intezaar kar raha hai 🧸</p>
  <button onclick="showSurprise()">Click for Your Teddy 🎁</button>
</div>

<div class="container hidden" id="surprise">
  <h1>Yeh Raha Aapka Teddy 🧸💞</h1>
  <p>
    Yeh teddy meri taraf se ek pyaara sa tight hug hai 🤗  
    Jo har din aapko yaad dilaye ki koi aapko bohot special maanta hai 💕
  </p>

  <!-- TEDDY VIDEO -->
  <video src="teddy.mp4" autoplay loop muted playsinline></video>

  <p>Happy Teddy Day meri pyaari si jaan 💖</p>
</div>

<script>
function showSurprise() {
  document.getElementById("home").classList.add("hidden");
  document.getElementById("surprise").classList.remove("hidden");
}

/* floating hearts create */
for (let i = 0; i < 15; i++) {
  let heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (4 + Math.random() * 3) + "s";
  heart.style.fontSize = (15 + Math.random() * 15) + "px";
  document.body.appendChild(heart);
}
</script>

</body>
</html>
