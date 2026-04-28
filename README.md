HTML
<!DOCTYPE html>
<html lang="kk">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Атом әлемі</title>

<style>
body {
    margin: 0;
    font-family: Arial;
    background: radial-gradient(circle, #1a1a2e, #16213e);
    color: white;
    text-align: center;
}

/* ЯДРО */
.atom {
    position: relative;
    width: 200px;
    height: 200px;
    margin: 40px auto;
}

.nucleus {
    width: 40px;
    height: 40px;
    background: red;
    border-radius: 50%;
    position: absolute;
    top: 80px;
    left: 80px;
}

/* ЭЛЕКТРОН */
.electron {
    width: 15px;
    height: 15px;
    background: cyan;
    border-radius: 50%;
    position: absolute;
    top: 0;
    left: 90px;
    animation: rotate 3s linear infinite;
    transform-origin: 10px 100px;
}

@keyframes rotate {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
}

.card {
    background: white;
    color: black;
    margin: 20px;
    padding: 15px;
    border-radius: 12px;
}

/* Батырма */
button {
    padding: 10px;
    margin: 5px;
    border: none;
    border-radius: 8px;
    background: #00adb5;
    color: white;
}

/* Телефонға */
@media (max-width:600px){
    .atom {
        transform: scale(0.7);
    }
}
</style>
</head>

<body>

<h1>⚛ Атом әлемі</h1>

<div class="atom">
    <div class="nucleus"></div>
    <div class="electron"></div>
</div>

<div class="card">
<h2>Атом деген не?</h2>
<p>Атом — заттың ең кіші бөлшегі. Ол ядро және электрондардан тұрады.</p>
</div>

<div class="card">
<h2>🎮 Ойын: Батырманы бас!</h2>
<button onclick="scoreGame()">Бас!</button>
<p id="gameScore">Ұпай: 0</p>
</div>

<div class="card">
<h2>🧪 Тест (10 сұрақ)</h2>

<p>1. Протон заряды?</p>
<button onclick="ans(1,'a')">Оң</button>
<button onclick="ans(1,'b')">Теріс</button>

<p>2. Электрон қайда?</p>
<button onclick="ans(2,'a')">Ядро</button>
<button onclick="ans(2,'b')">Айнала</button>

<p>3. Нейтрон?</p>
<button onclick="ans(3,'a')">Заряд жоқ</button>
<button onclick="ans(3,'b')">Оң</button>

<p>4. Атом не?</p>
<button onclick="ans(4,'a')">Кіші бөлшек</button>
<button onclick="ans(4,'b')">Планета</button>

<p>5. Электрон заряды?</p>
<button onclick="ans(5,'a')">Теріс</button>
<button onclick="ans(5,'b')">Оң</button>

<p>6. Ядро құрамында?</p>
<button onclick="ans(6,'a')">Протон, нейтрон</button>
<button onclick="ans(6,'b')">Электрон</button>

<p>7. Нейтрон қайда?</p>
<button onclick="ans(7,'a')">Ядро</button>
<button onclick="ans(7,'b')">Сыртта</button>

<p>8. Протон қайда?</p>
<button onclick="ans(8,'a')">Ядро</button>
<button onclick="ans(8,'b')">Айнала</button>

<p>9. Электрон не істейді?</p>
<button onclick="ans(9,'a')">Айналады</button>
<button onclick="ans(9,'b')">Тұрады</button>

<p>10. Атом бөліктері?</p>
<button onclick="ans(10,'a')">3</button>
<button onclick="ans(10,'b')">10</button>

<p id="res"></p>

</div>

<script>
let score = 0;
let game = 0;

function scoreGame(){
    game++;
    document.getElementById("gameScore").innerHTML = "Ұпай: " + game;
}

function ans(q,a){
    if(q==1 && a=='a') score++;
    if(q==2 && a=='b') score++;
    if(q==3 && a=='a') score++;
    if(q==4 && a=='a') score++;
    if(q==5 && a=='a') score++;
    if(q==6 && a=='a') score++;
    if(q==7 && a=='a') score++;
    if(q==8 && a=='a') score++;
    if(q==9 && a=='a') score++;
    if(q==10 && a=='a') score++;

    document.getElementById("res").innerHTML =
        "Сенің нәтижең: " + score + " / 10";
}
</script>

</body>
</html>
