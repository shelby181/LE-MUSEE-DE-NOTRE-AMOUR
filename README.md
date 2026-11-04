<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Le Musée de Notre Amour ❤️</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{
 background:#100d0b;color:#f4e8d5;
 font-family:Georgia,serif;text-align:center;
}
header{
 padding:75px 20px;
 background:linear-gradient(#39221d,#100d0b);
}
.label{color:#d4ae72;letter-spacing:4px;font-size:11px}
h1{color:#e9c58b;font-size:36px;margin:25px 0}
header p{line-height:1.9;color:#e4d1b5}
button,.btn{
 border:0;background:#bd955d;color:#170f0b;
 padding:13px 23px;border-radius:30px;
 margin:15px 5px;cursor:pointer;
 font-family:Georgia;font-size:15px;
}
nav{
 background:#1c1511;padding:15px 8px;
 position:sticky;top:0;z-index:5;
 display:flex;justify-content:center;flex-wrap:wrap;gap:12px;
}
nav a{color:#d9b77f;text-decoration:none;font-size:13px}
section{padding:65px 18px;scroll-margin-top:65px}
h2{color:#e1bd83;margin-bottom:18px;font-size:27px}
.subtitle{color:#c7b39a;line-height:1.8;margin-bottom:25px}
.card{
 max-width:600px;margin:20px auto;padding:25px;
 background:#1d1713;border:1px solid #705337;
 border-radius:14px;line-height:1.9;
}
.gallery{
 display:grid;grid-template-columns:repeat(2,1fr);
 gap:12px;max-width:650px;margin:auto;
}
.photo{
 min-height:140px;border:1px dashed #bd955d;
 border-radius:12px;display:flex;
 align-items:center;justify-content:center;
 color:#d5b47e;padding:15px;
}
.photo img{width:100%;height:170px;object-fit:cover;border-radius:9px}
.timeline{max-width:550px;margin:auto;text-align:left}
.event{border-left:2px solid #bd955d;padding:5px 20px 25px;margin-left:15px}
.event strong{color:#e5bd7d}
.envelope{
 font-size:65px;cursor:pointer;
 margin:20px;
}
.hidden{display:none}
input{
 padding:13px;border-radius:8px;border:1px solid #bd955d;
 background:#110e0c;color:white;width:80%;max-width:250px;
 text-align:center;font-size:16px;
}
#result{color:#e7c68d;margin-top:20px;line-height:1.8}
footer{padding:35px;color:#b99b75}
@media(max-width:450px){
 h1{font-size:29px}
 .gallery{grid-template-columns:1fr 1fr}
}
</style>
</head>

<body>

<header>
<div class="label">UN LIEU UNIQUE • UNE HISTOIRE UNIQUE</div>
<h1>Le Musée de Notre Amour ❤️</h1>
<p>
Bienvenue dans un endroit où chaque souvenir a sa place,<br>
où chaque instant devient un trésor.
</p>
<a href="#galerie" class="btn">Entrer dans notre musée ❤️</a>
</header>

<nav>
<a href="#galerie">Galerie</a>
<a href="#histoire">Notre histoire</a>
<a href="#lettre">Lettre</a>
<a href="#musique">Musique</a>
<a href="#secret">Secret</a>
<a href="#surprise">Surprise</a>
</nav>

<section id="galerie">
<h2>🖼️ Galerie des souvenirs</h2>
<p class="subtitle">
Chaque photo est une pièce précieuse de notre collection.
</p>

<div class="gallery">
<div class="photo">📷 Photo 1 à ajouter</div>
<div class="photo">📷 Photo 2 à ajouter</div>
<div class="photo">📷 Photo 3 à ajouter</div>
<div class="photo">📷 Photo 4 à ajouter</div>
</div>
<p class="subtitle" style="margin-top:20px">
Nos souvenirs méritent d'être exposés.
</p>
</section>

<section id="histoire">
<h2>📅 Notre histoire</h2>
<p class="subtitle">Quelques dates d'une histoire spéciale.</p>

<div class="timeline">
<div class="event">
<strong>6 juillet 2026</strong>
<p>Le début d'un nouveau chapitre de notre histoire.</p>
</div>
<div class="event">
<strong>7 juillet 2026</strong>
<p>Un jour qui nous rapproche du commencement.</p>
</div>
<div class="event">
<strong>10 juillet 2026 ❤️</strong>
<p>Un moment spécial qui restera gravé dans nos cœurs.</p>
</div>
<div class="event">
<strong>À suivre...</strong>
<p>Notre histoire continue de s'écrire chaque jour.</p>
</div>
</div>
</section>

<section id="lettre">
<h2>💌 Une lettre pour toi</h2>
<p class="subtitle">Il y a des mots qui attendent simplement d'être découverts.</p>

<div class="card">
<div class="envelope" onclick="openLetter()">💌</div>
<p>Clique sur l'enveloppe pour découvrir ton message.</p>
<div id="letterText" class="hidden">
<p>
Si tu pouvais voir notre histoire à travers mes yeux,
tu comprendrais pourquoi chaque petit moment avec toi
a autant de valeur pour moi.
</p>
<br>
<p>Tu es une partie précieuse de mon univers. ❤️</p>
</div>
</div>
</section>

<section id="musique">
<h2>🎵 Notre espace musical</h2>
<p class="subtitle">Une mélodie pour accompagner nos souvenirs.</p>
<div class="card">
🎶
<p>Notre chanson spéciale</p>
<br>
<p>Ajoute ici le lien de votre chanson préférée.</p>
</div>
</section>

<section id="secret">
<h2>🔐 La boîte secrète</h2>
<p class="subtitle">Seule la bonne combinaison peut révéler son contenu.</p>

<div class="card">
<p>Entre le code secret :</p>
<br>
<input type="password" id="code" placeholder="Code secret">
<br>
<button onclick="checkCode()">Ouvrir la boîte ❤️</button>
<div id="secretText" class="hidden">
<p>Bravo ! Tu as découvert le secret. 🥹</p>
<p>Le plus beau trésor de ce musée, c'est notre histoire.</p>
</div>
<p id="error"></p>
</div>
</section>

<section id="surprise">
<h2>❤️ Une dernière surprise</h2>
<p class="subtitle">Le dernier trésor de ce musée t'attend.</p>

<div class="card">
<button onclick="showSurprise()">Découvrir ma surprise 💝</button>
<div id="surpriseText" class="hidden">
<h3 style="color:#e6c58c;margin:20px">
Tu es mon plus beau souvenir.
</h3>
<p>
Et si je devais construire un musée encore une fois,
je choisirais toujours notre histoire pour en être
la plus belle exposition.
</p>
<br>
<p>Avec tout mon amour. ❤️</p>
</div>
</div>
</section>

<footer>
Le Musée de Notre Amour ❤️<br><br>
Une histoire, des souvenirs, un amour.
</footer>

<script>
function openLetter(){
 document.getElementById("letterText").classList.toggle("hidden");
}

function checkCode(){
 let code=document.getElementById("code").value;
 if(code==="1007"){
  document.getElementById("secretText").classList.remove("hidden");
  document.getElementById("error").textContent="";
 }else{
  document.getElementById("error").textContent="Ce n'est pas le bon code. Réessaie ❤️";
 }
}

function showSurprise(){
 document.getElementById("surpriseText").classList.toggle("hidden");
}
</script>

</body>
</html>
