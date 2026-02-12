[birthday.html](https://github.com/user-attachments/files/25249550/birthday.html)
[birthday.html](https://github.com/user-attachments/files/25249550/birthday.html)
<!DOCTYPE html>
<html>
<head>
    <title>Happy Birthday 💖</title>

    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', sans-serif;
            text-align: center;
            background: linear-gradient(-45deg, #ff758c, #ff7eb3, #ff4b5c, #ff0080);
            background-size: 400% 400%;
            animation: gradientBG 8s ease infinite;
            color: white;
            overflow: hidden;
        }

        @keyframes gradientBG {
            0% {background-position: 0% 50%;}
            50% {background-position: 100% 50%;}
            100% {background-position: 0% 50%;}
        }

        .container {
            margin-top: 150px;
            animation: fadeIn 3s ease-in-out;
        }

        h1 {
            font-size: 60px;
            animation: glow 2s infinite alternate;
        }

        p {
            font-size: 26px;
            margin-top: 20px;
        }

        @keyframes glow {
            from { text-shadow: 0 0 15px white; }
            to { text-shadow: 0 0 40px yellow; }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(40px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* BEAUTIFUL BUTTON */
        .surprise-btn {
            display: inline-block;
            margin-top: 50px;
            padding: 18px 40px;
            font-size: 22px;
            font-weight: bold;
            text-decoration: none;
            color: white;
            border-radius: 50px;
            background: linear-gradient(45deg, #ff4b5c, #ff0080, #ff4b5c);
            background-size: 200% 200%;
            animation: gradientMove 3s ease infinite, pulse 1.5s infinite;
            box-shadow: 0 0 25px rgba(255, 0, 128, 0.8);
            transition: 0.3s ease;
        }

        .surprise-btn:hover {z
            transform: scale(1.2);
            box-shadow: 0 0 50px white;
        }

        @keyframes gradientMove {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 15px #ff0080; }
            50% { box-shadow: 0 0 40px #ff0080; }
            100% { box-shadow: 0 0 15px #ff0080; }
        }

        .heart {
            position: absolute;
            color: white;
            font-size: 20px;
            animation: float 6s infinite linear;
        }

        @keyframes float {
            from { transform: translateY(100vh); }
            to { transform: translateY(-10vh); }
        }

        .footer {
            position: fixed;
            bottom: 10px;
            width: 100%;
            font-size: 14px;
            opacity: 0.8;
        }
    </style>
</head>

<body>

<div class="container">
    <h1>🎉 Happy Birthday Chidiya Jii 💖</h1>
    <p>You are the most special person in my life 💕</p>

    <a href="suprise.html" class="surprise-btn">
        Click for Surprise 🎁
    </a>
</div>

<div class="footer">
    Made with ❤️ by YOURS_PRAVEEN
</div>

<!-- 🎵 Auto Music -->
<audio id="music" loop>
    <source src="song.mp3" type="audio/mpeg">
</audio>

<script>
document.body.addEventListener("click", function() {
    document.getElementById("music").play();
}, { once: true });
</script>

<script>
    window.addEventListener('load', function () {
        var audio = document.getElementById("music");
        audio.play().catch(function() {
            console.log("Autoplay blocked");
        });
    });

    function createHeart() {
        const heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = (Math.random() * 20 + 15) + "px";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 6000);
    }

    setInterval(createHeart, 400);
</script>

</body>
</html>
