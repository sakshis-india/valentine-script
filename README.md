
<html>
<head>
    <title>Our Forever Begins ✨</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>

body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg,#8b0000,#b30000,#ff1a1a);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Poppins', sans-serif;
    overflow: hidden;
}

/* Overlay Card */
.overlay {
    background: rgba(0,0,0,0.55);
    backdrop-filter: blur(6px);
    padding: 60px;
    border-radius: 25px;
    text-align: center;
    color: #fff;
    box-shadow: 0 0 60px rgba(255,0,0,0.5);
    animation: fadeIn 2s ease-in-out;
    z-index: 2;
}

h1 {
    font-family: 'Great Vibes', cursive;
    font-size: 48px;
    color: gold;
}

p {
    font-size: 20px;
}

button {
    padding: 14px 35px;
    margin: 12px;
    border-radius: 40px;
    border: none;
    font-size: 18px;
    cursor: pointer;
    transition: 0.4s;
}

#yes {
    background: linear-gradient(45deg, gold, orange);
}

#yes:hover {
    transform: scale(1.15);
    box-shadow: 0 0 25px gold;
}

#no {
    background: Red;
}

/* Falling Animation */
.falling {
    position: absolute;
    font-size: 24px;
    animation: fall linear infinite;
    z-index: 1;
}

@keyframes fall {
    0% {
        transform: translateY(-10vh);
        opacity: 1;
    }
    100% {
        transform: translateY(110vh);
        opacity: 0;
    }
}

@keyframes fadeIn {
    from {opacity:0; transform:scale(0.9);}
    to {opacity:1; transform:scale(1);}
}

</style>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;500&display=swap" rel="stylesheet">

    <style>
        body {
            margin: 0;
            height: 100vh;
            background: url('IMG_1813.JPG') no-repeat center center/cover;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Poppins', sans-serif;
            overflow: hidden;
        }

        .overlay {
            background: rgba(0,0,0,0.55);
            backdrop-filter: blur(6px);
            padding: 60px;
            border-radius: 25px;
            text-align: center;
            color: #fff;
            box-shadow: 0 0 60px rgba(255,215,0,0.4);
            animation: fadeIn 2s ease-in-out;
        }

        h1 {
            font-family: 'Great Vibes', cursive;
            font-size: 48px;
            margin-bottom: 20px;
            color: #ffd700;
        }

        p {
            font-size: 20px;
            margin-bottom: 30px;
        }

        button {
            padding: 14px 35px;
            margin: 12px;
            border-radius: 40px;
            border: none;
            font-size: 18px;
            cursor: pointer;
            transition: 0.4s;
        }

        #yes {
            background: linear-gradient(45deg, #ffd700, #ffb347);
            color: black;
        }

        #yes:hover {
            transform: scale(1.15);
            box-shadow: 0 0 25px gold;
        }

        #no {
            background: white;
        }

        .sparkle {
            position: absolute;
            font-size: 22px;
            animation: float 6s linear infinite;
        }

        @keyframes float {
            0% { transform: translateY(100vh); opacity: 1; }
            100% { transform: translateY(-10vh); opacity: 0; }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }
    </style>
</head>

<body>

<div class="overlay">
    <h1>My Forever 💍</h1>
    <p>Will you continue this beautiful fairy-tale with me… forever? ✨</p>
    <button id="yes" onclick="sayYes()">Yes, My Bubu 👑</button>
    <button id="no" onmouseover="moveNo()">No 😅</button>
    <div id="result"></div>
</div>

<!-- Optional Romantic Music -->
<audio autoplay loop>
    <source src="romantic.mp3" type="audio/mpeg">
</audio>

<script>
function sayYes() {
    document.getElementById("result").innerHTML =
        "<h2 style='margin-top:20px; color:gold;'>And they lived happily ever after ✨💖</h2>";
    launchSparkles();
}

function moveNo() {
    const noBtn = document.getElementById("no");
    const x = Math.random() * 200 - 100;
    const y = Math.random() * 200 - 100;
    noBtn.style.position = "relative";
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}

function launchSparkles() {
    for (let i = 0; i < 25; i++) {
        const sparkle = document.createElement("div");
        sparkle.innerHTML = "✨";
        sparkle.classList.add("sparkle");
        sparkle.style.left = Math.random() * 100 + "vw";
        sparkle.style.animationDuration = Math.random() * 3 + 3 + "s";
        document.body.appendChild(sparkle);
        setTimeout(() => sparkle.remove(), 6000);
    }
}
</script>

</body>
</html>
