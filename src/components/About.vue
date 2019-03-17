<template lang="pug">
  .about-container
    .intro
      h2
        | Hello, My name is Ben.
      h2
        | Thanks for visiting my site!
    .about-text
      p
        | {{ text[0].text }}
      p
        | {{ text[1].text }}
      p
        | {{ text[2].text }}
      p
        | {{ text[3].text }}
</template>

<script lang="ts">
import Vue from 'vue'
const text = require("@/data/about-text.json")

export default Vue.extend({
  name: "about",
  data () {
    return {
      text: null
    }
  },
  mounted () {
    this.text = text
  }
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

.about-text {
  margin: 10px;
}
</style>


