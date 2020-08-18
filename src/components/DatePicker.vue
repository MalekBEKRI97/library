<template>
  <div class="datePicker">
    <h2>Choisir la date et l'heure du rendez-vous</h2>
    <div class="date">
      <h3>{{months[date.getMonth()]+' '+date.getFullYear()}}</h3>
      <suivant fillColor="#2b78aa" :size="50" @click="addWeek"/>
    </div>
    <div class="weekDays" >
      <div v-for="(day,i) in generatedDays" :key="i" :class="[{'check':i === activeItem} , {'weekend' : day[0] === 'Sam' || day[0] === 'Dim'}]" @click="selectItem(i)">
        <div>
          {{day[0]}}
        </div>
        <div>{{day[1]}}</div>
        <div>{{day[2]}}</div>
      </div>
    </div>
    <div class="hours">
      <div v-for="time in times" :key="time">
        {{time[0] + ' : ' + time[1]}}
      </div>
    </div>
  </div>
</template>

<script>
import suivant from 'vue-material-design-icons/ArrowRightBox.vue';

export default {
  data() {
    return {
      date: new Date(),
      months: ['Janvier', 'Fevrier', 'Mars', 'Avril', 'May', 'Juin', 'Juillet', 'Août', 'Septembre', 'Octobre', 'Novombre', 'Decembre'],
      days: ['Lun', 'Mar', 'Mer', 'Jeu', 'Ven', 'Sam', 'Dim'],
      activeItem: null,
    };
  },
  name: 'DatePicker',
  components: {
    suivant,
  },
  computed: {
    generatedDays() {
      let currentDay = this.date.getDay() - 1;
      let currentDate = this.date.getDate();
      let currentmonth = this.date.getMonth();
      const daysGenerated = [];
      for (let i = 0; i < 7; i += 1) {
        daysGenerated[i] = [];
      }
      for (let i = 0; i < 7; i += 1) {
        if (currentDate === 32) {
          currentDate = 1;
          currentmonth += 1;
        }
        if (currentDay === 7) {
          currentDay = 0;
        }
        daysGenerated[i][0] = this.days[currentDay];
        daysGenerated[i][1] = currentDate;
        daysGenerated[i][2] = this.months[currentmonth];
        // if( (daysGenerated[i][0] == 'Dim') || (daysGenerated[i][0] == 'Sam'))

        currentDay += 1;
        currentDate += 1;
      }
      return daysGenerated;
    },
    times() {
      const tabTimes = [];
      for (let i = 0; i < 32; i += 1) {
        tabTimes[i] = [];
      }
      let h = 8;
      let m = 0;
      for (let i = 0; i < 32; i += 1) {
        if (m === 60) {
          m = 0;
          h += 1;
        }
        if (Math.floor(h / 10) !== 0) {
          tabTimes[i][0] = h.toString();
        } else {
          tabTimes[i][0] = `0${h.toString()}`;
        }
        if (Math.floor(m / 10) !== 0) {
          tabTimes[i][1] = m.toString();
        } else {
          tabTimes[i][1] = `0${m.toString()}`;
        }
        m += 15;
      }
      return tabTimes;
    },
    change() {
      this.verifyWeekend = true;
      return this.verifyWeekend;
    }
  },
  methods: {
    selectItem(i) {
      if (this.activeItem === null){
        this.activeItem = i;
      } else {
        this.activeItem = null;
      }
    },
    addWeek(){
      this.date = new Date(this.date.getFullYear(),this.date.getMonth(),this.date.getDate()+7);
      generatedDays;
    }
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
  cursor: pointer;
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
.check{
  background-color: #19aa96 !important;
  color:white !important;
}
.weekend{
  background-color: #f2dede !important;
  border: 1px solid red !important;
  color: #938f8f !important;
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
