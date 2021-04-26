<template>
  <div>
    <h1>{{ hellotext }}</h1>
    <h2>当前时间：{{ currentTime }}</h2>
  </div>
</template>

<script>
  export default {
    name: "helloworld",
    data(){
      return{
        hellotext: "hello world, this is a simple vue project.",
        currentTime: new Date()
      }
    },
    created(){
      this.getCurrentTime();
    },
    methods: {
      getCurrentTime(){
        setInterval(()=>{
          this.currentTime = new Date();
        }, 1000)
      }
    }
  }
</script>

<style scoped>

</style>