<template>
  <carousel
    id="stock-carousel"
    :autoplay="3000"
    :wrapAround="true"
    :settings="settings"
    :breakpoints="breakpoints"
    v-model="currentSlide"
  >
    <slide v-for="slide in 5" :key="slide">
      <div class="carousel__item">
        <stock
          title="Name"
          description="Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maxime omnis, enim molestiae possimus maiores ipsam autem reiciendis non accusantium dolor sit blanditiis, hic iusto ad labore aperiam optio fugit cumque?"
        />
      </div>
    </slide>
    <template #addons>
      <pagination />
    </template>
  </carousel>
</template>

<script>
import { Carousel, Slide, Pagination } from "vue3-carousel";
import Stock from "../components/Stock.vue";
import 'vue3-carousel/dist/carousel.css';
export default {
    mounted()
    {
        this.currentSlide = 0;
    },
    data: () => ({
       breakpoints:{
           1366: {
               itemsToShow: 3,
           },
           700: {
               itemsToShow: 2,
           }
       },
       settings: {
           itemsToShow: 1
       },
       currentSlide: undefined 
    }),
    components: {
    Carousel,
    Slide,
    Stock,
    Pagination,
  },
};
</script>

<style scoped>
#stock-carousel .carousel__slide {
  padding: 32px;
}

#stock-carousel {
  margin-left: 1px;
  margin-right: 1px;
}

#billboard .carousel__item > img {
  border-radius: 10px;
}

.carousel__item {
  transition: 0.5s;
}

.carousel__slide--active > .carousel__item {
  transform: scale(1.1);
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid black;
}
</style>