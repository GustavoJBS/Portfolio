<script setup lang="ts">
  import { RouterView } from 'vue-router'
  import NavigationButtons from './components/NavigationButtons.vue';
</script>

<template>
  <NavigationButtons />
    
  <RouterView class="mt-10" />
</template>