<template>
  <div class="contact">
    <div class="mail" v-show="mail">
      <mail :size="12" />
      {{mail}}
    </div>
    <div class="phone" v-show="phone">
      <phone :size="12" />
      {{phone}}
    </div>
    <div class="adress" v-show="adress">
      <adress :size="12" />
      {{adress}}
    </div>
  </div>
</template>

<script>
import mail from 'vue-material-design-icons/EmailOpenMultipleOutline.vue';
import phone from 'vue-material-design-icons/PhoneHangupOutline.vue';
import adress from 'vue-material-design-icons/City.vue';

export default {
  props: ['mail', 'phone', 'adress'],
  name: 'Contact',
  components: {
    mail,
    phone,
    adress,
  },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
@import url('https://fonts.googleapis.com/css2?family=Nunito+Sans&display=swap');
.contact{
  color:#5a6268;
  font-family: 'Nunito Sans', sans-serif;
}
</style>
