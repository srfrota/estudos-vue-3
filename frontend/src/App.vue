<template>

<h2>Lista de users</h2>

<ul>
  <li v-for="user in users" :key="user.id">{{ user.firstName }}</li>
</ul>

</template>

<script>

import http from '@/services/http.js'

export default {
  data() {
  
  return{
    users: [],
  }
  },

  async mounted(){
    try {
      const {data} = await http.get('http://localhost:8000/api/users');
      
      this.users = data;
      
    } catch (error) {
      
    }
  }
};
</script>
