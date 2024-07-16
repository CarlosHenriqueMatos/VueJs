<template>
  <TheHeader v-if="showHeader"/>

  <div v-show = "showName">
    Nome: {{ firstName }}
    Sobrenome: {{ lastName }}
  </div>

  <div v-if="accessLevel==='admin'" > Admin </div>

  <div v-else-if="accessLevel==='marketing'"> Marketing </div>
  
  <div v-else> User </div>


  <img alt="Vue logo" src="./assets/capa.jpg" height="244px" width="326px">

  <HelloWorld msg="Brothers page"/>


</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader
  },
  data(){
    return{
      showHeader: true,
      firstName: 'Carlos',
      lastName: 'Matos',
      showName: false,
      accessLevel:'admin'
      
    }
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
