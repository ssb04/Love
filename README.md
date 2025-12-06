# Love
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Gülümse 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      animation: pop 1s ease;
      position: relative;
      z-index: 2;
    }

    h1 {
      color: #ff4b5c;
    }

    p {
      font-size: 18px;
      color: #444;
    }

    button {
      margin-top: 20px;
      padding: 12px 25px;
      font-size: 16px;
      border: none;
      border-radius: 30px;
      background: #ff4b5c;
      color: white;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #ff1e36;
      transform: scale(1.05);
    }

    .heart {
      position: absolute;
      color: red;
      font-size: 20px;
      animation: float 6s linear infinite;
      opacity: 0.7;
    }

    @keyframes float {
      0% {
        transform: translateY(0) translateX(0);
        opacity: 0;
      }
      10% { opacity: 1; }
      100% {
        transform: translateY(-800px) translateX(100px);
        opacity: 0;
      }
    }

    @keyframes pop {
      0% { transform: scale(0); }
      100% { transform: scale(1); }
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Canımın İçi 💖</h1>
    <p>Şu an moralin bozuk olabilir ama<br>
    bil ki seni düşünen biri var... hep 💕</p>
    <p>Bir gülümse bakalım, dünya güzelleşsin 😉</p>
    <button onclick="surpriz()">Sürprizi Aç 🎁</button>
    <p id="mesaj"></p>
  </div>

  <script>
    const mesajlar = [
      "Sen gülünce her şey düzeliyor 🌸",
      "Dünyanın en güzel gülüşü sende 😍",
      "Canın sıkkınken bile çok güzelsin 💖",
      "Ben hep buradayım, tamam mı? 🤍",
      "Bir sarılma borcun var bana 🤗"
    ];

    function surpriz() {
      const rastgele = Math.floor(Math.random() * mesajlar.length);
      document.getElementById("mesaj").innerText = mesajlar[rastgele];
    }

    function kalpUret() {
      const kalp = document.createElement("div");
      kalp.classList.add("heart");
      kalp.innerText = "💖";
      kalp.style.left = Math.random() * window.innerWidth + "px";
      kalp.style.fontSize = (15 + Math.random() * 25) + "px";
      document.body.appendChild(kalp);

      setTimeout(() => {
        kalp.remove();
      }, 6000);
    }

    setInterval(kalpUret, 300);
  </script>

</body>
</html>
