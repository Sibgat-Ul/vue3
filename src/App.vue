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
  height: 100%;
  padding-bottom: 20px;
}

html::-webkit-scrollbar {
  width: 10px;
}
 
html::-webkit-scrollbar-track {
  width: 5px;
}
 
html::-webkit-scrollbar-thumb {
  width: 5px;
  background-color: #6e00e4;
  outline: none;
}

#app {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 0px;
  margin: 0px;
}


</style>
