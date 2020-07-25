<template>
  <div class="button">
    <a class="with-link">click me</a>
  </div>
</template>

<script>
export default {
  name: 'ButtonWithLink',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.with-link {
  background-color: #f15458;
  font-size: 20px;
  padding: 5px 30px;
  border-radius: 50px;
  color: white;
  cursor: pointer;
}
</style>
