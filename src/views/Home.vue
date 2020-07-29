<template>
  <div class="home">
    <ButtonWithLink :btnTexte="btnTexte" />
    <br>
    <br>
    <Button>press here</Button>

  </div>
</template>

<script>
// @ is an alias to /src
import Button from '@/components/Button.vue';
import ButtonWithLink from '@/components/ButtonWithLink.vue';

export default {
  data() {
    return {
      btnTexte: 'click me ',
    };
  },
  name: 'Home',
  components: {
    Button,
    ButtonWithLink,
  },
};
</script>
