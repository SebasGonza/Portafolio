<template>
    <div class="background">

        <div class="navbar">
            <div class="logo">
                Sebastian
            </div>
            <div class="opciones">
                <a @click="toScrollPage('home')" class="opcion" data-page="home">Home</a>
                <a @click="toScrollPage('about-me')" class="opcion" data-page="about-me">Sobre mi</a>
                <a @click="toScrollPage('habilities')" class="opcion" data-page="habilities">Habilidades</a>
                <a @click="toScrollPage('experience')" class="opcion" data-page="experience">Experiencia</a>
                <a @click="toScrollPage('contact-me')" class="opcion" data-page="contact-me">Contactame</a>

                <div class="indicator"></div>
            </div>
        </div>
    </div>
</template>

<style scoped>
@import '../assets/base.css';
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;300;400;600&display=swap');

.opcion {
    margin-right: 12px;
    font-size: 1rem;
}

.logo::before {
    content: "<";
}

.logo::after {
    content: "/>";
}

.indicator {
    position: absolute;
    z-index: -5;
    background: rgba(93, 153, 98, 1);
    height: 2px;

}



.navbar {
    backdrop-filter: blur(40px);
    position: fixed;
    font-family: 'Montserrat', sans-serif;
    width: 100%;
    padding: 20px 50px;
    display: flex;
    justify-content: space-between;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 10px;
}

.logo {
    font-size: 1.5rem;
}

.opciones {
    width: 33vw;
    display: flex;
    flex-direction: row;
    column-gap: 4%;
    font-size: 1rem;

}

.opciones a:hover {
    cursor: pointer;
    background-color: none;
    color: none;
    /* color: #88EB90; */

}

@media screen and (min-width: 1326px) and (max-width: 1440px) {

    .opciones {

        display: flex;
        width: 50vw;
        column-gap: 2%;
    }


}
</style>

<script setup lang="ts">

function toScrollPage(a: string): void {
    document.querySelector(`.${a}`)?.scrollIntoView({ behavior: "smooth" });
}
</script>
