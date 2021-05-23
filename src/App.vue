<template>
  <div class="text-3xl uppercase mb-8">
    <HelloWorld />
    <Contact />
  </div>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Contact
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
