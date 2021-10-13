<template>
  <div>
    <billboard-carousel />

    <div class="container">
      <div class="section-stock">
        <div class="header">
          <h1>Акции</h1>
        </div>
        <stock-carousel />
      </div>
      <div class="section-products">
        <div class="flex">
          <div class="header">
            <h1>Пицца</h1>
          </div>
          <div id="sort" class="flex">
            <div>Сортировать по:</div>
            <horizontal-list :list="['популярности', 'категории']" />
          </div>
        </div>
        <div class="product-grid">
          <pizza-card />
          <pizza-card />
          <pizza-card />
          <pizza-card />
          <pizza-card />
          <pizza-card />
        </div>
      </div>
    </div>
    <div class="section-footer">
      <br v-for="o in 20" :key="o"/>
    </div>
  </div>
</template>

<script>
import BillboardCarousel from "../components/BillboardCarousel.vue";
import HorizontalList from "../components/HorizontalList.vue";
import PizzaCard from "../components/PizzaCard.vue";
import StockCarousel from "../components/StockCarousel.vue";

export default {
  name: "Home",
  components: {
    BillboardCarousel,
    StockCarousel,
    HorizontalList,
    PizzaCard,
  },
};
</script>

<style>
@media (max-width: 676px) {
  .section-products > .flex {
    flex-direction: column;
  }

  .header {
    text-align: center;
  }
}

#sort > div {
  white-space: nowrap;
}

.section-products > .flex {
  justify-content: space-between;
}

.section-footer {
  padding: 32px;
  margin-top: 24px;
  background: rgb(26, 26, 26);
}

.product-grid {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}

#sort > div {
  align-self: center;
}

.horizontal-list > li > a {
  background: 0;
  border: 0;
  color: #2c3e50;
  transition: 250ms;
  font-weight: bolder;
  margin: 5px;
}

.horizontal-list {
  list-style-type: none;
}

.horizontal-list > li > a:hover {
  color: #e6873b;
}

.horizontal-list > li > a:active {
  text-decoration: underline;
}
</style>
