<template>
  <div class="home">
      

      <div class="side-bar">
        <p @click="$parent.HomeOrLanding = 'Landing'">Landing</p>
        <p @click="page = 'Apparel'">Apparel</p>
        <p>Painting</p>
        <p>Sculture</p>
        <p @click="page = 'About'">About</p>
      </div>

      <div class="home-body">
        <Apparel v-if="page === 'Apparel'"/>
        <About v-if="page === 'About'"/>

      </div>
  </div>
</template>

<script>

import Apparel from './Apparel.vue'
import About from './About.vue'

export default {
  name: 'Home',
  components: {
    Apparel,
    About 
  },
  props: {

  },
  data() {
      return{
         page: null
      }
  },
  methods: {

  }
  
}
</script>

<style>

.home {
  display: flex;
}
.side-bar {
  width: 200px;
}

.side-bar p:hover {
  opacity: .3;
  transition: .3s;
  cursor: pointer;
}

.home-body{
  width: 100vw;

}

</style>