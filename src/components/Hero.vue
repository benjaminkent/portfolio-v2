<template lang="pug">
  .hero-container
    Carousel
</template>

<script lang="ts">
import Vue from 'vue'
import Carousel from "@/components/Carousel.vue"

export default Vue.extend({
  name: "hero",
  components: { Carousel }
})
</script>

