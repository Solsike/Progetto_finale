<template>
    <div>
        <header class="Header">
            <div class="container" id="homeUp">
                <div class="row NavRow" :class="{ 'scrolled': scrolled }">
                    <div class="col">
                        <nav class="navbar navbar-expand-lg">
                            <div class="container-fluid">
                                <a class="navbar-brand" href="#"><img class="logo" src="@/assets/images/logo.png"
                                        alt=""></a>
                                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
                                    aria-expanded="false" aria-label="Toggle navigation">
                                    <span class="navbar-toggler-icon"></span>
                                </button>
                                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                                    <ul class="navbar-nav mb-2 mb-lg-0">
                                        <li class="nav-item">
                                            <a class="nav-link arancione" aria-current="page" href="#homeUp">Home</a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="#about">About</a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="#portfolio">Portfolio</a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="#service">Service</a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="#blog">Blog</a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="#contact">Contact</a>
                                        </li>
                                        <li><a href="#" class="nav-link orange-button"><button
                                                    class=" slide_from_bottom rounded-pill">Download CV</button></a>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </nav>
                    </div>
                </div>
            </div>
            <section id="jumbotron">
                <div class="container">
                    <div class="row">
                        <div class="col-lg-6 jumboleft d-flex flex-column justify-content-center align-items-right ps-4">
                            <div class="hello d-flex">
                                <h3>Hello, I'm</h3>
                            </div>
                            <div class="name d-flex">
                                <h1>James Smith</h1>
                            </div>
                            <div class="job d-flex">
                                <p>A <span class="greenText">Creative Designer</span> From <span class="yellowText">New
                                        York</span></p>
                            </div>
                            <div class="text d-flex">
                                <p>I'm creative designer based in New York, and I'm very passionate and dedicated to my
                                    work.</p>
                            </div>
                            <div class="container bottone_icone d-flex align-items-center ps-5">
                                <div class="bottonedue">
                                    <a class="buttonTwo orange-button" href="#"><button
                                            class=" slide_from_top rounded-pill">About
                                            Me</button></a>
                                </div>
                                <div class="icone">
                                    <ul>
                                        <li><a href=""><i class="fa-brands fa-facebook-f"></i></a></li>
                                        <li><a href=""><i class="fa-brands fa-twitter"></i></a></li>
                                        <li><a href=""><i class="fa-brands fa-linkedin-in"></i></a></li>
                                        <li><a href=""><i class="fa-brands fa-behance"></i></a></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                        <div class="col-lg-6 DivAvatar">
                            <img src="@/assets/images/avatar.png" alt="james" class="avatar">
                            <div class="Ai animated">
                                <p>Ai</p>
                            </div>
                            <div class="Ps animated">
                                <p>Ps</p>
                            </div>
                            <div class="cerchietti animated">
                                <div class="containerCerchi">
                                    <div class="rosso"></div>
                                    <div class="rosa"></div>
                                    <div class="viola"></div>
                                    <div class="azzurro"></div>
                                    <div class="verde"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="row DivMouse">
                        <a href="#homeDown" class="mouse rounded-pill ps-2">
                            <div class="stanghetta animatedMouse"></div>
                        </a>
                    </div>
                </div>
            </section>
        </header>
    </div>
</template>









<script>
export default {
    name: 'HeaderSection',
    data() {
        return {
            scrolled: false
        };
    },
    methods: {
        handleScroll() {
            this.scrolled = window.scrollY > 0;
        }
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeUnmount() {
        window.removeEventListener('scroll', this.handleScroll);
    }
};
</script>









<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Jost:ital,wght@0,100..900;1,100..900&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

a,
img {
    cursor: pointer;
}


/* MENU IN ALTO*/




.logo {
    height: 31px;
    margin-top: 8px;
    padding-left: 90px;

}

#navbarSupportedContent {
    display: flex;
    justify-content: flex-end;
    padding-right: 92px;
    color: white;

}



.scrolled {
    background-color: #2b2d33;
    position: fixed;
    z-index: 9990;
    top: 0;
    right: 0;
    left: 0;
    box-shadow: 0 0 10px rgba(255, 255, 255, .05);
    padding-left: 100px;
    padding-right: 110px;
    bottom: -20;
  
}

    .nav-item {
    font-family: 'Jost', sans-serif;
    font-weight: 500;
    margin-right: 13px;
    padding-top: 15px;
}

a.nav-link {
    color: white;
}

a.nav-link:hover {
    color: #f75023;
}


a.arancione {
    color: #f75023;
}


.orange-button button {
    background-color: transparent;
    border: 2px solid #f75023;
    padding: 8px 25px 7px;
    position: relative;
    z-index: 1;
    overflow: hidden;
    text-align: center;
    font-size: 15px;
    font-weight: 500;
    font-family: 'Jost', sans-serif;
    color: white;
    margin-top: 5px;
   

}


.orange-button button:hover {
    color: #ffffff;
   
}


.orange-button button::after {
    content: "";
    background: #f75023;
    position: absolute;
    z-index: -1;
    padding: 0.85em 0.75em;
    display: block;

}

.orange-button button[class^="slide"]::after {
    transition: all 0.25s;
   
}


.orange-button button[class^="slide"]:hover::after {
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    transition: all 0.25s;
 
}


.orange-button button.slide_from_bottom::after {
    left: 0;
    right: 0;
    top: 100%;
    bottom: -100%;
}

.orange-button button.slide_from_top {
    background-color: #f75023;
    border: 2px solid #f75023;
    position: relative;
    z-index: 1;
    overflow: hidden;
    text-align: center;
    font-size: 16px;
    font-weight: 500px;
    font-family: 'Jost', sans-serif;
    color: white;
    padding: 10px 32px;
    margin-left: 18px;
}





.orange-button button.slide_from_top::after {
    left: 0;
    right: 0;
    top: -100%;
    bottom: 100%;
    transition: all 0.55s;
    background-color: transparent;
}

.orange-button button.slide_from_top:hover::after {
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    transition: all 0.35s;
}

button.slide_from_top:hover::after{
    background-color: #3e4352;
}


/* SFONDO JUMBOTRON */
#jumbotron {
    padding-top: 20px;
    margin-top: 10px;

}

.Header {

    background-image: url("https://marketifythemes.net/html/dizme/img/slider/2.jpg");
    height: 720px;
    width: 100%;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    
}


/*SINISTRA JUMBOTRON*/




.hello h3 {
    color: #f75023;
    font-size: 25px;
    margin-bottom: 2px;
    margin-top: 17px;

}

.hello,
.name {
    font-weight: 500;
    line-height: 1.3;
    font-family: 'Jost', sans-serif;
    padding-left: 90px;
}

.name h1 {
    font-size: 60px;
    color: white;
}

.job {
    color: white;
    padding-left: 90px;
    font-family: 'Open Sans', sans-serif;
    font-size: 19px;
    margin-top: 10px;
}

.greenText {
    color: #1cbe59;
}

.yellowText {
    color: #e8be5b;
}

.text {
    color: white;
    font-family: 'Open Sans', sans-serif;
    padding-left: 90px;
    text-align: left;
    margin-top: 10px;
}


.bottonedue {
    padding-left: 30px;
}



/* icone*/

.icone ul {
    padding-left: 12px;
}

.icone li {
    list-style-type: none;
    display: inline-block;
    margin-left: 16px;
    margin-top: 29px;



}

i {
    color: white;
}





/* DESTRA JUMBOTRON*/

.avatar {
    position: relative;
    max-height: 400px;
    padding-right: 135px;
    cursor: pointer;
    overflow: hidden;
}

.Ai {
    position: absolute;
    width: 50px;
    height: 50px;
    background-color: #390000;
    border-radius: 18%;
    margin: 20px;
    top: 22%;
    right: 40%;
}

.Ai p {
    color: #ff9a00;
    font-size: 30px;
    font-family: 'Open Sans', sans-serif;
    font-weight: bold;
    padding-top: 3px;
}

.Ps {
    position: absolute;
    width: 50px;
    height: 50px;
    background-color: #001631;
    border-radius: 18%;
    margin: 20px;
    right: 20%;
    top: 30%;
}

.Ps p {
    color: #00a9ff;
    font-size: 28px;
    font-family: 'Open Sans', sans-serif;
    font-weight: bold;
    padding-top: 3px;
}

.cerchietti {
    position: absolute;
    width: 50px;
    height: 50px;
    background-color: #ffffff;
    border-radius: 18%;
    margin: 20px;
    right: 32%;
    top: 65%;
}


.rosso {
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #f24e1e;
    margin: 20px;
    right: 10%;
    bottom: 15%;
    border-bottom-left-radius: 50%;
    border-top-left-radius: 50%;
}

.rosa {
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #ff7262;
    border-radius: 50%;
    margin: 20px;
    bottom: 15%;
    left: 10%;
    border-top-left-radius: 0%;
    border-bottom-left-radius: 0%;
}

.viola {
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #a259ff;
    margin: 20px;
    bottom: -1%;
    right: 10%;
    border-bottom-left-radius: 50%;
    border-top-left-radius: 50%;
}

.azzurro {
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #19bcfe;
    border-radius: 50%;
    margin: 20px;
    bottom: -1%;
    left: 10%;
}

.verde {
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #09cf83;
    border-radius: 50%;
    margin: 20px;
    bottom: -17%;
    right: 10%;
    border-top-right-radius: 0%;
}




/* icona mouse */

.DivMouse {
    display: flex;
    justify-content: center;
    padding-top: 115px;

}

a.mouse {
    display: inline-block;
    border: 2px solid white;
    height: 35px;
    width: 0px;
    border-radius: 37%;
    position: relative;

}

.stanghetta {
    width: 1px;
    height: 8px;
    border: 1px solid white;
    position: absolute;
    top: 30%;
    left: 45%;
}


/*animazioni*/

.animated {
    animation: move-up-down 3.25s ease-in-out infinite alternate-reverse;
}


@keyframes move-up-down {
    0% {
        transform: translateY(10px);
    }

    100% {
        transform: translateY(-12px);
    }
}




.animatedMouse {
    animation: move-up-down-mouse 1.25s ease-in-out infinite alternate-reverse;
}


@keyframes move-up-down-mouse {
    0% {
        transform: translateY(2px);
    }

    100% {
        transform: translateY(-8px);
    }
}
</style>