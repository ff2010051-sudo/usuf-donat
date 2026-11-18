# usuf-donat<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>USUF DONAT</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        :root {
            --bg-color: #0f1016;
            --card-bg: #1a1c29;
            --accent: #7c3aed;
            --text-main: #ffffff;
            --text-secondary: #9ca3af;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            margin: 0;
            padding: 15px;
        }
        .header {
            background: linear-gradient(135deg, #4f46e5, #7c3aed);
            padding: 20px;
            border-radius: 20px;
            text-align: center;
            margin-bottom: 20px;
            box-shadow: 0 10px 25px rgba(124, 58, 237, 0.3);
        }
        .balance-card {
            background: var(--card-bg);
            padding: 15px;
            border-radius: 16px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            border: 1px solid rgba(255,255,255,0.05);
        }
        .btn {
            background: var(--accent);
            color: white;
            border: none;
            padding: 10px 18px;
            border-radius: 10px;
            font-weight: bold;
            cursor: pointer;
        }
        .section-title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 12px;
        }
        .grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }
        .game-card {
            background: var(--card-bg);
            padding: 15px;
            border-radius: 16px;
            text-align: center;
            border: 1px solid rgba(255,255,255,0.05);
            cursor: pointer;
        }
        .game-card img {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            margin-bottom: 8px;
        }
        .lang-switch {
            text-align: right;
            margin-bottom: 10px;
        }
        .lang-btn {
            background: transparent;
            color: var(--text-secondary);
            border: 1px solid var(--text-secondary);
            padding: 4px 8px;
            border-radius: 6px;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <div class="lang-switch">
        <button class="lang-btn" onclick="setLang('tj')">TJ</button>
        <button class="lang-btn" onclick="setLang('ru')">RU</button>
    </div>

    <div class="header">
        <h1 id="title" style="margin:0; font-size: 22px;">🎮 USUF DONAT</h1>
        <p id="subtitle" style="margin:5px 0 0 0; color: #e0e7ff; font-size: 14px;">Беҳтарин магазин бозӣ дар Тоҷикистон</p>
    </div>

    <div class="balance-card">
        <div>
            <span id="bal-text" style="font-size: 13px; color: var(--text-secondary);">Баланси шумо / Баланс</span>
            <div style="font-size: 20px; font-weight: bold;">0.00 <span id="cur">сом</span></div>
        </div>
        <button class="btn" onclick="topUp()" id="topup-btn">Пур кардан</button>
    </div>

    <div class="section-title" id="games-title">Бозиҳо / Игры</div>
    <div class="grid">
        <div class="game-card" onclick="selectGame('Free Fire')">
            <div style="font-size: 30px;">🔥</div>
            <div style="font-weight: bold;">Free Fire</div>
            <div style="font-size: 12px; color: var(--text-secondary);">Диамантҳо / Алмазы</div>
        </div>
        <div class="game-card" onclick="selectGame('PUBG Mobile')">
            <div style="font-size: 30px;">🎯</div>
            <div style="font-weight: bold;">PUBG Mobile</div>
            <div style="font-size: 12px; color: var(--text-secondary);">UC / ЮСи</div>
        </div>
    </div>

    <script>
        const translations = {
            tj: {
                title: "🎮 USUF DONAT",
                subtitle: "Беҳтарин магазин бозӣ дар Тоҷикистон",
                balText: "Баланси шумо",
                currency: "сом",
                topupBtn: "Пур кардан",
                gamesTitle: "Бозиҳо"
            },
            ru: {
                title: "🎮 USUF DONAT",
                subtitle: "Лучший игровой магазин в Таджикистане",
                balText: "Ваш баланс",
                currency: "сом",
                topupBtn: "Пополнить",
                gamesTitle: "Игры"
            }
        };

        function setLang(lang) {
            document.getElementById('title').innerText = translations[lang].title;
            document.getElementById('subtitle').innerText = translations[lang].subtitle;
            document.getElementById('bal-text').innerText = translations[lang].balText;
            document.getElementById('cur').innerText = translations[lang].currency;
            document.getElementById('topup-btn').innerText = translations[lang].topupBtn;
            document.getElementById('games-title').innerText = translations[lang].gamesTitle;
        }

        function topUp() {
            alert("Барои пур кардани баланс ба админ нависед ё кортро истифода баред!");
        }

        function selectGame(game) {
        alert("Шумо бозии " + game + "-ро интихоб кардед.");
        }
    </script>
</body>
</html>
