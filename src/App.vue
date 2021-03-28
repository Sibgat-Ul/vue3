<template>
    <div id="nav">

        <div class="logo">
            <img alt="Vue logo" src="./assets/logo.png">
        </div>

        <div class="navs">
            <router-link to="/">Home</router-link> 
            <router-link to="/about">
                Blogs
            </router-link>
            <router-link to="/lib">Library</router-link>
            <router-link to="/cont">Contact</router-link>

           <Search :bg = "bg" :color="color" />

         
        </div>
    </div>
  
  <router-view/>
</template>

<script>
import Search from './components/Search.vue'

export default {
  components: {
    Search
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

#nav {
  position: sticky;
  top: 0;
  z-index: 9998;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
  padding: 10px 0px 5px 80px;
  font-size: 18px;
  background: #fff;
  text-decoration: none;
  border-bottom: 1px solid #efefef;
}

#nav > .logo > img {
  height: 50px;
}

#nav a {
  margin: 10px;
  font-weight: bold;
  color: rgb(70, 68, 68);
  text-decoration: none;
  transition: .1s;
}

#nav a.router-link-exact-active {
  color: #e84118;
}

.navs {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width: 70%;
}

</style>
