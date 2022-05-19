<template>
  <header>
    <div class="barra-logo">
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/1/19/Spotify_logo_without_text.svg"
        alt=""
      />
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
  height: 80px;
  background-color: #2e3a46;
  padding: 0.5rem;
  display: flex;
  align-items: center;

  img {
    height: 70%;
  }
}
</style>
