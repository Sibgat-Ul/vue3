<template>
    <div class="home">

        <Navbar :bg = "style.bg"/>

        <div class="hero">
            <div class="texts">
                <h1 class="ho txt">
                Welcome to my demo (library) project
                </h1>
                <span class="sm txt">
                This project was made for fun ;) .
                </span>
                <h2 class="ht txt">
                Why this website? (I dont know)
                </h2>
                <p class="txt">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi saepe harum est minus fugit voluptatibus obcaecati distinctio molestiae officia suscipit cum porro, neque quidem nostrum eveniet non magnam dolor fugiat?
                </p>
            </div>

            <div class="btncon">
                <button>
                    Join
                </button>
                <button>
                    Get Started
                </button>
                <button>
                  Why Me?
                </button>  
            </div>            

            <button class="btn herobtn">
                <svg class="btnsvg" aria-hidden="true" 
                role="presentation" focusable="false" 
                viewBox="0 0 25 30" 
                style="font-size: 50px; color: white;">
                    <path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z">
                    </path>
                </svg>

            </button>
           <Login v-if="login"/>

          <div class="lib">
              <button class="libtn" >

                <router-link to="/lib">
                    Start reading! 
                </router-link>

                <span>
                  <i class="fas fa-book"></i>
                </span>
          </button>
        </div>

        </div>

    </div>
</template>

<script>
// @ is an alias to /src
import Login from '@/components/Login.vue'
import Navbar from '@/components/Navbar.vue'

export default {
  name: 'Home',
  components: {
    Login,
    Navbar
  },
  setup () {
    const login = false;

    const style = {
        bg : "rgba(17, 17, 17, 0.534)",
        color : "42b9ac",
    }

    return {
      login,
      style
    }
  }
}
</script>

<style scoped>
  * {
    color: #fff;
    box-sizing: border-box;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }

  

  .sec1, .sec2 {
      color: #111;
      text-align: center;
      margin-bottom: 20px;
      background: #fff;
  }

  .hero {
      margin: auto;
      text-decoration: center;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      width: 640px;
  }

  .lib, .libtn {
    width: 300px;
    margin: 0px auto;
    height: 80px;
    font-size: 30px;
    text-align: center;
    border-radius: 10px;
    color: brown;
  }

  .libtn, .libtn > a, .libtn > span > i {
    color: brown;
    text-decoration: none;
  }


  .hero > .txt {
    color: #fff;
    margin: auto;
  }

  .home {
    position: relative;
    background-color: rgba(22, 22, 22, 0.219);
    text-align: center;
    min-height: 100vh;
    color: #fff;
  }

  .home:before {
    content: '';
    background-image: url("./../assets/hero-bg.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
  }

  .btnsvg {
    text-align: center;
    box-sizing: initial;
    fill: white;
    overflow: hidden;
    font-size: 50px;
  }

  .herobtn {
    background: none;
    color: white;
    height: 60px;
    width: 70px;
    text-align: center;
    outline: none;
    border: none;
    cursor: pointer;
    padding: 10px;
    margin: 10px auto;
  }

  .btncon > button {
      width: 95px;
      height: 35px;
      margin: 0px 5px;
      color: brown;
      font-size: 15px;
      padding: 2px;
      transition: .1s;
      border: none;
      outline: none;
      border-radius: 4px;
  }

  .btncon > button:hover {
    background: brown;
    color: white;
    transition: .2s ease-out;
  }

  .hero > .ho {
    font-size: 38px
  }

  .hero > .ht {
    font-size: 30px
  }

  .hero > p {
    font-size: 18px;
  }

  @media screen and (max-width: 640px) {
    #nav {
        padding: 0px 8px;
    }

    .hero {
        padding: 20px;
        width: 100%;
    }
  }
</style>