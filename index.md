<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>🌎 International Business</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

  <style>
    *, *::before, *::after {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Inter', sans-serif;
      background-color: #121212;
      color: #f0f0f0;
      padding: 20px;
    }

    .container {
      max-width: 900px;
      margin: auto;
      background-color: #1e1e1e;
      border-radius: 12px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
      padding: 30px;
    }

    h1 {
      text-align: center;
      color: #00bfff;
      margin-bottom: 20px;
    }

    input#searchInput {
      width: 100%;
      padding: 12px 16px;
      font-size: 16px;
      border-radius: 8px;
      border: none;
      margin-bottom: 30px;
      background-color: #2a2a2a;
      color: #ffffff;
    }

    .article-card {
      background-color: #2a2a2a;
      border-left: 4px solid #00bfff;
      padding: 20px;
      border-radius: 10px;
      margin-bottom: 20px;
      transition: transform 0.2s ease;
    }

    .article-card:hover {
      transform: translateY(-5px);
    }

    .article-card h2 {
      color: #00bfff;
      margin-top: 0;
    }

    .article-card p {
      color: #cccccc;
    }

    .article-card img {
      width: 100%;
      border-radius: 8px;
      margin: 15px 0;
    }

    a {
      color: #00bfff;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>🌎 International Business</h1>

    <input
      type="text"
      id="searchInput"
      placeholder="Поиск по названию статьи..."
      onkeyup="searchArticles()"
    />

    <div class="article-card">
      <h2>📈 3 формы выхода компании на международный рынок 📈</h2>
      <img src="un_speech.jpg" alt="Выступление у трибуны">
      <p>📌 Компании выходят за границу не только открывая филиалы. Вот 3 основные формы:</p>
      <p>1. Экспорт — самый простой путь...</p>
      <p>2. Лицензирование и франчайзинг — быстрый рост...</p>
      <p>3. Прямые инвестиции — создание дочерних компаний...</p>
    </div>

    <!-- Добавь остальные статьи тут по аналогии -->

  </div>

  <script>
    function searchArticles() {
      const input = document.getElementById("searchInput").value.toLowerCase();
      const cards = document.getElementsByClassName("article-card");

      for (let i = 0; i < cards.length; i++) {
        const title = cards[i].getElementsByTagName("h2")[0].innerText.toLowerCase();
        cards[i].style.display = title.includes(input) ? "" : "none";
      }
    }
  </script>

</body>
</html>
