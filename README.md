<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Mariel ❤️</title>
    <!-- Fuentes bonitas de Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Quicksand:wght@500;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #a1c4fd 100%);
            font-family: 'Quicksand', sans-serif;
            overflow-x: hidden;
            position: relative;
            padding: 20px;
        }

        /* Contenedor principal */
        .card {
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(10px);
            border-radius: 30px;
            padding: 40px 30px;
            max-width: 650px;
            width: 100%;
            text-align: center;
            box-shadow: 0 15px 35px rgba(255, 105, 180, 0.3),
                        0 5px 15px rgba(0, 0, 0, 0.07);
            border: 4px solid #fff;
            position: relative;
            z-index: 10;
            animation: fadeIn 1.5s ease-in-out;
        }

        /* Título decorativo */
        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 3.2rem;
            color: #ff3366;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(255, 105, 180, 0.2);
        }

        /* Mensaje central */
        .mensaje {
            font-size: 1.25rem;
            line-height: 1.8;
            color: #4a4a4a;
            font-weight: 500;
        }

        .highlight {
            color: #e6005c;
            font-weight: 700;
        }

        /* Decoración de tulipanes a los lados */
        .tulipanes-izquierda, .tulipanes-derecha {
            position: fixed;
            bottom: 10px;
            font-size: 3.5rem;
            z-index: 5;
            user-select: none;
            filter: drop-shadow(0 5px 5px rgba(0,0,0,0.1));
        }

        .tulipanes-izquierda {
            left: 20px;
            transform: rotate(-10deg);
        }

        .tulipanes-derecha {
            right: 20px;
            transform: rotate(10deg);
        }

        /* Animación de entrada */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px) scale(0.95);
            }
            to {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }

        /* Corazones flotantes de fondo */
        .heart {
            position: fixed;
            color: #ff4b72;
            font-size: 20px;
            user-select: none;
            pointer-events: none;
            z-index: 1;
            animation: floatUp 4s linear infinite;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(100vh) scale(0.5) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh) scale(1.3) rotate(360deg);
                opacity: 0;
            }
        }

        /* Responsivo para celulares */
        @media (max-width: 600px) {
            h1 { font-size: 2.5rem; }
            .mensaje { font-size: 1.1rem; }
            .tulipanes-izquierda, .tulipanes-derecha { font-size: 2.2rem; }
        }
    </style>
</head>
<body>

    <!-- Tulipanes laterales -->
    <div class="tulipanes-izquierda">🌷🌷🌷</div>
    <div class="tulipanes-derecha">🌷🌷🌷</div>

    <!-- Carta principal -->
    <div class="card">
        <h1>Hola Mariel 💕✨</h1>
        <p class="mensaje">
            Sé que te lo digo diario, pero <span class="highlight">eres lo mejor que me ha pasado</span>. 💗 
            Te quiero muchísimo y quiero que sepas que me estoy esforzando diario para ser mejor por ti, 
            porque te lo mereces y estaré para ti siempre sin importar qué. 💕<br><br>
            Eres lo que siempre soñé y te tengo. Sé que estamos a distancia, pero eso no implica que te deje de amar; 
            al contrario, <span class="highlight">se intensifica</span>. 💖<br><br>
            ¡Te quiero muchísimo! 💞
        </p>
    </div>

    <!-- Script para generar la lluvia/efecto de corazones flotantes -->
    <script>
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            
            // Variación de íconos de corazones
            const hearts = ['💖', '💗', '💓', '💞', '💕', '❤️', '🌸'];
            heart.innerText = hearts[Math.floor(Math.random() * hearts.length)];
            
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = Math.random() * 2 + 3 + "s"; // entre 3s y 5s
            heart.style.fontSize = Math.random() * 15 + 15 + "px";
            
            document.body.appendChild(heart);
            
            setTimeout(() => {
                heart.remove();
            }, 5000);
        }

        // Generar corazones continuamente
        setInterval(createHeart, 300);
    </script>
</body>
</html>
