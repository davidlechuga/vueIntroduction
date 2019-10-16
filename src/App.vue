<template>
  <div id='app'>
    <navbar />
    <router-view />
  </div>
</template>

<script>
import Navbar from './components/Navbar'

export default {
  name: 'App',
  components: {
    Navbar
  }
}

</script>

<style>
#app h1 {
  color: #4fa4f3;
}
</style>
