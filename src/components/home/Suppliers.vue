<template>
    <div class='mx-auto max-w-7xl lg:px-8 mb-3 cus-margin' >
        <div class='flex justify-between items-center px-4 py-5 mx-auto max-w-7xl sm:px-6 lg:px-8'>
            <div class='flex-1 min-w-0'>
              <h2 class='pb-4 text-xl font-bold lg:text-3xl text-second-color-600 custom-title'>
                Suppliers By Emirates
              </h2>
            </div>
          </div>
      <swiper

      :loop="true"
      :centeredSlides="false"
      :autoplay="{
        delay: 5000,
      }"
      :breakpoints="{
        '240': {
          slidesPerView: 2,
          spaceBetween: 5,
        },
        '1024': {
          slidesPerView: 4,
          spaceBetween: 5,
        },

      }"
      :modules="modules"
      >
        <swiper-slide  class='group items-start items-center  rounded-lg hover:shadow-lg'  style="margin-left: 0.8%;">
          <router-link :to="{ name: 'Home'}" >
            <button class="button-custom hover:bg-green-700 text-white font-bold py-2 px-8 rounded-full  bg-gray-300 hover:bg-gray-400 font-bold py-2 px-4 rounded inline-flex items-center">
              <img :src="'images/burj.png'" alt="" srcset="" class="button-icon-custom">
              <p class="pl-3 custom-text-button">
                FUJAIRAH
              </p>
            </button>
          </router-link>
        </swiper-slide>
        <swiper-slide  class='group items-start items-center rounded-lg hover:shadow-lg'>
          <router-link :to="{ name: 'Home'}" >
            <button class="button-custom bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-8 rounded-full  bg-gray-300 hover:bg-gray-400 font-bold py-2 px-4 rounded inline-flex items-center">
                <img :src="'images/burj.png'" alt="" srcset="" class="button-icon-custom">
                <p class="pl-3 custom-text-button">
                    RAS AL KHAIMAH
                </p>

            </button>
          </router-link>
        </swiper-slide> <swiper-slide  class='group items-start items-center rounded-lg hover:shadow-lg'>
          <router-link :to="{ name: 'Home'}" >
            <button class="button-custom bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-8 rounded-full  bg-gray-300 hover:bg-gray-400 font-bold py-2 px-4 rounded inline-flex items-center">
                <img :src="'images/burj.png'" alt="" srcset="" class="button-icon-custom">
                <p class="pl-3 custom-text-button">
                    RAS AL KHAIMAH
                </p>

            </button>
          </router-link>
        </swiper-slide> <swiper-slide  class='group items-start items-center rounded-lg hover:shadow-lg'>
          <router-link :to="{ name: 'Home'}" >
            <button class="button-custom bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-8 rounded-full  bg-gray-300 hover:bg-gray-400 font-bold py-2 px-4 rounded inline-flex items-center">
                <img :src="'images/burj.png'" alt="" srcset="" class="button-icon-custom">
                <p class="pl-3 custom-text-button">
                    RAS AL KHAIMAH
                </p>

            </button>
          </router-link>
        </swiper-slide> <swiper-slide  class='group items-start items-center rounded-lg hover:shadow-lg'>
          <router-link :to="{ name: 'Home'}" >
            <button class="button-custom bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-8 rounded-full  bg-gray-300 hover:bg-gray-400 font-bold py-2 px-4 rounded inline-flex items-center">
                <img :src="'images/burj.png'" alt="" srcset="" class="button-icon-custom">
                <p class="pl-3 custom-text-button">
                    RAS AL KHAIMAH
                </p>

            </button>
          </router-link>
        </swiper-slide>
        <swiper-slide  class='group items-start items-center rounded-lg hover:shadow-lg'>
          <router-link :to="{ name: 'Home'}" >
            <button class="button-custom bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-8 rounded-full  bg-gray-300 hover:bg-gray-400 font-bold py-2 px-4 rounded inline-flex items-center">
                <img :src="'images/burj.png'" alt="" srcset="" class="button-icon-custom">
                <p class="pl-3 custom-text-button">
                    UMM ALL QUWAIN
                </p>
            </button>
          </router-link>
        </swiper-slide>
      </swiper>

    </div>
</template>
<script>

import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import { Autoplay } from "swiper";
import { createNamespacedHelpers } from 'vuex'
const { mapState, mapActions } = createNamespacedHelpers('sliderTwo')

export default {
  name: 'SliderTwo',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
      return {
        modules: [Autoplay],
      };
    },
  mounted() {
    this.getSlidesAction()
  },
  computed: {
    ...mapState(['slider_two']),
  },
  methods: {
    ...mapActions(['getSlidesAction']),
  },
}
</script>
<style>
@media screen and (max-width: 768px) and (min-width: 300px){
  .custom-text-button{
    font-size: 8.5px;
    text-align: left;
  }
  .button-custom{
    margin-left:5px;
    width: 90%;
    background-color: #188400 !important;
  }
  .cus-margin{
    margin-top: 10%;
  }
  .button-icon-custom{
    height: 20px;
  }
}
@media screen and (min-width: 769px) {
  .button-icon-custom{
    height: 30px;
  }
  .button-custom{
    width: 80%;
    background-color: #188400 !important;
  }
  .custom-text-button{
    padding-left: 6%;
    font-size: 12px;
  }
  .custom-title{
    margin-left: -3%;
  }
  .cus-margin{
    //margin-top: ;
  }
}

</style>
