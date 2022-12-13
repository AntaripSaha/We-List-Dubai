<template>
  <Slider />
  <Suppliers />
  <FeaturedCategories />
  <RecommendedServices />
  <NewestServices />
  <SliderTwo />
  <RealestateServices />
</template>

<script>

import Suppliers from '../components/home/Suppliers.vue'
import Slider from '../components/home/slider.vue'
import SliderTwo from '../components/home/SliderTwo.vue'
import FeaturedCategories from '../components/home/featured_categories.vue'
import RecommendedServices from '../components/home/recommended_services.vue'
import NewestServices from '../components/home/newest_members.vue'
import RealestateServices from '../components/home/realestate.vue'

export default {
  components: {
    Suppliers,
    Slider,
    SliderTwo,
    FeaturedCategories,
    RecommendedServices,
    NewestServices,
    RealestateServices,
  },
}
</script>
<style>

</style>
