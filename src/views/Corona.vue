<template>
    <div class="mt-10 p-10 bg-slate-500 rounded-2xl">
        <h1 class="font-bold text-2xl">Corona Virus</h1>
        <div class=" bg-white p-5 rounded-2xl">
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eos dolorum porro debitis mollitia iure aperiam voluptate accusamus tenetur libero eaque, rem atque, culpa officia iste voluptas voluptates esse laborum fugiat quaerat exercitationem. Maxime architecto possimus iste, quis accusantium laboriosam ex repudiandae facere, quibusdam sit velit sequi. Amet, beatae aspernatur accusamus harum impedit dolor provident! Esse quaerat mollitia quod vitae maxime itaque dolorem illo at minima aliquid a recusandae facere, exercitationem ea quas. Totam voluptas, quasi sequi veniam, quidem praesentium sit accusamus error quod recusandae quas vitae quis. Ipsum eaque facilis ab. Iure quas, quos rerum deserunt, ab quidem explicabo nobis libero quam quia vel optio aspernatur nulla earum? Nostrum consequatur quae autem, soluta, delectus nulla nobis explicabo hic aspernatur totam, ipsam officia necessitatibus. Deserunt esse aliquam, dolores eligendi inventore quod tempora, impedit adipisci, debitis unde ipsum aperiam omnis commodi optio? Excepturi doloremque adipisci voluptas sint quod, facere veritatis officiis obcaecati quidem odit rem eum quibusdam facilis recusandae accusantium consectetur harum deserunt. At, numquam! Voluptatem laborum veritatis maiores repudiandae harum eveniet saepe fugit dolore distinctio, at aperiam quis recusandae odio, neque, magnam voluptas corporis animi illo suscipit nobis sapiente! Ipsam quas maiores laboriosam, autem error fugit eius explicabo possimus officiis provident.</p>
        </div>
        <div>
            <h1>Get Country specific data</h1>
            <CountrySelect />
        </div>
    </div>
</template>

<script>
import CountrySelect from '../components/CountrySelect.vue'
export default {
    name: 'corona',
  components: {
    CountrySelect
  }
}
</script>