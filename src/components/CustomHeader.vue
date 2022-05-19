<template>
  <header>
    <div class="barra-logo">
      <i class="fab fa-spotify"></i>
    </div>
  </header>
</template>

<script>
export default {
  name: "CustomHeader",
};
</script>

<style lang="scss">
@import "../style/common.scss";

.barra-logo {
  width: 100%;
  height: 100px;
  background-color: #2e3a46;
}
</style>
