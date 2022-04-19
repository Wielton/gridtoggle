<template>
  <div id="app">
    <TweetsComp/>
  </div>
</template>

<script>
import TweetsComp from "@/components/TweetsComp.vue";

export default {
  name: 'App',
  components: {
    TweetsComp
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
