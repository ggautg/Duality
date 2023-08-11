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
    <div class="grid grid-rows-2 bg-duality" id="grids">
      <div>
        <Section>
          <template #col1>
            <div class="py-36">
              <h1 class="text-white text-7xl font-roboto font-medium leading-tight px-20">
                <h1 class="vlt-heading">
                  "El juego de los vínculos"
                </h1>
              </h1>

              <p class="text-duality-secondary font-sans pt-7 font-normal text-lg pl-24 lg:pr-72 ">
                Duality, es un juego de cartas diseñado para
                vivir lo experimentado por el psicólogo
                Arthur Aron en 1997 en el cual elaboró 36
                preguntas y las aplicó en diversas parejas de personas desconocidas. Esto motivó elacercamiento de
                vínculos entre personas, al punto de quedar enamoradas.
              </p>

              <div class="pt-9 flex justify-end pr-28">
                <p class="text-white font-sans font-medium">
                  <a href="">Conocé más sobre Duality</a>
                </p>
              </div>
            </div>
          </template>

          <template #col2>
            <div class="bg-red-300 h-screen overflow-hidden">
              <video src="@/assets/videos/duality.mp4" autoplay loop muted class="w-full"></video>
            </div>
          </template>
        </section>
      </div>

      <div class="bg-black">
        <Section>
          <template #col1>
            <div class="absolute h-screen overflow-hidden" id="fontoimprovisado">
              <img src="@/assets/images/sinfondo.webp" alt="sinfondo" class="h-screen">
            </div>
            
            <div class="relative w-full flex justify-end pr-32 pt-32">
                <div class=" bg-white w-fit p-3 rounded-full flex">
                  <p>
                    <a href="" class="font-sans text-sm">
                      <i class="fa fa-eye" aria-hidden="true"></i>
                      Descubre Duality
                    </a>
                  </p>
                </div>
              </div>
          </template>

          <template #col2>
            <div class="h-screen bg-green-300">

            </div>
          </template>
        </Section>
      </div>
    </div>
  </DualityLayout>
</template>

<style scoped>
#fontoimprovisado{
  background-image: url("@/assets/images/mancha1.png");
}
</style>