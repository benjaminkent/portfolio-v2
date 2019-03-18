<template lang="pug">
  .carousel-container
    b-carousel(
      id="carousel-fade"
      style="text-shadow: 0px 0px 2px #000"
      :interval="2000"
      fade
      img-height="480"
    )
      b-carousel-slide
        img(
          slot="img"
          class="d-block img-fluid w-100"
          height="480"
          :src="require('../assets/beach-altered1.png')"
        )
        h1.creative
          | Creative
      b-carousel-slide
        img(
          slot="img"
          class="d-block img-fluid w-100"
          height="480"
          :src="require('../assets/beach-altered1.png')"
        )
        h1.innovative
          | Innovative
      b-carousel-slide
        img(
          slot="img"
          class="d-block img-fluid w-100"
          height="480"
          :src="require('../assets/beach-altered1.png')"
        )
        h1.forward-thinking
          | Dreamer
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: "carousel"
})
</script>

<style lang="scss" scoped>
.carousel-container {
  width: 100%;
}

.creative {
  font-family: 'Pacifico', cursive;
}

.innovative {
  font-family: 'Roboto Slab', serif;
}

.forward-thinking {
  font-family: 'Cabin', sans-serif;
}

h1 {
  font-size: 3rem;
  text-align: center;
  left: 100px;
  color: #fff;
  margin: 0 0 140px 0;
  text-shadow: 
    -1px -1px 0 #2d3319,
    1px -1px 0 #2d3319,
    -1px 1px 0 #2d3319,
    1px 1px 0 #2d3319;
}
</style>

