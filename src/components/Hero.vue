<template lang="pug">
  .hero-container
    .hero-text
      h1.hero-welcome
        | Creative
      h1.hill
        | Innovative
      h1
        | Forward Thinking
    .hero-image
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: "hero"  
})
</script>

<style lang="scss" scoped>
.hero-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.hero-image {
  margin-top: 30px;
  padding-top: 250px;
  background: url("../assets/beach-altered1.png");
  height: 290px;
  background-position: center center;
  background-size: cover;
  width: 100vw;
  z-index: -1000;
}

.hero-text {
  margin-top: 90px;
  position: absolute;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  height: 450px;
}

h1 {
  font-family: 'Raleway', sans-serif;
  font-size: 3rem;
  text-align: center;
  left: 100px;
  color: #fff;
  margin: 0;
}
</style>
