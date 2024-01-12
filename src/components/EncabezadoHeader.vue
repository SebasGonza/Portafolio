<template>
    <div class="navbar">
        <div class="logo">
            Sebastian;
        </div>
        <div class="opciones">
            <a data-page="home">Home</a>
            <a data-page="about-me">Sobre mi</a>
            <a data-page="habilities">Habilidades</a>
            <a data-page="expirience">Experiencia</a>
            <a data-page="contact-me">Contactame</a>
        </div>
    </div>
</template>

<style scoped>
@import '../assets/base.css';
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;300;400;600&display=swap');

body {
    background: var(--color-background);
}

.navbar {
    position: fixed;
    font-family: 'Montserrat', sans-serif;
    width: 95vw;
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
    /* border: white solid; */
    display: flex;
    flex-direction: row;
    column-gap: 10%;
    font-size: 1rem;

}

.opciones div:hover {
    cursor: pointer;
    color: #88EB90;

}
</style>