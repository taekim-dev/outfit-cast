<template>
  <div id="app" class="app-container">
    <AppHeader />
    <InputFields />
    <WeatherForecast />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import InputFields from './components/InputFields.vue'
import WeatherForecast from './components/WeatherForecast.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    InputFields,
    WeatherForecast,
    AppFooter
  }
}
</script>


<style>
.app-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  min-height: 100vh;
  padding: 20px;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

/* You may want to add specific styles to each component for better alignment and presentation */
</style>
