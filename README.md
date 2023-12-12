<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday!</title>
    <style>
        body {
            font-family: 'Impact', sans-serif;
            background-image: url("sneha.jpg"); /* Replace with your background image URL */
            background-size: cover;
            background-position: center;
            text-align: center;
            margin: 0;
            padding: 0;
            color: #fff; /* Set text color to be readable on the background */
        }

        #container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: rgba(255, 255, 255, 0.1); /* Add a semi-transparent white background to the content */
            padding: 20px;
        }

        #birthday-heading {
            color: Skyblue;
            font-size: 2.5em;
            margin-bottom: 20px;
        }

        #cake-image {
            width: 200px;
            margin-bottom: 20px;
        }

        #birthday-message {
            color: #ff4500;
            font-size: 1.2em;
            margin-bottom: 20px;
        }

        #balloons {
            font-size: 2em;
            color: #ff69b4;
        }

        #confetti {
            width: 100%;
            position: fixed;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 1000;
        }

        @keyframes confetti-fall {
            0% {
                transform: translateY(-100vh);
            }
            100% {
                transform: translateY(100vh);
            }
        }

        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #ff69b4;
            border-radius: 50%;
            animation: confetti-fall linear infinite;
        }

        .confetti:nth-child(1) {
            left: 5%;
            animation-duration: 5s;
        }

        .confetti:nth-child(2) {
            left: 15%;
            animation-duration: 7s;
        }

        .confetti:nth-child(3) {
            left: 25%;
            animation-duration: 6s;
        }

        .confetti:nth-child(4) {
            left: 35%;
            animation-duration: 5.5s;
        }

        .confetti:nth-child(5) {
            left: 45%;
            animation-duration: 7.5s;
        }

        .confetti:nth-child(6) {
            left: 55%;
            animation-duration: 6.5s;
        }

        .confetti:nth-child(7) {
            left: 65%;
            animation-duration: 5s;
        }

        .confetti:nth-child(8) {
            left: 75%;
            animation-duration: 6.7s;
        }

        .confetti:nth-child(9) {
            left: 85%;
            animation-duration: 5.2s;
        }

        .confetti:nth-child(10) {
            left: 95%;
            animation-duration: 7.2s;
        }
    </style>
</head>
<body>
    <div id="container">
        <h1 id="birthday-heading">Happy Birthday Sneha!</h1>
        <img id="cake-image" src="cake.jpg" alt="Birthday Cake">
        <p id="birthday-message">Wishing you a day filled with joy, laughter, and lots of surprises!</p>
        <div id="balloons">🎈🎈🎈</div>
        
        <!-- Music Player -->
        <audio controls autoplay>
            <source src="C:\Users\amank\Downloads\Badi Mushkil Baba Badi Mushkil.mp3" type="audio/mp3"> <!-- Replace with your music URL -->
            Your browser does not support the audio element.
        </audio>
    </div>
    <div id="confetti"></div>
    <script>
        // Generate random confetti
        const confettiContainer = document.getElementById('confetti');
        for (let i = 0; i < 10; i++) {
            const confetti = document.createElement('div');
            confetti.className = 'confetti';
            confetti.style.left = `${Math.random() * 100}%`;
            confettiContainer.appendChild(confetti);
        }
    </script>
</body>
</html>
