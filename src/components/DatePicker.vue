<template>
  <div class="datePicker">
    <h2>Choisir la date et l'heure du rendez-vous</h2>
    <div class="date">
      <h3>Aout 2020</h3>
      <suivant fillColor="#2b78aa" :size="50" />
    </div>
    <div class="weekDays">
      <div>
        <div>Mer</div>
        <div>05</div>
        <div>Aout</div>
      </div>
      <div>
        <div>Jeu</div>
        <div>06</div>
        <div>Aout</div>
      </div>
      <div>
        <div>Ven</div>
        <div>07</div>
        <div>Aout</div>
      </div>
      <div>
        <div>Sam</div>
        <div>08</div>
        <div>Aout</div>
      </div>
      <div>
        <div>Dim</div>
        <div>09</div>
        <div>Aout</div>
      </div>
      <div>
        <div>Lun</div>
        <div>10</div>
        <div>Aout</div>
      </div>
      <div>
        <div>Mar</div>
        <div>11</div>
        <div>Aout</div>
      </div>
    </div>
    <div class="hours">
      <div>08:00</div>
      <div>08:15</div>
      <div>08:30</div>
      <div>08:45</div>
      <div>09:00</div>
      <div>09:15</div>
      <div>09:30</div>
      <div>09:45</div>
      <div>10:00</div>
      <div>10:15</div>
      <div>10:30</div>
      <div>10:45</div>
      <div>11:00</div>
      <div>11:15</div>
      <div>11:30</div>
      <div>11:45</div>
      <div>12:00</div>
      <div>12:15</div>
      <div>12:30</div>
      <div>12:45</div>
      <div>13:00</div>
      <div>13:15</div>
      <div>13:30</div>
      <div>13:45</div>
      <div>14:00</div>
      <div>14:15</div>
      <div>14:30</div>
      <div>14:45</div>
      <div>15:00</div>
      <div>15:15</div>
      <div>15:30</div>
      <div>15:45</div>
    </div>
  </div>
</template>

<script>
import suivant from 'vue-material-design-icons/ArrowRightBox.vue';

export default {
  name: 'DatePicker',
  components: {
    suivant,
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap');
*{
  margin: 0;
  padding:0;
  box-sizing: border-box;
  font-family: 'Roboto', sans-serif;
}
.datePicker{
  width: 35rem;
  height: 35rem;
  background-color: #e4ecf4;
  text-align: center;
}
.weekDays{
  display: flex;
  justify-content: space-around;
  margin-right:7px;
  margin-top: 5px;
}
.weekDays > div {
  width: 5rem;
  height: 4rem;
  background-color: #f5f5f5;
  margin-left:6px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction:column;
  font-size:15px;
  border: 1px solid white;
  border-radius :5px ;
  font-size: 14px;
  color: #938f8f;
}
.weekDays > div > div:nth-child(2){
  font-weight: bolder;
  font-size: 1.25em;
  color:black;
}
.hours{
  display:flex;
  flex-wrap:wrap;
  justify-content: space-around;
  margin-top: 20px;
  margin-right:9px;
}
.hours > div{
  margin-left:6px;
  background-color: #f5f5f5;
  padding:7px 25px ;
  border-radius :4px ;
  font-weight: bolder;
  color:#797979;
  margin-bottom: 10px;
}
h2{
  padding:15px;
}
.date{
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 5px;
}
.date > h3{
  flex:2;
  padding-left:20px
}
</style>
