<template lang="pug">
  .home-container
    Header
    img(src="@/assets/vue-logo.png")
</template>

<script lang="ts">
import Vue from "vue";
import Header from "@/components/Header.vue"

export default Vue.extend({
  name: "home",
  components: {
    Header
  }
});
</script>
