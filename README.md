# Www<!DOCTYPE html>
<html>
<head>
    <title>Генератор идей для стартапов</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }

        .container {
            width: 80%;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            margin-bottom: 20px;
        }

        .options {
            display: flex;
            flex-direction: column;
            margin-bottom: 20px;
        }

        label {
            margin-bottom: 5px;
        }

        select {
            padding: 5px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }

        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        #idea {
            margin-top: 20px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Генератор идей для стартапов</h1>
        <div class="options">
            <label for="category">Категория:</label>
            <select id="category">
                <option value="technology">Технологии</option>
                <option value="services">Услуги</option>
                <option value="products">Продукты</option>
            </select>
            <label for="complexity">Сложность:</label>
            <select id="complexity">
                <option value="easy">Легко</option>
                <option value="medium">Средне</option>
                <option value="hard">Сложно</option>
            </select>
            <label for="budget">Бюджет:</label>
            <select id="budget">
                <option value="low">Низкий</option>
                <option value="medium">Средний</option>
                <option value="high">Высокий</option>
            </select>
        </div>
        <button id="generateBtn">Сгенерировать идею</button>
        <div id="idea"></div>
    </div>

    <script>
        const categorySelect = document.getElementById('category');
        const complexitySelect = document.getElementById('complexity');
        const budgetSelect = document.getElementById('budget');
        const generateBtn = document.getElementById('generateBtn');
        const ideaDiv = document.getElementById('idea');

        const ideas = {
            technology: [
                'Приложение для обмена домашней едой с соседями',
                'Сервис по аренде 3D-принтеров',
                'Платформа для обучения программированию в виртуальной реальности'
            ],
            services: [
                'Мобильная химчистка для одежды',
                'Сервис по доставке фермерских продуктов',
                'Агентство по организации детских праздников'
            ],
            products: [
                'Умный ошейник для животных с GPS-трекером',
                'Экологически чистая косметика на основе натуральных ингредиентов',
                'Набор для выращивания микрозелени дома'
            ]
        };

        generateBtn.addEventListener('click', () => {
            const category = categorySelect.value;
            const complexity = complexitySelect.value;
            const budget = budgetSelect.value;

            const categoryIdeas = ideas[category];
            const randomIdea = categoryIdeas[Math.floor(Math.random() * categoryIdeas.length)];

            ideaDiv.textContent = randomIdea;
        });
    </script>
</body>
</html>w
