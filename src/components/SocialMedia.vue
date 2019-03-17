<template lang="pug">
  ul
    li
      a(href="tel://17276199736")
        i.fas.fa-phone
     
</template>

<script lang="ts">
import Vue from 'vue'
const icons = require("@/data/social-media.json")

export default Vue.extend({
  name: "social-media",
  data () {
    return {
      icons: null
    }
  },
  mounted () {
    this.icons = icons
  }
})
</script>
