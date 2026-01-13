<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Feliz Aniversário ❤️</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, sans-serif;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .card {
      background: white;
      padding: 30px;
      border-radius: 25px;
      text-align: center;
      width: 90%;
      max-width: 400px;
      box-shadow: 0 15px 35px rgba(0,0,0,0.25);
      z-index: 2;
      animation: aparecer 1.5s ease;
    }

    h1 {
      color: #ff4d6d;
      margin-bottom: 10px;
    }

    p {
      color: #444;
      font-size: 18px;
    }

    .heart {
      font-size: 50px;
      animation: pulse 1s infinite;
    }

    button {
      margin-top: 20px;
      padding: 12px 25px;
      border: none;
      border-radius: 20px;
      background: #ff4d6d;
      color: white;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #e63956;
      transform: scale(1.05);
    }

    .mensagem {
      display: none;
      margin-top: 15px;
      font-weight: bold;
      color: #ff4d6d;
    }

    /* Balões */
    .balloon {
      position: absolute;
      bottom: -150px;
      width: 60px;
      height: 80px;
      border-radius: 50%;
      animation: subir 8s linear infinite;
      opacity: 0.8;
    }

    .balloon::after {
      content: '';
      position: absolute;
      width: 2px;
      height: 40px;
      background: #555;
      top: 80px;
      left: 50%;
    }

    .b1 { left: 10%; background: #ff4d6d; animation-delay: 0s; }
    .b2 { left: 30%; background: #ffb703; animation-delay: 2s; }
    .b3 { left: 50%; background: #8ecae6; animation-delay: 4s; }
    .b4 { left: 70%; background: #b5179e; animation-delay: 1s; }
    .b5 { left: 90%; background: #52b788; animation-delay: 3s; }

    @keyframes subir {
      0% {
        transform: translateY(0);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      100% {
        transform: translateY(-120vh);
        opacity: 0;
      }
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }

    @keyframes aparecer {
      from {
        opacity: 0;
        transform: translateY(40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <!-- Balões -->
  <div class="balloon b1"></div>
  <div class="balloon b2"></div>
  <div class="balloon b3"></div>
  <div class="balloon b4"></div>
  <div class="balloon b5"></div>

  <!-- Card -->
  <div class="card">
    <div class="heart">🎉❤️</div>
    <h1>Feliz Aniversário!</h1>
    <p>
      Hoje é seu dia 💖  
      Mesmo não estando juntos agora,  
      meu coração tá com você.
    </p>

    <button onclick="mostrarMensagem()">Clique aqui 🎁</button>

    <div class="mensagem" id="msg">
      Eu te amo. Que seu dia seja incrível ✨
    </div>
  </div>

  <script>
    function mostrarMensagem() {
      document.getElementById("msg").style.display = "block";
    }
  </script>

</body>
</html>