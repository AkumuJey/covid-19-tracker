<template>
  <main class="home" v-if="!loading">
    <dataTitle :text="title" :dataDate="dataDate" />
  </main>
  <main v-else class="flex flex-col align-center justify-center text-center">
    <div class="text-grey-500 text-3xl mt-10 mb-6">
      Fetching data
    </div>
    <img :src="loadingImage" class="w-24 mx-auto" alt="">
  </main>
</template>

<script>
import dataTitle from '../components/DataTitle.vue'

export default {
  name: 'HomeView',
  components: {
    dataTitle
  },
  data() {
    return {
      loading: true,
      title: 'Global',
      dataDate: '',
      stats: {},
      countries: [],
      loadingImage: require('../assets/loading.gif')
    }
  },
  async created() {
    const data = await this.fetchCovidData()
    this.dataDate = data.Date
    this.stats = data.Global
    this.countries = data.Countries
    this.loading = false
  },
  methods: {
    async fetchCovidData() {
      const res = await fetch('https://api.covid19api.com/summary')
      const data = await res.json()
      return data
    }
  }
}
</script>
