<template>
  <h1>---------templating--------</h1>
  {{ nama }}
  {{ number }}
  <div v-html="kelas"></div>
  <h1>-------dataBinding--------</h1>
  <button :disabled="nonaktif">button</button>
  <h2 v-bind="property">bang</h2>
  <input :type="textInput">

  <h1>-------dataBinding--------</h1>
  {{ count == 0 ? count + 1 : count + 3 }}
  <h1>-------V-if--------</h1>
  <button v-if="show">submit</button>
  <button v-show="show">submit</button>

  <div v-if="count == 1">
      number 1
  </div>

  <div v-else-if="count == 2">
      number 2
  </div>
  <div v-else>
      lebih dari 2
  </div>
</template>

<script>
export default {
  data() {
      return {
          show: false,
          count: 3,
          nama: 'bang',
          number: 17,
          kelas: '<h2>XI - 6</h2>',
          nonaktif: true,
          property: {
              id: 1,
              class: 'color'
          },
          textInput: 'password'
      }
  },
}
</script>

<style>
.color {
  color: purple;
}
</style>