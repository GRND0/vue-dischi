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
  width: calc(100% / 5);
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #2e3a46;
}
</style>
