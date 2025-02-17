imgur
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Магазин Браслетов</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f8f8f8;
            padding: 20px;
            margin: 0;
        }
        .container {
            max-width: 800px;
            margin: auto;
            background: white;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
        }
        .products {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }
        .product {
            background: #fff;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
            cursor: pointer;
        }
        .product img {
            width: 100%;
            border-radius: 10px;
            max-width: 300px;
            height: auto;
        }
        .button {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 20px;
            background: #ff5733;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            cursor: pointer;
            border: none;
        }

        /* Стили для модального окна */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background: white;
            padding: 20px;
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            text-align: left;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }
        .close-btn {
            background: red;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            float: right;
        }
        @media (max-width: 768px) {
            .products {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Стильные Плетеные Браслеты</h1>
        <div class="products">
            <div class="product" onclick="openModal()">
                <img src="https://i.imgur.com/9dMebEx.jpeg" alt="Браслет">
                <h2>Браслет с руническими  бусинами</h2>
                <p>Эксклюзивный аксессуар для мужчин и женщин.</p>
                <p><strong>Цена: 790 руб.</strong></p>
                <button class="button">Заказать</button>
            </div>
        </div>
    </div>

    <!-- Модальное окно -->
    <div id="modal" class="modal">
        <div class="modal-content">
            <button class="close-btn" onclick="closeModal()">Закрыть</button>
            <h2>🔥 Стильный браслет руническими бусинами – Идеальный подарок на 23 февраля! 🎁</h2>
            <p>🎄 <strong>Идеальный подарок на 23 февраля!</strong> 🎄</p>
            <p>Этот уникальный браслет сочетает в себе стиль, надежность и символизм. Плетеный шнур из прочного паракорда украшен четырьмя изящными руническими бусинами с древним узором, вдохновленным скандинавскими мотивами.</p>
            <h3>✅ Почему стоит купить этот браслет?</h3>
            <ul>
                <li>✔️ Высококачественные материалы – прочный паракорд и серебро</li>
                <li>✔️ Универсальный стиль – подходит как мужчинам, так и женщинам</li>
             <li>✔️ Оригинальный дизайн – эксклюзивный аксессуар с характером</li>
                <li>✔️ Идея подарка – стильное украшение для любого случая</li>
            </ul>
            <p>💥 Сделайте подарок себе или близким! Закажите прямо сейчас и подчеркните свою индивидуальность! 🎁</p>
        </div>
    </div>

    <script>
        function openModal() {
            document.getElementById("modal").style.display = "flex";
        }
        function closeModal() {
            document.getElementById("modal").style.display = "none";
        }
    </script>
</body>
</html>
