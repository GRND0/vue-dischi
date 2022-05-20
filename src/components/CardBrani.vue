<template>
  <div class="contenitore-card">
    <img :src="brani.poster" alt="" />
    <h3>{{ brani.title }}</h3>
    <small>{{ brani.author }}</small>
    <small>{{ brani.year }}</small>
  </div>
</template>

<script>
export default {
  name: "CardBrani",
  props: {
    brani: Object,
  },
};
</script>

<style lang="scss">
@import "../style/common.scss";

.contenitore-card {
  width: calc(100% / 5 - 3rem);
  max-height: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #2e3a46;
  margin: 1rem;
  padding: 1.2rem;

  img {
    width: 100%;
    margin-bottom: 0.5rem;
  }

  h3 {
    color: white;
    text-align: center;
    text-transform: uppercase;
    margin-bottom: 0.5rem;
  }

  small {
    color: #6d6f72;
  }
}
</style>
