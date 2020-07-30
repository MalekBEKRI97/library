<template>
  <div class="home">
    <Button size="30" color="black" backColor="green" toLink="http://www.google.com">press here</Button>
  </div>
</template>

<script>
// @ is an alias to /src
import Button from '@/components/Button.vue';

export default {
  data() {
    return {
      btnTexte: 'click me ',
    };
  },
  name: 'Home',
  components: {
    Button,
  },
};
</script>
