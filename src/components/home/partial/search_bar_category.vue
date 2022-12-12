<template>
  <div class="">

  </div>
</template>
<style>

</style>
<script>
import { mapState, mapActions } from 'vuex'
import SearchBar from './search_bar.vue'


export default {
  name: 'SearchBarCategory',
  components: {
    SearchBar,
  },
 
  mounted() {
     
  },
  methods: {
    ...mapActions('eService', [
      'updateKeywordsAction',
    ]),
    search(e) {
    },
  },
}

</script>