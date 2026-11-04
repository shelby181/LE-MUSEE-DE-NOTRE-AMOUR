<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Le Musée de Notre Amour ❤️</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    background: #160d18;
    color: #f8e9df;
    font-family: Georgia, serif;
    text-align: center;
}

header {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 25px;
    background: linear-gradient(#160d18dd, #160d18ee),
    url("https://images.unsplash.com/photo-1518199266791-5375a83190b7?w=1200");
    background-size: cover;
    background-position: center;
}

header h1 {
    color: #ffb6c9;
    font-size: 36px;
    margin-bottom: 20px;
}

header p {
    font-size: 17px;
    line-height: 1.8;
    max-width: 500px;
}

button {
    background: #ff6b91;
    color: white;
    border: none;
    padding: 13px 25px;
    border-radius: 30px;
    font-size: 15px;
    margin: 15px;
    cursor: pointer;
}

button:hover {
    background: #ff477e;
}

section {
    padding: 65px 20px;
}

h2 {
    color: #ffb6c9;
    margin-bottom: 25px;
    font-size: 27px;
}

.intro {
    line-height: 1.9;
    max-width: 650px;
    margin: auto;
    color: #ead6df;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
    max-width: 750px;
    margin: auto;
}

.gallery div {
    text-align: center;
}

.gallery img {
    width: 100%;
    height: 190px;
    object-fit: cover;
    border-radius: 12px;
    border: 1px solid #b68a69;
    transition: transform 0.3s ease;
}

.gallery img:hover {
    transform: scale(1.04);
}

.gallery div p {
    color: #ffb6c9;
    font-size: 14px;
    margin-top: 10px;
    margin-bottom: 20px;
    line-height: 1.5;
}

.timeline {
    max-width: 600px;
    margin: auto;
    border-left: 2px solid #ff6b91;
    text-align: left;
    padding-left: 25px;
}

.event {
    margin-bottom: 35px;
    position: relative;
}

.event::before {
    content: "❤";
    position: absolute;
    left: -36px;
    color: #ff6b91;
}

.event h3 {
    color: #ffb6c9;
    margin-bottom: 8px;
}

.event p {
    line-height: 1.7;
}

.card {
    max-width: 600px;
    margin: auto;
    background: #29182b;
    border: 1px solid #a77a68;
    padding: 30px 20px;
    border-radius: 15px;
    line-height: 1.9;
}

#letter {
    display: none;
    margin-top: 20px;
    color: #ffe4ec;
    text-align: left;
    white-space: pre-line;
}

.music-box {
    max-width: 550px;
    margin: auto;
    background: #29182b;
    padding: 25px;
    border-radius: 15px;
}

iframe {
    width: 100%;
    height: 200px;
    border: none;
    border-radius: 10px;
    margin-top: 15px;
}

input {
    padding: 13px;
    width: 80%;
    max-width: 250px;
    border-radius: 25px;
    border: 1px solid #ff6b91;
    background: #160d18;
    color: white;
    text-align: center;
    font-size: 16px;
}

#secretMessage, #finalMessage {
    display: none;
    margin-top: 20px;
    line-height: 1.9;
    color: #ffb6c9;
}

footer {
    padding: 35px 15px;
    background: #100810;
    color: #d8a8b8;
    line-height: 2;
}

.heart {
    position: fixed;
    bottom: -20px;
    color: #ff6b91;
    animation: float 5s linear forwards;
    pointer-events: none;
}

@keyframes float {
    to {
        transform: translateY(-110vh) rotate(360deg);
        opacity: 0;
    }
}

@media(max-width: 400px) {
    header h1 {
        font-size: 29px;
    }

    .gallery img {
        height: 145px;
    }
}
</style>
</head>

<body>

<header>
    <h1>Le Musée de Notre Amour ❤️</h1>

    <p>
        Chaque histoire possède ses souvenirs.
        La nôtre mérite un endroit où chaque moment
        pourra continuer à vivre.
    </p>

    <button id="entrer">
        Entrer dans notre univers ❤️
    </button>
</header>

<section id="accueil">
    <h2>Bienvenue dans notre univers</h2>

    <p class="intro">
        Ce petit musée n'est pas un endroit ordinaire.
        C'est un espace rempli de souvenirs, de sentiments,
        de moments précieux et de petites choses qui
        rendent notre histoire unique.
        <br><br>
        Prends ton temps... chaque partie a quelque chose
        à te raconter. ❤️
    </p>
</section>

<section>
    <h2>📸 Notre histoire en images</h2>

    <p class="intro">
        De personnes, un amour, un avenir à construire.
        Des moments de tendresse, un mariage rempli d'émotions
        et une vie heureuse à deux. ❤️
    </p>

    <br>

    <div class="gallery">

        <div>
            <img src="https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?w=600" alt="Couple amoureux">
            <p>Deux cœurs, un seul amour ❤️</p>
        </div>

        <div>
            <img src="https://images.unsplash.com/photo-1522673607200-164d1b6ce486?w=600" alt="Couple romantique">
            <p>La tendresse au quotidien 🥰</p>
        </div>

        <div>
            <img src="https://images.unsplash.com/photo-1519741497674-611481863552?w=600" alt="Mariage romantique">
            <p>Le jour où deux vies s'unissent 💍</p>
        </div>

        <div>
            <img src="https://images.unsplash.com/photo-1511285560929-80b456fea0bc?w=600" alt="Cérémonie de mariage">
            <p>Un engagement pour la vie ❤️</p>
        </div>

        <div>
            <img src="https://images.unsplash.com/photo-1511895426328-dc8714191300?w=600" alt="Couple heureux">
            <p>Construire une vie heureuse ensemble 🌹</p>
        </div>

        <div>
            <img src="https://images.unsplash.com/photo-1529333166437-7750a6dd5a70?w=600" alt="Bonheur à deux">
            <p>Vieillir ensemble, toujours amoureux 💕</p>
        </div>

    </div>
</section>

<section>
    <h2>🕰️ Notre histoire</h2>

    <div class="timeline">

        <div class="event">
            <h3>6 juillet 2026</h3>
            <p>Un départ qui allait marquer le début d'une belle histoire.</p>
        </div>

        <div class="event">
            <h3>7 juillet 2026</h3>
            <p>Une nouvelle étape, sans savoir encore tout ce que l'avenir réservait.</p>
        </div>

        <div class="event">
            <h3>10 juillet 2026 ❤️</h3>
            <p>Un moment spécial, le début de souvenirs que nous n'oublierons pas.</p>
        </div>

        <div class="event">
            <h3>La suite...</h3>
            <p>Notre histoire continue de s'écrire, un jour après l'autre.</p>
        </div>

    </div>
</section>

<section>
    <h2>💌 Une lettre pour toi</h2>

    <div class="card">
        <p>Il y a quelque chose que j'aimerais te rappeler...</p>

        <button id="ouvrirLettre">Ouvrir ma lettre ❤️</button>

        <div id="letter">
Ma douce,

Je ne sais pas toujours trouver les mots parfaits,
mais je sais une chose : ta présence compte énormément
pour moi.

Je ne veux pas seulement collectionner de beaux souvenirs
avec toi. Je veux aussi construire quelque chose de vrai,
avec de la patience, du respect et beaucoup d'amour.

Merci d'être une partie de mon histoire.

Avec tout mon amour. ❤️
        </div>
    </div>
</section>

<section>
    <h2>🎶 Notre petite mélodie</h2>

    <div class="music-box">
        <p>Parce que certaines mélodies nous font penser
        à des personnes particulières. ❤️</p>

        <iframe
            src="https://www.youtube.com/embed/W1tzURKYFNs"
            title="Notre chanson"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen>
        </iframe>

        <br>

        <a href="https://youtu.be/W1tzURKYFNs"
           target="_blank"
           style="color:#ffb6c9;">
           Si la vidéo ne fonctionne pas, écoute-la ici ❤️
        </a>
    </div>
</section>

<section>
    <h2>🔐 Un petit secret</h2>

    <p class="intro">
        Pour découvrir le prochain message,
        il faut trouver notre date spéciale.
    </p>

    <br>

    <input type="password" id="code" placeholder="Entre le code secret">

    <br>

    <button id="verifierCode">Déverrouiller ❤️</button>

    <div id="secretMessage">
        Bravo mon amour ! 🥰

        Tu viens de découvrir un petit secret.
        Mais le plus beau reste encore à venir...
    </div>
</section>

<section>
    <h2>🎁 La dernière surprise</h2>

    <div class="card">
        <p>
            Tu es arrivée jusqu'ici...
            Alors, il reste une dernière chose à découvrir.
        </p>

        <button id="boutonSurprise">Découvrir la surprise ❤️</button>

        <div id="finalMessage">
            Si je pouvais recommencer cette histoire,
            je voudrais encore découvrir ces petits moments
            qui nous ont rapprochés.

            Je ne promets pas une histoire parfaite,
            mais je veux continuer à écrire la nôtre
            avec toi.

            Tu occupes une place spéciale dans mon cœur. ❤️
        </div>
    </div>
</section>

<footer>
    <p>Le Musée de Notre Amour ❤️</p>
    <p>Une histoire, deux cœurs, des souvenirs infinis.</p>
    <p>Créé avec amour. ❤️</p>
</footer>

<script>
document.addEventListener("DOMContentLoaded", function () {

    document.getElementById("entrer").addEventListener("click", function () {
        document.getElementById("accueil").scrollIntoView({
            behavior: "smooth"
        });
    });

    document.getElementById("ouvrirLettre").addEventListener("click", function () {
        const lettre = document.getElementById("letter");

        lettre.style.display =
            lettre.style.display === "block" ? "none" : "block";
    });

    document.getElementById("verifierCode").addEventListener("click", function () {
        const code = document.getElementById("code").value.trim();

        if (code === "1007") {
            document.getElementById("secretMessage").style.display = "block";
        } else {
            alert("Ce n'est pas le bon code. Essaie encore ❤️");
        }
    });

    document.getElementById("boutonSurprise").addEventListener("click", function () {
        document.getElementById("finalMessage").style.display = "block";

        for (let i = 0; i < 25; i++) {
            const coeur = document.createElement("div");

            coeur.innerHTML = "❤";
            coeur.className = "heart";
            coeur.style.left = Math.random() * 100 + "vw";
            coeur.style.fontSize = (15 + Math.random() * 25) + "px";

            document.body.appendChild(coeur);

            setTimeout(function () {
                coeur.remove();
            }, 5000);
        }
    });

});
</script>

</body>
</html>
