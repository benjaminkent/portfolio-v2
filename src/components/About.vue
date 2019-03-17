<template lang="pug">
  .about-container
    .intro
      h2
        | Hello, My name is Ben.
      h2
        | Thanks for visiting!
    .about-text
      p
        | I like being a software engineer!
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: "about"
})
</script>

<style lang="scss" scoped>
.about-container {
  background-color: #f4f4f4;
}

.intro {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;

  h2 {
    margin: 0;
    padding: 0;
  }
}
</style>


