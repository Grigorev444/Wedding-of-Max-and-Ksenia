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
            background-attachment: fixed; /* Фиксированный фон */
        }
        .hero {
            background-image: url('https://balthazar.club/uploads/posts/2023-09/1694502961_balthazar-club-p-krasivii-svadebnii-fon-pinterest-3.jpg'); /* Замените на свадебный фон */
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
            background-image: url('https://balthazar.club/uploads/posts/2023-09/1694502961_balthazar-club-p-krasivii-svadebnii-fon-pinterest-3.jpg'); /* Замените на второй фон */
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        .details h2 {
            font-size: 2.5em;
            color: #ffd700;
        }
        .details p {
            font-size: 1.2em;
            line-height: 1.6;
        }
        .details img {
            width: 300px;
            border-radius: 10px;
            margin: 20px 0;
            border: 5px solid white;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        .dress-code {
            font-style: italic;
            color: #ffd700;
        }
        .confirmation {
            font-weight: bold;
            color: white;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Первая секция: Приглашение -->
    <section class="hero">
        <h1>Добрый день, уважаемые гости!</h1>
        <p>Приглашаем вас на нашу  свадьбу!</p>
        <div class="names">Максим & Ксения</div>
        <div class="countdown" id="countdown">
            <div><span id="days"></span>  дней</div>
            <div><span id="hours"></span>  часов</div>
            <div><span id="minutes"></span>  минут</div>
            <div><span id="seconds"></span>  секунд</div>
        </div>
    </section>

    <!-- Вторая секция: Детали мероприятия -->
    <section class="details">
        <h2>Место проведения</h2>
        <p>Город Екатеринбург, 08.08.2025 года</p>
        <p>ЗАГС Пышма, время 10:00</p>
        <img src="https://sun9-46.userapi.com/impg/c855536/v855536779/1d7184/rM3p_aTuV-w.jpg?size=980x1472&quality=96&sign=161c080c7c48661f2bbab79a2c4c7602&type=album> <!-- Замените на ваше фото -->
        <p class="dress-code">Дресс-код: При выборе одежды придерживаемся постельных тонов.</p>
        <p class="confirmation">Пожалуйста, сообщите о своем присутствии до 01.03.2025 года.</p>
        <img src="https://sun9-55.userapi.com/impg/uPWA1ZWxK4Egjtev0ysN-OAoNxv5PXU_j8rRSA/V6XaCjUNL6w.jpg?size=719x960&quality=96&sign=d9cf3127fe18e706f953ce93d0d351ec&type=album"> <!-- Замените на ваше фото -->
        <h2>Ждем вас на свадьбе!</h2>
    </section>

    <script>
        // Таймер до свадьбы
        const weddingDate = new Date('2025-08-08T10:00:00').getTime();

        function updateCountdown() {
            const now = new Date().getTime();
const timeLeft = weddingDate - now;

            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);

            document.getElementById('days').innerText = days;
            document.getElementById('hours').innerText = hours;
            document.getElementById('minutes').innerText = minutes;
            document.getElementById('seconds').innerText = seconds;

            if (timeLeft < 0) {
                clearInterval(interval);
                document.getElementById('countdown').innerHTML = "<div>Свадьба началась!</div>";
            }
        }

        const interval = setInterval(updateCountdown, 1000);
        updateCountdown();
    </script>
</body>
</html>
