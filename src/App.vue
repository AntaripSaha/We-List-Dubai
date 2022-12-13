<template>
  <TopBar />
  <HSMenu />
  <!-- <CategoryMenu /> -->
  <router-view />
  <HSFooter />
  <Snackbar />
</template>
<script>
import TopBar from './components/home/TopBar.vue'
import HSMenu from './components/header/main_header.vue'
import CategoryMenu from './components/header/CategoryMenu.vue'
import HSFooter from './components/footer/footer.vue'
import Snackbar from './components/partial/snackbar.vue'

export default {
  components: {
    TopBar,
    HSMenu,
    CategoryMenu,
    HSFooter,
    Snackbar,
  },

}

</script>
