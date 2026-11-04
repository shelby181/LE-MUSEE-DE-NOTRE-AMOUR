<script>
document.addEventListener("DOMContentLoaded", function () {

    // Bouton pou antre nan univers nou
    const entrer = document.querySelector("header button");

    entrer.addEventListener("click", function () {
        document.getElementById("accueil").scrollIntoView({
            behavior: "smooth"
        });
    });

    // Bouton pou ouvri lèt la
    const boutonLettre = document.querySelector(".card button");
    
    boutonLettre.addEventListener("click", function () {
        const lettre = document.getElementById("letter");

        lettre.style.display =
            lettre.style.display === "block" ? "none" : "block";
    });

    // Bouton pou verifye kòd la
    const boutons = document.querySelectorAll("button");

    boutons[2].addEventListener("click", function () {
        const code = document.getElementById("code").value.trim();

        if (code === "1007") {
            document.getElementById("secretMessage").style.display = "block";
        } else {
            alert("Ce n'est pas le bon code. Essaie encore ❤️");
        }
    });

    // Bouton surprise
    boutons[3].addEventListener("click", function () {
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
