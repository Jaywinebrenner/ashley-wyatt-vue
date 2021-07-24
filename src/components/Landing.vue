<template>
  <div class="landing">
    <h1 @click="$parent.homeOrLanding = 'Home'">Ashley Wyatt</h1>

  </div>
</template>

<script>


export default {
  name: 'Landing',
  components: {

  },
  props: {
  }
  
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cabin+Sketch&display=swap');
.landing {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 90vh;
}
.landing h1 {
  font-family: 'Cabin Sketch', cursive;

}

.landing h1:hover {
  opacity: .3;
  transition: .3s;
  cursor: pointer;
}

</style>