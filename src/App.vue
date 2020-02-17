<template>
  <div id="app">
    <hr/>
    <button @click="selectedComponent = 'myQuote'">Quote</button>
    <hr/>
    <button @click="selectedComponent = 'Author'">Author</button>
    <hr/>
    <button @click="selectedComponent = 'newQuote'">New</button>

   <keep-alive>
     <component :is="selectedComponent">
       <p>Default</p>
     </component>
   </keep-alive>
        <my-quote>
      <h2 slot="title">{{ quoteTitle }}</h2>
      <p>A wonderful quote</p>
    </my-quote>
  </div>
</template>

<script>

import Quote from './components/Quote'
import theAutor from './components/theAutor'
import Another from './components/Another'
export default {
  data: function() {
    return {
      quoteTitle: 'Quote from data',
      selectedComponent: 'myQuote'
    }
  },
  components: {
    myQuote: Quote,
    Author: theAutor,
    newQuote: Another
  }
}

</script>

<style scoped>

</style>
