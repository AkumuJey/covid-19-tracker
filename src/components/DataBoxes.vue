<template>
 <div class="bg-violet-100 p-5 rounded-xl">
    <div class="grid md:grid-col-2 gap-4 my-4 mx-10">
        <div class="shadow:md bg-slate-300 text-center rounded">
            <h3 class="text-3xl text-purple-900 font-bold mb-4">
                Covid Cases
            </h3>
            <div class="text-2xl mb-4">
                <span class="font-bold">New:</span>
                {{ numberWithCommas(stats.NewConfirmed) }}
            </div>
            <div class="text-2xl mb-4">
                <span class="font-bold">Total:</span>
                {{ numberWithCommas(stats.TotalConfirmed) }}
            </div>
        </div>
    </div>
    <div class="grid md:grid-col-2 gap-4 mt-4 mx-10">
        <div class="shadow:md bg-slate-500 text-center rounded">
            <h3 class="text-3xl text-purple-900 font-bold mb-4">
                Covid Deaths
            </h3>
            <div class="text-2xl mb-4">
                <span class="font-bold">New:</span>
                {{ numberWithCommas(stats.NewDeaths) }}
            </div>
            <div class="text-2xl mb-4">
                <span class="font-bold">Total:</span>
                {{ numberWithCommas(stats.TotalDeaths) }}
            </div>
        </div>
    </div>
    <!-- <div class="grid md:grid-col-2 gap-4 mb-4">
        <div class="shadow:md bg-slate-800 text-center rounded">
            <h3 class="text-3xl text-purple-600 font-bold mb-4">
                Recovered Patients
            </h3>
            <div class="text-2xl mb-4">
                <span class="font-bold">New:</span>
                {{ numberWithCommas(stats.NewRecovered) }}
            </div>
            <div class="text-2xl mb-4">
                <span class="font-bold">Total:</span>
                {{ numberWithCommas(stats.TotalRecovered) }}
            </div>
        </div>
    </div> -->
 </div>
</template>

<script>
export default{
    name: 'Data Boxes',
    props: ['stats'],
    methods: {
        numberWithCommas(x) {
            return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',')
        }
    }
}
</script>
