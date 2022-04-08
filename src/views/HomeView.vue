<script>
import WeatherCard from "../components/WeatherCard.vue";

export default {
  components: {
    WeatherCard,
  },
  data() {
    return {
    // Mock Api Data
      tempData: [
        {
          lowTemp: 27.5,
          highTemp: 47.1,
          location: {
            city: "Melbourne",
            state: "VIC",
          },
          weatherIcon:
            "https://cdn.icon-icons.com/icons2/2505/PNG/512/sunny_weather_icon_150663.png",
          tempUnit: "°C",
        },
        {
          lowTemp: 10.5,
          highTemp: 17.6,
          location: {
            city: "Darwin",
            state: "NT",
          },
          weatherIcon:
            "https://cdn.icon-icons.com/icons2/2505/PNG/512/sunny_weather_icon_150663.png",
          tempUnit: "°C",
        },
        {
          lowTemp: -10.6,
          highTemp: 55.3,
          location: {
            city: "Amaroo",
            state: "ACT",
          },
          weatherIcon:
            "https://cdn.icon-icons.com/icons2/2505/PNG/512/sunny_weather_icon_150663.png",
          tempUnit: "°C",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="main">
    <div class="card" v-for="weather in tempData" :key="weather.lowTemp">
      <weather-card :objData="weather" />
    </div>
  </div>
</template>

<style scoped>
.main {
  display: flex;
  justify-content: center;
}

.card {
    margin-right: 16px;
}
.card:last-child{
    margin-right: 0px;
}
</style>
