<template>
  <div id="app">
    <Navbar></Navbar>
    <Jumbotron></Jumbotron>
    <Card></Card>
    <Formulario></Formulario>
    <Footer></Footer>
  </div>
</template>

<script>
import Jumbotron from './components/Jumbotron.vue'
import Navbar from './components/Navbar.vue'
import Formulario from './components/Formulario.vue'
import Card from './components/Card.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Jumbotron, Navbar, Formulario, Card, Footer
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
  margin-top: 5px;
}
</style>
