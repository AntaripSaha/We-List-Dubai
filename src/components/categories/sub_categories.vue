<template>
  <ul class='-mx-6 mt-6 divide-y divide-gray-200'>
    <li v-for='category in subCategories' :key='category.id'
        class='relative bg-white py-2 px-2 hover:bg-gray-50 focus-within:ring-2 focus-within:ring-inset focus-within:ring-main-color-600'>
      <div class='min-w-0 flex-1'>
        <router-link :to="{ name: 'Category', params: { id: category.id }}" class='block focus:outline-none'>
          <p class='ml-2 text-sm text-second-color-600 truncate'>{{ $filters.transString(category.name) }}</p>
        </router-link>
      </div>
    </li>
  </ul>
</template>

<script>


export default {
  props: ['subCategories'],
}
</script>