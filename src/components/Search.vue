<template>
    <div class="wrapper"
        :style="
            {
                color: `#${color}`,
                background: `#${bg}`
            }
        "
    >
        <div class="form">
            <input class = "bar" 
                placeholder="Type to search"
                type="text" v-model="search"
                :style="
                    {
                        color: `#${color}`,
                    }
                " 
                >

            <span>
                <i class="fas fa-search"></i>
            </span>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue'

export default {
    props: {
        bg: {
            default: "#2f3640"
        },

        color: {
            default: "#e84118"
        },

    },
    setup (props) {
        const search = ref(' ');
        console.log(props.bg);
        
        return {
            search,
            props
        }
    }
}
</script>

<style scoped>
    .wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 35px;
        height: 35px;
        padding: 5px;
        border-radius: 30px;
        text-align: center;
        transition: .4s;
        background: #2f3640;
    }

    input {
        border: none;
        outline: none;
        line-height: 30px;
        float: left;
        width: 0px;
        background: none;
        font-size: 16px;
        transition: .3s;
        padding: 0px;
        background: #2f3640;
    }

    span {
        float: right;
        width: 30px;
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        border-radius: 50%;
    }
       
    .wrapper:hover {
        width: 200px;
        transition: .3s;
    }

    .wrapper:hover input {
        width: 160px;
        transition: .4s;
    }

</style>