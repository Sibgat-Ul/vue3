<template>
  <router-view/>
</template>

<script>
import Navbar from '@/components/Navbar.vue'

export default {
  components: {
    Navbar
  },
  setup() {
    const color = "42b9ac";
    const bg = "efefef"

    return {
      color,
      bg
    }
  },
}
</script>

<style>
@import url('./../../fa/css/all.min.css');

html, body {
  margin: 0px;
  padding: 0px;
  scroll-behavior: smooth;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 0px;
  margin: 0px;
}


</style>
