<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>💗</title>

<style>
body {
    margin: 0;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #ffd6e7, #fff0f6);
    text-align: center;
}

.kutu {
    background: white;
    width: 85%;
    max-width: 430px;
    padding: 30px;
    border-radius: 25px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
}

h1 {
    color: #ff4f91;
}

p {
    font-size: 18px;
    color: #555;
    line-height: 1.5;
}

input {
    width: 80%;
    padding: 12px;
    border: 2px solid #ffb5cf;
    border-radius: 12px;
    font-size: 16px;
}

button {
    border: none;
    padding: 12px 22px;
    margin-top: 12px;
    border-radius: 15px;
    font-size: 16px;
    background: #ff6fa5;
    color: white;
    cursor: pointer;
}
</style>
</head>

<body>

<div class="kutu">

    <h1 id="baslik">Hoşgeldinnnnnnn 💗</h1>

    <p id="soru">Nasılsın? 👀</p>

    <input id="cevap" type="text" placeholder="Cevabını yaz...">

    <br>

    <button id="buton" onclick="ilkCevap()">
        Gönder 💗
    </button>

    <p id="mesaj"></p>

</div>


<script>

function ilkCevap() {

    let cevap = document.getElementById("cevap").value
        .toLowerCase()
        .trim();

    if (cevap == "") {
        document.getElementById("mesaj").innerHTML =
            "Cevap bekliyorum 😂";
        return;
    }

    if (
        cevap.includes("iyi") ||
        cevap.includes("güzel") ||
        cevap.includes("guzel") ||
        cevap.includes("harika") ||
        cevap.includes("mutlu") ||
        cevap.includes("süper") ||
        cevap.includes("super")
    ) {

        document.getElementById("baslik").innerHTML =
            "Hoşgeldin 💗";

        document.getElementById("soru").innerHTML =
            "İyi olmana sevindimmm 🥹💗";

    }

    else if (
        cevap.includes("kötü") ||
        cevap.includes("kotu") ||
        cevap.includes("üzgün") ||
        cevap.includes("uzgun") ||
        cevap.includes("berbat") ||
        cevap.includes("moralim bozuk")
    ) {

        document.getElementById("baslik").innerHTML =
            "Olsun 🥺";

        document.getElementById("soru").innerHTML =
            "Canını sıkma, umarım birazdan daha iyi hissedersin. 💗";

    }

    else {

        document.getElementById("baslik").innerHTML =
            "Anladım 👀";

        document.getElementById("soru").innerHTML =
            "Umarım günün güzel geçer 💗";
    }

    document.getElementById("cevap").value = "";

    setTimeout(function() {

        document.getElementById("soru").innerHTML =
            "Yanında kim var? 👀";

        document.getElementById("buton").innerHTML =
            "Gönder 💗";

        document.getElementById("buton").onclick =
            yanindaKimVar;

    }, 1200);
}


function yanindaKimVar() {

    let cevap = document.getElementById("cevap").value
        .toLowerCase()
        .trim();

    if (cevap == "") {
        document.getElementById("mesaj").innerHTML =
            "Cevap yazsana 😂";
        return;
    }

    /*
    YANINDA KİMSE YOKSA DEVAM EDER
    "yok" da yalnız anlamına gelir.
    */

    if (
        cevap == "yok" ||
        cevap.includes("yalnız") ||
        cevap.includes("yalniz") ||
        cevap.includes("kimse yok") ||
        cevap == "kimse" ||
        cevap.includes("tekim") ||
        cevap.includes("tek başıma") ||
        cevap.includes("tek basima")
    ) {

        document.getElementById("baslik").innerHTML =
            "Tamamdır 👀";

        document.getElementById("soru").innerHTML =
            "O zaman sana bir şey söyleyeceğim...";

        document.getElementById("cevap").value = "";

        document.getElementById("buton").innerHTML =
            "Devam 💗";

        document.getElementById("buton").onclick =
            devamEt;

    }

    else {

        document.getElementById("baslik").innerHTML =
            "Tamamdır 😌";

        document.getElementById("soru").innerHTML =
            "O zaman bunu başka zaman yapalım. Görüşürüz 💗";

        document.getElementById("cevap").style.display =
            "none";

        document.getElementById("buton").style.display =
            "none";
    }
}


function devamEt() {

    document.getElementById("baslik").innerHTML =
        "Bir şey söyleyeceğim... 👀";

    document.getElementById("soru").innerHTML =
        "Sana bir sır vereyim mi?";

    document.getElementById("cevap").value = "";

    document.getElementById("buton").innerHTML =
        "Gönder 💗";

    document.getElementById("buton").onclick =
        sirCevap;
}


function sirCevap() {

    let cevap = document.getElementById("cevap").value
        .toLowerCase()
        .trim();

    if (cevap == "") {
        document.getElementById("mesaj").innerHTML =
            "Bir cevap bekliyorum 👀";
        return;
    }

    if (
        cevap.includes("evet") ||
        cevap.includes("ver") ||
        cevap.includes("olur") ||
        cevap.includes("tabii") ||
        cevap.includes("tabi") ||
        cevap.includes("anlat") ||
        cevap.includes("söyle") ||
        cevap.includes("soyle") ||
        cevap.includes("merak") ||
        cevap.includes("hadi") ||
        cevap.includes("tamam") ||
        cevap.includes("isterim")
    ) {

        document.getElementById("baslik").innerHTML =
            "O zaman sır geliyor... 🤫";

        document.getElementById("soru").innerHTML =
            "Bu mesajı sana yollayan kişi sana çok aşıkmış. 💗";

        document.getElementById("cevap").value = "";

        document.getElementById("buton").innerHTML =
            "Devamını gör 👀";

        document.getElementById("buton").onclick =
            sonMesaj;

    }

    else {

        document.getElementById("baslik").innerHTML =
            "Peki... 😒";

        document.getElementById("soru").innerHTML =
            "Sana sır verecektik ama istemedin. Küstüm biraz. 😤💗";

        document.getElementById("cevap").style.display =
            "none";

        document.getElementById("buton").style.display =
            "none";
    }
}


function sonMesaj() {

    document.getElementById("baslik").innerHTML =
        "Son bir şey... 🥹";

    document.getElementById("soru").innerHTML =
        "Seni kendinden çok seven sevgilin senin o güzel gözlerini özlemiş. 💗";

    document.getElementById("cevap").style.display =
        "none";

    document.getElementById("buton").innerHTML =
        "💗";

    document.getElementById("buton").onclick =
        finalMesaj;
}


function finalMesaj() {

    document.getElementById("baslik").innerHTML =
        "Seni seviyorum 💗";

    document.getElementById("soru").innerHTML =
        "Umarım bu küçük sürpriz yüzünde güzel bir gülümseme bırakmıştır. 🥹💗<br><br>" +
        "Şimdilik bu kadar... ama seni özleyen biri var. 🌸";

    document.getElementById("buton").style.display =
        "none";
}

</script>

</body>
</html># surprisee