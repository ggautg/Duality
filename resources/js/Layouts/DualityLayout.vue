<script>
export default {
  name: "DualityLayout"
}
</script>

<script setup>
import { Head, Link } from '@inertiajs/vue3';
import ApplicationMark from '@/Components/ApplicationMark.vue';
import { onBeforeMount, ref } from 'vue';

defineProps({
  title: String
})

const scrollPosition = ref(0);
const isAtTop = ref(true);

onBeforeMount(() => {
  window.addEventListener('scroll', handleScroll);
})

function handleScroll() {
  scrollPosition.value = window.scrollY;
  if (scrollPosition.value > 0) {
    isAtTop.value = false;
  } else if (scrollPosition.value == 0) {
    isAtTop.value = true;
  }
}




</script>

<template>
  <div>

    <Head :title="title" />

    <div class="min-h-screen bg-duality">
      <nav class="fixed w-full z-10" :class="{ 'bg-duality': !isAtTop, 'bg-none': isAtTop }">
        <!--Primary Navigation Menu-->
        <div class="max-w pt-9 pb-3" id="logohead">
          <div class="flex justify-between h-16">
            <div class="flex">
              <!-- Logo-->
              <div class="shrink-0 flex items-center px-1">
                <Link :href="route('home')">
                <ApplicationMark />
                </Link>
              </div>
            </div>

            <div class="grid grid-cols-4 pr-14 gap-10">
              <button class="text-white focus:outline-none">
                <i class="fas fa-desktop text-xl"></i>
              </button>

              <button class="text-white focus:outline-none">
                <i class="fas fa-search text-xl"></i>
              </button>

              <button class="text-white focus:outline-none">
                <i class="fas fa-shopping-bag text-xl"></i>
              </button>

              <button class="text-white focus:outline-none">
                <i class="fas fa-bars text-xl"></i>
              </button>
            </div>
          </div>
        </div>
      </nav>

      <!--Page Content-->
      <main clasS="z-0 absolute">
        <slot />

      </main>

    </div>
  </div>
</template>

<style scoped>
#logohead {
  padding-left: 2.85rem;
}
</style>