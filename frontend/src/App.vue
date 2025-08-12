<!-- <script setup>
import { RouterLink, RouterView } from 'vue-router'
</script> -->

<template>

  <Header />

  <button v-on:click="add">Add {{ count }}</button>

  <h2>App</h2>

  <Footer />


</template>

<!-- // Options api -->
<!-- <script>
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue'

export default{
  components:{Header, Footer},
  
  data(){
    return{
      count:0
    }
  },

  methods:{
    add(){
      this.count++
    }
  }
}
</script> -->

<!-- Composition api -->
<script setup>
import { ref } from 'vue';

import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';

  const count = ref(0);

  function add(){
    count.value++
  }


</script>

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
