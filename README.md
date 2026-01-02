<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Günaydın</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      background-color: #ffe6f0;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: "Segoe UI", Arial, sans-serif;
    }

    /* Ortadaki yazı */
    h1 {
      position: relative;
      z-index: 2;
      font-size: 48px;
      color: #ff2f6e;
      background: rgba(255, 255, 255, 0.8);
      padding: 20px 40px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.15);
    }

    /* Kalpler */
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: #ff5c8a;
      transform: rotate(45deg);
      animation: float 6s linear infinite;
      opacity: 0.8;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: #ff5c8a;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg);
        opacity: 0;
      }
      10% {
        opacity: 0.8;
      }
      100% {
        transform: translateY(-10vh) rotate(45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <h1>Günaydın Bebeğim 💖</h1>

  <!-- Kalpler -->
  <script>
    const heartCount = 40;

    for (let i = 0; i < heartCount; i++) {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (4 + Math.random() * 4) + "s";
      heart.style.width = heart.style.height = (10 + Math.random() * 20) + "px";
      document.body.appendChild(heart);
    }
  </script>

</body>
</html>
