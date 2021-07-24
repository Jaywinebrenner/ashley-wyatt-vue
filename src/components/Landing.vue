<template>
  <div class="landing">
    <h1 @click="$parent.HomeOrLanding = 'Home'">Ashley Wyatt</h1>

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

.landing {
  display: flex;
  justify-content: center;
  align-items: center;
}

.landing h1:hover {
  opacity: .3;
  transition: .3s;
  cursor: pointer;
}

</style>