  <!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Любимая, я тебя люблю!</title>
  <style>
    /* Основные стили */
    body {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #6a1b9a, #8e24aa, #ab47bc);
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }

    h1, p {
      text-align: center;
      margin: 0;
      padding: 0;
    }

    h1 {
      font-size: 2.5rem;
      animation: fadeIn 2s ease-in-out forwards;
    }

    p {
      font-size: 1.2rem;
      margin-top: 20px;
      animation: fadeIn 3s ease-in-out forwards;
    }

    /* Анимация */
    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .container {
      text-align: center;
      max-width: 90%;
      margin: auto;
    }

    .button {
      display: inline-block;
      background: white;
      color: #6a1b9a;
      font-size: 1.5rem;
      font-weight: bold;
      text-decoration: none;
      border-radius: 50px;
      padding: 15px 30px;
      margin-top: 30px;
      cursor: pointer;
      transition: all 0.3s ease-in-out;
      animation: bounce 2s infinite ease-in-out;
    }

    .button:hover {
      background: #ab47bc;
      color: white;
      transform: scale(1.1);
    }

    @keyframes bounce {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-10px);
      }
    }

    .hidden {
      display: none;
      opacity: 0;
      animation: appear 2s ease-in-out forwards;
    }

    @keyframes appear {
      from {
        opacity: 0;
        transform: scale(0.8);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    /* Адаптация */
    @media (max-width: 600px) {
      h1 {
        font-size: 2rem;
      }
      p {
        font-size: 1rem;
      }
      .button {
        font-size: 1rem;
        padding: 10px 20px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Моя дорогая, любимая, ненаглядная...</h1>
    <p>Ты даже не представляешь, насколько сильно я тебя люблю.</p>
    <a href="#love-message" class="button" onclick="document.getElementById('message').classList.remove('hidden');">Нажми меня</a>
    <div id="message" class="hidden">
      <h1>Ты для меня всё!</h1>
      <p>Каждый день с тобой – это счастье. Ты мой свет, моя радость и моя душа. Спасибо, что ты есть.</p>
    </div>
  </div>
</body>
</html>
