<!-- <script setup>
import { RouterLink, RouterView } from 'vue-router'
</script> -->

<template>
  <h2 id="my-app">App</h2>

  <p id="teste">Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque, voluptatibus. Mollitia iusto aliquid consectetur quae voluptas minima blanditiis perspiciatis error repellat, temporibus sit officiis doloremque odio praesentium, repellendus at omnis.</p>

  <header>
    <div class="wrapper">
      <nav>
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/products">Products</router-link>
      </nav>
    </div>
  </header>

  <router-view />
</template>

<style scoped>
  /* @import "@/assets/app.css"; */

#my-app{
  background-color: aqua;
  color: black;
}

#teste{
  color: red;
}

</style>
