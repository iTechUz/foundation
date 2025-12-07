1. "Sehrli Chiroq" (Background Switcher)
Mavzu: Click event, variables, DOM style. Maqsad: Tugmani bosganda sahifa rangini o'zgartirish.

HTML

<button onclick="changeColor()">Rangni o'zgartir</button>

<script>
function changeColor() {
  const colors = ["red", "green", "blue", "yellow", "purple", "orange"];
  const random = colors[Math.floor(Math.random() * colors.length)];
  document.body.style.backgroundColor = random;
}
</script>
2. "Omadli Raqam" (Random Number Generator)
Mavzu: Math object, innerHTML. Maqsad: 1 dan 100 gacha tasodifiy raqam chiqarish.

HTML

<h1>Sening omadli raqaming: <span id="num">0</span></h1>
<button onclick="generate()">Omadni sinash</button>

<script>
function generate() {
  let lucky = Math.floor(Math.random() * 100) + 1;
  document.getElementById('num').innerText = lucky;
}
</script>
3. "Salom beruvchi" (Input greeting)
Mavzu: Variables, Birlashtirish (Concatenation). Maqsad: Inputga yozilgan ismni olib, unga salom berish.

HTML

<input type="text" id="userName" placeholder="Ismingizni yozing">
<button onclick="sayHello()">Salomlashish</button>
<p id="result"></p>

<script>
function sayHello() {
  let name = document.getElementById('userName').value;
  document.getElementById('result').innerText = "Salom, " + name + "! Dasturlashga xush kelibsiz!";
}
</script>
4. "Yashirin Xabar" (Toggle Visibility)
Mavzu: If/Else, Style display. Maqsad: Tugma orqali matnni ko'rsatish yoki yashirish.

HTML

<button onclick="toggle()">Xabarni ko'rish/yashirish</button>
<div id="secret" style="display:none;">🔑 Bu maxfiy xabar!</div>

<script>
function toggle() {
  let msg = document.getElementById('secret');
  if (msg.style.display === "none") {
    msg.style.display = "block";
  } else {
    msg.style.display = "none";
  }
}
</script>
5. "Oddiy Kalkulyator" (Sum of two)
Mavzu: Arifmetik, Casting (Number transformation). Maqsad: Ikkita sonni qo'shish.

HTML

<input type="number" id="n1"> + <input type="number" id="n2">
<button onclick="plus()">=</button>
<span id="sum">0</span>

<script>
function plus() {
  let num1 = Number(document.getElementById('n1').value);
  let num2 = Number(document.getElementById('n2').value);
  document.getElementById('sum').innerText = num1 + num2;
}
</script>
6. "Array Ro'yxati" (Task List basics)
Mavzu: Array methods (push), Loop yoki innerHTML. Maqsad: Ro'yxatga yangi element qo'shish.

HTML

<input type="text" id="task" placeholder="Reja yozing">
<button onclick="add()">Qo'shish</button>
<ul id="list"></ul>

<script>
function add() {
  let item = document.getElementById('task').value;
  if(item !== "") {
    let li = "<li>" + item + "</li>";
    document.getElementById('list').innerHTML += li;
    document.getElementById('task').value = ""; // Tozalash
  }
}
</script>




=======

2. Hisoblagich (Click Counter)
Har bosganda raqam oshadi — bolalar “rekord” qo‘yishni yaxshi ko‘radi.
HTML<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Bosishlar soni</title>
  <style>
    body { text-align: center; padding-top: 100px; font-family: Arial; }
    button { padding: 20px 40px; font-size: 30px; }
    h1 { font-size: 80px; margin: 50px; }
  </style>
</head>
<body>
  <h1>0</h1>
  <button onclick="bos()">BOS!</button>

  <script>
    let count = 0;
    function bos() {
      count++;
      document.querySelector('h1').innerText = count;
    }
  </script>
</body>
</html>
3. Yorqin lampochka (ON/OFF chiroq)
Rasm yo‘q — faqat CSS bilan yonadi-o‘chadi.
HTML<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Lampochka</title>
  <style>
    body { text-align: center; padding-top: 100px; background: #222; }
    .lamp { width: 150px; height: 150px; margin: 50px auto;
            border-radius: 50%; background: #333; transition: 0.5s; }
    .yon { background: yellow; box-shadow: 0 0 100px yellow; }
    button { padding: 15px 30px; font-size: 20px; }
  </style>
</head>
<body>
  <h1 style="color:white">Lampochkani yoq/o'chir</h1>
  <div class="lamp" id="lamp"></div>
  <button onclick="toggle()">Yoq/O'chir</button>

  <script>
    let yoniq = false;
    function toggle() {
      yoniq = !yoniq;
      if (yoniq) {
        document.getElementById('lamp').classList.add('yon');
      } else {
        document.getElementById('lamp').classList.remove('yon');
      }
    }
  </script>
</body>
</html>
4. Tasodifiy meme generator (bolalar uchun toza matnlar)
Har bosganda boshqa kulgili gap chiqadi.
HTML<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Kulgili gaplar</title>
  <style>
    body { text-align: center; padding-top: 100px; font-family: Comic Sans MS, Arial; }
    h1 { font-size: 50px; min-height: 120px; }
    button { padding: 15px 40px; font-size: 25px; }
  </style>
</head>
<body>
  <h1>😄</h1>
  <button onclick="yangiGap()">Yangi gap!</button>

  <script>
    const gaplar = [
      "Darsda uxlab qoldim... orzuimda dars o'tyordum 😂",
      "Internet yo'q — hayot yo'q!",
      "Bugun matematika darsi 10 soat bo'ldi shekilli",
      "Telefonim 1% qoldi... xayr dunyo!",
      "Uyga vazifa bormi? Yo'qmi? Bor ekan... 😭",
      "Men daho emasman, lekin Google bor!"
    ];

    function yangiGap() {
      const i = Math.floor(Math.random() * gaplar.length);
      document.querySelector('h1').innerText = gaplar[i];
    }
  </script>
</body>
</html>
5. Oddiy kalkulyator (faqat qo‘shish va ko‘paytirish)
Input + tugma = natija
HTML<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Mening kalkulyatorim</title>
  <style>
    body { text-align: center; padding-top: 100px; font-size: 30px; }
    input { padding: 10px; font-size: 25px; width: 100px; text-align: center; }
    button { padding: 15px 30px; font-size: 25px; margin: 10px; }
  </style>
</head>
<body>
  <h1>Kalkulyator</h1>
  <input type="number" id="a" value="5">
  <span> + </span>
  <input type="number" id="b" value="3">
  <button onclick="qosh()">=</button>
  <h2 id="natija">8</h2>

  <script>
    function qosh() {
      let a = Number(document.getElementById('a').value);
      let b = Number(document.getElementById('b').value);
      document.getElementById('natija').innerText = a + b;
    }
  </script>
</body>
</html>
6. Tasodifiy parol generatori (juda qiziqarli)
Har bosganda yangi “kuchli” parol chiqaradi.
HTML<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Parol generatori</title>
  <style>
    body { text-align: center; padding-top: 100px; font-family: Arial; }
    #parol { font-size: 40px; letter-spacing: 5px; margin: 50px; 
             background: #000; color: lime; padding: 20px; display: inline-block; }
    button { padding: 15px 40px; font-size: 25px; }
  </style>
</head>
<body>
  <h1>Kuchli parol yarat!</h1>
  <div id="parol">BOS!</div>
  <button onclick="parolYarat()">Yangi parol</button>

  <script>
    function parolYarat() {
      const belgilar = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%";
      let parol = "";
      for(let i = 0; i < 12; i++) {
        parol += belgilar.charAt(Math.floor(Math.random() * belgilar.length));
      }
      document.getElementById('parol').innerText = parol;
    }
  </script>
</body>
</html>