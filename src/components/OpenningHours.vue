<template>
  <div class="oponingHours">
    <div class="days" v-for="day in days" :key="day">
      <div class="day">
        {{day.name}}
      </div>
      <div class="time">
        {{day.oponing}} > {{day.closing}}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['days'],
  name: 'OponingHours',
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
@import url('https://fonts.googleapis.com/css2?family=Nunito+Sans&display=swap');
.oponingHours{
  color:#5a6268;
  font-family: 'Nunito Sans', sans-serif;
}
.days{
  display : flex;
  justify-content:space-between;
  width:50%;
  border-bottom: 1px black dashed;
}
.day{
  font-weight: bold;
}
</style>
