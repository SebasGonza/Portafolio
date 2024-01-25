<template>
    <div class="navbar">
        <div class="logo">
            Sebastian;
        </div>
        <div class="opciones">
            <a href="#home" class="opcion" data-page="home">Home</a>
            <a href="#about-me" class="opcion" data-page="about-me">Sobre mi</a>
            <a href="#habilities" class="opcion" data-page="habilities">Habilidades</a>
            <a href="#experience" class="opcion" data-page="experience">Experiencia</a>
            <a href="#contact" class="opcion" data-page="contact-me">Contactame</a>
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

.opcion{
    margin-right: 12px
}
.indicator{

    position: absolute;
    z-index: -5;
    background:  rgba(93,153,98,1);
    top: 15px;
    height: 2px;
    margin-top: 3px;

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
    column-gap: 4%;
    font-size: 1rem;

}

.opciones   a:hover {
    cursor: pointer;
    background-color: none;
    /* color: #88EB90; */

}

@media screen and (min-width: 1326px) and (max-width: 1440px){

    .opciones{
        display: flex;
        width: 50vw;
        column-gap: 2%;
    }

    
}


</style>