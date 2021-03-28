<template>
    <div class="wrapper">
        <div class="dis">
            <form action="">
                <input type="text" placeholder="Username">
                <input type="text" placeholder="Subject">
                <input type="email" placeholder="Email">
                <textarea name="" id="textBox"
                          placeholder="Type here"
                ></textarea>
                <button>
                    Send
                </button>
            </form>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.wrapper {
    margin: 50px;
}

input, #textBox {
    display: block;
    margin: 30px auto;
    width: 350px;
    height: 40px;
    border-radius: 40px;
    outline: none;
    border: 1px;
    background: #efefef;
    font-size: 16px;
    padding: 0px 15px;
}

#textBox {
    height: 150px;
    padding: 15px;
    border-radius: 15px;
}

button {
    width: 100px;
    height: 40px;
    font-size: 16px;
    color: white;
    background: #42cb9e;
    border: 1px;
    border-radius: 5px;
}

</style>