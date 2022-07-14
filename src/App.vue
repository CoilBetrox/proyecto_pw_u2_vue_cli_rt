<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <Contador2 titulo="titulo1" v-bind:inicio="valorInicio"/> -->
  <!-- <Contador2 titulo="titulo3" v-bind:inicio="6"/> -->
  <datosBasicos v-bind:nombre="tipo" v-bind:apellido="tipo" v-bind:correo="tipo"/>

  <h1 />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Contador from './components/contador.vue'
import Contador2 from './components/contador2.vue'
import datosBasicos from './components/datosBasicos.vue'



export default {
  name: 'App',
  data () {
        return{
           valorInicio: 26,
           tipo: 'Estudiante'
        }
  },
  components: {
    Contador,
    Contador2,
    datosBasicos
    
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
