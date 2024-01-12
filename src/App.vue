<script setup lang="ts">
import { onMounted } from 'vue';
import EncabezadoHeader from './components/EncabezadoHeader.vue';
// import PresentationComponent from './components/PresentationComponent.vue';

onMounted(() => {

  const secciones = document.querySelectorAll("Section") as NodeListOf<HTMLElement>;

  console.log(secciones);

  const options: IntersectionObserverInit = {
    threshold: 0.7
  };

  function navcheck(entradas: IntersectionObserverEntry[]) {
    entradas.forEach((entrada) => {
      const nombreClase: String = entrada.target.className;
      const seccionActiva: HTMLElement | null = document.querySelector(`[data-page=${nombreClase}]`);
      const index = entrada.target.getAttribute('data-index');


    })
  };

  const observer = new IntersectionObserver(navcheck, options);

  secciones.forEach((seccion) => {
    observer.observe(seccion);
  })
});

</script>

<template>
  <header>
    <EncabezadoHeader></EncabezadoHeader>
  </header>

  <main>
    <section data-index="0" class="home">
      <!-- <PresentationComponent></PresentationComponent> -->
      HOME
    </section>

    <section data-index="1" class="about-me">
      ABOUT ME
    </section>

    <section data-index="2" class="habilities">
      HABILITIES
    </section>

    <section data-index="3" class="experience">
      EXPERIENCE
    </section>

    <section data-index="4" class="contact-me">
      CONTACT-ME
    </section>

  </main>
</template>

<style scoped>
section {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}


@media (min-width: 1024px) {
  /* header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  } */

  /* .logo {
    margin: 0 2rem 0 0;
  } */

  /* header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  } */
}
</style>
