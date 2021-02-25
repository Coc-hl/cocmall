<template>
<div>
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide><slot name="picture1"></slot></swiper-slide>
    <swiper-slide><slot name="picture2"></slot></swiper-slide>
    <swiper-slide><slot name="picture3"></slot></swiper-slide>
    <swiper-slide><slot name="picture4"></slot></swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper></div>
</template>

<script>
  export default {
    name: 'myswiper',
    data() {
      return {
        swiperOptions: {

          pagination: {
            el: '.swiper-pagination',            
            clickable: true
          },
          loop:true
    }}},
    computed: {
      swiper() {
        return this.$refs.mySwiper.$swiper
      }
    },
    mounted() {
      this.swiper.slideTo(3, 1000, false)
    }
  }
</script>

<style scoped>
</style>