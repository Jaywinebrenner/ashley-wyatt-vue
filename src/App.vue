<template>
  <div id="app">
    <Landing  v-if="HomeOrLanding === 'Landing'" />
    <Home v-if="HomeOrLanding === 'Home'" />


  </div>
</template>

<script>

import Landing from './components/Landing'
import Home from './components/Home'



export default {
  name: 'App',
  components: {
    Landing,
    Home

  },
  data() {
    return{
        HomeOrLanding: "Landing",
      

    }
  },
  methods: {

  }
}
</script>

<style>

</style>
