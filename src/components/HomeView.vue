<template>
    <div class="decoraciones">
        <div class="consola3">
            <img src="../assets/consola3.svg" height="100" />
        </div>
        <div class="consola1">
            <img src="../assets/consola1.svg" height="1000" />
        </div>
        <div class="consola2">
            <img src="../assets/consola2.svg" height="100" />
        </div>

        <div class="bola bola1">
            <img src="../assets/bola1.svg" height="10" />
        </div>
        <div class="bola bola8">
            <img src="../assets/bola3.svg" height="10" />
        </div>
        <div class="bola bola2">
            <img src="../assets/bola1.svg" height="5" />
        </div>
        <div class="bola bola3">
            <img src="../assets/bola1.svg" height="5" />
        </div>
        <div class="bola bola4">
            <img src="../assets/bola1.svg" height="8" />
        </div>
        <div class="bola bola5">
            <img src="../assets/bola2.svg" height="20" />
        </div>
        <div class="bola bola6">
            <img src="../assets/bola2.svg" height="15" />
        </div>
        <div class="bola bola7">
            <img src="../assets/bola1.svg" height="10" />
        </div>
    </div>

    <div class="container_presentacion">

        <div class="foto">
            <img src="../assets/fondo_foto.svg" alt="" height="500">
        </div>

        <div class="presentacion">
            <p>Hola mi nombre es:</p>
            <span class="nombre">
                Sebastian Gonzalez Romero
            </span>
            <span class="predicado">& Soy Front-end Developer</span>

            <div class="botones">
                <a class="boton boton-principal" href="https://www.linkedin.com/in/sebastian-gonzalez-romero-5b4aa91b9/"
                    title="LinkedIn">
                    Mi perfil de linkedIn
                </a>
                <a class="boton boton-secundario" @click="showCV">
                    Ver mi CV
                </a>
            </div>

        </div>
    </div>
</template>

<style>
@import '../assets/base.css';

/* Fondo */
.consola3 {
    position: absolute;
    top: 5rem;
    right: 1rem;
    z-index: -1;
}

.consola1 {
    position: absolute;
    top: 25rem;
    left: -16rem;
    z-index: -1;
}

.consola2 {
    position: absolute;
    top: 45rem;
    right: 1rem;
    z-index: -1;

}

.bola {
    position: absolute;
    z-index: -1;
    animation: movimientoBola 5s infinite;
    animation-direction: alternate;

}

@keyframes movimientoBola {
    from {
        translate: 0 50px;
        /* scale: 200% 1; */
    }

    to {
        translate: 0 0;
        /* scale: 100% 1; */
    }
}

.bola1 {
    top: 5rem;
    right: 2rem;
}

.bola3 {
    top: 20rem;
    right: 50rem;
}

.bola4 {
    top: 7rem;
    left: 50rem;
}

.bola5 {
    top: 7rem;
    left: 80rem;
}

.bola6 {
    top: 15rem;
    left: 10rem;
}

.bola7 {
    bottom: 10rem;
    right: 15rem;
}

.bola8 {
    top: 20rem;
    left: 40rem;
}

/* Presentación */

.container_presentacion {
    display: flex;
    /* border: white solid; */
    width: 60vw;
}

.nombre {
    color: #00bd7e;
    display: block;
    font-family: Poppins, monospace;
    font-weight: 600;
    font-size: 2rem;
    white-space: nowrap;
    border-right: 4px solid;
    width: 460px;
    animation: typing 2s steps(25), blink .5s infinite step-end alternate;
    overflow: hidden;
}

.presentacion {
    /* margin-left: 30%; */
    width: 29vw;
    /* border: orange solid; */
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.botones {
    margin-top: 20px;
    display: flex;
    width: 456px;
    height: 40px;
}

.boton {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    width: 45%;
    border: solid hsla(160, 100%, 37%, 1) 1px;
    border-radius: 3px;
    cursor: pointer;

}

.boton-principal {
    background-color: hsla(160, 100%, 37%, 1);
    color: white;
}

.boton-secundario {
    margin-left: 50px;
    background-color: var(--vt-c-black);
}

.boton-secundario:hover {
    background-color: hsla(160, 100%, 37%, 1);
    color: white;
}

.boton-principal:hover {
    background-color: var(--vt-c-black);
    color: hsla(160, 100%, 37%, 1);
}

.predicado {
    font-size: 2rem;
    font-family: Poppins, monospace;
    color: rgba(93, 153, 98, 1);
}

@keyframes typing {
    from {
        width: 0
    }
}

@keyframes blink {
    50% {
        border-color: transparent;
    }
}
</style>

<script setup lang="ts">

function showCV() {
    console.log('Are u dumb stupid?');
}

</script>