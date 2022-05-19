<template>
  <main>
    <div class="wrapper">
      <div v-if="caricamento" class="caricamento">
        <CardCaricamento />
      </div>
      <div v-else class="contenitore-brani">
        <CardBrani v-for="(item, index) in brani" :key="index" :brani="item" />
      </div>
    </div>
  </main>
</template>

<script>
import CardBrani from "./CardBrani.vue";
import CardCaricamento from "./CardCaricamento.vue";
import axios from "axios";

export default {
  name: "CustomMain",
  components: {
    CardBrani,
    CardCaricamento,
  },

  data: function () {
    return {
      brani: [],
      caricamento: true,
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((resp) => {
        this.brani = resp.data.response;
        this.caricamento = false;
      });
  },
};
</script>

<style lang="scss">
@import "../style/common.scss";

.wrapper {
  width: 100%;
  height: calc(100vh - 80px);
  background-color: #1e2d3b;
  display: flex;
  justify-content: center;
  align-items: center;

  .contenitore-brani {
    width: 70%;
    height: 90%;
    padding: 1rem;
    display: flex;
    flex-wrap: wrap;
  }
}
</style>
