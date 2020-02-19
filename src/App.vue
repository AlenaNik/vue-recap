<template>
  <div id="app">
        <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid'
    export default {
      data: function () {
        return {
          quotes: ['Just to see something'],
          maxQuotes: 10
        }
      },
      components: {
        appQuoteGrid: QuoteGrid
      }
    }
</script>

<style scoped>

</style>
