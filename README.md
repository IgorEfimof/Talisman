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
        @media (max-width: 768px) {
            .products {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <script>
        function sendOrder(productName, price) {
            let botToken = "7586155168:AAFBM7F2HgtL1_DGtDqil60AhJ0E3LODwLM";
            let chatId = "@IgEfR"; // Используем @username канала
            let message = `\u{1F4E6} Новый заказ:\n\n\u{1F4DC} Название: ${productName}\n\u{1F4B0} Цена: ${price} руб.`;

            let url = `https://api.telegram.org/bot${botToken}/sendMessage?chat_id=${chatId}&text=${encodeURIComponent(message)}`;
            
            fetch(url)
                .then(response => response.json())
                .then(data => {
                    if (data.ok) {
                        alert("Заказ отправлен!");
                    } else {
                        alert("Ошибка при отправке заказа!");
                    }
                })
                .catch(error => console.error("Ошибка:", error));
        }
    </script>
</head>
<body>
    <div class="container">
        <h1>Стильные Плетеные Браслеты</h1>
        <div class="products">
            <div class="product">
                <img src="https://i.imgur.com/9dMebEx.jpeg" alt="Браслет 1">
                <h2>Браслет "Шепот Земли"</h2>
                <p>Ручная работа, натуральные материалы, оберег.</p>
                <p><strong>Цена: 590 руб.</strong></p>
                <button class="button" onclick="sendOrder('Браслет Шепот Земли', 590)">Заказать</button>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/E7bluXe.jpeg" alt="Браслет 2">
                <h2>Браслет "Тень и Пламя"</h2>
                <p>Мощный оберег для уверенности и силы.</p>
                <p><strong>Цена: 590 руб.</strong></p>
                <button class="button" onclick="sendOrder('Браслет Тень и Пламя', 590)">Заказать</button>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/STeB3WV.jpeg" alt="Браслет 3">
                <h2>Браслет "Северный страж"</h2>
                <p>Сила природы в каждой нити.</p>
                <p><strong>Цена: 790 руб.</strong></p>
                <button class="button" onclick="sendOrder('Браслет Северный страж', 790)">Заказать</button>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/NN5a7Nq.jpeg" alt="Браслет 4">
                <h2>Браслет "Светлая Нить"</h2>
                <p>Талисман страсти и решимости.</p>
                <p><strong>Цена: 390 руб.</strong></p>
                <button class="button" onclick="sendOrder('Браслет Светлая Нить', 390)">Заказать</button>
            </div>
        </div>
    </div>
</body>
</html>
