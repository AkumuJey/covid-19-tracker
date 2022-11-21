<template>
  <header class="text-center bg-blue-400 text-white p-4 mb-10">
    <div class="text-3xl md:text-3xl font-bold mb-3"> COVID-19 Tracker</div>
    <p class="text-blue-800">Source of data <a href="https://covid19api.com" target="_blank">covid19api.com</a></p>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return{
      covid: require('../assets/corona.jpg')
    }
  }
}
</script>

