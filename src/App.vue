<template>
  <Header />
  <div class="container text-center">
    <div>
      <router-link to="/" class="p-3 mx-4 rounded-2xl bg-black text-center text-3xl text-white hover:bg-slate-600">Our World in Data</router-link>
      <router-link :to="{ name: 'corona' }" class="p-3 mx-4 rounded-2xl bg-black text-center text-3xl text-white hover:bg-slate-600">Covid-19</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
  import Header from './components/Header.vue'
  export default {
    components: {
      Header
    }
  }
</script>
