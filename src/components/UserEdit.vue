<template>
    <div>
        <h1>{{ userage }}</h1>
        <button @click="sumAge">Edit Age</button>

    </div>
</template>

<script>
export default {
  props: {
    userage: {
      type: Number,
      required: true
    }
  },
  methods: {
    sumAge() {
      this.userage++;
      this.$emit('AgeUpdate', this.userage)
    }
  }
}
</script>

<style scoped>
    div {
        background-color: wheat;
        padding: 100px;
    }

</style>
