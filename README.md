<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,700;1,400&family=Poppins:wght@300;400;600;700;800;900&family=Roboto:ital,wght@0,500;0,700;1,400;1,500;1,700&display=swap" rel="stylesheet">
<link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
<style>
    *,*::before,*::after{
    box-sizing: border-box;
}
*{
    margin: 0;
    padding: 0;
    line-height: 1.5;
}
body{
    font-family: 'Poppins', sans-serif;
    background-color:rgb(10,10,10);
    color: white;
    height: 100vh;
}
button{
    border: none;
    background:none;
    color:inherit;
    font-family: inherit;
}
a{
    color:white;
    text-decoration: none;
}
input,select,option{
    outline: none;
    width: 50%;
    /* height: 50px; */
    /* border-radius: 5px; */
    padding: 0.5rem;
    /* border: 3px solid black; */
    
    
}

button{
    border: none;
    background: none;
    cursor: pointer;
    color: inherit;
    font-family: inherit;
}
.header{
    display: flex;
    align-items: center;
    width: 100%;
    margin-bottom: 5rem;
}
.header__title{
    font-size: 3rem;
    /* border: 3px solid green; */
    flex-grow:1;
}
.menu.show{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    /* border: 3px solid green; */
    background-color: rgb(0, 0, 0);
    position: absolute;
    top: 0;
    right:0;
    width: 100%;
    height: 100vh;
    z-index: 1;
    overflow: hidden;
    /* border: 3px solid red; */
}
.exit-menu {
display: none;
/* color: rgb(189, 27, 149); Cambia il colore a tuo piacimento */
color: white;
font-size: 1.5rem;
z-index: 2;
cursor:pointer;
}

.exit-menu.show {
    display: block;
}
.menu{
    /* border: 3px solid blue; */
    display: none;
}
.menu__link:hover{
    text-decoration: underline;
    text-decoration-thickness: 0.2rem;
    text-decoration-color:rgb(189, 27, 149);
    
}
.menu-bar{
    display: none;
}

.info{
    text-align: center;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    
}
.info__title{
    text-transform: uppercase;
    text-align: center;
    font-size: 2.2rem;

}
.info_paragraph1{
    max-width: 60ch;
    font-size: 1rem;
    /* border: 3px solid yellow; */
    margin: 0 auto;

}
.info-btn{
    padding: 0.5rem;
    background-color: rgb(189, 27, 149);
    width: 200px;
    font-size: inherit;
    /* font-weight: bold; */
    color: white;
    cursor: pointer;
}
.info-btn:hover{
    color: rgb(189, 27, 149);
    background-color: white;
    transition: all 0.5s ease;
}
.servizi{
    /* border: 3px solid red; */
    text-align: center;
}
.servizi__title{
    font-size: 2.2rem;
    margin-bottom: 0.5rem;
}

.servizi__box{
    background-color: white;
    color: black;
    padding: 1rem;
    border-radius: 8px;
    margin-bottom: 1rem;
    
}
.pricing__box__description1{
    margin-bottom: 1rem;
    font-size: 0.75rem;
    color: rgb(189, 27, 149);
}
.pricing__box__description2{
    /* border: 3px solid pink; */
    max-width: 55ch;
    /* margin-bottom: 1rem; */
    /* background-color: rgb(189, 27, 149); */
    padding: 0.5rem;
    border-radius: 5px;
    color: black;
    margin-bottom: 1rem;
    margin-inline: auto;
}


.btn{
    background-color:rgb(189, 27, 149);
    color: white;
    padding: 0.5em 1em;
    border-radius: 6px;
    font-weight: 500;
    font-size: 1rem;
    cursor: pointer;
}
.btn:hover{
    background-color: rgb(10,10,10);
    transition: all 0.5s ease;
    
}
.tr{
    display:flex;
    width: 100%;
    justify-content: flex-end;
    
}
.container{
    width: 100%;
    /* border: 3px solid red; */
    margin-inline: auto;
    margin-bottom: 5rem;
    padding-inline: 0.5rem;
}
.contacts{
    background-color: white;
    width: 100%;
}
.contenitore__contacts{
    display: flex;
    /* gap: 1rem; */
    /* padding: 1rem 1rem 0 1rem; */
}
.contacts__box{
    background-color: white;
    color: black;
    flex-grow: 1;
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    
    border-width: 100%;
}

.contact__box__title{
    color: rgb(189, 27, 149);
}
.contacts__info a{
    color: black;
}
.contacts__info:hover a{
    color: rgb(189, 27, 149);
    transition: all 0.3s ease;
}
.icon__box{
    
}
.contacts__icon{
    color: inherit;
    font-size: 3rem;
    cursor: pointer;
}
.contacts__icon:hover{
    color: rgb(189, 27, 149);
}
.icon__box{
    display: flex;
    justify-content: flex-start;
    gap: 2rem;
}
@media (min-width:320px){
    body{
        overflow: hidden;
    }
    .header__title{
        font-size: 1.8rem;
    }
    .show{
        display: none;
        /* font-size: 0.6rem; */
    }
    .menu-bar{
        display: block;
        font-size: 1.5rem;
        cursor: pointer;
    }
    .info__title{
        font-size: 1.2rem;
    }
    .info_paragraph1{
        font-size: 0.5rem;
    }
    .info-btn{
        width: 70px;
        font-size: 0.5rem;
    }
    .menu.show .menu__link{
        background-color: rgb(1, 1, 1);
        color: rgb(255, 255, 255);
        width: 100px;
        padding: 0.5rem;
        text-align: center;
        border-radius: 5px;
        
    }
    .menu.show .menu__link:hover{
        background-color: rgb(189, 27, 149);
        text-decoration: none;
        transition: background-color, 0.5s ease;
    }
    .servizi__title{
        font-size: 1.2rem;
    }
    
    .pricing__box__title{
        font-size: 0.8rem;
    }
    .pricing__box__description1,.pricing__box__description2{
        font-size: 0.5rem;
    }
    .pricing__btn{
        font-size: 0.5rem;
    }
    /* .form__section{
        border: 3px solid orange;
    }
    .form{
        border: 10px solid green;
    } */
    
    .contenuto{
        width:100%;
    }
    
    .contenitore__contacts{
        flex-wrap: wrap;
    }
    .contenitore__contacts .contacts__box:nth-child(1){
        border-bottom: 2px solid #ccc;
    }
    .contenitore__contacts .contacts__box:nth-child(2){
        border-bottom: 2px solid #ccc;
    }
    .contacts__box{
        /* border: 3px solid red; */
    }
    .contact__box__title{
        font-size: 1rem;
    }
    .contacts__info{
        font-size: 0.5rem;
    }
    .contacts__icon{
        font-size: 0.8rem;
    }
    
}
@media (min-width:475px){
    .container{
        max-width:475px;
    }
    .header__title{
        font-size: 2rem;
    }
    .info_paragraph1{
        font-size: 0.rem;
    }
    
    
}

/* sm */
@media (min-width:640px){
    .container{
        max-width:640px;
    }
    .header__title{
        font-size: 2.5rem;
        margin-left: 2.5rem;
    }
    .menu{
        display: flex;
        font-size: 1rem;
        justify-content: end;
        gap: 1rem;
        flex-grow:1;
        margin-right: 2.5rem;
        /* font-size: 1.1rem; */
        /* border: 3px solid blue; */
    }
    .menu__link{
        background: none;
        color: white;
    }
    .menu__link:hover{
        background:none;
        text-decoration-color: rgb(189, 27, 149);
    }
    .menu-bar{
        display: none;
    }
    .info__title{
        font-size: 1.5rem;
    }
    .info_paragraph1{
        font-size: 0.7rem;
    }
    .info-btn{
        width: 100px;
        font-size: 0.7rem;
    }
    .servizi__title{
        font-size: 1.5rem;
    }
    .pricing__box__title{
        font-size: 1rem;
    }
    .pricing__box__description1,.pricing__box__description2{
        font-size: 0.8rem;
    }
    .pricing__btn{
        font-size: 0.8rem;
    }
    
    .input-box,.scelta-servizio{
        font-size: 0.8rem;
    }
    .contenitore__contacts{
        flex-wrap: nowrap;
    }
    .contenitore__contacts .contacts__box:nth-child(1){
        border-right: 2px solid #ccc;
    }
    .contenitore__contacts .contacts__box:nth-child(2){
        border-right: 2px solid #ccc;
    }
    
    .contact__box__title{
        font-size: 1rem;
    }
    .contacts__info{
        font-size: 0.8rem;
    }
    .contacts__icon{
        font-size: 1rem;
    }
} 

/* md */
@media (min-width:768px){
    .container{
        max-width:768px;
    }
    .header__title{
        font-size: 3rem;
    }
    .menu{
        font-size:1.2rem;
    }
    .info__title{
        font-size: 2rem;
    }
    .info_paragraph1{
        font-size: 1rem;
    }
    .info-btn{
        font-size: 1rem;
    }
    .servizi__title{
        font-size: 2rem;
    }
    .pricing__box__title{
        font-size: 1.2rem;
    }
    .pricing__box__description1,.pricing__box__description2{
        font-size: 1rem;
    }
    .pricing__btn{
        font-size: 1rem;
    }
    
    .input-box,.scelta-servizio{
        font-size: 1rem;
    }
    .contact__box__title{
        font-size: 1.2rem;
    }
    .contacts__info{
        font-size: 1rem;
    }
    .contacts__icon{
        font-size: 2.5rem;
    }
    
}

/* lg */
@media (min-width:1024px){
    .container{
        max-width:1024px;
    }
    .contenitore__servizi{
        /* border:3px solid blue; */
        display: grid;
        grid-template-areas:
        'a a a b b'
        'c c d d e';
        gap: 1.2rem;
        padding: 1rem;
    }
    .servizi__box{
        background-color: white;
        color: black;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        gap: 1rem;
        padding: 1rem;
        border-radius: 8px;
    }
    .servizi__box--a{
        grid-area: a;
    }
    .servizi__box--b{
        grid-area: b;
    }
    .servizi__box--c{
        grid-area: c;
    }
    .servizi__box--d{
        grid-area: d;
    }
    .servizi__box--e{
        grid-area: e;
    }
    
}

/* xl */
@media (min-width:1280px){
    .container{
        max-width:1280px;
    }
}

/* 2xl */
@media (min-width:1536px){
    .container{
        max-width:1536px;
    }
}

</style>

</head>
<body>
    <header class="header " id="header">
        <h1 class="header__title"><a href="#header">Tony's & Remo's</a></h1>
        <i class='menu-bar bx bx-menu' id="menu-bar" ></i>
        <i class='exit-menu bx bx-x' id="exit-menu"></i>
        <nav class="menu" id="menu">
            <a class="menu__link" href="https://drive.google.com/file/d/1B3HtF8eZ5I1jc6JNRIfUezk6HxLcZ00x/view?usp=drive_link">Prenota</a>
            <a class="menu__link" href="">Info</a>
            <a class="menu__link" href="">Contatti</a>
        </nav>
    </header>

    <section class="info container">
        <h2 class="info__title">Eleva il Tuo Stile con Tony's & Remo's</h2>
        <div class="contenitore">
            <!-- <img src="remo1.jpg" alt=""> -->
            <p class="info_paragraph1">
                Il tuo stile è la tua firma, la tua identità nel mondo.
                 Presso Tony's & Remo's, ti offriamo l'elevazione dello stile,
                  trasformando la tua visione in realtà con precisione e
                   maestria.
            </p>
        </div>
        <div class="contenitore">
            <a class="info-btn" id="mostraForm" href="form-barber.php">Prenota</a>
        </div>
    </section>
    
    <section class="servizi container">
        <h2 class="servizi__title">I Nostri Servizi</h2>
        <div class="contenitore__servizi">
            <div class="servizi__box servizi__box--a">
                <div>
                    <h2 class="pricing__box__title">Taglio di Capelli Personalizzato</h2>
                <p class="pricing__box__description1">Stile Su Misura</p>
                </div>
                <div>
                    <p class="pricing__box__description2">
                        Lascia che i nostri esperti barbieri trasformino il tuo look con tagli di capelli personalizzati.
                         Approfitta della nostra consulenza professionale per un taglio che si adatti perfettamente alla 
                         tua fisionomia e al tuo stile di vita, seguendo le ultime tendenze e tecniche di precisione.
                    </p>            
                </div>
                <div class="tr">
                    <button class="btn pricing__btn">Prenota</button> 
                </div>
            </div>
            <div class="servizi__box servizi__box--b">
                <div>
                    <h2 class="pricing__box__title">Rasature e Trattamenti Barba</h2>
                <p class="pricing__box__description1">Eleganza Grooming</p>
                </div>
                <div>
                    <p class="pricing__box__description2">
                        Dai un tocco di classe al tuo grooming quotidiano. Offriamo rasature classiche e trattamenti
                         per la barba che vanno oltre il semplice taglio. I nostri servizi di grooming garantiscono 
                         un aspetto curato e impeccabile, mantenendo la salute della tua pelle e della tua barba.
                    </p>
                </div>
                <div class="tr">
                    <button class="btn pricing__btn">Prenota</button>
                </div>
            </div>
            <div class="servizi__box servizi__box--c">
                <div>
                    <h2 class="pricing__box__title">Colore e Trattamenti per Capelli Unisex</h2>
                <p class="pricing__box__description1">Colori e Cura Profonda</p>
                </div>
                <div>
                    <p class="pricing__box__description2">
                        Sia che tu sia un uomo o una donna, offriamo servizi di colorazione e trattamenti
                         mirati per i capelli. Il nostro team di esperti utilizza prodotti di alta qualità
                          e tecniche avanzate per garantire risultati duraturi e un look impeccabile.
                    </p>
                </div>
                <div class="tr">
                    <button class="btn pricing__btn">Prenota</button>
                </div>
            </div>
            <div class="servizi__box servizi__box--d">
                <div>
                    <h2 class="pricing__box__title">Trattamenti per Sopracciglia e Rifiniture</h2>
                <p class="pricing__box__description1">Dettagli di Bellezza</p>
                </div>
                <div>
                    <p class="pricing__box__description2">
                         I dettagli fanno la differenza. Oltre ai servizi per capelli, offriamo rifiniture
                          professionali per le sopracciglia. Con la massima precisione, modelliamo 
                          e definiamo le sopracciglia per migliorare l'aspetto naturale del tuo viso.
                    </p>
                </div>
                <div class="tr">
                    <button class="btn pricing__btn">Prenota</button>
                </div>
            </div>
            <div class="servizi__box servizi__box--e">
                <div>
                    <h2 class="pricing__box__title">Stile e Consulenza per Acconciature</h2>
                <p class="pricing__box__description1">Idee per il Look Perfetto</p>
                </div>
                <div>
                    <p class="pricing__box__description2">
                        Approfitta della nostra consulenza professionale sull'acconciatura e lo stile.
                         Dai consigli su misura e suggerimenti pratici, il nostro obiettivo è realizzare 
                         il look desiderato, garantendo soddisfazione e fiducia nel tuo nuovo stile.
                    </p>
                </div>
                <div class="tr">
                    <button class="btn pricing__btn">Prenota</button>
                </div>
            </div>
        </div>
    </section>

    <footer class="contacts ">
        <div class="contenitore__contacts">
            <div class="contacts__box">
                <h3 class="contact__box__title">Contatti</h3>
                <p class="contacts__info">Indirizzo: Via Nome della Strada, Numero Civico</p>
                <p class="contacts__info">Telefono: <a href="tel:+ +39 0123456789">+39 0123456789</a> </p>
                <p class="contacts__info">Email:<a class="email__link" href="mailto: info@tonyeremo.com"> info@tonyeremo.com</a></p>
                <div class="icon__box">
                    <i class='contacts__icon bx bxl-instagram-alt' ></i>
                    <i class='contacts__icon bx bxl-facebook-circle'></i>
                    <i class='contacts__icon bx bxl-whatsapp' ></i> 
                </div>
            </div>
            <div class="contacts__box">
                <h3 class="contact__box__title">Contatti</h3>
                <p class="contacts__info">Indirizzo: Via Nome della Strada, Numero Civico</p>
                <p class="contacts__info">Telefono: +39 0123456789</p>
                <p class="contacts__info">Email: info@tonyeremo.com</p>
            </div>
            <div class="contacts__box">
                <h3 class="contact__box__title">Contatti</h3>
                <p class="contacts__info">Indirizzo: Via Nome della Strada, Numero Civico</p>
                <p class="contacts__info">Telefono: +39 0123456789</p>
                <p class="contacts__info">Email: info@tonyeremo.com</p>
            </div>
        </div>
    </footer>
    <script>
        
        function toggleBodyOverflow() {
    const body = document.body;
    if (body.style.overflow === 'hidden') {
        body.style.overflow = 'auto';
    } else {
        body.style.overflow = 'hidden';
    }
}

document.addEventListener("DOMContentLoaded", function() {
    const menuToggle = document.getElementById("menu-bar");
    const menu = document.getElementById("menu");
    const exitMenu = document.getElementById("exit-menu");

    menuToggle.addEventListener("click", function() {
        menu.classList.toggle("show");
        exitMenu.classList.toggle("show");
        toggleBodyOverflow(); // Chiama la funzione per cambiare l'overflow del body
    });

    exitMenu.addEventListener("click", function() {
        menu.classList.remove("show");
        exitMenu.classList.remove("show");
        toggleBodyOverflow(); // Chiama la funzione per cambiare l'overflow del body
    });
});
;

    </script>
</body>

</html>
