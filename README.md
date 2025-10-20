<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>TamzStore</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      overflow-x: hidden;
      font-family: 'Poppins', sans-serif;
      background: radial-gradient(circle at center, #0b0f29 0%, #050814 100%);
      color: #fff;
    }
    .stars {
      width: 100%;
      height: 100%;
      background: url('https://cdn.jsdelivr.net/gh/JulianLaval/canvas-particle-network/img/stars.png');
      background-size: cover;
      position: fixed;
      top: 0;
      left: 0;
      z-index: -2;
      animation: moveStars 200s linear infinite;
    }
    @keyframes moveStars {
      from {background-position: 0 0;}
      to {background-position: -2000px 1000px;}
    }
    .saturn {
      position: fixed;
      top: 50%;
      left: 50%;
      width: 280px;
      height: 280px;
      background: radial-gradient(circle at 30% 30%, #d2c6ff 0%, #5a4ea3 60%, #1b164a 100%);
      border-radius: 50%;
      box-shadow: 0 0 60px rgba(124,92,255,0.6);
      transform: translate(-50%, -50%);
      animation: spinPlanet 60s linear infinite;
      z-index: -1;
    }
    .ring {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 420px;
      height: 120px;
      border: 4px solid rgba(180,160,255,0.3);
      border-radius: 50%;
      transform: translate(-50%, -50%) rotateX(65deg);
      animation: spinRing 40s linear infinite;
    }
    @keyframes spinPlanet {
      from {transform: translate(-50%, -50%) rotate(0deg);}
      to {transform: translate(-50%, -50%) rotate(360deg);}
    }
    @keyframes spinRing {
      from {transform: translate(-50%, -50%) rotateX(65deg) rotate(0deg);}
      to {transform: translate(-50%, -50%) rotateX(65deg) rotate(360deg);}
    }
    header {
      text-align: center;
      padding: 40px 20px 10px;
    }
    header img {
      width: 110px;
      height: 110px;
      border-radius: 50%;
      box-shadow: 0 0 20px rgba(124,92,255,0.5);
    }
    header h1 {
      margin: 15px 0 5px;
      font-size: 32px;
      color: #eae6ff;
      text-shadow: 0 0 15px rgba(124,92,255,0.9), 0 0 25px rgba(91,182,255,0.5);
      animation: glow 3s ease-in-out infinite alternate;
    }
    @keyframes glow {
      from {text-shadow: 0 0 10px rgba(124,92,255,0.5), 0 0 20px rgba(91,182,255,0.3);}
      to {text-shadow: 0 0 20px rgba(124,92,255,1), 0 0 40px rgba(91,182,255,0.8);}
    }
    header p {color: #aaa;}
    .contacts {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin: 20px 0;
    }
    .contacts a {
      color: white;
      text-decoration: none;
      font-size: 22px;
      transition: 0.3s;
    }
    .contacts a:hover {color: #7c5cff;}
    .store {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
      padding: 20px;
      max-width: 900px;
      margin: 0 auto;
    }
    .card {
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.1);
      border-radius: 16px;
      padding: 15px;
      text-align: center;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
    }
    .card img {
      width: 50%;
      display: block;
      margin: 0 auto 10px;
      border-radius: 12px;
    }
    .card button {
      background: linear-gradient(90deg,#7c5cff,#5bb6ff);
      border: none;
      color: #000;
      padding: 10px 20px;
      border-radius: 10px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
    }
    .card button:hover {filter: brightness(1.2);}
    .mute-btn {
      position: fixed;
      top: 15px;
      right: 20px;
      background: rgba(255,255,255,0.1);
      border: none;
      color: #fff;
      font-size: 20px;
      padding: 10px;
      border-radius: 50%;
      cursor: pointer;
      z-index: 10;
    }
  </style>
</head>
<body>
  <div class="stars"></div>
  <div class="saturn"><div class="ring"></div></div>

  <button class="mute-btn" id="muteBtn">🔊</button>
  <audio id="bgm" autoplay loop>
    <source src="https://cdn.pixabay.com/audio/2024/04/03/audio_41eac7c5f5.mp3" type="audio/mpeg">
  </audio>

  <header>
    <img src="https://images.unsplash.com/photo-1606813902788-48a6b3b6f6b8?q=80&w=800" alt="profile">
    <h1>TamzStore</h1>
    <p>@Dikzx_48 | Paid Edit & App Premium</p>
  </header>

  <div class="contacts">
    <a href="https://wa.me/6285782306302" target="_blank">📞</a>
    <a href="https://instagram.com/Dikzx_48" target="_blank">📸</a>
    <a href="https://t.me/tamz_channel" target="_blank">📢</a>
  </div>

  <section class="store">
    <div class="card">
      <img src="https://images.unsplash.com/photo-1559028012-481c04fa702d?q=80&w=800" alt="Paid Edit & App Premium">
      <h3>TamzStore</h3>
      <p>Paid Edit & App Premium</p>
      <button onclick="window.open('https://wa.me/6285782306302?text=Halo%2C+saya+mau+beli+Paid+Edit+atau+App+Premium')">Open</button>
    </div>
    <div class="card">
      <img src="https://upload.wikimedia.org/wikipedia/commons/8/82/Telegram_logo.svg" alt="Telegram Channel">
      <h3>TamzStore</h3>
      <p>Saluran Store Telegram</p>
      <button onclick="window.open('https://t.me/tamaStore_AM_PREM_10k_1thn')">Open</button>
    </div>
    <div class="card">
      <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp Channel">
      <h3>TamzStore</h3>
      <p>Saluran Store WhatsApp</p>
      <button onclick="window.open('https://whatsapp.com/channel/0029Vb5i3i3AojYnGF1zYy2t')">Open</button>
    </div>
  </section>

  <script>
    const bgm = document.getElementById('bgm');
    const btn = document.getElementById('muteBtn');
    let muted = false;

    btn.addEventListener('click', ()=>{
      muted = !muted;
      bgm.muted = muted;
      btn.textContent = muted ? '🔇' : '🔊';
    });
  </script>
</body>
</html>
