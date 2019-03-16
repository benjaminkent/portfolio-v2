<template lang="pug">
  .header-container
    header.header
      .logo-container
        img.logo(src="@/assets/logo.png" alt="logo")
        img.logo-right(src="@/assets/logo.png" alt="logo")
      nav.big-nav
        ul.nav-list
          li.big-header
            a(href="#")
              | Home
          li.big-header
            a(href="#")
              | About
          li.big-header
            a(href="#")
              | in the Hill
      .hamburger(v-on:click="hide = !hide")
        .hamburger-line
        .hamburger-line
        .hamburger-line
    .pop-menu(:class="{ hide: hide }")
      .pop-extra(v-on:click="hide = !hide")
      .pop-flex-container
        .pop-header(v-on:click="hide = !hide")
          img.pop-logo(src="@/assets/logo.png" alt="logo")
          p.pop-menu-x
            | X
        nav(v-on:click="hide = !hide")
          ul
            li.link
              | Home
            li.link
              | About
            li.link
              | in the Hill
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
  font-family: "Major Mono Display", monospace;
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
  background-color: black;
  color: white;
  box-shadow: 0px 0.5px 5px black;
  z-index: 2;
  display: flex;
  justify-content: space-between;
}

.nav-list {
  list-style-type: none;
  display: flex;
  margin: 2.5rem 0 0 0;
  padding: 0;
  justify-content: space-around;

  a {
    color: #59E0FF;
    text-decoration: none;
    font-size: 1.3rem;
  }
}

.big-header {
  margin: 0 1rem;
}

.hamburger {
  margin: 27px 20px 27px 0;
  cursor: pointer;
}

.hamburger-line {
  border: 1.5px solid #59E0FF;
  width: 25px;
  margin: 5px;
}

.pop-header {
  display: flex;
  background-color: #000;
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
  color: #59E0FF;
  opacity: 0.93;
  z-index: 3;
  transition: 0.2s ease-in-out;
  display: flex;

  .pop-menu-x {
    position: absolute;
    right: 23.5px;
    font-size: 1.8rem;
    margin-top: 26px;
    margin-right: 4px;
    cursor: pointer;
    color: #59E0FF;
  }

  nav {
    margin: 0;
    background-color: #000;
    width: 100%;
    height: 100%;
    padding-top: 20px;

    ul {
      padding-left: 30px;
    }

    li {
      list-style: none;
      font-size: 1.5rem;
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

@media (max-width: 559px) {
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