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
    <div class="grid grid-rows-2">
      <Section>
        <template #col1>
          <div class="px-20 py-5">
            <h1 class="text-white text-7xl font-roboto font-medium leading-tight">
              <h1 class="vlt-heading">
                "El juego de los vínculos"
              </h1>
            </h1>

            <p class="text-duality-secondary font-sans py-7 pr-52 font-normal text-lg">
              Duality, es un juego de cartas diseñado para vivir lo experimentado por el psicólogo Arthur Aron en 1997 en
              el
              cual elaboró 36 preguntas y las aplicó en diversas parejas de personas desconocidas. Esto motivó el
              acercamiento
              de vínculos entre personas, al punto de quedar enamoradas.
            </p>
          </div>

          <div class="flex justify-end pr-36">
            <p class="text-white font-sans font-medium">
              <a href="">Conocé más sobre Duality</a>
            </p>
          </div>
        </template>

        <template #col2>
          <video src="@/assets/videos/duality.mp4" autoplay loop muted class="h-screen"></video>

        </template>
      </section>

      <div>
        <Section></Section>
      </div>
    </div>
  </DualityLayout>
</template>