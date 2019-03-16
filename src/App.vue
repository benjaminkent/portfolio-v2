<template lang="pug">
  #app
    router-view
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
@import url('https://fonts.googleapis.com/css?family=Raleway:400,700');

body {
  margin: 0;
}

h1 {
  font-family: 'Raleway', sans-serif;
}
</style>
