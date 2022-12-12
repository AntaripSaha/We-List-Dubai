<template>
  <div class='flex flex-col rounded-lg shadow-xl overflow-hidden'>
    <div class='flex-shrink-0'>
      <img :src='this.$filters.getFirstMediaThumb(eService)' alt='' class='w-full object-cover'  style="height:10rem;" />
    </div>
    <div class='flex-1 bg-white p-6 flex flex-col justify-between'>
      <div class='flex-1'>
        <router-link :to='{name:"EService", params:{ id:eService.id }}' class='block'>
          <p class='text-normal font-semibold text-second-color-600'>
            {{ this.$filters.transString(eService.name).substring(0,15)+".." }}
          </p>
          <div class='h-6 flex items-center min-w-0 text-sm'>
            <!-- <span class='hidden sm:block text-xs text-second-color-400 mx-2'>{{ $t('Starts From') }}</span> -->
            <span class='text-normal font-bold text-main-color-600' style="color: #e00000;">{{ this.$filters.formatPrice(eService.price) }} </span>
            <!-- <span class='text-sm text-main-color-600'> /{{ $t(eService['price_unit'] || '') }}</span> -->
          </div>
          <!-- <p class='mt-3 text-sm text-second-color-400 line-clamp-3'>
            {{ this.$filters.stripHtml(eService.description) }}
          </p> -->
        </router-link>
      </div>
      <div class='flex items-end justify-between'>
        <div class='h-6 flex'>
          <StarIcon v-for='i in Math.ceil(eService.rate)' :key='i' aria-hidden='true' class='w-5 h-5 text-yellow-400' />
          <StarIcon v-for='i in Math.floor(5 - eService.rate)' :key='i' aria-hidden='true' class='w-5 h-5 text-gray-300' />
        </div>
        <span class="text-sm font-semibold text-second-color-500">({{ eService.total_reviews }})</span>
        <div class='flex flex-col pt-1 items-end  sm:pt-3'>
          <div v-if='eService.discount_price' class='flex items-center min-w-0 text-sm text-gray-400'>
            <!-- <span class='text-normal font-bold line-through'>{{ this.$filters.formatPrice(eService.discount_price) }} </span> -->
            <!-- <span class='text-sm '> /{{ $t(eService['price_unit'] || '') }}</span> -->
          </div>
          <div class='h-6 flex items-center min-w-0 text-sm'>
            <!-- <span class='hidden sm:block text-xs text-second-color-400 mx-2'>{{ $t('Starts From') }}</span> -->
            <!-- <span class='text-normal font-bold text-main-color-600'>{{ this.$filters.formatPrice(eService.price) }} </span> -->
            <!-- <span class='text-sm text-main-color-600'> /{{ $t(eService['price_unit'] || '') }}</span> -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { StarIcon } from '@heroicons/vue/solid'

export default {
  components: {
    StarIcon,
  },
  props: ['eService'],
}
</script>
