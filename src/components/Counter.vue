<template>
  <div v-if="formdata">
    <template v-for="value of formdata">
      <span class="pa1 ma1 white bold dib" :style="`background: ${value % 2 ? 'blue' : 'black'}; border-top: ${value % 5 ? '' : '5px solid #ffcc00'}`" :key="value">{{value}}</span>
    </template>
    <span class="db ma3" :style="`font-size: ${formdata * 0.5 + 1}em`">{{formdata}}</span>
  </div>
  <span v-else class="db">No boxes</span>
</template>

<script>
export default {
  name: 'Counter',
  props: {
    formdata: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
