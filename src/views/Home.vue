<template lang="pug">
  .home-container
    Header
    Hero
</template>

<script lang="ts">
import Vue from "vue";
import Header from "@/components/Header.vue"
import Hero from "@/components/Hero.vue"

export default Vue.extend({
  name: "home",
  components: {
    Header,
    Hero
  }
});
</script>
