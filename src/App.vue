<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/ProyectoCiclo3_Mesa de trabajo 1.png">
    <!---HelloWorld msg="bienvenido a la creación de app web con VUE"/----->
    <calculadora/>

    
  </div>
</template>

<script> /* logica de app, importación de componenetes*/
import Calculadora from './components/Calculadora.vue'
/*import HelloWorld from './components/HelloWorld.vue' /* ruta de componente*/

export default {
  name: 'App',
  components: {
    Calculadora /*se colocan los componentes importados */
    /*HelloWorld*/
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
