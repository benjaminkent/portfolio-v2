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
    SocialMedia
    ul.contact
      li
        i.fas.fa-phone
      li
        i.fas.fa-envelope
      li
        i.fab.fa-linkedin-in
      li
        i.fab.fa-github
      li
        i.fab.fa-twitter
      li
        i.fab.fa-instagram

</template>

<script lang="ts">
import Vue from 'vue'
import SocialMedia from "@/components/SocialMedia.vue"
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
  },
  components: { SocialMedia }
})
</script>

<style lang="scss" scoped>
.about-container {
  color: #0f0f0f;
  background-image: -webkit-repeating-radial-gradient(center center, rgba(0,0,0,.1), rgba(0,0,0,.1) 1px, transparent 1px, transparent 100%);
  background-image: -moz-repeating-radial-gradient(center center, rgba(0,0,0,.1), rgba(0,0,0,.1) 1px, transparent 1px, transparent 100%);
  background-image: -ms-repeating-radial-gradient(center center, rgba(0,0,0,.1), rgba(0,0,0,.1) 1px, transparent 1px, transparent 100%);
  background-image: repeating-radial-gradient(center center, rgba(0,0,0,.1), rgba(0,0,0,.1) 1px, transparent 1px, transparent 100%);
  -webkit-background-size: 3px 3px;
  -moz-background-size: 3px 3px;
  background-size: 3px 3px;
  padding-bottom: 20px;
}

.intro {
  padding: 20px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  font-family: 'Roboto Slab', serif;

  h2 {
    margin: 0;
    padding: 0;
  }
}

.about-text {
  margin: 0 20px 20px 20px;
  font-family: 'Roboto Slab', serif;
}

p {
  margin: 0 0 15px 0;
  padding: 0;
}

ul  {
  margin-top: 30px;
  font-size: 25px;
  display: flex;
  justify-content: center;
  list-style-type: none;
  padding: 0;
}

svg {
  margin: 0 8px;
  color: #0f0f0f;
}
</style>


