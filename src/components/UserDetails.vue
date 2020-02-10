<template>
    <div>
        <div>Hi from user details</div>
        <p>User name: {{ myName }}</p>
        <button @click="resetName">Reset</button>
    </div>
</template>

<script>
  export default {
    name: "UserDetails",
    props: {
      myName: {
        type: String,
        required: true
      }
    },
    methods: {
      resetName() {
        this.myName = 'Max';
        this.$emit('nameWasReset', this.myName);
      }
    }

  }
</script>

<style scoped>
    div {
        padding: 30px;
    }
</style>
