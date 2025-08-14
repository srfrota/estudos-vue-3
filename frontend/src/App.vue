<template>

<div v-if="showView">
  
  <Header />

</div>

<button v-on:click="showView = !showView">Apresentar Header</button>

<br>


  {{ count }}
  
  <button v-on:click="count++">Add 1</button>
  
  <h2>App</h2>

  <router-link to="/">Home</router-link>
  <router-link to="/about">About</router-link>

  <router-view></router-view>

</template>


<script setup>
import { onMounted, onUpdated, ref } from 'vue';

  import Header from '@/components/Header.vue';

  // const routes = {
  //   '/': Header
  // }

  const count = ref(0);

  const showView = ref(false)

  onMounted(() => {
    console.log('mounted');
  })

  onUpdated(() => {
    console.log('update');
  })


</script>