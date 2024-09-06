import { LogsComponent } from
'../../../../repositorios/integrador_recaudo/Cliente/Web/IntegradorRecaudo/src/app/modules/monitoring/logs/logs.component';
<template>
  <div class="contenedor-principal">
    <div class="titulo">
      <h1>#habilidades</h1>
    </div>
    <div class="contenedor-logos">
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
          <img src="../assets/vue-9.svg" alt="Vue" />
          <p>Vue</p>
        </div>
        <div class="logo">
          <img src="../assets/sass-1.svg" alt="Sass" />
          <p>Sass</p>
        </div>
        <div class="logo">
          <img src="../assets/nodejs-icon.svg" alt="Nodejs" />
          <p>NodeJS</p>
        </div>
        <div class="logo">
          <img src="../assets/figma-icon.svg" alt="Figma" />
          <p>Figma</p>
        </div>
        <div class="logo">
          <img src="../assets/logo-javascript.svg" alt="Javascript" />
          <p>JavaScript</p>
        </div>
        <div class="logo">
          <img src="../assets/css-3.svg" alt="Css" />
          <p>Css</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.contenedor-principal {
  height: 100%;
  width: 100%;
  /* border: solid white; */
  position: absolute;
}

.contenedor-logos {
  /* border: white solid; */
  display: flex;
  justify-content: center;
  margin-top: 20vh;
}

.logos {
  /* border: yellow solid; */
  width: 70vw;
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-wrap: wrap;
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
  background: #282828;
  transition: background 1s linear;
}

.logo:hover {
  background: linear-gradient(
    99deg,
    rgba(35, 171, 124, 1) 10%,
    rgba(17, 105, 75, 1) 36%,
    rgba(26, 73, 56, 1) 65%,
    rgba(40, 40, 40, 1) 98%
  );
}

.logo img {
  filter: grayscale(80%);
}

.logo:hover img {
  filter: grayscale(0%);
  transition: all 0.5s ease-in-out;
}

.logo p {
  color: #fafafa !important;
}
</style>

<script setup lang="ts"></script>
