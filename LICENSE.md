<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Untuk Kamu 🤍</title>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Poppins', sans-serif;
    }

    body {
        height: 100vh;
        background: linear-gradient(135deg, #ff9a9e, #fad0c4);
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
    }

    .card {
        background: white;
        padding: 50px 40px;
        border-radius: 20px;
        width: 90%;
        max-width: 500px;
        text-align: center;
        box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        animation: fadeIn 2s ease;
        position: relative;
        z-index: 2;
    }

    h1 {
        color: #e91e63;
        margin-bottom: 20px;
    }

    p {
        color: #555;
        line-height: 1.7;
        margin-bottom: 15px;
    }

    button {
        margin-top: 20px;
        padding: 12px 25px;
        border: none;
        border-radius: 30px;
        background: #e91e63;
        color: white;
        font-size: 15px;
        cursor: pointer;
        transition: 0.3s;
    }

    button:hover {
        background: #c2185b;
        transform: scale(1.05);
    }

    @keyframes fadeIn {
        from {opacity: 0; transform: translateY(20px);}
        to {opacity: 1; transform: translateY(0);}
    }

    /* Hati melayang */
    .heart {
        position: absolute;
        bottom: -20px;
        font-size: 20px;
        color: #fff;
        animation: floatUp 6s linear infinite;
        opacity: 0.7;
    }

    @keyframes floatUp {
        0% {transform: translateY(0) scale(1);}
        100% {transform: translateY(-100vh) scale(1.5);}
    }

</style>
</head>

<body>

<div class="card">
    <h1>Maaf 🤍</h1>
    <p>
        minta maaf dengan tulus atas kita pe sikap yang beking ngana marah marah deng rasa nda nyaman.
        kita sadar tape kesalahan sekali lagi kita minta maaf.
    </p>
    <p>
        Maaf ya karena tanpa sadar kita beking hal bagitu.
    </p>
    <button onclick="showMessage()">Klik Jika Kamu Mau Maafkan 🤍</button>
</div>

<script>
    function showMessage() {
        alert("Terima kasih sudah mau membaca dan memberi kesempatan 🤍");
    }

    // Membuat hati melayang otomatis
    function createHeart() {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "🤍";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = Math.random() * 20 + 15 + "px";
        heart.style.animationDuration = Math.random() * 3 + 3 + "s";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 6000);
    }

    setInterval(createHeart, 800);
</script>

</body>
</html>

