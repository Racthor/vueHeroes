<template>
  <div id="app">
    <Main titre="Bienvenu dans la première version de vueHeroes" version="alpha 0.1"/>
    <p>
    	------------------------------------------------------------------------------------------------------------------------------------------------------------<br/>
    	                             V On garde le HelloWorld juste pour comprendre vitef comment ça marche, mais en vrai on s'en balec frère V
    	------------------------------------------------------------------------------------------------------------------------------------------------------------<br/>
    </p>
    <img src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Main 	  from './components/Main.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Main
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
