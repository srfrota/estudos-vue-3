<template>

  <span v-if="showName">Mostrar o nome</span>

  <div :class="teste">teste</div>

  <img :src="image">


  <ul>
    <template v-for="(user, key) in users" :key="user.id">
      <li v-if="user.is_admin == 1">
          {{ key }} - {{ user.firstName }}
      </li>
    </template>
  </ul>



</template>

<script>

export default {

data(){

  return{

    image: 'https://picsum.photos/200/300',

    teste:'class',

    showName:false,

    user:{name:'Eduardo', age:29},

    users:[
      {
        id:1,
        firstName:'Alexandre',
        age:40,
        is_admin:1
      },
      {
        id:2,
        firstName:'Maria',
        age:40,
        is_admin:0
      },
      {
        id:3,
        firstName:'João',
        age:40,
        is_admin:0
      },
      {
        id:3,
        firstName:'Pedro',
        age:40,
        is_admin:1
      },
    ]
  }

}

}

</script>