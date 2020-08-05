<template>
  <div class="home">
  <!--<Button size="30" color="black" backColor="green" toLink="http://www.google.com"
      >press here</Button
    >-->
    <Contact mail="malekbekri97@gmail.com" phone="52827123"  adress="Ben Arous"></Contact>
    <br/>
    <OpenningHours :days="days" :key="id"></OpenningHours>
  </div>
</template>

<script>
// @ is an alias to /src
// import Button from '@/components/Button.vue';
import Contact from '@/components/Contact.vue';
import OpenningHours from '@/components/OpenningHours.vue';

export default {
  data() {
    return {
      days: [{ name: 'monday', oponing: '08:00', closing: '16:00' }, { name: 'monday', oponing: '08:00', closing: '16:00' }],
    };
  },
  name: 'Home',
  components: {
    // Button,
    Contact,
    OpenningHours,
  },
};
</script>
