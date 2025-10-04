<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>La Jefa - La Que Manda</title>

  <!-- Font Awesome para iconos -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(180deg, #660000, #000);
      color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
    }

    .logo {
      width: 260px;
      border-radius: 16px;
      margin-bottom: 25px;
      box-shadow: 0 0 25px rgba(255, 0, 0, 0.6);
    }

    .title {
      font-size: 28px;
      font-weight: bold;
      color: #ff0000;
      text-shadow: 0 0 10px #ff4d4d;
      margin-bottom: 8px;
    }

    .subtitle {
      font-size: 18px;
      color: #fff;
      margin-bottom: 20px;
    }

    .status {
      font-size: 16px;
      color: #fff;
      background: #ff0000;
      padding: 5px 14px;
      border-radius: 8px;
      margin-bottom: 25px;
      text-transform: uppercase;
      font-weight: bold;
    }

    .player button {
      background: #ff0000;
      border: none;
      border-radius: 50%;
      width: 90px;
      height: 90px;
      font-size: 34px;
      color: #fff;
      cursor: pointer;
      box-shadow: 0 0 30px rgba(255, 0, 0, 0.8);
      transition: transform 0.2s ease;
    }

    .player button:hover {
      transform: scale(1.1);
    }

    .socials {
      margin-top: 35px;
      display: flex;
      gap: 30px;
    }

    .socials a {
      font-size: 38px;
      text-decoration: none;
      color: #ff0000;
      transition: 0.3s;
    }

    .socials a:hover {
      color: #fff;
    }
  </style>
</head>
<body>
  <!-- Logo -->
  <img src="https://i.ibb.co/chCCQMpR/IMG-20251002-WA0033.jpg" alt="La Jefa - La Que Manda" class="logo">

  <!-- Título -->
  <div class="title">LA JEFA</div>
  <div class="subtitle">La Que Manda 🔥</div>

  <!-- Estado -->
  <div class="status">EN VIVO</div>

  <!-- Reproductor -->
  <div class="player">
    <button id="playBtn"><i class="fas fa-play"></i></button>
    <audio id="radio" src="https://lavoz14.vitrinamusical.com/listen/la_jefa_/radio.mp3"></audio>
  </div>

  <!-- Redes sociales -->
  <div class="socials">
    <a href="https://facebook.com" target="_blank"><i class="fab fa-facebook"></i></a>
    <a href="https://instagram.com" target="_blank"><i class="fab fa-instagram"></i></a>
    <a href="https://youtube.com" target="_blank"><i class="fab fa-youtube"></i></a>
  </div>

  <script>
    const playBtn = document.getElementById("playBtn");
    const radio = document.getElementById("radio");
    let playing = false;

    playBtn.addEventListener("click", () => {
      if (playing) {
        radio.pause();
        playBtn.innerHTML = '<i class="fas fa-play"></i>';
      } else {
        radio.play();
        playBtn.innerHTML = '<i class="fas fa-pause"></i>';
      }
      playing = !playing;
    });
  </script>
</body>
</html>
