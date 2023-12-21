
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>K+Y ∞</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Open+Sans:wght@400;700&display=swap">
  <style>
    body {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      background: linear-gradient(to right, #6A0572, #AB83A1);
      margin: 0;
      font-family: 'Montserrat', sans-serif;
    }

    .header_text {
      font-size: 24px;
      font-weight: bold;
      color: white;
      text-align: center;
      margin-top: 20px;
      margin-bottom: 0px;
    }

    .buttons {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      margin-top: 20px;
      margin-left: 20px;
    }

    .btn {
      background-color: #8A2BE2;
      color: white;
      padding: 12px 28px;
      text-align: center;
      display: inline-block;
      font-size: 14px;
      margin: 4px 2px;
      cursor: pointer;
      border: none;
      border-radius: 12px;
      transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .btn:hover {
      background-color: #6A5ACD;
      transform: scale(1.05);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    .start_gif_container,
    .ergebnis_gif_container {
      justify-content: center;
      align-items: center;
      margin-top: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      overflow: hidden;
    }

    .start_gif_container img,
    .ergebnis_gif_container img {
      width: 300px; /* Etwas größere GIFs */
      height: auto;
      border-radius: 12px;
    }

    .ergebnis_gif_container {
      display: none;
    }
  </style>
</head>
<body>

<div class="header_text">Keine Lust auf streiten. Du bist mein Teddy + ich liebe dich. Versöhnen und kuscheln?</div>

<div class="buttons">
  <button class="btn" onclick="antwort('Tabiki Askim, immer')">Tabiki Askim, immer</button>
  <button class="btn" onmouseover="moveButton()" onclick="antwort('Nö, kein 🐧 + 🐼 Duo mehr')" id="hayir">Nö, kein 🐧 + 🐼 Duo mehr</button>
</div>

<div class="start_gif_container" id="start_gif">
  <img src="https://media1.tenor.com/m/ivICbYcOlBMAAAAd/jimmiran-china.gif" alt="Start-GIF">
</div>

<div class="ergebnis_gif_container" id="ergebnis_gif">
  <img src="https://media1.tenor.com/m/NJMkAoGOGrkAAAAd/rohee.gif" alt="Neues GIF">
</div>

<script>
  function antwort(antwort) {
    if (antwort === 'Tabiki Askim, immer') {
      document.querySelector('.header_text').innerHTML = 'Wir treffen uns am Montag. Haben noch viel vor uns, Meleğim 🧸♥️';
      document.getElementById('hayir').style.pointerEvents = 'none';
      document.querySelector('.buttons').style.display = 'none';
      document.querySelector('.start_gif_container').style.display = 'none';
      document.querySelector('.ergebnis_gif_container').style.display = 'flex';
    }
  }

  function moveButton() {
    var hayirButton = document.getElementById('hayir');
    var randomX = Math.floor(Math.random() * (window.innerWidth - hayirButton.clientWidth));
    var randomY = Math.floor(Math.random() * (window.innerHeight - hayirButton.clientHeight));

    hayirButton.style.position = 'absolute';
    hayirButton.style.left = randomX + 'px';
    hayirButton.style.top = randomY + 'px';
  }
</script>

</body>
</html>
