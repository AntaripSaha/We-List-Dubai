<template>
  <div class='px-4 py-10 bg-gray-100 sm:px-0'>
    <CategoriesLoader v-if='allCategoriesWithSubcategories.length === 0' />
    <div v-else class='grid overflow-hidden grid-cols-2 gap-4 px-4 mx-auto max-w-7xl sm:py-6 sm:px-6 lg:px-8 sm:grid-cols-3 lg:grid-cols-5 sm:gap-8'>
      <div v-for='category in allCategoriesWithSubcategories' :key='category.id'
           class='bg-white rounded-lg'>
        <div class="cus-column mt-2">
            <div class="mr-5">
              <img :alt='$filters.transString(category.name)' :src='$filters.getFirstMediaUrl(category)' class="img-custom">
              <!-- <img  src=''> -->
            </div>
          <h3 class='text-sm font-bold cus-title ml-2'>
            <router-link :to="{ name: 'Category', params: { id: category.id }}" class='focus:outline-none text-second-color-600'>
              {{ $filters.transString(category?.name) }}
            </router-link>
          </h3>
        </div>
        <div class='cus-margin relative p-6 group'>
          <SubCategories :subCategories='category?.sub_categories || []' aria-hidden='true' />
        </div>
      </div>
    </div>
  </div>

</template>

<script>
import { createNamespacedHelpers } from 'vuex'

const { mapState, mapActions } = createNamespacedHelpers('category')

import SubCategories from './sub_categories.vue'
import CategoriesLoader from './partial/categories_loader.vue'

export default {
  components: { CategoriesLoader, SubCategories },
  mounted() {
    this.getAllWithSubCategoriesAction()
  },
  computed: {
    ...mapState(['allCategoriesWithSubcategories']),
  },
  methods: {
    ...mapActions(['getAllWithSubCategoriesAction']),
  },
}
</script>
<style scoped>

.cus-column{
  display: flex;
 }
 .cus-margin{
  margin-top: -15% !important;
  margin-bottom: -7%;
 }
 .img-custom{
  width: 40px;
  height: auto;
}
.cus-title{
  justify-content: flex-start;
}
</style>