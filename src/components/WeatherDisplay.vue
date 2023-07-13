<template>
  <div class="weather-display">
    <h2>Feeling: {{ weatherCategory }}</h2>
    <div class="avatar-wrapper">
      <img
        :src="require(`@/assets/${avatarImage}`)"
        alt="Avatar Image"
        class="avatar"
      />
    </div>
    <p>{{ weatherDescription }}</p>
  </div>
</template>

<script>
export default {
  name: "WeatherDisplay",
  props: ["weatherCategory", "avatarImage", "weatherDescription"],
};
</script>

<style scoped>
.weather-display {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 20px;
  max-width: 200px;
}

.avatar-wrapper {
  width: 100%;
  padding-bottom: 200%;
  position: relative;
}

.avatar {
  position: absolute;
  object-fit: cover;
  width: 100%;
  height: 100%;
}
</style>
