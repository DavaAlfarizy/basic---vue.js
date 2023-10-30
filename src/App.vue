<template>
<p>----------------------------------templating----------------------------------------</p>
{{ message }}
<div v-html="kelas"></div>
<div v-html="number"></div>

<p>----------------------------------data binding----------------------------------------</p>
<!-- untuk mengikat html dengan data properti di dalam script -->
<button :disabled ="nonaktif">PENCET</button>
<h3 v-bind="property">alfa</h3>
<input :type="typeInput">
<p>----------------------------------data binding----------------------------------------</p>
{{ count == 0 ? count + 7 : count + 2 }}

</template>

<script>
export default{
data() {
  return {
    count : 0,
    message: 'Hello Vue!', 
    kelas : ' <h1>p6</h1>',
    number: '<h2>17 </h2> ',
    nonaktif: false,
    property : {
      id : 1,
      class : 'color'
    },
    typeInput : 'password'
  }
}
}
</script>
<style>
.color{
  color: green;
}</style>