<script setup>
  import Navbar from '@/components/NavBar.vue';
  import { RouterView} from 'vue-router';
</script>

<template>
  <Navbar />
  <div class="pt-16">
    <RouterView/>
  </div>
</template>