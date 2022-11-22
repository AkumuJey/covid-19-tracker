<template>
  <main class="home p-10" v-if="!loading">
    <dataTitle :text="title" :dataDate="dataDate" />

    <DataBoxes :stats="stats"/>
    <CountrySelect :countries="countries" @get-country="getCountryData"/>
    <button class="bg-purple-900 text-white rounded p-3 mt-10 mb-10 focus:outline-none hover:bg-purple-500" v-if="stats.Country" @click="clearCountryData">
      Clear Country Data
    </button>
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
import DataBoxes from '../components/DataBoxes.vue'
import CountrySelect from '../components/CountrySelect.vue'

export default {
  name: 'HomeView',
  components: {
    dataTitle, DataBoxes, CountrySelect
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
    },
    getCountryData(country) {
      this.stats = country
      this.title = country.Country
    },
    async clearCountryData() {
      this.loading = true
      const data = await this.fetchCovidData()
      this.title = 'Global'
      this.stats = data.Global
      this.loading = false
    }
  }
}
</script>
