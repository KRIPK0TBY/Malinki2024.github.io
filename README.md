<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Люблю тебя</title>
    <style>
        /* Основные стили */
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background: radial-gradient(circle, #6a0dad, #4b0082, #2a006a);
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            overflow: hidden;
        }

        h1, h2, h3, p {
            text-align: center;
            margin: 10px 0;
            padding: 0 15px; /* Отступы для маленьких экранов */
        }

        h1 {
            font-size: 3em;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
        }

        h2 {
            font-size: 2em;
        }

        h3 {
            font-size: 1.5em;
        }

        p {
            font-size: 1.2em;
        }

        /* Анимации текста */
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

        .fade-in {
            animation: fadeIn 2s ease-out;
        }

        /* Анимация звезд */
        .stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: white;
            opacity: 0.8;
            animation: sparkle 5s infinite ease-in-out;
        }

        @keyframes sparkle {
            0%, 100% {
                opacity: 0.3;
                transform: scale(0.5);
            }
            50% {
                opacity: 1;
                transform: scale(1);
            }
        }

        /* Сердечки */
        .hearts {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }

        .heart {
            width: 20px;
            height: 20px;
            background: rgba(255, 0, 150, 0.8);
            position: absolute;
            animation: float 6s ease-in infinite;
            clip-path: polygon(50% 0%, 61% 19%, 80% 25%, 85% 50%, 50% 100%, 15% 50%, 20% 25%, 39% 19%);
        }

        @keyframes float {
            0% {
                transform: translateY(100vh) scale(0.5);
                opacity: 0;
            }
            50% {
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh) scale(1);
                opacity: 0;
            }
        }

        /* Кнопка */
        .button {
            margin-top: 20px;
            padding: 15px 30px;
            font-size: 1.2em;
            color: white;
            background: #800080;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
            transition: transform 0.3s ease, background 0.3s ease;
        }

        .button:hover {
            background: #a020f0;
            transform: scale(1.1);
        }

        /* Скрытый текст */
        .hidden-message {
            display: none;
            margin-top: 20px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.6);
            border-radius: 15px;
            text-align: center;
            animation: fadeIn 2s ease-out;
        }

        /* Адаптивные стили */
        @media screen and (max-width: 1024px) {
            h1 {
                font-size: 2.5em;
            }

            h2 {
                font-size: 1.8em;
            }

            h3 {
                font-size: 1.3em;
            }

            .button {
                font-size: 1.1em;
            }
        }

        @media screen and (max-width: 768px) {
            h1 {
                font-size: 2em;
            }

            h2 {
                font-size: 1.5em;
            }

            h3 {
                font-size: 1em;
            }

            .button {
                font-size: 1em;
                padding: 10px 20px;
            }

            p {
                font-size: 1em;
            }
        }

        @media screen and (max-width: 480px) {
            h1 {
                font-size: 1.8em;
            }

            h2 {
                font-size: 1.2em;
            }

            h3 {
                font-size: 0.9em;
            }

            .button {
                font-size: 0.9em;
                padding: 8px 15px;
            }

            p {
                font-size: 0.9em;
            }
        }
    </style>
</head>
<body>
    <div class="fade-in">
        <h1>Моей единственной 💜</h1>
        <h2>Ты - вся моя жизнь</h2>
        <h3>Я не могу представить свою жизнь без тебя</h3>
        <p>Каждый день с тобой - это чудо</p>
        <button class="button" onclick="showMessage()">Показать, как сильно я тебя люблю</button>
    </div>

    <div class="hidden-message" id="message">
        <h2>Моя дорогая...</h2>
        <p>Ты самое прекрасное, что случилось в моей жизни. Ты – моя опора, моя радость, мой смысл. С каждым твоим взглядом мое сердце замирает. Я люблю тебя больше, чем слова могут передать. Ты – моя мечта, моя звезда, мой мир. Я всегда буду рядом с тобой, поддерживать, любить и беречь тебя. Ты — мой свет в темноте и моя надежда на будущее. Спасибо за то, что ты есть, моя любовь. 💜</p>
    </div>

    <!-- Звезды -->
    <div class="stars">
        <!-- Генерируем звезды -->
        <div class="star" style="top: 10%; left: 20%; animation-delay: 0s;"></div>
        <div class="star" style="top: 30%; left: 40%; animation-delay: 1s;"></div>
        <div class="star" style="top: 50%; left: 60%; animation-delay: 2s;"></div>
        <div class="star" style="top: 70%; left: 80%; animation-delay: 3s;"></div>
        <div class="star" style="top: 90%; left: 10%; animation-delay: 4s;"></div>
    </div>

    <!-- Сердечки -->
    <div class="hearts">
        <div class="heart" style="left: 10%; animation-delay: 0s;"></div>
        <div class="heart" style="left: 30%; animation-delay: 1s;"></div>
        <div class="heart" style="left: 50%; animation-delay: 2s;"></div>
        <div class="heart" style="left: 70%; animation-delay: 3s;"></div>
        <div class="heart" style="left: 90%; animation-delay: 4s;"></div>
    </div>

    <script>
        function showMessage() {
            document.getElementById('message').style.display = 'block';
        }
    </script>
</body>
</html>
