<template>
    <div class="quote-row">
           <app-quote v-for="quote in quotes" :key="quote">
               {{ quote }}
           </app-quote>
    </div>
</template>

<script>
import Quote from './Quote'

  export default {
    props: {
      quotes: {
        type: String,
        required: true
      }
    },
    components: {
      appQuote: Quote
    }
  }
</script>

<style>
    .quote-row {
        display: flex;
       justify-content: space-evenly;
    }

</style>
