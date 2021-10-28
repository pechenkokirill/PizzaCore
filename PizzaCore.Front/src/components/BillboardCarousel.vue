s<template>
  <carousel
    id="billboard"
    :autoplay="3000"
    :wrapAround="true"
    :settings="settings"
    :breakpoints="breakpoints"
    :pauseAutoplayOnHover="true"
    v-model="currentSlide"
  >
    <slide v-for="slide in 10" :key="slide">
      <div class="carousel__item">
        <img src="../../public/img/carusel1.png" style="width: 100%" alt="" />
      </div>
    </slide>
    <template #addons>
      <pagination />
    </template>
  </carousel>
</template>

<script>
import { Carousel, Slide, Pagination } from "vue3-carousel";
import "../../public/styles/custom_carousel.css";

export default {
  name: "BillboardCarousel",
  mounted() {
    this.currentSlide = 0;
  },
  data: () => ({
    breakpoints: {
      1366: {
        itemsToShow: 1.5,
      },
    },
    settings: {
      itemsToShow: 1,
    },
    currentSlide: undefined,
  }),
  components: {
    Carousel,
    Slide,
    Pagination
  },
};
</script>

<style scoped>
#billboard .carousel {
  margin-top: 32px;
}

#billboard .carousel__slide {
  padding: 48px;
}

#billboard .carousel__item > img {
  border-radius: 10px;
  box-shadow: 0 4px 10px rgb(63 93 138 / 10%);
}

.carousel__item {
  transition: 0.5s;
}

.carousel__slide--active > .carousel__item {
  transform: scale(1.1);
}
</style>