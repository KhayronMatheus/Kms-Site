<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite Interativo de Aniversário da Sophia - Tema Stitch</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Bubblegum+Sans&family=Nunito:wght@400;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Nunito', sans-serif;
            background: linear-gradient(180deg, #87CEEB 0%, #1E90FF 100%);
            color: #333;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 100%;
            margin: 0 auto;
            overflow: hidden;
        }
        
        .background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background-image: url('https://assets-persist.lovart.ai/agent_images/c5b52f09-7e57-4511-b823-17a1547aefd7.jpg');
            background-size: cover;
            background-position: center;
            opacity: 0.8;
        }
        
        header {
            text-align: center;
            padding: 20px 0;
            position: relative;
        }
        
        .logo {
            max-width: 80%;
            margin: 0 auto;
            animation: float 3s ease-in-out infinite;
        }
        
        .music-control {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.7);
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: transform 0.3s;
        }
        
        .music-control:hover {
            transform: scale(1.1);
        }
        
        .welcome-section {
            text-align: center;
            padding: 40px 20px;
            position: relative;
        }
        
        .stitch-animation {
            max-width: 300px;
            margin: 0 auto;
        }
        
        .speech-bubble {
            background: white;
            border-radius: 30px;
            padding: 20px;
            margin: 20px auto;
            max-width: 80%;
            position: relative;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .speech-bubble:after {
            content: '';
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            border: 10px solid transparent;
            border-bottom-color: white;
        }
        
        .speech-bubble h2 {
            font-family: 'Bubblegum Sans', cursive;
            color: #FF69B4;
            font-size: 2rem;
            margin-bottom: 10px;
        }
        
        .invitation-section {
            background: rgba(255, 255, 255, 0.85);
            border-radius: 30px;
            padding: 40px 20px;
            margin: 20px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }
        
        .decoration {
            position: absolute;
            width: 100px;
            height: 100px;
            opacity: 0.6;
        }
        
        .decoration-1 {
            top: -20px;
            left: -20px;
            transform: rotate(-30deg);
        }
        
        .decoration-2 {
            bottom: -20px;
            right: -20px;
            transform: rotate(30deg);
        }
        
        .invitation-section h1 {
            font-family: 'Bubblegum Sans', cursive;
            color: #FF69B4;
            font-size: 2.5rem;
            margin-bottom: 20px;
            animation: pulse 2s infinite;
        }
        
        .info-card {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            padding: 20px;
            margin: 20px 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .info-card:hover {
            transform: translateY(-5px);
        }
        
        .info-card h3 {
            font-family: 'Bubblegum Sans', cursive;
            color: #1E90FF;
            margin-bottom: 10px;
        }
        
        .info-card p {
            font-size: 1.2rem;
            color: #333;
        }
        
        .location-section {
            padding: 40px 20px;
            text-align: center;
        }
        
        .map-container {
            position: relative;
            margin: 20px auto;
            max-width: 90%;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .map-container img {
            width: 100%;
            display: block;
        }
        
        .map-pin {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -100%);
            width: 60px;
            animation: bounce 2s infinite;
        }
        
        .map-button {
            display: inline-block;
            background: #1E90FF;
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-family: 'Bubblegum Sans', cursive;
            font-size: 1.2rem;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: transform 0.3s, background 0.3s;
        }
        
        .map-button:hover {
            transform: scale(1.05);
            background: #FF69B4;
        }
        
        .rsvp-section {
            padding: 40px 20px;
            text-align: center;
        }
        
        .whatsapp-button {
            display: inline-block;
            background: #25D366;
            color: white;
            padding: 20px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-family: 'Bubblegum Sans', cursive;
            font-size: 1.5rem;
            margin: 20px 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }
        
        .whatsapp-button:hover {
            transform: scale(1.1);
        }
        
        .whatsapp-icon {
            width: 30px;
            vertical-align: middle;
            margin-right: 10px;
        }
        
        footer {
            text-align: center;
            padding: 40px 20px;
            position: relative;
        }
        
        .footer-stitch {
            max-width: 150px;
            margin: 0 auto;
            animation: wave 2s infinite;
        }
        
        .footer-message {
            font-family: 'Bubblegum Sans', cursive;
            color: white;
            font-size: 1.5rem;
            margin-top: 20px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
        }
        
        /* Animations */
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0); }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        @keyframes bounce {
            0%, 100% { transform: translate(-50%, -100%); }
            50% { transform: translate(-50%, -120%); }
        }
        
        @keyframes wave {
            0% { transform: rotate(0); }
            25% { transform: rotate(10deg); }
            75% { transform: rotate(-10deg); }
            100% { transform: rotate(0); }
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .invitation-section h1 {
                font-size: 2rem;
            }
            
            .speech-bubble h2 {
                font-size: 1.5rem;
            }
            
            .info-card p {
                font-size: 1rem;
            }
            
            .whatsapp-button {
                font-size: 1.2rem;
                padding: 15px 30px;
            }
            
            .footer-message {
                font-size: 1.2rem;
            }
        }
        
        /* Easter Eggs */
        .easter-egg {
            position: absolute;
            width: 50px;
            height: 50px;
            opacity: 0;
            cursor: pointer;
            transition: opacity 0.3s;
        }
        
        .easter-egg:hover {
            opacity: 1;
        }
        
        .easter-egg-1 {
            top: 100px;
            right: 50px;
        }
        
        .easter-egg-2 {
            bottom: 150px;
            left: 30px;
        }
        
        /* Floating Elements */
        .floating-element {
            position: absolute;
            pointer-events: none;
            animation: float 5s ease-in-out infinite;
        }
        
        .floating-star-1 {
            top: 10%;
            left: 10%;
            width: 30px;
        }
        
        .floating-star-2 {
            top: 30%;
            right: 15%;
            width: 20px;
            animation-delay: 1s;
        }
        
        .floating-flower-1 {
            bottom: 20%;
            left: 5%;
            width: 40px;
            animation-delay: 2s;
        }
        
        .floating-flower-2 {
            top: 60%;
            right: 8%;
            width: 35px;
            animation-delay: 3s;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="background"></div>
        
        <!-- Floating Elements -->
        <img src="https://assets-persist.lovart.ai/agent_images/61c724ce-ba06-48bc-8584-aafc13c2fbba.jpg" alt="Estrela" class="floating-element floating-star-1">
        <img src="https://assets-persist.lovart.ai/agent_images/61c724ce-ba06-48bc-8584-aafc13c2fbba.jpg" alt="Estrela" class="floating-element floating-star-2">
        <img src="https://assets-persist.lovart.ai/agent_images/61c724ce-ba06-48bc-8584-aafc13c2fbba.jpg" alt="Flor" class="floating-element floating-flower-1">
        <img src="https://assets-persist.lovart.ai/agent_images/61c724ce-ba06-48bc-8584-aafc13c2fbba.jpg" alt="Flor" class="floating-element floating-flower-2">
        
        <header>
            <img src="https://assets-persist.lovart.ai/agent_images/265a2673-945b-4a81-9259-ae444e1e0755.jpg" alt="Festa da Sophia" class="logo">
            <div class="music-control" id="musicControl">🔊</div>
            <audio id="bgMusic" loop>
                <source src="https://assets-persist.lovart.ai/agent_images/b9ac5e6c-3872-4ead-abe7-1ff397553f55.mp3" type="audio/mp3">
            </audio>
        </header>
        
        <section class="welcome-section">
            <img src="https://assets-persist.lovart.ai/agent_images/24e49b49-c0a5-45e2-bdd3-10e9dfa3ef23.gif" alt="Stitch Animado" class="stitch-animation">
            <div class="speech-bubble">
                <h2>Oi! Eu sou o Stitch!</h2>
                <p>Você foi convidado para a festa da Sophia! Venha se divertir comigo!</p>
            </div>
        </section>
        
        <section class="invitation-section">
            <img src="https://assets-persist.lovart.ai/agent_images/61c724ce-ba06-48bc-8584-aafc13c2fbba.jpg" alt="Decoração" class="decoration decoration-1">
            <img src="https://assets-persist.lovart.ai/agent_images/61c724ce-ba06-48bc-8584-aafc13c2fbba.jpg" alt="Decoração" class="decoration decoration-2">
            
            <h1>🎉 Você está convidado para a festa da Sophia! 🎉</h1>
            
            <div class="info-card">
                <h3>📅 Data e Hora</h3>
                <p>18/10/2025 às 10:00h</p>
            </div>
            
            <div class="info-card">
                <h3>📍 Local</h3>
                <p>Sítio do Preto</p>
            </div>
        </section>
        
        <section class="location-section">
            <div class="map-container">
                <img src="https://maps.googleapis.com/maps/api/staticmap?center=-4.9641885,-37.9919023&zoom=15&size=600x300&maptype=roadmap&markers=color:red%7C-4.9641885,-37.9919023&key=YOUR_API_KEY" alt="Mapa">
                <img src="https://assets-persist.lovart.ai/agent_images/4bf9c68e-a602-49e8-8338-c81cc4963e05.jpg" alt="Localização" class="map-pin">
            </div>
            <a href="https://google.com/maps?q=-4.9641885,-37.9919023&z=17&hl=pt-BR" target="_blank" class="map-button">Ver no Mapa</a>
        </section>
        
        <section class="rsvp-section">
            <h2>Confirme sua presença!</h2>
            <a href="https://wa.me/5588992074226?text=Olá!%20Confirmo%20minha%20presença%20na%20festa%20da%20Sophia!" target="_blank" class="whatsapp-button">
                <img src="https://assets-persist.lovart.ai/agent_images/240e18a0-321d-4a02-b64a-bc79cd6365bc.jpg" alt="WhatsApp" class="whatsapp-icon">
                Confirmar Presença
            </a>
        </section>
        
        <footer>
            <img src="https://assets-persist.lovart.ai/agent_images/93fec6ec-43fe-4ef6-90b9-50ec148d96a0.jpg" alt="Stitch" class="footer-stitch">
            <p class="footer-message">Espero você na festa! Vai ser ohana!</p>
        </footer>
        
        <!-- Easter Eggs -->
        <img src="https://assets-persist.lovart.ai/agent_images/93fec6ec-43fe-4ef6-90b9-50ec148d96a0.jpg" alt="Easter Egg" class="easter-egg easter-egg-1">
        <img src="https://assets-persist.lovart.ai/agent_images/93fec6ec-43fe-4ef6-90b9-50ec148d96a0.jpg" alt="Easter Egg" class="easter-egg easter-egg-2">
    </div>
    
    <script>
        // Music Control
        const musicControl = document.getElementById('musicControl');
        const bgMusic = document.getElementById('bgMusic');
        let isMusicPlaying = false;
        
        musicControl.addEventListener('click', function() {
            if (isMusicPlaying) {
                bgMusic.pause();
                musicControl.textContent = '🔊';
            } else {
                bgMusic.play();
                musicControl.textContent = '🔇';
            }
            isMusicPlaying = !isMusicPlaying;
        });
        
        // Interactive Stitch
        const stitchAnimation = document.querySelector('.stitch-animation');
        stitchAnimation.addEventListener('mouseover', function() {
            this.style.transform = 'scale(1.1)';
        });
        stitchAnimation.addEventListener('mouseout', function() {
            this.style.transform = 'scale(1)';
        });
        
        // Easter Eggs
        const easterEggs = document.querySelectorAll('.easter-egg');
        easterEggs.forEach(egg => {
            egg.addEventListener('click', function() {
                alert('Você encontrou um easter egg! Stitch está feliz!');
                this.style.transform = 'rotate(360deg)';
            });
        });
        
        // Scroll Animation
        window.addEventListener('scroll', function() {
            const elements = document.querySelectorAll('.info-card, .speech-bubble, .map-container');
            elements.forEach(element => {
                const position = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if (position < screenPosition) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        });
        
        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            const elements = document.querySelectorAll('.info-card, .speech-bubble, .map-container');
            elements.forEach(element => {
                element.style.opacity = '0';
                element.style.transform = 'translateY(20px)';
                element.style.transition = 'opacity 0.5s, transform 0.5s';
            });
            
            // Trigger scroll event to animate elements in view
            window.dispatchEvent(new Event('scroll'));
        });
    </script>
</body>
</html>
