<template>
  <div class='relative pb-32 bg-accent-color-50'>
    <div class='flex justify-between items-center px-4 pt-6 pb-16 mx-auto max-w-7xl sm:px-6 lg:px-8'>
      <div class='flex-1 min-w-0'>
        <h2 class='py-3 text-xl font-bold lg:text-4xl text-second-color-600'>{{ $t('Popular Services') }}</h2>
        <!-- <p class='text-sm sm:text-base text-second-color-400 sm:truncate'>
          {{ $t('Recommended Listings For You') }}
        </p> -->
      </div>
      <div class='flex mt-4 md:mt-0'>
        <router-link :to='{name:"Categories"}'
                     class='inline-flex items-center px-4 py-2 ml-3 text-sm font-medium text-white rounded-md border border-transparent shadow-sm bg-main-color-600 hover:bg-main-color-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-main-color-500'
                     type='button'>
          {{ $t('View All') }}
        </router-link>
      </div>
    </div>
  </div>

  <section aria-labelledby='contact-heading'
           class='relative z-10 px-4 pb-10 mx-auto -mt-40 max-w-7xl sm:px-6 lg:px-8'>
    <div class='grid grid-cols-2 gap-y-3 gap-x-3 lg:grid-cols-5 lg:gap-y-3 lg:gap-x-3'>
      <EServiceItem v-for='eService in recommendedEServices' :key='eService.id' :eService='eService' />
    </div>
  </section>
</template>

<script>
import EServiceItem from './partial/e_service_item.vue'

import { createNamespacedHelpers } from 'vuex'

const { mapState, mapActions } = createNamespacedHelpers('eService')

export default {
  components: {
    EServiceItem,
  },
  mounted() {
    this.getRecommendedEServicesAction()
  },
  computed: {
    ...mapState(['recommendedEServices']),
  },
  methods: {
    ...mapActions(['getRecommendedEServicesAction']),
  },
}
</script>