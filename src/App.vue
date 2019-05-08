<template>
  <div id="app">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    HelloWorld
  },
  data: function () {
    return {
      msg: "Test String!",
      year: "2019"
    }
  }
}
</script>

<style>

</style>
