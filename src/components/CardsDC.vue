<template>
  <div class="card">
    <img :src="cardSrc" :alt="cardTitle" />
    <h3></h3>
  </div>
</template>

<script>
export default {
  name: "CardsDC",
  props: {
    cardSrc: String,
    cardTitle: String,
  },
};
</script>

<style>
@import "../temporary/variables";
</style>
