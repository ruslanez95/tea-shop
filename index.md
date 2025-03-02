<!DOCTYPE html>

<html lang="ru">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Магазин чая</title>

    <style>

        body {

            font-family: Arial, sans-serif;

            text-align: center;

            padding: 20px;

            background-color: #f8f8f8;

        }

        h1 {

            color: #333;

        }

        .button {

            display: block;

            width: 200px;

            margin: 10px auto;

            padding: 10px;

            font-size: 18px;

            color: white;

            background-color: #4CAF50;

            border: none;

            border-radius: 5px;

            cursor: pointer;

        }

        .button:hover {

            background-color: #45a049;

        }

    </style>

</head>

<body>

    <h1>Выберите чай:</h1>

    <button class="button" onclick="sendData('Черный чай')">Черный чай</button>

    <button class="button" onclick="sendData('Зеленый чай')">Зеленый чай</button>



    <script>

        function sendData(product) {

            const tg = window.Telegram.WebApp;

            tg.sendData(product);

            tg.close();

        }

    </script>

</body>

</html>
