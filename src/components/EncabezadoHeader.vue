<template>
    <div class="navbar">
        <div class="logo">
            Sebastian;
        </div>
        <div class="opciones">
            <a data-page="home">Home</a>
            <a data-page="about-me">Sobre mi</a>
            <a data-page="habilities">Habilidades</a>
            <a data-page="experience">Experiencia</a>
            <a data-page="contact-me">Contactame</a>
            <div class="indicator"></div>
        </div>
    </div>
</template>

<style scoped>
@import '../assets/base.css';
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;300;400;600&display=swap');

body {
    background: var(--color-background);
}

.indicator{

    position: absolute;
    z-index: -5;
    background: linear-gradient(90deg, rgba(216,235,220,1) 0%, rgba(155,244,163,1) 13%, rgba(135,207,141,1) 34%, rgba(93,153,98,1) 95%);
    top: 15px;

}

.navbar {
    position: fixed;
    font-family: 'Montserrat', sans-serif;
    width: 100%;
    margin-top: 20px;
    display: flex;
    justify-content: space-around;
}

.logo {
    /* border: 2px solid white; */
    font-size: 1.5rem;
    /* margin-right: 20vw; */
}

.opciones {
    width: 33vw;
    display: flex;
    flex-direction: row;
    column-gap: 10%;
    font-size: 1rem;

}

.opciones   a:hover {
    cursor: pointer;
    background-color: none;
    /* color: #88EB90; */

}
</style>