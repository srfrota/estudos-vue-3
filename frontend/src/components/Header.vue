<template>
  <h2>Header</h2>
</template>

<script setup>
import { onUnmounted } from 'vue';


  onUnmounted(() => {
    console.log('unmounted no Header');
    
  })

</script>

<style scoped>

</style>
