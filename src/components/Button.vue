<template>
  <div class="button">
    <button class="without-link">click me</button>
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
  border:none;
  background-color: #f15458;
  font-size: 17px;
  padding: 5px 30px;
  border-radius: 50px;
  color: white;
  cursor: pointer;
}
</style>
