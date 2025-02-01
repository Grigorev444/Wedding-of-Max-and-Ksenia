<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Свадьба Максима и Ксении</title>
    <style>
        body {
            font-family: 'Playfair Display', serif;
            margin: 0;
            padding: 0;
            color: #5a4a42;
            background-color: #f7f3e9;
            scroll-behavior: smooth;
        }
        section {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
            padding: 20px;
            background-size: cover;
            background-position: center;
        }
        .hero {
            background-image: url('https://png.pngtree.com/thumb_back/fw800/background/20210925/pngtree-wedding-invitation-poster-background-image_907215.png'); /* Замените на свадебный фон */
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        .hero h1 {
            font-size: 4em;
            margin: 0;
        }
        .hero p {
            font-size: 1.5em;
            margin: 20px 0;
        }
        .names {
            font-size: 2.5em;
            color: #ffd700;
            margin: 20px 0;
        }
        .countdown {
            display: flex;
            gap: 20px;
            margin-top: 20px;
        }
        .countdown div {
            font-size: 2em;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 10px 20px;
            border-radius: 10px;
        }
        .details {
            background-color: rgba(255, 255, 255, 0.9);
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        .details h2 {
            font-size: 2.5em;
            color: #b76e79;
        }
        .details p {
            font-size: 1.2em;
            line-height: 1.6;
        }
        .details img {
            width: 300px;
            border-radius: 10px;
            margin: 20px 0;
        }
        .dress-code {
            font-style: italic;
            color: #b76e79;
        }
        .confirmation {
            font-weight: bold;
            color: #5a4a42;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Первая секция: Приглашение -->
    <section class="hero">
        <h1>Добрый день, уважаемые гости!</h1>
        <p>Приглашаем вас на свадьбу!</p>
        <div class="names">Максим & Ксения</div>
        <div class="countdown" id="countdown">
            <div><span id="days"></span> дней</div>
            <div><span id="hours"></span> часов</div>
            <div><span id="minutes"></span> минут</div>
            <div><span id="seconds"></span> секунд</div>
        </div>
    </section>

    <!-- Вторая секция: Детали мероприятия -->
    <section class="details">
        <h2>Место проведения</h2>
        <p>Город Екатеринбург, 08.08.2025 года</p>
        <p>ЗАГС Пышма, время 10:00</p>
        <img src="https://sun9-60.userapi.com/impg/ltCjRdRsCeZW40L4SJptPPKkLBLsWoo3JG1Frw/8a-ifuKKYeU.jpg?size=960x1280&quality=96&sign=731d2469af4d0515dce8e3a73c034ba0&type=album"> <!-- Замените на ваше фото -->
        <p class="dress-code">Дресс-код: При выборе одежды придерживаемся постельных тонов.</p>
        <p class="confirmation">Пожалуйста, сообщите о своем присутствии до 01.03.2025 года.</p>
        <img src="https://sun9-13.userapi.com/impg/c855528/v855528779/1dc276/eQONg0uSdKU.jpg?size=640x854&quality=96&sign=9dfc455ff74876a0e06fbc28000f754d&type=album"> <!-- Замените на ваше фото -->
        <h2>Ждем вас на свадьбе!</h2>
    </section>

    <script>
        // Таймер до свадьбы
        const weddingDate = new Date('2025-08-08T10:00:00').getTime();

        function updateCountdown() {
            const now = new Date().getTime();
            const timeLeft = weddingDate - now;

            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
