<script setup>
import Navigate from './components/Navigate.vue'
import ContentSection from './components/Section.vue'
</script>

<template>
  <Navigate />
  <ContentSection id="about" >
    <h1 class="section-title">Qui-suis-je ?</h1>
    <p class="section-paragraph">Je m'appelle Cathy, j'ai 25 ans et je suis une photographe amateur passionnée. Depuis que j'ai eu mon premier appareil photo, j'ai commencé à explorer le monde autour de moi avec un œil attentif et créatif. La photographie m'offre une chance unique de capturer des moments fugaces et de les transformer en souvenirs durables.</p>
    <p class="section-paragraph">En tant que photographe, j'aime explorer différents styles et techniques pour trouver celui qui convient le mieux à chaque sujet. Je suis particulièrement fascinée par la nature, les paysages, les portraits et la photographie de rue. J'adore capturer des moments de la vie quotidienne et des émotions authentiques, en créant des images qui racontent des histoires et qui inspirent les gens.</p>
    <p class="section-paragraph">Je suis heureuse de partager mes photos avec les autres et j'espère que mes images pourront susciter des émotions et des réflexions chez ceux qui les regardent. Je crois que la photographie est un moyen puissant de communiquer et de connecter les gens, et je suis impatiente de continuer à explorer cet art fascinant.</p>
  </ContentSection>
  <ContentSection id="portfolio" />
  <ContentSection id="offer" />
  <ContentSection id="contact" />
</template>

<style scoped>
  .section-paragraph {
    margin: 2rem 0;
  }
</style>
