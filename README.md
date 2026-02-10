<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Teddy Day</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<style>
* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #ff9ecb, #ffc1dd);
  color: white;
  height: 100vh;
  width: 100vw;
  overflow: hidden; /* NO SCROLL */
  position: relative;
}

.screen {
  position: absolute;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 20px;
}

h1 {
  font-family: 'Pacifico', cursive;
  font-size: 32px;
  margin-bottom: 12px;
}

p {
  font-size: 15px;
  max-width: 320px;
  line-height: 1.5;
  margin-bottom: 8px;
}

button {
  margin-top: 15px;
  padding: 12px 28px;
  border-radius: 30px;
  border: none;
  font-size: 16px;
  font-weight: bold;
  background: white;
  color: deeppink;
}

.hidden { display: none; }

video {
  width: 80%;
  max-width: 300px;
  border-radius: 18px;
  margin: 12px 0;
  box-shadow: 0 0 15px rgba(255,255,255,0.6);
}

/* Floating Hearts */
.heart {
  position: absolute;
  bottom: -30px;
  font-size: 20px;
  animation: floatUp linear infinite;
}

@keyframes floatUp {
  0% { transform: translateY(0); opacity: 1; }
  100% { transform: translateY(-120vh); opacity: 0; }
}
</style>
</head>

<body>

<!-- HOME SCREEN -->
<div class="screen" id="home">
  <h1>Happy Teddy Day 🧸💖</h1>
  <p>Tum meri life ka sabse soft aur cutest hug ho 🤗</p>
  <p>Jab bhi tum yaad aati ho, dil teddy ki tarah warm ho jata hai 💕</p>
  <p>🧸 Teddy aapka intezaar kar raha hai 🧸</p>
  <button onclick="showSurprise()">Click for Your Teddy 🎁</button>
</div>

<!-- SURPRISE SCREEN -->
<div class="screen hidden" id="surprise">
  <h1>Yeh Raha Aapka Teddy 🧸💞</h1>
  <p>Yeh teddy meri taraf se ek pyaara sa tight hug hai 🤗</p>

  <video src="teddy.mp4" autoplay loop muted playsinline></video>

  <p>Happy Teddy Day meri pyaari si jaan 💖</p>
</div>

<script>
function showSurprise() {
  document.getElementById("home").classList.add("hidden");
  document.getElementById("surprise").classList.remove("hidden");
}

/* Hearts generator */
for (let i = 0; i < 20; i++) {
  let heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (5 + Math.random() * 4) + "s";
  heart.style.fontSize = (14 + Math.random() * 18) + "px";
  document.body.appendChild(heart);
}
</script>

</body>
</html>
