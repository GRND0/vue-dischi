<template>
  <div>
    <label for="selettore-genere">Filtra per genere</label>

    <select
      v-model="selezione"
      @change="$emit('opzione', selezione)" id="selettore-genere">
      <option value="All">Tutti i generi</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "CustomSelettore",
  data: function () {
    return {
      selezione: "All",
    };
  },
};
</script>

<style></style>
