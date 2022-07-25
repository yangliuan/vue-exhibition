<template>
  <div class="container">
    <swiper
        :slides-per-view="1"
        :space-between="50"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
    >
        <swiper-slide> <img src="@/assets/1.jpeg"> </swiper-slide>
        <swiper-slide> <img src="@/assets/2.gif"> </swiper-slide>
        <swiper-slide> <img src="@/assets/3.gif"> </swiper-slide>
        <swiper-slide> <img src="@/assets/4.gif"> </swiper-slide>
        <swiper-slide> <img src="@/assets/5.jpg"> </swiper-slide>
    </swiper>
  </div>
  
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
export default {
  name: 'App',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
      };
    }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  .container {
    width:800px;
    height:600px;
    margin: auto;
  }
</style>
