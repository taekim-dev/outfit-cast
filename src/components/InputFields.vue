<template>
  <div>
    <input type="text" placeholder="From" />
    <input type="text" placeholder="To" />
    <!-- For date, we are just using a simple input field here, but you might want to use a date picker library for a better UX -->
    <input type="date" placeholder="Date" />
  </div>
</template>

<script>
export default {
  name: "InputFields",
};
</script>

<style scoped>
div {
  display: flex;
  justify-content: space-around;
  margin-bottom: 20px;
}
input {
  width: 30%;
}
</style>
