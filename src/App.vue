<template>
  <div id="app">
    <Nav />
    <Sidenav />
    <Billing msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Billing from './components/Billing.vue'
import Nav from './components/Nav.vue'
import Sidenav from './components/Sidenav.vue'

export default {
  name: 'App',
  components: {
    Billing,
    Sidenav,
    Nav,
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
  background-color: #F7F8FA;
  overflow: hidden;
}
</style>
