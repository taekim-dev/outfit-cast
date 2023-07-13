<template>
  <div class="input-fields">
    <div class="text-inputs">
      <input type="text" placeholder="From" />
      <input type="text" placeholder="To" />
    </div>
    <div class="date-input">
      <input type="date" placeholder="Date" />
    </div>
  </div>
</template>

<script>
export default {
  name: "InputFields",
};
</script>

<style scoped>
.input-fields {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10px 0;
}

.text-inputs {
  width: 100%;
  width: 40%;
  display: flex;
  justify-content: space-evenly;
  margin-bottom: 10px;
}

.text-inputs input {
  width: 45%;
  height: 40px;
}

.date-input {
  width: 100%;
  display: flex;
  justify-content: center;
}

.date-input input {
  width: 15%;
  height: 40px; 
  
}

@media (max-width: 600px) {
  .text-inputs {
    width: 100%;
  }
  .text-inputs input {
    width: calc(50% - 10px); /* calculate the width taking the margin into account */
    box-sizing: border-box; /* include padding and border in element's total width and height */
    margin: 0 5px; /* add margin to the sides */
  }
  .date-input input {
    width: 100%;
    box-sizing: border-box;
  }
}

</style>
