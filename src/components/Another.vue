<template>
    <div>
        Another quote
        <button @click="counter++">
        </button>
        <p>{{ counter }}</p>
    </div>
</template>

<script>
    export default {
      data: function () {
        return {
          counter: 0
        }
      }
    }
</script>

<style>

</style>
