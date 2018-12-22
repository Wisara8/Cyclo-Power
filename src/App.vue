<template>
  <div id="app">
    <Cyclopower msg="Welcome to Cyclopower"/>
  </div>
</template>

<script>
import Cyclopower from './components/Cyclopower.vue'

require('./assets/css/main.css')
require('./assets/css/nav.css')
require('./assets/css/normalize.css')

export default {
  name: 'app',
  components: {
    Cyclopower
  }
}
</script>

<style>
#app {
  font-family: "Lucida Sans", Verdana, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;

}
</style>
