<template>
  <div class="weather-display">
    <h2 class="weather-category">Feeling: {{ weatherCategory }}</h2>
    <div class="avatar-wrapper">
      <img
        :src="require(`@/assets/${avatarImage}`)"
        alt="Avatar Image"
        class="avatar"
      />
    </div>
    <p class="weather-description">{{ weatherDescription }}</p>
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
  max-width: 50%;
}

.avatar-wrapper {
  width: 100%;
  position: relative;
}

.avatar {
  width: 100%;
  height: auto;
  max-width: 100%;
  max-height: 100%;
}

.weather-category,
.weather-description {
  height: 50px; /* Adjust this value accordingly */
  text-align: center;
}

@media (max-width: 600px) {
  .weather-display {
    max-width: 100%;
    align-items: flex-start;
  }

  .avatar {
    width: 100%;
  }
}
</style>
