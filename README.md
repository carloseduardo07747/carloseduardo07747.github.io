<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliz Dia das Mulheres</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4, #fbc2eb);
            text-align: center;
            font-family: Arial, sans-serif;
            overflow: hidden;
            position: relative;
        }
        .container {
            position: relative;
            width: 90%;
            max-width: 400px;
            overflow: hidden;
        }
        .carousel {
            display: flex;
            width: 300%;
            animation: slide 20s linear infinite;
        }
        .carousel img {
            width: 100%;
            height: 400px;
            object-fit: cover;
            border-radius: 10px;
        }
        @keyframes slide {
            0% { transform: translateX(0); }
            33.33% { transform: translateX(-33.33%); }
            66.66% { transform: translateX(-66.66%); }
            100% { transform: translateX(0); }
        }
        .message {
            margin-top: 10px;
            font-size: 1.5em;
            color: #6a1b9a;
            background: rgba(255, 255, 255, 0.8);
            padding: 10px;
            border-radius: 10px;
        }
        .floating {
            position: absolute;
            font-size: 24px;
            animation: fall 5s linear infinite;
        }
        @keyframes fall {
            0% { transform: translateY(-100px) scale(1); opacity: 1; }
            100% { transform: translateY(100vh) scale(0.5); opacity: 0; }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="carousel">
            <img src="img1.jpg" alt="Sua Foto" onerror="this.style.display='none'">
            <img src="img2.jpg" alt="Sua Foto" onerror="this.style.display='none'">
            <img src="img3.jpg" alt="Sua Foto" onerror="this.style.display='none'">
            <img src="img4.jpg" alt="Sua Foto" onerror="this.style.display='none'">
            <img src="img5.jpg" alt="Sua Foto" onerror="this.style.display='none'">
            <img src="img6.jpg" alt="Sua Foto" onerror="this.style.display='none'">
        </div>
        <p class="message">Meu amor, hoje é um dia especial para celebrar a mulher incrível que você é. 💜 Obrigado por iluminar minha vida com seu amor e carinho. Feliz Dia das Mulheres! ❤️</p>
    </div>
    <script>
        function createFloatingElement() {
            const elements = ["❤️", "🌹", "💖", "💘"];
            const floating = document.createElement("div");
            floating.classList.add("floating");
            floating.innerHTML = elements[Math.floor(Math.random() * elements.length)];
            floating.style.left = Math.random() * 100 + "vw";
            floating.style.animationDuration = Math.random() * 2 + 3 + "s";
            document.body.appendChild(floating);
            setTimeout(() => {
                floating.remove();
            }, 5000);
        }
        setInterval(createFloatingElement, 300);
    </script>
</body>
</html>
