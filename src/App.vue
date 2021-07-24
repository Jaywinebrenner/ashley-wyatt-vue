<template>
  <div id="app">
    <Landing  v-if="homeOrLanding === 'Landing'" />
    <Home v-if="homeOrLanding === 'Home'" />


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
        homeOrLanding: "Landing",
    }
  },
  methods: {

  }
}
</script>

<style>

body, html {
  height: 100%;
}

@media only screen and (max-width: 600px) {
  body {
    margin: 0px;
    padding: 0px;
  }

}

    

</style>
