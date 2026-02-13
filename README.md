<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>💝 Pregunta Importante 💝</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 50%, #fbc2eb 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        /* Decoración de fondo */
        .bg-hearts {
            position: fixed;
            width: 100%;
            height: 100%;
            overflow: hidden;
            pointer-events: none;
            z-index: 0;
        }

        .bg-heart {
            position: absolute;
            font-size: 40px;
            opacity: 0.15;
            animation: floatHeart 15s infinite ease-in-out;
        }

        @keyframes floatHeart {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-30px) rotate(10deg);
            }
        }

        .container {
            text-align: center;
            background: linear-gradient(135deg, #fff5f7 0%, #ffe8f0 100%);
            padding: 60px 40px;
            border-radius: 30px;
            box-shadow: 0 20px 60px rgba(255, 105, 180, 0.3);
            max-width: 500px;
            width: 90%;
            position: relative;
            z-index: 1;
            border: 3px solid rgba(255, 182, 193, 0.5);
        }

        /* Pantalla de introducción */
        #intro {
            animation: fadeIn 0.8s ease;
        }

        #intro h1 {
            color: #ff1493;
            font-size: 2.8em;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(255, 105, 180, 0.3);
            line-height: 1.3;
        }

        #intro .emoji {
            font-size: 6em;
            margin-bottom: 30px;
            display: inline-block;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        #intro button {
            background: linear-gradient(135deg, #ff6b9d 0%, #c06c84 100%);
            color: white;
            padding: 18px 50px;
            font-size: 1.3em;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 8px 20px rgba(255, 105, 180, 0.4);
            margin-top: 20px;
        }

        #intro button:hover {
            transform: scale(1.1) translateY(-3px);
            box-shadow: 0 12px 30px rgba(255, 105, 180, 0.5);
        }

        .sparkles {
            position: absolute;
            font-size: 25px;
            opacity: 0.6;
            animation: twinkle 1.5s infinite ease-in-out;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.6; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.2); }
        }

        .sparkle-1 { top: 20px; left: 20px; animation-delay: 0s; }
        .sparkle-2 { top: 20px; right: 20px; animation-delay: 0.3s; }
        .sparkle-3 { bottom: 20px; left: 30px; animation-delay: 0.6s; }
        .sparkle-4 { bottom: 20px; right: 30px; animation-delay: 0.9s; }

        h1 {
            color: #ff1493;
            font-size: 2.5em;
            margin-bottom: 30px;
            animation: pulse 1.5s ease-in-out infinite;
            text-shadow: 2px 2px 4px rgba(255, 105, 180, 0.2);
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .emoji {
            font-size: 5em;
            margin-bottom: 20px;
            display: inline-block;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .buttons {
            margin-top: 40px;
            display: flex;
            gap: 20px;
            justify-content: center;
            position: relative;
            height: 80px;
        }

        button {
            padding: 15px 40px;
            font-size: 1.2em;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(255, 105, 180, 0.3);
        }

        #yesBtn {
            background: linear-gradient(135deg, #ff6b9d 0%, #ff1493 100%);
            color: white;
            border: 3px solid #ff69b4;
        }

        #yesBtn:hover {
            transform: scale(1.15);
            box-shadow: 0 10px 30px rgba(255, 20, 147, 0.5);
        }

        #noBtn {
            background: linear-gradient(135deg, #ffb6c1 0%, #ffc0cb 100%);
            color: #666;
            position: absolute;
            transition: all 0.1s ease;
            border: 2px solid #ffb6c1;
        }

        #noBtn:hover {
            transform: scale(1.05);
        }

        .celebration {
            display: none;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }

        .celebration h2 {
            color: #ff1493;
            font-size: 2.2em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(255, 105, 180, 0.3);
        }

        .celebration p {
            font-size: 1.3em;
            color: #ff69b4;
            margin-top: 20px;
            font-weight: bold;
        }

        .hearts {
            position: fixed;
            pointer-events: none;
        }

        .heart {
            position: absolute;
            font-size: 35px;
            animation: fall 3s linear;
            opacity: 0;
        }

        @keyframes fall {
            0% {
                opacity: 1;
                transform: translateY(0) rotate(0deg) scale(1);
            }
            50% {
                transform: translateY(50vh) rotate(180deg) scale(1.2);
            }
            100% {
                opacity: 0;
                transform: translateY(100vh) rotate(360deg) scale(0.8);
            }
        }

        /* Ocultar pantallas */
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <!-- Decoración de fondo -->
    <div class="bg-hearts">
        <div class="bg-heart" style="top: 10%; left: 10%;">💕</div>
        <div class="bg-heart" style="top: 20%; right: 15%;">💖</div>
        <div class="bg-heart" style="top: 60%; left: 20%;">💗</div>
        <div class="bg-heart" style="bottom: 15%; right: 10%;">💝</div>
        <div class="bg-heart" style="top: 40%; right: 30%;">💓</div>
        <div class="bg-heart" style="bottom: 30%; left: 15%;">💞</div>
    </div>

    <div class="container">
        <!-- Pantalla de introducción -->
        <div id="intro">
            <span class="sparkles sparkle-1">✨</span>
            <span class="sparkles sparkle-2">✨</span>
            <span class="sparkles sparkle-3">✨</span>
            <span class="sparkles sparkle-4">✨</span>
            
            <div class="emoji">💌</div>
            <h1>Tengo algo que preguntarte<br>muy importante...</h1>
            <button onclick="showQuestion()">Continuar 💕</button>
        </div>
        
        <!-- Pantalla de pregunta -->
        <div id="question" class="hidden">
            <span class="sparkles sparkle-1">✨</span>
            <span class="sparkles sparkle-2">✨</span>
            <span class="sparkles sparkle-3">✨</span>
            <span class="sparkles sparkle-4">✨</span>
            
            <div class="emoji">💖</div>
            <h1>¿Quieres ser mi San Valentín?</h1>
            <div class="buttons">
                <button id="yesBtn" onclick="sayYes()">¡Sí! 💕</button>
                <button id="noBtn" onmouseover="moveButton()" onclick="moveButton()">No 😢</button>
            </div>
        </div>
        
        <div id="celebration" class="celebration">
            <span class="sparkles sparkle-1">✨</span>
            <span class="sparkles sparkle-2">✨</span>
            <span class="sparkles sparkle-3">✨</span>
            <span class="sparkles sparkle-4">✨</span>
            
            <div class="emoji">🎉</div>
            <h2>¡Sabía que dirías que sí!</h2>
            <p>¡Eres la mejor! 💝✨<br>¡Feliz San Valentín! 💑</p>
        </div>
    </div>

    <div class="hearts" id="hearts"></div>

    <script>
        const noBtn = document.getElementById('noBtn');
        
        function showQuestion() {
            document.getElementById('intro').classList.add('hidden');
            document.getElementById('question').classList.remove('hidden');
        }
        
        function moveButton() {
            const container = document.querySelector('.buttons');
            const containerRect = container.getBoundingClientRect();
            
            // Obtener dimensiones del botón
            const btnRect = noBtn.getBoundingClientRect();
            
            // Generar posición aleatoria dentro del contenedor
            const maxX = containerRect.width - btnRect.width;
            const maxY = containerRect.height - btnRect.height;
            
            const randomX = Math.random() * maxX;
            const randomY = Math.random() * maxY;
            
            noBtn.style.left = randomX + 'px';
            noBtn.style.top = randomY + 'px';
        }

        function sayYes() {
            document.getElementById('question').style.display = 'none';
            document.getElementById('celebration').style.display = 'block';
            createHearts();
        }

        function createHearts() {
            const heartsContainer = document.getElementById('hearts');
            const heartEmojis = ['❤️', '💕', '💖', '💗', '💓', '💝', '💞', '💘'];
            
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.className = 'heart';
                    heart.innerHTML = heartEmojis[Math.floor(Math.random() * heartEmojis.length)];
                    heart.style.left = Math.random() * window.innerWidth + 'px';
                    heart.style.top = '-50px';
                    heart.style.animationDelay = Math.random() * 2 + 's';
                    heartsContainer.appendChild(heart);
                    
                    setTimeout(() => {
                        heart.remove();
                    }, 3000);
                }, i * 100);
            }
        }

        // Posicionar el botón "No" inicialmente
        window.addEventListener('load', () => {
            if (noBtn) {
                noBtn.style.left = '0px';
                noBtn.style.top = '0px';
            }
        });
    </script>
</body>
</html># SanValentin.epic
