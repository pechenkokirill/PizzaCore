<template>
  <div class="product-card">
    <div class="product-image">
      <img
        class="img-lazy"
        @load="onImgLoad"
        src="https://images.dominos.by/media/dominos/osg/api/2018/09/12/carbonara.png"
        alt=""
        loading="lazy"
      />
    </div>
    <div class="product-desc">
      <div class="product-name"><h3>{{ name }}</h3><span class="product-postfix">{{ postfix }}</span></div>
      <div></div>
      <div class="product-composition">
        {{ composition }}
      </div>
      <div class="product-mods">
          <custom-select/>
          <custom-select/>
      </div>
      <div>
            <div>{{ cost }}</div>
            <button class="btn" id="product-card-btn">В корзину</button>
      </div>
    </div>
  </div>
</template>

<script>
import CustomSelect from './CustomSelect.vue';
export default {
  props: [ 'name', 'postfix', 'composition', 'cost' ],
  data()
  {
    return {
      imgLoaded: false,
    }
  },
  methods:
  {
    onImgLoad(e)
    {
      e.target.classList.add("img-lazy-loaded");
    }
  },
  components: { CustomSelect },
  };
</script>

<style>

.product-postfix
{
  margin-left: 4px;
  font-size: 11px;
  font-weight: bold;
  color: red;
  text-transform: uppercase;
}

.product-name
{
  display: flex;
  justify-content: center;
  align-items: center;
}

.product-card #product-card-btn
{
   background: rgb(255, 194, 102);
}

.product-mods
{
    margin-top: 16px;
    display: flex;
}

.product-composition
{
  color: gray;
  height: 100%;
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
  transition: box-shadow 250ms, transform 250ms;
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
  height: 100%;
}
</style>