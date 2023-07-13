<template>
  <div class="forecast-wrapper">
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
    <div class="more-forecast">
      More Forecast ➡
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
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  flex-wrap: wrap;
  width: 100%;
}

.more-forecast {
  padding: 20px;
  font-size: 1.2em;
  cursor: pointer;
  align-self: center;
  text-align: center;
}
</style>
