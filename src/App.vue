<template>
  <!--<img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>-->
  
  <mainPage/>
 

  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import mainPage from './components/Main.vue'


export default {
  name: 'App',
  components: {
    mainPage,
    

  }
}
</script>

<style>
/*
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  background-color: #2c3e50
}
  */
  /* main background-color: rgb(34, 24, 24) */
  * {
    margin: 30px;
    margin-top: 5px;
    background-color: black;
    color: white;
    letter-spacing: 4px;
  }





</style>
