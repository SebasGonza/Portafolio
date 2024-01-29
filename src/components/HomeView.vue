<template>
    <div class="decoraciones">
        <div class="consola3">
            <img src="../assets/consola3.svg" height="100" />
        </div>
        <div class="consola1">
            <img src="../assets/consola1.svg" />
        </div>
        <div class="consola2">
            <img src="../assets/consola2.svg" />
        </div>

        <div class="bola1">
            <img src="../assets/bola1.svg" height="10" />
        </div>
    </div>


    <div class="presentacion">
        <span>Hola mi nombre es:</span>
        <span class="nombre">
            Sebastian Gonzalez Romero
        </span>

    </div>
</template>

<style >
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

.bola1 {
    position: absolute;
    top: 5rem;
    right: 2rem;
    z-index: -1;
}

.nombre {
    color: hsla(160, 100%, 37%, 1);
    display: block;
    font-family: monospace;
    font-size: 2rem;
    white-space: nowrap;
    border-right: 4px solid;
    width: 442px;
    animation: typing 1.5s steps(12), blink .5s infinite step-end alternate;
    overflow: hidden;
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