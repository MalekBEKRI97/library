<template>
  <div class="contact">
    <div class="mail" v-show="mail">
      <i class="far fa-envelope"></i>
      {{mail}}
    </div>
    <div class="phone" v-show="phone">
      <i class="fas fa-phone"></i>
      {{phone}}
    </div>
    <div class="adress" v-show="adress">
      {{adress}}
    </div>
  </div>
</template>

<script>
export default {
  props: ['mail', 'phone', 'adress'],
  name: 'Contact',
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
@import url('/assets/all.min.css');
@import url('https://fonts.googleapis.com/css2?family=Nunito+Sans&display=swap');
.contact{
  color:#5a6268;
  font-family: 'Nunito Sans', sans-serif;
}
</style>
