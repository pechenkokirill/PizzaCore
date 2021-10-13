<template>
  <div>
    <select name="" id="">
      <option value="" v-for="o in 10" :key="o">{{ o }}</option>
    </select>
    <svg
      xmlns="http://www.w3.org/2000/svg"
      width="24"
      height="24"
      viewBox="0 0 24 24"
    >
      <path
        d="M0 7.33l2.829-2.83 9.175 9.339 9.167-9.339 2.829 2.83-11.996 12.17z"
      />
    </svg>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
div {
  position: relative;
  width: 100%;
}

svg
{
  position: absolute;
  top: 0;
  right: 12px;
  bottom: 0;
  margin: auto;
  width: 12px;
  height: 12px;
  user-select: none;
  pointer-events: none;
}

select {
  width: inherit;
  height: 36px;
  padding: 0px 32px 0px 8px;
  border-radius: 5px;
  border-color: #dbdbdd;
  appearance: none;
  -moz-appearance: none;
  -webkit-appearance: none;
}
</style>