<template>

  {{ count }}
  {{ userName }}

  <ul>
    <li v-for="user in users">{{ user.firstName }} - {{ user.age }}</li>
  </ul>

  <div v-if="showHeader">
    <Header />
  </div>

  <button v-on:click="showHeader = !showHeader">Toggle header</button>

  <h2>App</h2>

  <button v-on:click="count++">Add 1</button>

  <router-link to="/">Home</router-link>

  <router-link to="about">About</router-link>

  <router-view></router-view>

</template>

<script>

  import Header from "@/components/Header.vue";

export default {

  components: {Header},

  data(){
    return{
      count:0,
      showHeader:false,
      userName:'Eduardo Frota',
      users:[
        {
          firstName:'Eduardo',
          age:29
        },
        {
          firstName:'Eliane',
          age:29
        }
      ]
      
    }
  },

  mounted(){
    console.log(this.count);
  },

  updated(){
    console.log('update');
  }
}

</script>