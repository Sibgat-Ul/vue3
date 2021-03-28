<template>
    <div class="home">
        <div class="hero">
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

        </div>

        <div class="txtBox">
            <div class="sec1">
                <h1>
                    Section One
                </h1>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis in, velit ratione magni sunt placeat officia quasi culpa minus consequatur ea fugiat esse quibusdam? Nobis odio voluptatum consectetur dolores quas.
                Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vel illum aperiam illo quos rem eaque ducimus, ad doloremque id quam sequi facilis repellat inventore. Explicabo eaque aspernatur animi aliquam eveniet!
            </div>

            <div class="sec2">
                <h1>
                    Section Two
                </h1>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores nisi est quibusdam aperiam eos reiciendis vitae sequi quis eveniet sed voluptates sit a expedita eum iure eligendi, hic excepturi ex.
                Lorem ipsum dolor, sit amet consechgfhjgtetur adipisicing elit. Vel illum aperiam illo quos rem eaque ducimus, ad doloremque id quam sequi facilis repellat inventore. Explicabo eaque aspernatur animi aliquam eveniet!
            </div>
        </div>

    </div>
</template>

<script>
// @ is an alias to /src
import Login from '@/components/Login.vue'

export default {
  name: 'Home',
  components: {
    Login
  },
  setup () {
    const login = false

    return {
      login
    }
  }
}
</script>

<style scoped>
  * {
    color: #111
  }

  .txtBox {
      
  }

  .sec1, .sec2 {
      color: #111;
      height: 100%;
      text-align: center;
      margin-bottom: 20px;
      background: #fff;
  }

  .hero {
      color: #fff;
      padding: 250px 100px 250px;
  }

  .hero > .txt {
      color: #fff;
  }

  .home {
    position: relative;
    background: url("./../assets/hero-bg.jpg");
    top: 0;
    height: 100%;
    background-repeat: no-repeat;
    overflow: hidden;
    background-repeat: no-repeat;
    background-attachment: fixed;
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
    margin: auto;
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
</style>