<template>
  <div id="app">
    <h1 class="f1 bold">Box Builder</h1>
    <h2 class="f3 bold ma2">Start Building</h2>
    <button class="bg-green white pa2 pointer ma2" @click="formdata++">Add Box</button>
    <button class="bg-red white pa2 pointer ma2" @click="formdata--">Remove Box</button>
    <Counter :formdata="parseInt(formdata)" class="ma3"/>
    <input v-model="formdata" placeholder="Enter a number"/>
  </div>
</template>

<script>
import Counter from './components/Counter.vue'

export default {
  name: 'app',
  components: {
    Counter
  },
  data () {
    return {
      formdata: 0
    }
  }
}
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  margin-top: 60px;
}
</style>
