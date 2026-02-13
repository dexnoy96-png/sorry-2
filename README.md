
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ดีกันนะคนดี.. ❤️</title>
    <style>
        body {
            background-color: #ffeef2;
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            text-align: center;
        }

        .container {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            max-width: 400px;
            z-index: 10;
        }

        h1 { color: #ff4d6d; font-size: 2rem; }
        p { color: #555; line-height: 1.6; }

        .gif-container img {
            width: 150px;
            border-radius: 10px;
            margin-bottom: 1rem;
        }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
        }

        button {
            padding: 10px 25px;
            font-size: 1rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.3s;
        }

        #yesBtn { background-color: #ff4d6d; color: white; }
        #yesBtn:hover { transform: scale(1.1); background-color: #ff758f; }

        #noBtn { background-color: #ccc; color: white; position: relative; }

        /* หัวใจลอยๆ */
        .heart {
            position: absolute;
            color: #ff4d6d;
            font-size: 20px;
            animation: float 3s linear infinite;
            opacity: 0;
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="gif-container">
            <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHpueGZ4bm9uM2R6eGZ4bm9uM2R6eGZ4bm9uM2R6eGZ4bm9uJmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1z/3o7TKVUn7iM8FMEU24/giphy.gif" alt="cute bear">
        </div>
        <h1>เค้าขอโทษน้าาา.. ❤️</h1>
        <p>เค้ารู้ตัวแล้วว่าเค้าผิด.. หายโกรธเค้านะครับคนเก่ง <br> สัญญาว่าต่อไปเค้าไปทำงานจะบอกตหลอด 🥺</p>
        
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">ดีกันนะ</button>
            <button id="noBtn" onmouseover="moveButton()">ไม่หาย!</button>
        </div>
    </div>

    <script>
        // ฟังก์ชันทำให้ปุ่ม "ไม่หาย" หนีหายไปเรื่อยๆ (กดไม่ได้)
        function moveButton() {
            const btn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            btn.style.position = 'absolute';
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }

        function celebrate() {
            document.querySelector('.container').innerHTML = "<h1>เย้! รักที่สุดเลย ❤️</h1><p>เดี๋ยวเย็นนี้เค้ามีรางวัลให้ 4 ดอกนะ!</p><img src='https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHpueGZ4bm9uM2R6eGZ4bm9uM2R6eGZ4bm9uM2R6eGZ4bm9uJmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1z/v3p3CtSrNYNLa/giphy.gif' width='150'>";
            setInterval(createHeart, 300);
        }

        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 2 + 3 + 's';
            document.body.appendChild(heart);
            setTimeout(() => { heart.remove(); }, 5000);
        }
    </script>
</body>
</html>
