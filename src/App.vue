<template lang="pug">
  #app
    Home
    h1
      | this is my app.. Portfolio version 2 baby!
</template>

<script lang="ts">
import Vue from 'vue'
import Home from '@/views/Home.vue'

export default Vue.extend({
  name: 'App',
  components: {
    Home
  }
})
</script>


<style lang="scss">
body {
  margin: 0;
}
</style>
