import { LogsComponent } from
'../../../../repositorios/integrador_recaudo/Cliente/Web/IntegradorRecaudo/src/app/modules/monitoring/logs/logs.component';
<template>
    <div class="contenedor-principal">
        <div class="titulo">
            <h1>#habilidades</h1>
            <div class="logos">
                <div class="logo">
                    <img src="../assets/angular-icon-1.svg" alt="Angular" />
                    <p>Angular</p>
                </div>
                <div class="logo">
                    <img src="../assets/html-1.svg" alt="Html" />
                    <p>Html</p>
                </div>
                <div class="logo">
                    <img src="../assets/vue-9.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>
                <div class="logo">
                    <img src="../assets/sass-1.svg" alt="Html" />
                    <p>Vue</p>
                </div>



            </div>
        </div>
    </div>
</template>

<style scoped>
.contenedor-principal {
    height: 100%;
    border: solid white;
    /* position: absolute; */
}

.logo {
    width: 10vw;
    height: 20vh;
    margin: 10px;
    display: flex;
    border-radius: 20px;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    background-color: #282828;
    transition: all 3s ease-in-out;
    -webkit-transition: all 0.2s linear;
    -moz-transition: all 0.2s linear;
    -o-transition: all 0.2s linear;
    transition: all 0.2s linear;
}

.logo:hover {
    background: rgb(35, 171, 124);
    background: linear-gradient(99deg, rgba(35, 171, 124, 1) 10%, rgba(17, 105, 75, 1) 36%, rgba(26, 73, 56, 1) 65%, rgba(40, 40, 40, 1) 98%);
    transition: background 2s ease-out;

}

.logo img {
    filter: grayscale(80%);
}

.logo:hover img {
    filter: grayscale(0%);
    transition: all .5s ease-in-out;

}

.logo p {
    color: #fafafa !important;
}

.logos {
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
}
</style>

<script setup lang="ts"></script>
