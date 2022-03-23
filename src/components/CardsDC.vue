<template>
  <div class="card">
    <div class="container-image">
      <img :src="cardSrc" :alt="cardTitle" />
    </div>

    <h3 class="subtitle">{{ cardTitle }}</h3>
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

<style scoped lang="scss">
@import "../temporary/variables";

.card {
  flex-basis: calc(100% / 6 - 1rem);
  display: flex;
  flex-direction: column;
  padding: 1rem;
}

.container-image {
  width: 100%;

  img {
    width: 160px;
    height: 160px;
    object-fit: cover;
    object-position: top;
  }
}

.subtitle {
  text-transform: uppercase;
  color: white;
  font-size: 0.8rem;
  padding-top: 1rem;
}
</style>
