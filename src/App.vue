<template>
  <div id="app">
    <my-quote>
      <h2 slot="title">{{ quoteTitle }}</h2>
      <p slot="content">A wonderful quote</p>
    </my-quote>
  </div>
</template>

<script>

import Quote from './components/Quote'
export default {
  data: function() {
    return {
      quoteTitle: 'Quote from data'
    }
  },
  components: {
    myQuote: Quote
  }
}

</script>

<style scoped>

</style>
