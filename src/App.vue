<script setup lang="ts">
import { onMounted } from 'vue';
import EncabezadoHeader from './components/EncabezadoHeader.vue';
import HomeView from './components/HomeView.vue';
import PresentationComponent from './components/PresentationComponent.vue';




onMounted(() => {

  const secciones = document.querySelectorAll("Section") as NodeListOf<HTMLElement>;
  const indicador = document.querySelector(".indicator") as HTMLElement | null;


  const options: IntersectionObserverInit = {
    threshold: 0.7
  };


  function navcheck(entradas: IntersectionObserverEntry[]) {
    entradas.forEach((entrada) => {
      const nombreClase: String = entrada.target.className;
      const seccionActiva: HTMLElement | null = document.querySelector(`[data-page=${nombreClase}]`);
      const coords = seccionActiva!.getBoundingClientRect();
      // const index = entrada.target.getAttribute('data-index');

      const directs = {
        height: coords?.height,
        width: coords?.width,
        top: coords?.top + 30,
        left: coords?.left,
        right: coords?.right,
      };

      console.log(entrada);

      if (entrada.isIntersecting) {
        // console.log(seccionActiva);
        // console.log(indicador);
        indicador?.style.setProperty(
          'left', `${directs.left}px`
        );
        indicador?.style.setProperty(
          'right', `${directs.right}px`
        );
        indicador?.style.setProperty(
          'top', `${directs.top}px`
        );
        indicador?.style.setProperty(
          'width', `${directs.width}px`
        );

      }

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
    <section ref="home" id="home" data-index="0" class="home">
      <HomeView></HomeView>
    </section>

    <section ref="about-me" data-index="1" class="about-me">
      <PresentationComponent></PresentationComponent>
    </section>

    <section ref="habilities" data-index="2" class="habilities">
      HABILITIES
    </section>

    <section ref="experience" data-index="3" class="experience">
      EXPERIENCE
    </section>

    <section ref="contact" data-index="4" class="contact-me">
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
  z-index: -1;
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
