<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Le Musée de Notre Amour ❤️</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Poppins:wght@300;400;500&display=swap');

:root {
 --gold:#d6b477;
 --cream:#f4e9d6;
 --dark:#100c0b;
 --card:#211815;
}

*{margin:0;padding:0;box-sizing:border-box}

html{scroll-behavior:smooth}

body{
 background:var(--dark);
 color:var(--cream);
 font-family:'Poppins',sans-serif;
 overflow-x:hidden;
}

body::before{
 content:"";
 position:fixed;
 inset:0;
 background:radial-gradient(circle at 50% 20%,#49302055,transparent 60%);
 pointer-events:none;
 z-index:-1;
}

header{
 min-height:100vh;
 display:flex;
 flex-direction:column;
 justify-content:center;
 align-items:center;
 padding:30px 20px;
 text-align:center;
 background:
 linear-gradient(#100c0b77,#100c0b),
 url("https://images.unsplash.com/photo-1518199266791-5375a83190b7?w=1600");
 background-size:cover;
 background-position:center;
}

.small-title{
 color:var(--gold);
 letter-spacing:5px;
 font-size:11px;
}

header h1{
 font-family:'Cormorant Garamond',serif;
 font-size:clamp(45px,10vw,85px);
 color:var(--gold);
 margin:25px 0;
 animation:appear 2s ease;
}

header p{
 max-width:500px;
 line-height:2;
 font-size:14px;
}

.gold-button{
 display:inline-block;
 padding:14px 28px;
 background:var(--gold);
 color:#160e09;
 border:0;
 border-radius:30px;
 text-decoration:none;
 cursor:pointer;
 margin-top:30px;
 font-family:inherit;
 transition:.3s;
}

.gold-button:hover{
 transform:scale(1.07);
 box-shadow:0 0 25px #d6b47766;
}

nav{
 position:sticky;
 top:0;
 z-index:20;
 background:#120d0bf2;
 border-bottom:1px solid #80633b;
 padding:15px 8px;
 display:flex;
 justify-content:center;
 flex-wrap:wrap;
 gap:17px;
}

nav a{
 color:var(--gold);
 text-decoration:none;
 font-size:11px;
}

nav a:hover{color:white}

section{
 padding:85px 20px;
 text-align:center;
 scroll-margin-top:65px;
}

.section-label{
 color:var(--gold);
 letter-spacing:4px;
 font-size:10px;
}

h2{
 font-family:'Cormorant Garamond',serif;
 color:var(--gold);
 font-size:42px;
 margin:15px 0;
}

.description{
 max-width:550px;
 margin:0 auto 35px;
 line-height:1.9;
 color:#c9bba7;
 font-size:13px;
}

.line{
 width:65px;
 height:1px;
 background:var(--gold);
 margin:20px auto 30px;
}

/* GALERIE */

.gallery{
 max-width:1000px;
 margin:auto;
 display:grid;
 grid-template-columns:repeat(3,1fr);
 gap:15px;
}

.gallery-item{
 height:230px;
 overflow:hidden;
 border:1px solid #725735;
 cursor:pointer;
 position:relative;
 border-radius:5px;
}

.gallery-item img{
 width:100%;
 height:100%;
 object-fit:cover;
 transition:.6s;
}

.gallery-item:hover img{
 transform:scale(1.12);
}

.gallery-item span{
 position:absolute;
 bottom:0;
 left:0;
 width:100%;
 padding:15px 5px;
 background:linear-gradient(transparent,#000c);
 color:white;
 font-family:'Cormorant Garamond',serif;
 font-size:19px;
}

/* AGRANDIR FOTO */

#lightbox{
 display:none;
 position:fixed;
 inset:0;
 z-index:100;
 background:#000e;
 justify-content:center;
 align-items:center;
 padding:20px;
}

#lightbox img{
 max-width:95%;
 max-height:85vh;
 border:2px solid var(--gold);
}

#lightbox span{
 position:absolute;
 top:20px;
 right:25px;
 font-size:35px;
 cursor:pointer;
 color:white;
}

/* HISTOIRE */

.timeline{
 max-width:650px;
 margin:auto;
 text-align:left;
}

.timeline-item{
 position:relative;
 border-left:1px solid var(--gold);
 padding:5px 25px 35px;
 margin-left:15px;
}

.timeline-item::before{
 content:"";
 position:absolute;
 left:-6px;
 top:8px;
 width:11px;
 height:11px;
 background:var(--gold);
 border-radius:50%;
}

.timeline-item strong{
 color:var(--gold);
 font-family:'Cormorant Garamond',serif;
 font-size:23px;
}

.timeline-item p{
 color:#c9bba7;
 font-size:13px;
 line-height:1.9;
 margin-top:8px;
}

/* CARDS */

.card{
 max-width:600px;
 margin:25px auto;
 background:linear-gradient(145deg,#2b2019,#17110f);
 border:1px solid #80613d;
 padding:35px 22px;
 border-radius:8px;
 box-shadow:0 10px 40px #0005;
}

.envelope{
 font-size:75px;
 cursor:pointer;
 display:inline-block;
 transition:.4s;
}

.envelope:hover{transform:scale(1.15) rotate(-8deg)}

.letter-content{
 display:none;
 margin-top:25px;
 padding:25px;
 background:#f1dfbd;
 color:#3a2519;
 line-height:2;
 font-family:'Cormorant Garamond',serif;
 font-size:20px;
 text-align:left;
 animation:appear 1s;
}

/* MUSIQUE */

.music-disc{
 width:115px;
 height:115px;
 margin:15px auto 25px;
 border-radius:50%;
 border:5px solid var(--gold);
 display:flex;
 align-items:center;
 justify-content:center;
 font-size:45px;
 background:radial-gradient(circle,#6a4830,#17100d);
}

.playing{
 animation:rotate 5s linear infinite;
}

audio{
 width:100%;
 max-width:350px;
 margin-top:20px;
}

/* SECRET */

input{
 background:#100c0b;
 border:1px solid var(--gold);
 padding:14px;
 width:85%;
 max-width:270px;
 color:white;
 border-radius:5px;
 text-align:center;
 outline:none;
 font-size:16px;
}

#secret-result{
 display:none;
 margin-top:25px;
 color:var(--gold);
 line-height:2;
}

/* SURPRISE */

#surprise-content{
 display:none;
 padding:25px 10px;
 animation:appear 1s;
}

#surprise-content h3{
 font-family:'Cormorant Garamond',serif;
 color:var(--gold);
 font-size:35px;
 margin:20px 0;
 line-height:1.4;
}

.heart{
 position:fixed;
 bottom:-30px;
 font-size:20px;
 pointer-events:none;
 animation:float 5s linear forwards;
 z-index:200;
}

footer{
 border-top:1px solid #705337;
 padding:35px 15px;
 text-align:center;
 color:#c4a779;
 font-family:'Cormorant Garamond',serif;
 font-size:19px;
}

@keyframes appear{
 from{opacity:0;transform:translateY(20px)}
 to{opacity:1;transform:translateY(0)}
}

@keyframes rotate{
 to{transform:rotate(360deg)}
}

@keyframes float{
 to{transform:translateY(-110vh) rotate(360deg);opacity:0}
}

@media(max-width:650px){
 .gallery{grid-template-columns:repeat(2,1fr)}
 .gallery-item{height:170px}
 h2{font-size:35px}
 nav{gap:12px}
 nav a{font-size:10px}
}

@media(max-width:380px){
 .gallery{grid-template-columns:1fr}
 .gallery-item{height:230px}
}
</style>
</head>

<body>

<header>
 <div class="small-title">COLLECTION PRIVÉE • ÉDITION SPÉCIALE</div>

 <h1>Le Musée<br>de Notre Amour</h1>

 <p>
 Bienvenue dans un univers où les souvenirs deviennent des œuvres d'art,
 où chaque instant possède une valeur particulière.
 </p>

 <a href="#galerie" class="gold-button">
 Découvrir notre musée ❤️
 </a>
</header>

<nav>
 <a href="#galerie">GALERIE</a>
 <a href="#histoire">HISTOIRE</a>
 <a href="#lettre">LETTRE</a>
 <a href="#musique">MUSIQUE</a>
 <a href="#secret">SECRET</a>
 <a href="#surprise">SURPRISE</a>
</nav>

<!-- GALERIE -->

<section id="galerie">
 <div class="section-label">COLLECTION N° 01</div>
 <h2>La Galerie des Souvenirs</h2>
 <div class="line"></div>

 <p class="description">
 Chaque image est une petite œuvre.
 Chaque instant mérite une place dans notre collection.
 Clique sur les photos pour les admirer.
 </p>

 <div class="gallery">

  <div class="gallery-item" onclick="enlarge(this)">
   <img src="https://images.unsplash.com/photo-1518199266791-5375a83190b7?w=700" alt="Fleurs">
   <span>Un joli commencement</span>
  </div>

  <div class="gallery-item" onclick="enlarge(this)">
   <img src="https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?w=700" alt="Couple">
   <span>La tendresse</span>
  </div>

  <div class="gallery-item" onclick="enlarge(this)">
   <img src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?w=700" alt="Coucher de soleil">
   <span>Nos beaux horizons</span>
  </div>

  <div class="gallery-item" onclick="enlarge(this)">
   <img src="https://images.unsplash.com/photo-1490750967868-88aa4486c946?w=700" alt="Fleurs">
   <span>La beauté des détails</span>
  </div>

  <div class="gallery-item" onclick="enlarge(this)">
   <img src="https://images.unsplash.com/photo-1518621736915-f3b1c41bfd00?w=700" alt="Nature">
   <span>Les instants précieux</span>
  </div>

  <div class="gallery-item" onclick="enlarge(this)">
   <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?w=700" alt="Paysage">
   <span>Un monde à deux</span>
  </div>

 </div>

 <p class="description" style="margin-top:30px">
 Ces images sont provisoires. Notre véritable collection attend vos propres photos. ❤️
 </p>
</section>

<div id="lightbox" onclick="this.style.display='none'">
 <span>×</span>
 <img id="large-image" src="" alt="Photo agrandie">
</div>

<!-- HISTOIRE -->

<section id="histoire">
 <div class="section-label">COLLECTION N° 02</div>
 <h2>Notre Histoire</h2>
 <div class="line"></div>

 <p class="description">
 Certaines dates ne sont pas de simples chiffres.
 Elles représentent des souvenirs que le temps ne peut effacer.
 </p>

 <div class="timeline">

  <div class="timeline-item">
   <strong>06 Juillet 2026</strong>
   <p>Un départ, un changement de décor et le début d'un nouveau chapitre.</p>
  </div>

  <div class="timeline-item">
   <strong>07 Juillet 2026</strong>
   <p>Une arrivée qui allait bientôt prendre une signification particulière.</p>
  </div>

  <div class="timeline-item">
   <strong>10 Juillet 2026 ❤️</strong>
   <p>Une rencontre, des regards, des paroles et le commencement d'une histoire spéciale.</p>
  </div>

  <div class="timeline-item">
   <strong>Notre présent</strong>
   <p>Deux personnes, des souvenirs et une histoire qui continue de s'écrire.</p>
  </div>

  <div class="timeline-item">
   <strong>Notre avenir...</strong>
   <p>Une page encore blanche, prête à accueillir nos prochains souvenirs.</p>
  </div>

 </div>
</section>

<!-- LETTRE -->

<section id="lettre">
 <div class="section-label">COLLECTION N° 03</div>
 <h2>Une Lettre du Cœur</h2>
 <div class="line"></div>

 <p class="description">
 Une enveloppe, quelques mots et beaucoup de sentiments.
 </p>

 <div class="card">
  <div class="envelope" onclick="openLetter()">💌</div>

  <p style="color:var(--gold)">Une lettre t'attend...</p>

  <button class="gold-button" onclick="openLetter()">
   Ouvrir ma lettre
  </button>

  <div class="letter-content" id="letter">
   <p>À toi, mon cœur... ❤️</p>
   <br>
   <p>
    Si j'ai créé cet endroit, c'est parce que certaines personnes
    méritent plus qu'un simple message.
   </p>
   <br>
   <p>
    Je voulais construire un petit univers où chaque souvenir,
    chaque sourire et chaque moment partagé auraient leur place.
   </p>
   <br>
   <p>
    Je ne sais pas tout ce que l'avenir nous réserve,
    mais je sais que notre histoire mérite d'être vécue,
    protégée et écrite avec sincérité.
   </p>
   <br>
   <p>Avec tout mon amour. ❤️</p>
  </div>
 </div>
</section>

<!-- MUSIQUE -->

<section id="musique">
 <div class="section-label">COLLECTION N° 04</div>
 <h2>Notre Univers Musical</h2>
 <div class="line"></div>

 <p class="description">
 Certaines mélodies racontent ce que les mots n'arrivent pas toujours à exprimer.
 </p>

 <div class="card">
  <div class="music-disc" id="disc">🎵</div>
  <h3 style="color:var(--gold)">Une mélodie pour nous</h3>
  <p style="font-size:12px;color:#c9bba7;margin-top:10px">
   Musique de démonstration — à remplacer par votre chanson.
  </p>

  <audio id="audio" controls
   src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
  </audio>
 </div>
</section>

<!-- SECRET -->

<section id="secret">
 <div class="section-label">COLLECTION N° 05</div>
 <h2>La Boîte Secrète</h2>
 <div class="line"></div>

 <p class="description">
 Tous les visiteurs ne peuvent pas accéder à ce trésor.
 Seule la bonne combinaison ouvrira cette boîte.
 </p>

 <div class="card">
  <div style="font-size:55px">🔐</div>

  <p style="margin:15px 0;color:var(--gold)">
   Entre le code secret
  </p>

  <input id="secret-code" type="password" placeholder="Ton code secret">

  <br>

  <button class="gold-button" onclick="unlock()">
   Déverrouiller ❤️
  </button>

  <div id="secret-result">
