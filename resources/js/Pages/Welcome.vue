<script>
export default {
  name: 'home',
}
</script>

<script setup>
import DualityLayout from '@/Layouts/DualityLayout.vue';
import Section from './Partials/Section.vue';
import DuaLityInput from '@/Components/DualityInput.vue';
import DualityTextArea from '@/Components/DualityTextArea.vue';
import { useForm } from '@inertiajs/vue3';


defineProps({
  canLogin: Boolean,
  canRegister: Boolean,
  laravelVersion: String,
  phpVersion: String,
});

const form = useForm({
  name: '',
  email: '',
  message: '',
});



</script>

<template>
  <DualityLayout title="Duality">
    <div class="grid grid-rows-5 bg-duality w-full" id="grids">
      <!--Section 1-->
      <div>
        <Section>
          <template #col1>
            <div class="mt-36">
              <h1 class="text-white text-7xl font-roboto font-medium leading-tight mx-20">
                "El juego de los vínculos"
              </h1>

              <p class="text-duality-secondary font-sans mt-7 font-normal text-lg ml-24 lg:mr-72 ">
                Duality, es un juego de cartas diseñado para
                vivir lo experimentado por el psicólogo
                Arthur Aron en 1997 en el cual elaboró 36
                preguntas y las aplicó en diversas parejas de personas desconocidas. Esto motivó elacercamiento de
                vínculos entre personas, al punto de quedar enamoradas.
              </p>

              <div class="mt-9 flex justify-end mr-28">
                <p class="text-white font-sans font-medium">
                  <a href="#">Conocé más sobre Duality</a>
                </p>
              </div>
            </div>
          </template>

          <template #col2>
            <div class="h-screen overflow-hidden">
              <video src="@/assets/videos/duality.mp4" autoplay loop muted class="w-full"></video>
            </div>
          </template>
        </section>
      </div>
      <!--End Section 1-->

      <!--Section 2-->
      <div>
        <Section>
          <template #col1>
            <div class="parent">

              <img class="mancha w-fit" src="@/assets/images/mancha1.png" alt="mancha">

              <a href="#" class="boton w-full flex justify-end mt-36 mr-12">
                <div class="bg-white w-fit py-4 px-7 rounded-full">
                  <p class="font-sans text-sm font-medium">
                    <i class="fa fa-eye" aria-hidden="true"></i>
                    Descubre Duality
                  </p>
                </div>
              </a>

              <img class="sinfondo w-9/12" src="@/assets/images/sinfondo.webp" alt="sinfondo">

            </div>
          </template>

          <template #col2>
            <h1 class="text-white text-5xl font-roboto font-medium leading-tight mx-12 mt-52 mb-3">
              Pureza y neutralidad
            </h1>

            <p class="text-duality-secondary font-sans font-normal ml-12 lg:mr-72">
              Descubre
              Duality
              Pureza y neutralidad
              Duality te ofrece un mazo de cartas con un diseño puro y neutro pensado en el mensaje que posee cada una de
              las preguntas del experimento, lo que le permitirá tener conversaciones profundas con su compañero o
              invitado de juego respetando la manera autentica de realizar el experimento.
            </p>

            <div class="mt-8 ml-12">
              <a href="#">
                <div class="bg-white w-fit py-3 px-7 rounded-full">
                  <p class="font-sans  font-normal">
                    Consigue el tuyo aquí
                  </p>
                </div>
              </a>
            </div>
          </template>
        </Section>
      </div>
      <!--End Section 2-->

      <!--Section 3-->
      <div class="bg-white">
        <Section>
          <template #col1>
            <div class="h-screen overflow-hidden">
              <video src="@/assets/videos/humoblanco.mp4" autoplay loop muted class="w-full"></video>
            </div>
          </template>

          <template #col2>
            <div class="mt-36 ml-20">
              <h1 class="text-duality text-5xl font-roboto font-medium leading-tight mr-72">
                "Las mentes
                tienen dualidad,
                pero el alma un
                solo camino"
              </h1>

              <p class=" text-duality font-sans font-normal mt-12 mr-48">
                Las preguntas que se encuentran en las cartas tienen un orden secuencial de distintos grados de intensidad
                para conocerse mejor, empatizar con sus emociones, o para generar nuevos sentimientos...
              </p>

              <div class="mt-20 flex justify-start mr-28">
                <p class="text-duality font-sans font-medium">
                  <a href="#">Descubre más sobre las 36 preguntas</a>
                </p>
              </div>
            </div>
          </template>
        </Section>
      </div>
      <!--End Section 3-->

      <div>

      </div>


      <div class="bg-white">
        <Section>
          <template #col1>
            <div class="h-screen overflow-hidden">
              <video src="@/assets/videos/gente.mp4" autoplay loop muted class="w-full"></video>
            </div>
          </template>

          <template #col2>
            <div class="mt-32 ml-28 mr-48 sm:ml-16 sm:mt-16">
              <a href="#" class="text-duality text-5xl font-roboto font-medium leading-tight">
                Contáctanos
              </a>

              <p class="text-duality font-sans font-normal mt-8">
                Vendemos y hacemos cobertura de distribución y envió de pedidos online en Asunción y todo el Paraguay .
                Para
                compra o distribución de productos a su tienda no dude en dejarnos su mensaje.
              </p>

              <form action="">
                <div class="mt-8">
                  <DuaLityInput label="Nombre" v-model="form.name" />
                </div>

                <div class="mt-8">
                  <DuaLityInput label="Email" v-model="form.email" />
                </div>

                <div class="mt-8">
                  <DualityTextArea label="Mensaje(Opcional)" v-model="form.message" />
                </div>

                <div class="mt-8">
                  <button type="submit" class="bg-duality text-white font-sans font-medium py-6 px-14">
                    Enviar
                  </button>
                </div>
              </form>
            </div>
          </template>
        </Section>
      </div>
    </div>
  </DualityLayout>
</template>

<style scoped>
.parent {
  position: relative;
  top: 0;
  left: 0;
}

.mancha {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
}


.sinfondo {
  position: absolute;
  top: 150px;
  left: 30px;
}

.boton {
  position: absolute;
  top: 0;
  z-index: 1;
}
</style>