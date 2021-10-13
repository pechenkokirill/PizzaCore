<template>
  <div class="product-card">
    <div class="product-image">
      <img
        src="https://images.dominos.by/media/dominos/osg/api/2018/09/12/carbonara.png"
        alt=""
      />
    </div>
    <div class="product-desc">
      <div><h3>Name goes here</h3></div>
      <div></div>
      <div style="color: gray">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Culpa
        accusamus quisquam reprehenderit eveniet veritatis fugiat, error, esse
        dignissimos aliquid a eum tempore qui natus laudantium ad, mollitia ut
        aut dolor?
      </div>
      <div class="product-mods">
          <custom-select/>
          <custom-select/>
      </div>
      <div>
            <div>25.99 руб.</div>
            <button class="btn" id="product-card-btn">В корзину</button>
      </div>
    </div>
  </div>
</template>

<script>
import CustomSelect from './CustomSelect.vue';
export default {
  components: { CustomSelect },};
</script>

<style>

.product-card #product-card-btn
{
   background: rgb(255, 194, 102);
}

.product-mods
{
    margin-top: 16px;
    display: flex;
}

.product-mods > div:first-child
{
    margin-right: 8px;
}

@media (max-width: 1366px) { 
    .product-card
    {
        width: calc(33% - 16px)!important;
    }
}

@media (max-width: 992px) { 
    .product-card
    {
        width: calc(50% - 16px)!important;
    }
}

@media (max-width: 676px) { 
    .product-card
    {
        width: calc(100% - 16px)!important;
    }
}

.product-card {
  display: flex;
  flex-direction: column;
  background: white;
  border-radius: 10px;
  margin: 0px 8px 16px;
  width: calc(25% - 16px);
  box-shadow: 0 4px 10px rgb(63 93 138 / 10%);
  transition: 250ms;
}

.product-card div
{
    padding: 8px;
}

.product-card:hover
{
    box-shadow: 0 4px 10px rgb(63 93 138 / 50%);
    transform: translate(0px, -5px);
}

.product-card:hover .product-image
{
    opacity: 0.5;
}

.product-image {
    transition: 250ms;
    margin: auto;
}

.product-desc {
  display: flex;
  text-align: center;
  flex-direction: column;
}
</style>