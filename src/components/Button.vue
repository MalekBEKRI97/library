<template>
  <div class="button">
    <button class="btn" :style="cssProp" @click="goTo">
      <slot></slot>
    </button >

  </div>
</template>

<script>
export default {
  props: ['size', 'color', 'backColor', 'toLink'],
  name: 'Button',
  computed: {
    cssProp() {
      return `font-size: ${this.size}px;color: ${this.color};background-color: ${this.backColor};`;
    },
  },
  methods: {
    goTo() {
      window.location.href = this.toLink;
      return window.location.href;
    },
  },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.btn {
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
.btn:active {
  transform: scale(0.95,0.95);
}
</style>
