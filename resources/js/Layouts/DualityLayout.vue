<script>
export default {
  name: "DualityLayout"
}
</script>

<script setup>
import { ref } from 'vue';
import { Head, Link, router } from '@inertiajs/vue3';
import ApplicationMark from '@/Components/ApplicationMark.vue';
defineProps({
  title: String
})

const showingNavigationDropdown = ref(false);
</script>

<template>
  <div>

    <Head :title="title" />

    <div class="min-h-screen bg-duality">
      <nav class="bg-duality fixed w-full">
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
      <main >
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