<template lang="pug">
  .about-container
    .intro
      h2
        | Hello! My name is Ben
      h2
        | Thanks for visiting my site
    .about-text
      p(v-for="paragraph in text")
        | {{ paragraph.text }}
    ul.contact
      li
        a.fa-phone(href="tel://17276199736" title="Call or Text")
          i.fas.fa-phone
      li
        a.fa-envelope(href="mailto:benjamin.k.jehl@gmail.com" title="Send an email")
          i.fas.fa-envelope
      li
        a.fa-linkedin-in(href="https://www.linkedin.com/in/benjaminkentjehl" title="LinkedIn" target="_blank")
          i.fab.fa-linkedin-in
      li
        a.fa-github(href="https://github.com/benjaminkent?tab=repositories" title="Github" target="_blank")
          i.fab.fa-github
      li
        a.fa-twitter(href="https://twitter.com/BenjaminJehl" title="Twitter" target="_blank")
          i.fab.fa-twitter
      li
        a.fa-instagram(href="https://www.instagram.com/benjaminkent7/" title="Instagram" target="_blank")
          i.fab.fa-instagram
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
.fa-instagram:hover {
  color: #7f00ff;
}

.fa-twitter:hover {
  color: #0000ff;
}

.fa-github:hover {
  color: #00ff00;
}

.fa-linkedin-in:hover {
  color: #cccc00;
}

.fa-envelope:hover {
  color: #ff5000;
}

.fa-phone:hover {
  color: #ff0000;
}

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
    font-size: 1.5rem;
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

.contact {
  margin-top: 20px;
}

ul  {
  margin-top: 30px;
  font-size: 25px;
  display: flex;
  justify-content: center;
  list-style-type: none;
  padding: 0;
}

a {
  color: #0f0f0f;
}

svg {
  margin: 0 8px;
}
</style>


