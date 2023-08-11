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
      <nav class="bg-duality border-b ">
        <!--Primary Navigation Menu-->
        <div class="max-w pt-9 pb-2 pl-12">
          <div class="flex justify-between h-16">
            <div class="flex">
              <!-- Logo-->
              <div class="shrink-0 flex items-center px-1">
                <Link :href="route('home')">
                <ApplicationMark/>
                </Link>
              </div>
            </div>

            <div class="grid grid-cols-4 gap-4">
              <button class="text-white focus:outline-none">
                <i class="fas fa-desktop text-2xl"></i>
              </button>

              <button class="text-white focus:outline-none">
                <i class="fas fa-search text-2xl"></i>
              </button>

              <button class="text-white focus:outline-none">
                <i class="fas fa-shopping-bag text-2xl"></i>
              </button>

              <button class="text-white focus:outline-none mr-6">
                <i class="fas fa-bars text-2xl"></i>
              </button>
            </div>
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>