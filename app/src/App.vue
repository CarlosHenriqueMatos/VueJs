<!-- Qual a diferença de colocar o main.js lendo do App.vue e do HelloWorld.vue? e porque não roda quando eu faço o contrario
 -->
<template>
  <TheHeader v-if="showHeader"/>

  <div v-show = "showName">
    Nome: {{ firstName }}
    Sobrenome: {{ lastName }}
  </div>


    <div>
      {{ fullName }}
    </div>


  <div v-if="accessLevel==='admin'" > Perfil Administrador </div>

  <div v-else-if="accessLevel==='marketing'"> Marketing </div>
  
  <div v-else> User </div>


  <img alt="Vue logo" src="./assets/econocargo.png">

  <HelloWorld msg="Econocargo Gestão Colaborativa"/>
  <CicloDeVida/>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue';
import CicloDeVida from './components/CicloDeVida.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader,
    CicloDeVida,
  },
  data(){
    return{
      showHeader: true,
      firstName: 'Econocargo',
      lastName: 'Gestão Colaborativa',
      showName: false,
      accessLevel:'admin',
      user:{
        firstName: "Carlos",
        lastName: "Matos",
      }
      
    }
  },
  computed: {
    fullName(){
      return `${this.user.firstName} ${this.user.lastName}`
    },
  },
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
