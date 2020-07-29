<template>
  <div class="button">
    <button class="without-link">
      <slot></slot>
    </button>
  </div>
</template>

<script>
export default {
  name: 'Button',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.without-link {

  outline: none;
  border: none;
  box-sizing: border-box;
  background-color: #f15458;
  font-size: 17px;
  padding: 6px 30px;
  border-radius: 50px;
  color: white;
  cursor: pointer;
}
</style>
