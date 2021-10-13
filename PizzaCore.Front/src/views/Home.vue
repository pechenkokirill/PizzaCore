<template>
  <div>
    <billboard-carousel/>

    <div class="container">
      <div>
        <div>
          <h1>Акции</h1>
        </div>
        <stock-carousel/>
      </div>
    </div>
  </div>
</template>

<script>
import BillboardCarousel from '../components/BillboardCarousel.vue';
import StockCarousel from '../components/StockCarousel.vue';

export default {
  name: "Home",
  components: {
    BillboardCarousel,
    StockCarousel
  },
};
</script>

<style scoped>

</style>
