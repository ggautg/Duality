<script>
export default {
  name: 'duality-home',
}
</script>

<script setup>
import DualityLayout from '@/Layouts/DualityLayout.vue';
import Section from './Partials/Section.vue';


defineProps({
  canLogin: Boolean,
  canRegister: Boolean,
  laravelVersion: String,
  phpVersion: String,
});
</script>

<template>
  <DualityLayout title="Duality">
    <Section>
      <template #col1>
        <h1 class="text-white text-5xl">
          "El juego de los vínculos"
        </h1>

        <p class="text-white">
          Duality, es un juego de cartas diseñado para vivir lo experimentado por el psicólogo Arthur Aron en 1997 en el
          cual elaboró 36 preguntas y las aplicó en diversas parejas de personas desconocidas. Esto motivó el acercamiento
          de vínculos entre personas, al punto de quedar enamoradas.
        </p>
      </template>

      <template #col2>
        <!--Insert video-->
        <img src="@/assets/images/duality.mp4" alt="">
      </template>
    </Section>
</DualityLayout></template>