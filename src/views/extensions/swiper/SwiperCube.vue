<script setup>
import { register } from 'swiper/element/bundle'
import swiper1 from '@images/swiper/colorful-heart.jpg'
import swiper3 from '@images/swiper/colorful-wallpaper.jpg'
import swiper2 from '@images/swiper/exploding-burger.jpg'
import swiper4 from '@images/swiper/fruit-is-word-fruit.jpg'
import swiper5 from '@images/swiper/single-tree.jpg'

register()
</script>

<template>
  <swiper-container
    pagination="true"
    centered-slides="true"
    effect="cube"
    grab-cursor="true"
    cube-effect-shadow="true"
    cube-effect-slide-shadows="true"
    cube-effect-shadow-scale="0.94"
    events-prefix="swiper-"
  >
    <swiper-slide
      v-for="swiperImg in [
        swiper2,
        swiper1,
        swiper4,
        swiper3,
        swiper5,
      ]"
      :key="swiperImg"
    >
      <VImg
        :src="swiperImg"
        height="400"
        cover
      />
    </swiper-slide>
  </swiper-container>
</template>

<style lang="scss" scoped>
swiper-slide {
  background-position: center;
  background-size: cover;
  block-size: 300px;
  inline-size: 300px;
}

swiper-container {
  margin: auto;
  block-size: 300px;
  inline-size: 300px;
}
</style>
