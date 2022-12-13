<template>
  <div class="hidden sm:flex p-10  absolute custo-search inset-x-0 items-center">
    <div class="bg-black opacity-90 m-auto rounded-lg p-5 flex w-3/4">
      <div class="w-full">
          <!-- <p class="text-lg font-semibold text-white mr-8 whitespace-nowrap ">searching in</p>  -->
          <ul class="nav nav-tabs flex flex-col items-center md:flex-row flex-wrap list-none border-b-0 pl-0 mb-4" id="tabs-tab"
          role="tablist">
          <li class="nav-item text-lg font-semibold text-white mr-8 whitespace-nowrap " role="presentation">Searching in</li>
          <li class="nav-item" role="presentation">
          <a href="#tabs-home" class="
              nav-link
              block
              font-medium
              text-xs
              leading-tight
              uppercase
              px-6
              py-3
              my-2
              rounded-full
          " id="tabs-home-tab" data-bs-toggle="pill" data-bs-target="#tabs-home" role="tab" aria-controls="tabs-home"
              aria-selected="true">All</a>
          </li>
          <li class="nav-item" role="presentation">
          <a href="#tabs-profile" class="
          nav-link
              block
              font-medium
              text-xs
              leading-tight
              uppercase
              px-6
              py-3
              my-2
              active
              rounded-full
          " id="tabs-profile-tab" data-bs-toggle="pill" data-bs-target="#tabs-profile" role="tab"
              aria-controls="tabs-profile" aria-selected="false">Motors</a>
          </li>
          <li class="nav-item" role="presentation">
          <a href="#tabs-profile" class="
          nav-link
              block
              font-medium
              text-xs
              leading-tight
              uppercase
              px-6
              py-3
              my-2
              rounded-full
          " id="tabs-profile-tab" data-bs-toggle="pill" data-bs-target="#tabs-profile" role="tab"
              aria-controls="tabs-profile" aria-selected="false">Classified</a>
          </li>
          <li class="nav-item" role="presentation">
          <a href="#tabs-profile" class="
          nav-link
              block
              font-medium
              text-xs
              leading-tight
              uppercase
              px-6
              py-3
              my-2
              rounded-full
          " id="tabs-profile-tab" data-bs-toggle="pill" data-bs-target="#tabs-profile" role="tab"
              aria-controls="tabs-profile" aria-selected="false">Property for Rent</a>
          </li>
          <li class="nav-item" role="presentation">
          <a href="#tabs-profile" class="
          nav-link
              block
              font-medium
              text-xs
              leading-tight
              uppercase
              px-6
              py-3
              my-2
              rounded-full
          " id="tabs-profile-tab" data-bs-toggle="pill" data-bs-target="#tabs-profile" role="tab"
              aria-controls="tabs-profile" aria-selected="false">Property for Sale</a>
          </li>
          <li class="nav-item" role="presentation">
          <a href="#tabs-profile" class="
          nav-link
              block
              font-medium
              text-xs
              leading-tight
              uppercase
              px-6
              py-3
              my-2
              rounded-full
          " id="tabs-profile-tab" data-bs-toggle="pill" data-bs-target="#tabs-profile" role="tab"
              aria-controls="tabs-profile" aria-selected="false">Jobs</a>
          </li>
          <li class="nav-item" role="presentation">
          <a href="#tabs-profile" class="
          nav-link
              block
              font-medium
              text-xs
              leading-tight
              uppercase
              px-6
              py-3
              my-2
              rounded-full
          " id="tabs-profile-tab" data-bs-toggle="pill" data-bs-target="#tabs-profile" role="tab"
              aria-controls="tabs-profile" aria-selected="false">Community</a>
          </li>
          <!-- <li class="nav-item" role="presentation">
          <a href="#tabs-messages" class="
              nav-link
              block
              font-medium
              text-xs
              leading-tight
              uppercase
              border-x-0 border-t-0 border-b-2 border-transparent
              px-6
              py-3
              my-2
              hover:border-transparent hover:bg-gray-100
              focus:border-transparent
          " id="tabs-messages-tab" data-bs-toggle="pill" data-bs-target="#tabs-messages" role="tab"
              aria-controls="tabs-messages" aria-selected="false">Messages</a>
          </li> -->
          
          </ul>
          <div class="tab-content" id="tabs-tabContent">
              <div class="tab-pane fade" id="tabs-home" role="tabpanel" aria-labelledby="tabs-home-tab">
                  <div class="flex gap-3 bg-transparent">
                      <input type="text" class="w-5/6 text-base rounded-md p-4" placeholder="Search For Anything">
                      <button class="bg-main-color-600 w-1/6 rounded-md font-semibold text-white hover:bg-[#0f5100]">Search</button>
                  </div>
                  
              </div>
              <div class="tab-pane fade show active" id="tabs-profile" role="tabpanel" aria-labelledby="tabs-profile-tab">
                  <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-3 gap-3">
                      <div class="flex justify-center">
                          <div class="mb-3 w-full">
                            <select class="form-select appearance-none
                              block
                              w-full
                              p-3
                              text-base
                              font-normal
                              text-gray-700
                              bg-white bg-clip-padding bg-no-repeat
                              border border-solid border-gray-300
                              rounded
                              transition
                              ease-in-out
                              m-0
                              focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" aria-label="Default select example">
                                <option selected>Select menu</option>
                                <option value="1">One</option>
                                <option value="2">Two</option>
                                <option value="3">Three</option>
                            </select>
                          </div>
                      </div>
                      <div class="flex justify-center">
                          <div class="mb-3 w-full">
                            <select class="form-select appearance-none
                              block
                              w-full
                              p-3
                              text-base
                              font-normal
                              text-gray-700
                              bg-white bg-clip-padding bg-no-repeat
                              border border-solid border-gray-300
                              rounded
                              transition
                              ease-in-out
                              m-0
                              focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" aria-label="Default select example">
                                <option selected>Open this select menu</option>
                                <option value="1">One</option>
                                <option value="2">Two</option>
                                <option value="3">Three</option>
                            </select>
                          </div>
                      </div>
                      <div class="flex justify-center">
                          <div class="mb-3 w-full">
                            <select class="form-select appearance-none
                              block
                              w-full
                              p-3
                              text-base
                              font-normal
                              text-gray-700
                              bg-white bg-clip-padding bg-no-repeat
                              border border-solid border-gray-300
                              rounded
                              transition
                              ease-in-out
                              m-0
                              focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" aria-label="Default select example">
                                <option selected>Open this select menu</option>
                                <option value="1">One</option>
                                <option value="2">Two</option>
                                <option value="3">Three</option>
                            </select>
                          </div>
                      </div>
                  </div>
                  <hr>
                  <div class="flex gap-3 bg-transparent mt-4">
                      <input type="text" class="w-5/6 text-base rounded-md p-4" placeholder="Search For Anything">
                      <button class="bg-main-color-600 w-1/6 rounded-md font-semibold text-white hover:bg-[#0f5100]">Search</button>
                  </div>
              </div>
              
          
          </div>
      </div>
  </div>
  </div>
</template>

<style scoped>
.wrapper::before {
  content: "";
  background-color: black;
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: -1;
  padding: 20px;
  opacity: 0.5;
  border-radius: 12px;
}
a{
    color: white !important;
}
.active{
    background-color: #188400;
}
/* .nav-item a:hover{
    background-color: #0f5100;
} */
.tab-content .active{
    background-color: transparent !important;
}
input:focus, textarea:focus, select:focus{
    outline: none;
}
.custo-search{
  position: absolute;
  bottom: 0;
  z-index: 1;
}
@media screen and (min-width: 320px) and (max-width: 634px){
.custo-search{
  position: absolute;
  bottom: -30%;
  z-index: 1;
}

}
@media screen and (min-width: 1500px){
  .custo-search{
    margin-bottom: -10% !important;
  }
}
@media screen and (min-width: 1700px){
  .custo-search{
    margin-bottom: -10% !important;
  }
}
@media screen and (min-width: 2000px){
  .custo-search{
    margin-bottom: -7% !important;
  }
}
</style>
<script>
import { mapState, mapActions } from 'vuex'
import SearchBar from './search_bar.vue'
import 'tw-elements';


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