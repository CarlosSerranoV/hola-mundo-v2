<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <titulo texto="Mi banco dinamico"></titulo>
    <cuenta></cuenta>
  </div>

</template>

<script>
import titulo from "./components/Titulo";
import cuenta from "./components/Cuenta"

export default {
  name: 'app',
  components: {
    titulo,
    cuenta
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
