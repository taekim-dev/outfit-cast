<template>
  <div class="forecast-wrapper">
    <div class="weather-display-container">
      <WeatherDisplay 
        weatherCategory="Warm" 
        avatarImage="avatar_warm.png" 
        weatherDescription="It's a warm day today!" 
      />
      <WeatherDisplay 
        weatherCategory="Cool" 
        avatarImage="avatar_cool.png" 
        weatherDescription="It's a cool day tomorrow!" 
      />
    </div>
    <div class="more-forecast">
      5 Days Forecast ➡
    </div>
  </div>
</template>

<script>
import WeatherDisplay from './WeatherDisplay.vue'

export default {
  name: 'WeatherForecast',
  components: {
    WeatherDisplay
  }
}
</script>

<style scoped>
.forecast-wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10px 0;
}

.weather-display-container {
  width: 40%;
  display: flex;
  justify-content: space-evenly;
  margin-bottom: 10px;
}

.weather-display-container weatherdisplay {
  width: 45%;
}

.more-forecast {
  width: 15%;
  padding: 20px;
  font-size: 1.2em;
  cursor: pointer;
  text-align: center;
}

@media (max-width: 600px) {
  .weather-display-container {
    width: 100%;
  }
  .weather-display-container weatherdisplay {
    width: calc(50% - 10px);
    box-sizing: border-box;
    margin: 0 5px;
  }
  .more-forecast {
    width: 50%;
    box-sizing: border-box;
    margin: 0 auto;
  }
}
</style>
