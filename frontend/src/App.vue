<template>

<div v-if="showView">
  
  <Header />

</div>

<button v-on:click="showView = !showView">Apresentar Header</button>

<br>

  {{ count }}

  {{ userName }}

  {{ myName }}

  <ul>
    <li v-for="user in users">{{ user.firstName }} - {{ user.age }}</li>
  </ul>
  
  <button v-on:click="count++">Add 1</button>
  
  <h2>App</h2>

  <router-link to="/">Home</router-link>
  <router-link to="/about">About</router-link>

  <router-view></router-view>

</template>


<script setup>
import { onMounted, onUpdated, reactive, ref } from 'vue';

  import Header from '@/components/Header.vue';

  // const routes = {
  //   '/': Header
  // }

  const count = ref(0);
  const userName = ref('Eduardo')

  const users = reactive([
    {
      firstName:'Eduardo',
      age:29
    },
    {
      firstName:'Eliane',
      age:29
    }
  ])

  let myName = ref('Eduardo');

  const showView = ref(false)

  onMounted(() => {
    console.log(users);
  })

  onUpdated(() => {
    console.log('update');
  })


</script>