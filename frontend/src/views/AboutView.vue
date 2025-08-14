<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script>

  export default{

    data(){
      return{
        interval: ""
      }
    },

    mounted() {
      this.interval = setInterval(()=> {
        console.log('mounted');
      },1000)
    },

    unmounted(){
      clearInterval(this.interval);
    }

  }

</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
