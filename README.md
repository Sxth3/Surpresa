<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Meu Amor ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 50%, #16213e 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
        }

        /* Efeitos de partículas/estrelas brancas no fundo */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                radial-gradient(2px 2px at 20px 30px, #ffffff, transparent),
                radial-gradient(2px 2px at 40px 70px, rgba(255,255,255,0.8), transparent),
                radial-gradient(1px 1px at 90px 40px, #ffffff, transparent),
                radial-gradient(1px 1px at 130px 80px, rgba(255,255,255,0.6), transparent),
                radial-gradient(2px 2px at 160px 30px, #ffffff, transparent);
            background-repeat: repeat;
            background-size: 200px 100px;
            animation: sparkle 8s linear infinite;
            pointer-events: none;
            opacity: 0.6;
        }

        /* Efeito de ondas flutuantes */
        body::after {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 120%;
            height: 120%;
            background: 
                radial-gradient(ellipse at 10% 20%, rgba(255,255,255,0.1) 0%, transparent 50%),
                radial-gradient(ellipse at 80% 80%, rgba(255,255,255,0.08) 0%, transparent 50%),
                radial-gradient(ellipse at 40% 40%, rgba(255,255,255,0.06) 0%, transparent 50%);
            animation: float 12s ease-in-out infinite;
            pointer-events: none;
        }

        @keyframes sparkle {
            0% { transform: translateY(0px); }
            100% { transform: translateY(-100px); }
        }

        @keyframes float {
            0%, 100% { transform: translate(0px, 0px) rotate(0deg); }
            33% { transform: translate(30px, -30px) rotate(1deg); }
            66% { transform: translate(-20px, 20px) rotate(-1deg); }
        }

        .container {
            background: rgba(20, 20, 30, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            max-width: 800px;
            width: 100%;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            animation: fadeIn 1s ease-out;
            position: relative;
            z-index: 10;
        }

        /* Efeito de brilho nos cantos do container */
        .container::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, 
                rgba(255,255,255,0.1), 
                transparent, 
                rgba(255,255,255,0.1), 
                transparent, 
                rgba(255,255,255,0.1));
            border-radius: 20px;
            z-index: -1;
            animation: borderGlow 3s ease-in-out infinite;
        }

        @keyframes borderGlow {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 0.8; }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 {
            color: #ffffff;
            font-size: 2.5em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 8px rgba(255, 255, 255, 0.3);
            background: linear-gradient(
                45deg,
                #ff6b6b,
                #ffd93d,
                #6bcf7f,
                #4d9de0,
                #9b59b6,
                #ff6b6b
            );
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: waveColors 4s ease-in-out infinite;
        }

        @keyframes waveColors {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        .heart {
            font-size: 3em;
            color: #ff6b6b;
            animation: heartbeat 1.5s ease-in-out infinite;
            display: inline-block;
            margin: 20px 0;
            filter: drop-shadow(0 0 10px rgba(255, 107, 107, 0.5));
        }

        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        .message {
            font-size: 1.2em;
            line-height: 1.6;
            color: #e0e0e0;
            margin: 30px 0;
            padding: 20px;
            background: rgba(0, 0, 0, 0.4);
            border-radius: 15px;
            border-left: 4px solid #ff6b6b;
            backdrop-filter: blur(5px);
        }

        .photo-gallery {
            display: flex;
            justify-content: center;
            margin: 30px 0;
        }

        .photo-placeholder {
            background: linear-gradient(45deg, #2d1b4e 0%, #1a1a2e 50%, #0f0f23 100%);
            height: 300px;
            width: 300px;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #ffffff;
            font-size: 1.1em;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.8);
            transition: transform 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(5px);
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }

        .photo-placeholder img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 15px;
        }

        .photo-placeholder:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(255, 255, 255, 0.2);
        }

        .reasons {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            padding: 25px;
            margin: 30px 0;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(5px);
        }

        .reasons h3 {
            color: #ffffff;
            margin-bottom: 20px;
            font-size: 1.5em;
        }

        .reason-item {
            background: linear-gradient(45deg, #1a1a2e, #16213e);
            color: #ffffff;
            padding: 15px;
            margin: 10px 0;
            border-radius: 10px;
            transform: translateX(-10px);
            animation: slideIn 0.5s ease-out forwards;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .reason-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, 
                transparent, 
                rgba(255, 255, 255, 0.2), 
                transparent);
            transition: left 1.5s;
        }

        .reason-item:hover::before {
            left: 100%;
        }

        .reason-item:nth-child(even) {
            background: linear-gradient(45deg, #2d1b4e, #1a1a2e);
        }

        @keyframes slideIn {
            to { transform: translateX(0); }
        }

        .footer {
            margin-top: 40px;
            font-style: italic;
            color: #b0b0b0;
            font-size: 1.1em;
        }

        .date {
            background: rgba(255, 107, 107, 0.2);
            border-radius: 10px;
            padding: 15px;
            margin: 20px 0;
            color: #ff6b6b;
            font-weight: bold;
            border: 1px solid rgba(255, 107, 107, 0.3);
        }

        @media (max-width: 600px) {
            .container {
                padding: 20px;
            }
            
            h1 {
                font-size: 2em;
            }
            
            .message {
                font-size: 1.1em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Dedico meu amor pra você</h1>
        <div class="heart">❤️</div>
        
        <div class="message">
            <strong>Oi, minha princesa.</strong><br><br>
            Criei este cantinho especial e diferente do normal pq sou uma pessoa inovadora, só queria dizer o quanto te amo através de cálculos e comandos. O bagulho chatinho de fazer.
        </div>

        <div class="date">
            📅 Amando você desde 03/09/2023.❤️
        </div>

        <div class="photo-gallery">
            <div class="photo-placeholder">
                <!-- Sua foto especial -->
                <img src="https://photos.app.goo.gl/EKufz4XqYbWug1yNA">
            </div>
        </div>

        <div class="reasons">
            <h3>Por que eu te amo:</h3>
            <div class="reason-item">💫 Amar você me trás felicidades.</div>
            <div class="reason-item">🌟 Seu lindo sorriso ilumina meus dias.</div>
            <div class="reason-item">💝 Sua personalidade e seu jeito gentil e delicada.</div>
            <div class="reason-item">🎵 Amar você é o que eu escolheria todas as vezes.</div>
            <div class="reason-item">🌷 Sua forma única de ver o mundo.</div>
            <div class="reason-item">💕 Como você me faz rir mesmo nos dias difíceis.</div>
        </div>

        <div class="message">
            <strong>Uma promessa:</strong><br>
            Prometo ama-la cada vez mais, estarei sempre ao seu lado em qualquer situação, pq foi você q eu escolhi pra minha vida. 🌷
        </div>

        <div class="footer">
            Com todo meu amor,<br>
            <strong>[Gui] 🐒</strong>
        </div>
    </div>
</body>
</html>
