<script>
export default {
  name: "WeatherCard",
  props: {
    objData: Object
    // lowTemp: Number,
    // highTemp: Number,
    // location: Object,
    // weatherIcon: String,
    // tempUnit: String,
  },
  // data() {
  //   return {
  //     lowTemp: 27.5,
  //     highTemp: 55.3,
  //     location: {
  //       city: "Melbourne",
  //       state: "VIC",
  //     },
  //     weatherIcon:
  //       "https://cdn.icon-icons.com/icons2/2505/PNG/512/sunny_weather_icon_150663.png",
  //     tempUnit: "°C",
  //   };
  // },
};
</script>

<template>
  <div>
    <h1>Weather</h1>
    <img :src="objData.weatherIcon" />
    <ul>
      <li>
        Low : <span id="high">{{ objData.lowTemp }} {{ objData.tempUnit }}</span>
      </li>
      <li>
        High : <span id="low">{{ objData.highTemp }} {{ objData.tempUnit }}</span>
      </li>
    </ul>
    <p>
      Showing temps of : <b>{{ objData.location.city }} {{ objData.location.state }}</b>
    </p>
  </div>
</template>

<style scoped>
div {
  border: 3px black solid;
  padding: 10px;
  width: 400px;
  font-size: 2em;
  font-family: "Comic Sans MS", "Comic Sans", cursive;
  text-align: center;
  box-shadow: 5px 5px #888888;
}

img {
  margin: auto;
  display: block;
  width: 8em;
}
li {
  list-style-type: none;
  margin-left: -15%;
}
#high {
  color: red;
}
#low {
  color: blue;
}
</style>