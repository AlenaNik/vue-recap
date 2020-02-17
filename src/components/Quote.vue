<template>
    <div class="wrap">
       <div class="title">
           <slot name="title"></slot>
           <span><slot name="subtitle">Subtitle</slot></span>
       </div>
        <div>
            <slot></slot>
        </div>
    </div>

</template>

<script>

</script>
<style scoped>
    .wrap {
        font-family: ".SF NS Mono";
        text-align: center;
        color: black;
        padding: 10px;
        font-size: 1em;
        height: 200px;
        width: auto;
        display: grid;
        place-items: center;
        margin: 100px;
        border-radius: 20px;
        box-shadow: 2px -7px 23px -1px rgba(184,184,184,1);
        -moz-box-shadow: 2px -7px 23px -1px rgba(184,184,184,1);
        box-shadow: 2px -7px 23px -1px rgba(184,184,184,1);
    }

    button {
        border-radius: 10px;
        background-color: black;
        padding: 5px 10px;
        color: white
    }
    .title {
        color: mediumslateblue;
    }

</style>
