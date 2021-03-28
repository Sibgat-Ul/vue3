<template>
    <div id="nav">

        <div class="logo">
            <img alt="Vue logo" src="@/assets/logo.png">
        </div>

        <div class="navs">
            <router-link to="/">Home</router-link> 
            <router-link to="/about">
                Blogs
            </router-link>
            <router-link to="/lib">Library</router-link>
            <router-link to="/cont">Contact</router-link>

           <Search :bg = "bg"  :color = "color" />

        </div>
    </div>

    <div id="nav2">
        <div class="logo">
            <img alt="Vue logo" src="@/assets/logo.png">
        </div>

        <button aria-label="Open navigation menu" class="style__HamburgerBtn-sc-1twqwji-6 gpByEo"><svg class="style__HamburgerIcon-sc-1twqwji-5 cmzBnq" viewBox="0 0 26 18"><g fill-rule="evenodd"><rect width="18" height="2" x="4" rx="1"></rect><rect width="18" height="2" x="4" y="16" rx="1"></rect><rect width="26" height="2" y="8" rx="1"></rect></g></svg></button>
    </div>
</template>

<script>
import Search from './Search'

export default {
    components: {
        Search
    },
    props: {
        bg: {
            default: "#2f3640"
        },

        color: {
            default: "#e84118"
        },
    },
    setup(props) {

        return {
            props
        }
    }

}
</script>

<style scoped>

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
        background: transparent;
        text-decoration: none;
        border-bottom: 1px solid #efefef;
        display: none;
    }

    #nav2 > .logo > img, #nav > .logo > img {
        height: 50px;
    }

    #nav a {
        margin: 10px;
        font-weight: bold;
        color: rgb(214, 214, 214);
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

    #nav2 > button {
        height: 50px;
        width: 50px;
        background: none;
        color: #fff;
        fill: #fff;
        outline: none;
        border: 0px;
        cursor: pointer
    }

    #nav2 {
        display: flex;
    
        justify-content: space-between;
        align-items: center;
        
        padding: 10px 20px;
    }

</style>