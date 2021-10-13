<template>
  <ul class="flex">
    <li
      v-for="(item, index) in list"
      :key="index"
      :class="{ active: index == active }"
    >
      <button @click="onClick(index, item)">
        <span>{{ item }}</span>
      </button>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    list: {
      type: Array,
      default: () => [],
    },
  },
  data: () => ({
      active: 0,
  }),
  methods: {
    onClick(index, item) {
      this.active = index;
      this.$emit('itemClick', item);
    },
  },
};
</script>

<style scoped>
ul {
  list-style-type: none;
  align-items: center;
  margin: 0;
  padding: 0;
}

ul > li > button::before
{
    transition: 250ms;
    content: '';
    background: rgb(255, 94, 0);
    height: 2px;
    left: 0;
    right: 0;
    bottom: 0;
    width: 0%;
    margin: auto;
    position: absolute;
}

ul > li > button
{
    position: relative;
    padding: 10px;
    font-size: 100%;
    font-weight: 600;
    background: 0;
    border: 0;
    cursor: pointer;
    transition: 250ms;
    color: inherit;
    text-decoration: inherit;
}

ul > li > button:hover
{
    color: rgb(255, 132, 61);
}

ul > li.active 
{
    color: rgb(255, 94, 0);
}

ul > li.active > button::before
{
    width: 80%;
}
</style>