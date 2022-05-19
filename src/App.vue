<template>
  <div id="app">
    <CustomHeader />
    <CustomMain />
  </div>
</template>

<script>
import CustomHeader from "./components/CustomHeader.vue";
import CustomMain from "./components/CustomMain.vue";

export default {
  name: "App",
  components: {
    CustomHeader,
    CustomMain,
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
