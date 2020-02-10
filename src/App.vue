<template>
  <div id="app">
    <User/>
  </div>
</template>

<script>

import User from './components/User'

export default {
  name: "App",
  components: {
    User
  }
};
</script>

<style>
div.component {
  border: 1px solid red;
}
</style>
