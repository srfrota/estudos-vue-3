<template>

  <div v-if="showHeader">
    <Header />
  </div>

  <button v-on:click="showHeader = !showHeader">Toggle header</button>

  <h2>App</h2>

  <button v-on:click="count++">Add 1</button>

  <router-link to="/">Home</router-link>

  <router-link to="about">About</router-link>

  <router-view></router-view>

  {{ count }}

</template>

<script>

  import Header from "@/components/Header.vue";

export default {

  components: {Header},

  data(){
    return{
      count:0,
      showHeader:false
    }
  },

  mounted(){
    console.log('mounted');
  },

  updated(){
    console.log('update');
  }
}

</script>