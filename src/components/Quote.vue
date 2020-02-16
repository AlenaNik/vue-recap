<template>
    <div class="wrap">
        <p>{{ quote }}</p>
       <div v-for="catquote in catquotes" :key="catquote"
       >{{ catquote }}</div>
        <button @click="fetchCatFact">Fetch random quote 🐈</button>
    </div>

</template>

<script>
import axios from 'axios';

export default {
  props: {
    quote: {
      type: String
    }
  },
  data() {
    return {
      catquotes: []
    }
  },
  methods: {
    fetchCatFact() {
      axios.get("https://catfact.ninja/fact")
        .then(res => (this.catquotes = res.data))
      console.log(this.catquotes)
    }
  }
}
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

</style>
