<template>
<div>
    User Details
    <p> User name: {{ user }}</p>
    <p> {{ backwardName() }}</p>
    <p>{{ userage }}</p>
    <button @click="resetName">Reset a name</button>
    <button @click="resetFn">Reset function</button>

</div>
</template>

<script>
    export default {
      props: {
        user: {
          type: String,
          required: true,
        },
        userage: {
          type: Number
        },
        resetFn: Function
      },

      methods: {
        backwardName() {
          this.user.split("").reverse().join("");
        },
        resetName() {
          this.user = 'Alena';
          this.$emit('nameWasReset', this.user)
        }
      }
    }
</script>

<style scoped>
    div {
        background-color: pink;
        padding: 100px;
    }

</style>
