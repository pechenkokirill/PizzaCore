<template>
  <div class="stock-card flex">
    <img src="../../public/img/pizzaicon.png" alt="">
    <div class="stock-text">
      <h3>{{title}}</h3>
      <div>
        {{description}}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StockCard',
  props: ['title', 'description'],
};
</script>

<style scoped>

@media (max-width: 1366px) { 
    .stock-card
    {
        flex-direction: column;
    }
}

.stock-card
{
    background: rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    padding: 0.25rem;
    widows: 33.33%;
    box-shadow: 0 4px 10px rgb(63 93 138 / 10%);
}

.stock-card > img
{
    border-radius: 10px;
    margin: auto;
    width: 64px;
}

.stock-text
{
    margin: 1rem;
    text-align: start;
}

</style>