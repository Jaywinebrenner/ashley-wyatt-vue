<template>
  <div class="apparel">
      <h1>Apparel</h1>
      <img src="../media/ashley1.jpg"/>
      <img src="../media/ashley2.jpg"/>
      <img src="../media/ashley3.jpg"/>
      <img src="../media/ashley4.jpg"/>
      <img src="../media/ashley5.jpg"/>
      <img src="../media/ashley6.jpg"/>
      <img src="../media/ashley7.jpg"/>
 
  </div>
</template>

<script>



export default {
  name: 'Apparel',
  components: {
      
  },
  data() {
      return{
         
      }
  },
  methods: {

  }
  
}
</script>

<style>

.apparel img {
  width: 200px;
  padding: 5px;
}

@media only screen and (max-width: 600px) {
  .apparel img {
    display: block;
    margin: 0 auto;
        width: 90vw;

  }
}

</style>