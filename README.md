<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Browser Games</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background: #111827;
            color: white;
        }

        header {
            text-align: center;
            padding: 40px 20px 30px;
            background: #1f2937;
            border-bottom: 3px solid #374151;
        }

        header h1 {
            margin: 0 0 10px;
            font-size: 42px;
        }

        header p {
            margin: 0;
            color: #9ca3af;
            font-size: 17px;
        }

        .container {
            max-width: 1200px;
            margin: auto;
            padding: 35px 20px;
        }

        .search {
            width: 100%;
            padding: 15px 18px;
            margin-bottom: 30px;
            border: none;
            border-radius: 10px;
            background: #374151;
            color: white;
            font-size: 16px;
            outline: none;
        }

        .search::placeholder {
            color: #9ca3af;
        }

        .game-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 22px;
        }

        .game-card {
            display: block;
            text-decoration: none;
            color: white;
            background: #1f2937;
            border-radius: 15px;
            overflow: hidden;
            border: 2px solid transparent;
            transition: transform 0.2s, border-color 0.2s, box-shadow 0.2s;
        }

        .game-card:hover {
            transform: translateY(-5px);
            border-color: #60a5fa;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }

        .game-icon {
            height: 150px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 65px;
            background: #374151;
        }

        .game-info {
            padding: 18px;
        }

        .game-info h2 {
            margin: 0 0 7px;
            font-size: 21px;
        }

        .game-info p {
            margin: 0;
            color: #9ca3af;
            font-size: 14px;
        }

        footer {
            text-align: center;
            padding: 30px;
            color: #6b7280;
        }

        @media (max-width: 500px) {
            header h1 {
                font-size: 32px;
            }

            .game-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>🎮 Browser Games</h1>
        <p>Choose a game and start playing!</p>
    </header>

    <main class="container">

        <input
            type="text"
            id="search"
            class="search"
            placeholder="🔎 Search games..."
        >

        <div class="game-grid" id="gameGrid">

            <a class="game-card" href="geometry-dash.html" data-name="Geometry Dash">
                <div class="game-icon">🟨</div>
                <div class="game-info">
                    <h2>Geometry Dash</h2>
                    <p>Jump, dodge, and survive!</p>
                </div>
            </a>

            <a class="game-card" href="snake.html" data-name="Snake">
                <div class="game-icon">🐍</div>
                <div class="game-info">
                    <h2>Snake</h2>
                    <p>Eat the food and grow!</p>
                </div>
            </a>

            <a class="game-card" href="pong.html" data-name="Pong">
                <div class="game-icon">🏓</div>
                <div class="game-info">
                    <h2>Pong</h2>
                    <p>Classic paddle action.</p>
                </div>
            </a>

            <a class="game-card" href="breakout.html" data-name="Breakout">
                <div class="game-icon">🧱</div>
                <div class="game-info">
                    <h2>Breakout</h2>
                    <p>Destroy all the blocks!</p>
                </div>
            </a>

            <a class="game-card" href="space-shooter.html" data-name="Space Shooter">
                <div class="game-icon">🚀</div>
                <div class="game-info">
                    <h2>Space Shooter</h2>
                    <p>Defend yourself from enemies.</p>
                </div>
            </a>

            <a class="game-card" href="flappy.html" data-name="Flappy">
                <div class="game-icon">🐦</div>
                <div class="game-info">
                    <h2>Flappy</h2>
                    <p>Fly through the obstacles!</p>
                </div>
            </a>

            <a class="game-card" href="tictactoe.html" data-name="Tic Tac Toe">
                <div class="game-icon">❌</div>
                <div class="game-info">
                    <h2>Tic-Tac-Toe</h2>
                    <p>Get three in a row.</p>
                </div>
            </a>

            <a class="game-card" href="memory.html" data-name="Memory">
                <div class="game-icon">🃏</div>
                <div class="game-info">
                    <h2>Memory</h2>
                    <p>Match all the cards.</p>
                </div>
            </a>

        </div>

    </main>

    <footer>
        Browser Games &copy; 2026
    </footer>

    <script>
        const search = document.getElementById("search");
        const cards = document.querySelectorAll(".game-card");

        search.addEventListener("input", function () {
            const searchText = search.value.toLowerCase();

            cards.forEach(function (card) {
                const gameName = card.dataset.name.toLowerCase();

                if (gameName.includes(searchText)) {
                    card.style.display = "block";
                } else {
                    card.style.display = "none";
                }
            });
        });
    </script>

</body>
</html># HTML-Games
