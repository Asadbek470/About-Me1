# About-Me
....1
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Modern Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
  <title>About me</title>
  <style>
    body {
      margin: 0;
      min-height: 100vh;
      font-family: 'Poppins', Arial, sans-serif;
      background: linear-gradient(120deg, #232526, #414345, #1a2980, #26d0ce);
      background-size: 200% 200%;
      animation: gradientMove 12s ease infinite;
      overflow-x: hidden;
    }
    @keyframes gradientMove {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }
    #matrix {
      position: fixed;
      top: 0; left: 0;
      width: 100vw; height: 100vh;
      z-index: 0;
      pointer-events: none;
      opacity: 0.5;
      mix-blend-mode: lighten;
    }
    .container {
      position: relative;
      z-index: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      min-height: 100vh;
      padding: 40px 0;
    }
    .glass-card {
      background: rgba(255,255,255,0.15);
      box-shadow: 0 8px 32px 0 rgba(31,38,135,0.37);
      backdrop-filter: blur(8px);
      border-radius: 24px;
      border: 1px solid rgba(255,255,255,0.18);
      padding: 32px;
      max-width: 800px;
      width: 90%;
      margin-bottom: 32px;
    }
    h1.rainbow {
      font-size: 2.5rem;
      background: linear-gradient(90deg, #ff512f, #dd2476, #1fa2ff, #fbc2eb, #a1c4fd);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      animation: flow 5s linear infinite;
      background-size: 400% 100%;
      text-shadow: 0 2px 8px rgba(0,0,0,0.2);
      margin-bottom: 16px;
    }
    @keyframes flow {
      0% {background-position: 0%;}
      100% {background-position: 100%;}
    }
    .fire {
      font-size: 2.2rem;
      color: #ff9800;
      text-shadow: 0 0 8px #ff0, 0 0 16px #f00, 0 0 32px #f80, 0 0 64px #ff0;
      animation: flicker 0.2s infinite alternate;
      margin-bottom: 16px;
    }
    @keyframes flicker {
      from { text-shadow: 0 0 8px #ff0, 0 0 16px #f00, 0 0 32px #f80, 0 0 64px #ff0; }
      to   { text-shadow: 0 0 4px #ff0, 0 0 8px #f00, 0 0 16px #f80, 0 0 32px #ff0; }
    }
    .btn3d {
      display: inline-block;
      text-decoration: none;
      background: linear-gradient(180deg, #4facfe 0%, #00f2fe 100%);
      color: white;
      font-size: 1.1rem;
      font-weight: bold;
      padding: 14px 32px;
      border-radius: 12px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.2), 0 2px 0 #0d6efd;
      cursor: pointer;
      transition: transform 0.2s, box-shadow 0.2s;
      margin: 8px;
      border: none;
    }
    .btn3d:hover {
      transform: translateY(-4px) scale(1.05);
      box-shadow: 0 16px 32px rgba(0,0,0,0.3), 0 4px 0 #0d6efd;
    }
    .btn3d:active {
      transform: translateY(2px);
      box-shadow: 0 4px 8px rgba(0,0,0,0.2), 0 1px 0 #0d6efd;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      font-family: inherit;
      margin-top: 24px;
      background: rgba(255,255,255,0.12);
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 2px 12px rgba(0,0,0,0.08);
    }
    thead th {
      background: #232526;
      color: #fff;
      padding: 12px;
      text-align: left;
    }
    tbody td {
      padding: 12px;
      border: 1px solid #ccc;
      background: rgba(255,255,255,0.18);
      color: #232526;
    }
    footer {
      margin-top: 32px;
      color: #fff;
      text-align: center;
      font-size: 1.2rem;
      opacity: 0.8;
    }
    img {
      border-radius: 16px;
      box-shadow: 0 4px 24px rgba(0,0,0,0.18);
      max-width: 320px;
      margin: 16px 0;
    }
    /* Dark theme toggle */
    body.dark {
      background: #181818;
      color: #eee;
    }
    body.dark .glass-card {
      background: rgba(24,24,24,0.7);
      color: #eee;
    }
    body.dark table {
      background: rgba(24,24,24,0.7);
    }
    body.dark thead th {
      background: #333;
      color: #fff;
    }
    body.dark tbody td {
      background: rgba(24,24,24,0.9);
      color: #eee;
    }
  </style>
  <script>
    // Password gate
    (function () {
      var css = document.createElement('style');
      css.id = 'gate-css';
      css.textContent = 'body{visibility:hidden}';
      document.head.appendChild(css);
      function ask() {
        var pass = prompt('Введите пароль для входа:');
        if (pass === null) { ask(); return; }
        if (pass === '0903') {
          document.body.style.visibility = 'visible';
          var el = document.getElementById('gate-css');
          if (el) el.remove();
        } else {
          alert('Неверный пароль. Попробуйте снова.');
          ask();
        }
      }
      window.addEventListener('DOMContentLoaded', ask);
    })();
  </script>
</head>
<body>
  <canvas id="matrix"></canvas>
  <div class="container">
    <div class="glass-card">
      <h1 class="rainbow">Welcome To my website</h1>
      <h1 class="fire">SECRET</h1>
      <button onclick="document.body.classList.toggle('dark')" class="btn3d">🌙 Тема</button>
      <p>
        Hi my Name is Asadbek. I'm 12 y.o. I want to work in all jobs in the world!<br>
        My second usual work is business. I read "Rich Dad Poor Dad" and Robert says it's interesting to try different jobs. I want to try it too!
      </p>
      <img src="https://img.moneytimes.ru/preview/article/4/8/5/76485_w.jpeg" alt="Me">
      <article><p style="color: #2196f3;">My Photo</p></article>
      <p>
        I Have a question! Did you want to try Hacking? This Site can help with them!
      </p>
      <h1 class="fire" style="color: #00ff48;">Hacking</h1>
      <button class="btn3d"><a href="https://asadbek470.github.io/Hacking2.3.5/" style="color:inherit;text-decoration:none;">Hacking</a></button>
      <button class="btn3d"><a href="../public/contact.html" style="color:inherit;text-decoration:none;">My number</a></button>
      <p style="color: #2196f3;">My phone number</p>
      <hr>
      <!-- Facts, table, etc. -->
      <h2>Самые лучшие искусственные интеллекты</h2>
      <table>
        <thead>
          <tr>
            <th>#</th>
            <th>Название</th>
            <th>Разработчик</th>
            <th>Особенности</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>ChatGPT</td>
            <td>OpenAI</td>
            <td>Мультимодальный ассистент, сильный в диалогах и коде</td>
          </tr>
          <tr>
            <td>2</td>
            <td>DeepSeek</td>
            <td>DeepSeek AI</td>
            <td>Эффективный, хорош в коде и математике</td>
          </tr>
          <tr>
            <td>3</td>
            <td>Gemini</td>
            <td>Google</td>
            <td>Понимает текст, изображения и видео</td>
          </tr>
          <tr>
            <td>4</td>
            <td>Claude</td>
            <td>Anthropic</td>
            <td>Длинный контекст, аккуратный стиль общения</td>
          </tr>
          <tr>
            <td>5</td>
            <td>Llama</td>
            <td>Meta</td>
            <td>Открытая модель, удобна для доработки</td>
          </tr>
        </tbody>
      </table>
      <a href="https://www.Youtube.com" class="btn3d">Youtube</a>
      <a href="https://www.google.com" class="btn3d">Google</a>
      <hr>
      <footer>
        <h1>Asadbek 2025</h1>
        <u>Thanks For Reading</u>
      </footer>
    </div>
    <iframe width="800" height="450" src="https://www.youtube.com/embed/numCkbbyzJk" title="АДЛИН — Dead Inside (официальная премьера трека)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen style="margin-top:32px;border-radius:16px;box-shadow:0 4px 24px rgba(0,0,0,0.18);"></iframe>
  </div>
  <script>
    // Matrix effect
    const c = document.getElementById("matrix");
    const ctx = c.getContext("2d");
    function resizeMatrix() {
      c.width = window.innerWidth;
      c.height = window.innerHeight;
    }
    resizeMatrix();
    window.addEventListener('resize', resizeMatrix);
    const letters = "101010101";
    const fontSize = 16;
    let columns = Math.floor(c.width / fontSize);
    let drops = Array(columns).fill(1);
    function draw() {
      ctx.fillStyle = "rgba(0, 0, 0, 0.08)";
      ctx.fillRect(0, 0, c.width, c.height);
      ctx.fillStyle = "#0f0";
      ctx.font = fontSize + "px monospace";
      for (let i = 0; i < drops.length; i++) {
        const text = letters[Math.floor(Math.random() * letters.length)];
        ctx.fillText(text, i * fontSize, drops[i] * fontSize);
        if (drops[i] * fontSize > c.height && Math.random() > 0.975) drops[i] = 0;
        drops[i]++;
      }
    }
    setInterval(draw, 35);
    window.addEventListener('resize', () => {
      columns = Math.floor(c.width / fontSize);
      drops = Array(columns).fill(1);
    });
  </script>
</body>
</html>
  
