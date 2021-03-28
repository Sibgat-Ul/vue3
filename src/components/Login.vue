<template>
  <div class="hello">
    <h3>
      Signup/login
    </h3>
    <form 
      action="" @submit.prevent="submmit"
    >
      <div class="box">
        <div class="sec1">
    
          <input type="text" placeholder="Username">
          <input type="email" placeholder="Email">
          <input type="password" placeholder="password">
          <input type="password" placeholder="confirm password">

          <button class="sub">
            Submit
          </button>

        </div>

        <div class="sec2">

          <input type="email" placeholder="Email">
          <input type="password" placeholder="Password">

          <button class="sub">
            Login
          </button>
        </div>

      </div>
    </form>   
   
  </div>
</template>

<script>
import Search from './Search.vue'

export default {
  name: 'HelloWorld',
  
  components: {
    Search
  },

  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.sec1, .sec2 {
  display: block;
  margin: auto;
}

.sec1 > input, .sec2 > input {
  width: 180px;
  margin: 15px auto;
  display: block;
  padding: 5px;
  border-radius: 35px;
  outline: none;
  border: 1px;
  background: #efefef;
  height: 35px;
  padding: 0px 15px;
  font-size: 16px;
  font-weight: lighter;
}

button {
  width: 115px;
  height: 30px;
  border: 1px;
  outline: none;
  background: #42be93;
  color: #fff;
  font-size: 16px;
  border-radius: 5px;
}

.box {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
  width: 500px;
  margin: 13px auto;
}

</style>
