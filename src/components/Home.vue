<template>
  <div class="home">
      
      <div class="side-bar">
        <h4 @click="$parent.homeOrLanding = 'Landing'"><strong>Ashley Wyatt</strong></h4>
        <p v-bind:class="{ active: isActive('Apparel') }" @click="setActive('Apparel')" >Apparel</p>
        <p v-bind:class="{ active: isActive('Painting') }" @click="setActive('Painting')" >Painting</p>
        <p v-bind:class="{ active: isActive('Sculpture') }" @click="setActive('Sculpture')" >Sculpture</p>
        <p v-bind:class="{ active: isActive('About') }" @click="setActive('About')">About</p>
      </div>

      <div class="home-body">
        <Apparel v-if="page === 'Apparel'"/>
        <About v-if="page === 'About'"/>
        <Sculpture v-if="page === 'Sculpture'"/>
        <Painting v-if="page === 'Painting'"/>
      </div>
  </div>
</template>

<script>

import Apparel from './Apparel.vue'
import About from './About.vue'
import Painting from './Painting.vue'
import Sculpture from './Sculpture.vue'

export default {
  name: 'Home',
  components: {
    Apparel,
    About, 
    Painting,
    Sculpture
  },
  props: {

  },
  data() {
      return{
         page: 'Apparel', 
      }
  },
  computed: {

  },
  methods: {
    isActive(page) {
      if(page === this.page){
        console.log("page",page)
        return true
      }
      return false
    },
    setActive(menuItem) {
      console.log("click")
      this.page = menuItem
      this.activeItem = menuItem;
    }
  },
  mounted() {

  }
  
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Cabin+Sketch&display=swap');

.active {
  text-decoration: underline;
  pointer-events: none;
}

.active:hover {
  opacity: 1;
}

.home {
  display: flex;
}
.side-bar {
  width: 200px;
      padding: 10px;
}

.side-bar p, h4 {
  font-family: 'Cabin Sketch', cursive;
  cursor: pointer;

}

.side-bar p:hover {
  opacity: .3;
  transition: .3s;
  cursor: pointer;
}

.home-body{
  width: 100vw;

}

@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
  .home {
    flex-direction: column;
  }
  .side-bar {
    width: 100vw;
    text-align: center;
  }
}

</style>