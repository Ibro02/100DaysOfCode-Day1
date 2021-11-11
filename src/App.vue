<template>
  <div class="app">
    <h1 class="title">#100DaysOfCode</h1>
    <div class="calendar">
      <div id="calendar-box">
        <button
          type="button"
          id="clicker"
          v-on:click="clicked.push(this.num)"
          v-for="num in number"
          v-bind:key="num"
        >
          {{ num }}
        </button>
      </div>
    </div>
    <h1 v-for="click in clicked" v-bind:key="click">{{ click }}</h1>
  </div>
</template>

<script>
export default {
  name: "calendar",
  data() {
    return {
      number: [],
      clicked: [],
    };
  },
  mounted() {
    this.fillArray();
  },

  addToArray(num) {
    this.clicked.push(num);
  },
  methods: {
    fillArray() {
      for (let i = 1; i <= 100; i++) {
        this.number.push(i);
      }
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Arimo:wght@500;700&family=Bebas+Neue&family=Dancing+Script:wght@700&family=Mochiy+Pop+P+One&family=Oswald&family=Roboto+Condensed:wght@300;400&family=Varela+Round&display=swap");
body {
  background-color: #ff9d00;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100%25' height='100%25' viewBox='0 0 1600 800'%3E%3Cg stroke='%23000' stroke-width='66.7' stroke-opacity='0.05' %3E%3Ccircle fill='%23ff9d00' cx='0' cy='0' r='1800'/%3E%3Ccircle fill='%23fb8d17' cx='0' cy='0' r='1700'/%3E%3Ccircle fill='%23f47d24' cx='0' cy='0' r='1600'/%3E%3Ccircle fill='%23ed6e2d' cx='0' cy='0' r='1500'/%3E%3Ccircle fill='%23e35f34' cx='0' cy='0' r='1400'/%3E%3Ccircle fill='%23d85239' cx='0' cy='0' r='1300'/%3E%3Ccircle fill='%23cc453e' cx='0' cy='0' r='1200'/%3E%3Ccircle fill='%23be3941' cx='0' cy='0' r='1100'/%3E%3Ccircle fill='%23b02f43' cx='0' cy='0' r='1000'/%3E%3Ccircle fill='%23a02644' cx='0' cy='0' r='900'/%3E%3Ccircle fill='%23901e44' cx='0' cy='0' r='800'/%3E%3Ccircle fill='%23801843' cx='0' cy='0' r='700'/%3E%3Ccircle fill='%236f1341' cx='0' cy='0' r='600'/%3E%3Ccircle fill='%235e0f3d' cx='0' cy='0' r='500'/%3E%3Ccircle fill='%234e0c38' cx='0' cy='0' r='400'/%3E%3Ccircle fill='%233e0933' cx='0' cy='0' r='300'/%3E%3Ccircle fill='%232e062c' cx='0' cy='0' r='200'/%3E%3Ccircle fill='%23210024' cx='0' cy='0' r='100'/%3E%3C/g%3E%3C/svg%3E");
  background-attachment: fixed;
  background-size: cover;
}
.title {
  font-family: "Mochiy Pop P One";
  font-weight: 400;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f7fbff;
  margin-top: 60px;
}
.calendar {
  background-color: rgba(0, 0, 0, 0.377);
  margin: 0px 5px;
  padding: 3vw;
  border-radius: 2vw;
}
#calendar-box {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
  align-content: center;
}
button {
  width: 9vh;
  display: flex;
  padding: 15px 15px;
  font-size: 30px;
  margin: 10px;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  background-color: rgb(240, 240, 240);
  border: 1px solid rgb(53, 53, 53);
  border-radius: 1vh;
  cursor: pointer;
  color: rgb(31, 30, 30);
  box-shadow: rgba(0, 0, 0, 0.17) 0px -23px 25px 0px inset,
    rgba(0, 0, 0, 0.15) 0px -36px 30px 0px inset,
    rgba(0, 0, 0, 0.1) 0px -79px 40px 0px inset, rgba(0, 0, 0, 0.06) 0px 2px 1px,
    rgba(0, 0, 0, 0.09) 0px 4px 2px, rgba(0, 0, 0, 0.09) 0px 8px 4px,
    rgba(0, 0, 0, 0.09) 0px 16px 8px, rgba(0, 0, 0, 0.09) 0px 32px 16px;
  justify-content: center;
}
button:focus {
  background-color: red;
  color: #cecece;
  border-color: #f7fbff;
}
.red {
  background-color: red;
}
@media (max-width: 400px) {
  button {
    width: unset;
  }
}
</style>
