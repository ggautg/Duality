<script>
export default {
  name: 'duality-home',
}
</script>

<script setup>
import DualityLayout from '@/Layouts/DualityLayout.vue';

defineProps({
  canLogin: Boolean,
  canRegister: Boolean,
  laravelVersion: String,
  phpVersion: String,
});
</script>

<template>
  <DualityLayout title="Duality"></DualityLayout>
</template>