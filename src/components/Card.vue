<template>
    <div class="cards">
        <!--
        <div class="header">
            <slot name="header">
            </slot>
        </div>
        -->
         <div class="bookimg">
            <slot name="bookimg">
            </slot>
         </div>

        <button class="reader">
            Read Now
        </button>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.cards {
    display: grid;
    grid-template-rows: 1fr 4fr 1fr;
    align-items: center;
    justify-content: center;
    text-align: center;
    margin: 0px 0px 0px 0px;
    text-align: center;
    color: rgb(214, 214, 214);
    background: #0f001f;
    min-height: 400px;
    max-height: 400px;
    max-width: 300px;
    border-radius: 30px;
    box-shadow: 1px  #111;
}

.header {
    padding: 15px;
}

.bookimg {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 260px;
    min-height: 300px;
    margin: auto;
}


button {
    height: 35px;
    width: 175px;
    margin: auto;
    background-color: #CC3363;
    color: white;
    outline: none;
    border: none;
    border-radius: 25px;
}
</style>