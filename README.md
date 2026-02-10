<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>¿Quieres ser mi San Valentín?</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff5f6d, #ffc371);
      font-family: 'Arial', sans-serif;
    }

    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
      max-width: 350px;
    }

    h1 {
      color: #e63946;
      font-size: 28px;
    }

    p {
      font-size: 18px;
      color: #333;
    }

    .buttons {
      margin-top: 30px;
    }

    button {
      padding: 12px 25px;
      font-size: 16px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      margin: 10px;
    }

    .yes {
      background-color: #e63946;
      color: white;
    }

    .no {
      background-color: #ccc;
      color: #333;
      position: absolute;
    }

    .heart {
      font-size: 40px;
      animation: pulse 1.2s infinite;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }
  </style>
</head>
<body>

  <div class="card">
    <div class="heart">❤️</div>
    <h1>¿Quieres ser mi San Valentín?</h1>
    <p>Prometo risas, cariño y muchos momentos bonitos contigo ✨</p>

    <div class="buttons">
      <button class="yes" onclick="aceptar()">Sí 💕</button>
      <button class="no" id="noBtn">No 😢</button>
    </div>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
      const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    });

    function aceptar() {
      document.body.innerHTML = `
        <div style="
          display:flex;
          justify-content:center;
          align-items:center;
          height:100vh;
          background:linear-gradient(135deg,#ff5f6d,#ffc371);
          color:white;
          text-align:center;
          font-family:Arial;
          padding:20px;">
          <div>
            <h1>¡Sabía que dirías que sí! ❤️</h1>
            <p style="font-size:22px;">Este San Valentín será especial 💖</p>
            <div style="font-size:50px;">🥰🌹✨</div>
          </div>
        </div>
      `;
    }
  </script>

</body>
</html>
