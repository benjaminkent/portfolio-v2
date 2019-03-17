<template lang="pug">
  .header-container
    header.header
      .logo-container
        <i class="fas fa-elephant"></i>
      nav.big-nav
        ul.nav-list
          li.big-header
            a(href="#")
              | Home
          li.big-header
            a(href="#")
              | Portfolio
          li.big-header
            a(href="#")
              | Resume
          li.big-header
            a(href="#")
              | Blog
      .hamburger(v-on:click="hide = !hide")
        .hamburger-line
        .hamburger-line
        .hamburger-line
    .pop-menu(:class="{ hide: hide }")
      .pop-extra(v-on:click="hide = !hide")
      .pop-flex-container
        .pop-header(v-on:click="hide = !hide")
          p.pop-menu-x
            | X
        nav(v-on:click="hide = !hide")
          ul
            li.link
              | Home
            li.link
              | Portfolio
            li.link
              | Resume
            li.link
              | Blog
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: "Header",
  data: function () {
    return {
      hide: true
    }
  }
})
</script>


<style lang="scss" scoped>
.header-container {
  font-family: 'Raleway', sans-serif;
}

.logo {
  height: 2.5rem;
  margin: 22px 0 0 1rem;
}

.logo-right {
  height: 2.5rem;
  margin: 2rem 0 1.5rem 5px;
}

.header {
  position: fixed;
  width: 100%;
  background-color: #0f0f0f;
  color: white;
  box-shadow: 0px 0.5px 5px #0f0f0f;
  z-index: 2;
  display: flex;
  justify-content: space-between;
  opacity: 0.9;
}

.nav-list {
  list-style-type: none;
  display: flex;
  margin: 12px 0 0 0;
  padding: 0 0 12px 0;
  justify-content: space-around;

  a {
    color: #fff;
    text-decoration: none;
    font-size: 1rem;
  }
}

.big-header {
  margin: 0 1rem;
}

.fa-elephant {
  font-size: 1.2rem;
  margin: 12px 0 0 20px;
}

.hamburger {
  margin: 8px 20px 8px 0;
  cursor: pointer;
}

.hamburger-line {
  border: 1px solid #fff;
  width: 25px;
  margin: 5px;
}

.pop-header {
  display: flex;
  background-color: #0f0f0f;
  width: 100%;
}

.pop-logo {
  height: 2.5rem;
  margin: 22px 0 0 5px;
}

.pop-menu {
  position: fixed;
  right: 0;
  width: 100%;
  top: 0;
  height: 100%;
  color: #fff;
  opacity: 0.93;
  z-index: 3;
  transition: 0.2s ease-in-out;
  display: flex;

  .pop-menu-x {
    position: absolute;
    right: 23.5px;
    font-size: 1.8rem;
    margin-top: 4px;
    margin-right: 6px;
    cursor: pointer;
    color: #fff;
  }

  nav {
    margin: 0;
    background-color: #0f0f0f;
    width: 100%;
    height: 100%;
    padding-top: 20px;

    ul {
      padding-left: 30px;
      margin-top: 25px;
    }

    li {
      list-style: none;
      font-size: 1.2rem;
      padding: 1.5rem 0;
    }
  }
}

.pop-flex-container {
  width: 75%;
  display: flex;
  flex-direction: column;
}

.pop-extra {
  width: 25%;
  background-color: #00000035;
}

.hide {
  margin-right: -100%;
}

@media (max-width: 550px) {
  .big-header {
    display: none;
  }

  .logo-right {
    display: none;
  }
}

@media(min-width: 551px) {
  .hamburger {
    display: none;
  }
}

@media (min-width: 627px) {
  .big-header {
    margin: 0 1.7rem;
  }
}
</style>